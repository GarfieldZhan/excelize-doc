# 走勢圖

走勢圖是 Excel 2010 及以上版本中的功能，是放入儲存格中的小型圖，每個走勢圖代表所選內容中的一行資料。將走勢圖放在其資料附近可提供非常好的視覺衝擊。

<p align="center"><img width="612" src="./images/sparkline_01.png" alt="使用 Go 語言通過 Excelize 創建走勢圖"></p>

[走勢圖](https://en.wikipedia.org/wiki/Sparklines) 是由 [Edward Tufte](https://en.wikipedia.org/wiki/Edward_Tufte) 發明的。

## 添加走勢圖

```go
func (f *File) AddSparkline(sheet string, opt *SparklineOption) error
```

根據給定的工作表名和走勢圖屬性添加走勢圖。走勢圖是工作表儲存格中直觀表示資料的微型圖表。使用走勢圖以一系列值顯示趨勢（如季節性增加或減少、經濟週期），或突出顯示最大值和最小值。走勢圖在 Excel 2007 中將不會顯示。例如添加組走勢圖：

```go
err := f.AddSparkline("Sheet1", &excelize.SparklineOption{
    Location: []string{"A1", "A2", "A3"},
    Range:    []string{"Sheet2!A1:J1", "Sheet2!A2:J2", "Sheet2!A3:J3"},
    Markers:  true,
})
```

<p align="center"><img width="653" src="./images/sparkline_02.png" alt="使用 Go 語言通過 Excelize 創建走勢圖"></p>

下表為 Excelize 支持的走勢圖格式選項：

參數 | 描述
---|---
Location  | 必須參數, 數目需要與 `Range` 保持一致
Range     | 必須參數, 數目需要與 `Location` 保持一致
Type      | 枚舉值: `line`, `column`, `win_loss`
Style     | 數值範圍: 0 - 35
Hight     | 切換走勢圖高點：突出顯示所選走勢圖組中資料的最高點
Low       | 切換走勢圖低點：突出顯示所選走勢圖組中資料的最低點
First     | 切換走勢圖首點：突出顯示所選走勢圖組中資料的第一點
Last      | 切換走勢圖尾點：突出顯示所選走勢圖組中資料的最後一點
Negative  | 切換走勢圖負點：突出顯示所選走勢圖組中資料的負值
Markers   | 切換走勢圖標記：突出顯示所選走勢圖組中資料的每個點
ColorAxis | 走勢圖色彩，形如 `RRGGBB` 格式的 RGB 色值
Axis      | 顯示走勢圖坐標軸
