# Сводная таблица {#PivotTable}

Сводная таблица - это таблица статистики, которая суммирует данные более обширной таблицы (например, из базы данных, электронной таблицы или программы бизнес-аналитики). Эта сводка может включать суммы, средние значения или другие статистические данные, которые сводная таблица группирует значимым образом.

PivotTableOption напрямую отображает настройки формата сводной таблицы.

```go
type PivotTableOption struct {
    DataRange           string
    PivotTableRange     string
    Rows                []PivotTableField
    Columns             []PivotTableField
    Data                []PivotTableField
    Filter              []PivotTableField
    RowGrandTotals      bool
    ColGrandTotals      bool
    ShowDrill           bool
    UseAutoFormatting   bool
    PageOverThenDown    bool
    MergeItem           bool
    CompactData         bool
    ShowError           bool
    ShowRowHeaders      bool
    ShowColHeaders      bool
    ShowRowStripes      bool
    ShowColStripes      bool
    ShowLastColumn      bool
    PivotTableStyleName string
}
```

`PivotTableStyleName`: Имена стилей встроенных сводных таблиц:

```text
PivotStyleLight1 - PivotStyleLight28
PivotStyleMedium1 - PivotStyleMedium28
PivotStyleDark1 - PivotStyleDark28
```

PivotTableField непосредственно привязки параметров поля сводной таблицы.

```go
type PivotTableField struct {
    Compact         bool
    Data            string
    Name            string
    Outline         bool
    Subtotal        string
    DefaultSubtotal bool
}
```

Subtotal указывает функцию агрегирования, которая применяется к этому полю данных. Значением по умолчанию является `Sum`. Возможные значения для этого атрибута:

|Необязательное значение|
|---|
|Average|
|Count|
|CountNums|
|Max|
|Min|
|Product|
|StdDev|
|StdDevp|
|Sum|
|Var|
|Varp|

Name указывает имя поля данных. В имени поля данных допускается максимум `255` символов, лишние символы будут обрезаны.

## Создать сводную таблицу {#AddPivotTable}

```go
func (f *File) AddPivotTable(opt *PivotTableOption) error
```

AddPivotTable предоставляет метод для добавления сводной таблицы с помощью заданных опций сводной таблицы.

Например, создайте сводную таблицу в области `Sheet1!$G$2:$M$34` с регионом `Sheet1!$A$1:$E$31` в качестве источника данных, суммируйте по сумме продаж:

<p align="center"><img width="1117" src="./images/pivot_table_01.png" alt="создать сводную таблицу с Excelize с помощью Go"></p>

```go
package main

import (
    "fmt"
    "math/rand"

    "github.com/xuri/excelize/v2"
)

func main() {
    f := excelize.NewFile()
    // Создать некоторые данные на листе
    month := []string{"Jan", "Feb", "Mar", "Apr", "May",
        "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"}
    year := []int{2017, 2018, 2019}
    types := []string{"Meat", "Dairy", "Beverages", "Produce"}
    region := []string{"East", "West", "North", "South"}
    f.SetSheetRow("Sheet1", "A1", &[]string{"Month", "Year", "Type", "Sales", "Region"})
    for i := 0; i < 30; i++ {
        f.SetCellValue("Sheet1", fmt.Sprintf("A%d", i+2), month[rand.Intn(12)])
        f.SetCellValue("Sheet1", fmt.Sprintf("B%d", i+2), year[rand.Intn(3)])
        f.SetCellValue("Sheet1", fmt.Sprintf("C%d", i+2), types[rand.Intn(4)])
        f.SetCellValue("Sheet1", fmt.Sprintf("D%d", i+2), rand.Intn(5000))
        f.SetCellValue("Sheet1", fmt.Sprintf("E%d", i+2), region[rand.Intn(4)])
    }
    if err := f.AddPivotTable(&excelize.PivotTableOption{
        DataRange:       "Sheet1!$A$1:$E$31",
        PivotTableRange: "Sheet1!$G$2:$M$34",
        Rows: []excelize.PivotTableField{
            {Data: "Month", DefaultSubtotal: true}, {Data: "Year"}},
        Filter: []excelize.PivotTableField{
            {Data: "Region"}},
        Columns: []excelize.PivotTableField{
            {Data: "Type", DefaultSubtotal: true}},
        Data: []excelize.PivotTableField{
            {Data: "Sales", Name: "Summarize", Subtotal: "Sum"}},
        RowGrandTotals: true,
        ColGrandTotals: true,
        ShowDrill:      true,
        ShowRowHeaders: true,
        ShowColHeaders: true,
        ShowLastColumn: true,
    }); err != nil {
        fmt.Println(err)
    }
    if err := f.SaveAs("Book1.xlsx"); err != nil {
        fmt.Println(err)
    }
}
```
