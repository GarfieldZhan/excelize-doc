# 多选列表

使用 Go 语言在 Excel 文档中无需 VBA 创建可多选菜单列表:

<p align="center"><img width="426" src="../images/multiselect_drop_list.gif" alt="使用 Go 语言在 Excel 文档中无需 VBA 创建可多选菜单列表"></p>

```go
package main

import (
    "fmt"

    "github.com/xuri/excelize/v2"
)

func main() {
    // 创建工作簿
    f := excelize.NewFile()
    var (
        sheetName = "Sheet1"
        selection = []string{"red", "blue", "green", "yellow"}
        // 定义单元格的值
        data = [][]interface{}{
            {"Element", "Picklist", nil, "Select below"},
            {selection[0] + " "},
            {selection[1] + " "},
            {selection[2] + " "},
            {selection[3] + " "},
        }
        cell string
        err  error
    )
    // 按行赋值
    for r, row := range data {
        if cell, err = excelize.JoinCellName("A", r+1); err != nil {
            fmt.Println(err)
            return
        }
        if err = f.SetSheetRow(sheetName, cell, &row); err != nil {
            fmt.Println(err)
            return
        }
    }
    // 设置自定义名称
    for index, value := range selection {
        if cell, err = excelize.CoordinatesToCellName(1, index+2, true); err != nil {
            fmt.Println(err)
            return
        }
        if err = f.SetDefinedName(&excelize.DefinedName{
            Name:     value,
            RefersTo: fmt.Sprintf("%s!%s", sheetName, cell),
            Scope:    sheetName,
        }); err != nil {
            fmt.Println(err)
            return
        }
        if cell, err = excelize.CoordinatesToCellName(2, index+2); err != nil {
            fmt.Println(err)
            return
        }
        formula := fmt.Sprintf("=IF(ISNUMBER(FIND(%s,D2)),\"\",D2&%s)", value, value)
        if err := f.SetCellFormula(sheetName, cell, formula); err != nil {
            fmt.Println(err)
            return
        }
    }
    // 设置数据验证
    dvRange := excelize.NewDataValidation(true)
    dvRange.Sqref = "D2:D2"
    dvRange.SetSqrefDropList("$B$2:$B$5", true)
    if err = f.AddDataValidation(sheetName, dvRange); err != nil {
        fmt.Println(err)
        return
    }
    // 自定义列宽
    for col, width := range map[string]float64{"A": 10, "B": 18, "D": 18} {
        if err = f.SetColWidth(sheetName, col, col, width); err != nil {
            fmt.Println(err)
            return
        }
    }
    // 创建表格
    if err = f.AddTable(sheetName, "A1", "B5", `{
        "table_name": "table",
        "table_style": "TableStyleMedium2"
    }`); err != nil {
        fmt.Println(err)
        return
    }
    // 保存工作簿
    if err := f.SaveAs("Book1.xlsx"); err != nil {
        fmt.Println(err)
    }
}
```
