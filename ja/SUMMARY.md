# 目次

* [はじめに](README.md)
* [基本的な使い方](base/installation.md)
  * [インストール](base/installation.md#install)
  * [アップグレード](base/installation.md#update)
  * [Excel 文書を作成する](base/installation.md#NewFile)
  * [Excel 文書を読む](base/installation.md#read)
  * [Excel 文書にチャートを追加する](base/installation.md#chart)
  * [Excel 文書に画像を追加する](base/installation.md#image)
* [ワークブック](workbook.md)
  * [Excel 文書を作成する](workbook.md#NewFile)
  * [開く](workbook.md#OpenFile)
  * [データストリームを開く](workbook.md#OpenReader)
  * [保存](workbook.md#Save)
  * [名前を付けて保存](workbook.md#SaveAs)
  * [閉じるワークブック](workbook.md#Close)
  * [ワークシートを作成する](workbook.md#NewSheet)
  * [ワークシートを削除する](workbook.md#DeleteSheet)
  * [ワークシートをコピーする](workbook.md#CopySheet)
  * [グループワークシート](workbook.md#GroupSheets)
  * [ワークシートのグループ化を解除する](workbook.md#UngroupSheets)
  * [ワークシートの背景](workbook.md#SetSheetBackground)
  * [デフォルトワークシートを設定する](workbook.md#SetActiveSheet)
  * [アクティブシートインデックスを取得する](workbook.md#GetActiveSheetIndex)
  * [ワークシートの表示設定](workbook.md#SetSheetVisible)
  * [ワークシートの表示設定を取得する](workbook.md#GetSheetVisible)
  * [ワークシート形式のプロパティを設定する](workbook.md#SetSheetFormatPr)
  * [ワークシート形式のプロパティを取得する](workbook.md#GetSheetFormatPr)
  * [ワークシートビューのプロパティを設定する](workbook.md#SetSheetViewOptions)
  * [ワークシートビュープロパティを取得する](workbook.md#GetSheetViewOptions)
  * [ワークシートのページレイアウトを設定する](workbook.md#SetPageLayout)
  * [ワークシートのページレイアウトを取得する](workbook.md#GetPageLayout)
  * [ワークシートのページ余白を設定する](workbook.md#SetPageMargins)
  * [ワークシートのページ余白を取得する](workbook.md#GetPageMargins)
  * [ヘッダとフッタを設定する](workbook.md#SetHeaderFooter)
  * [名前を設定する](workbook.md#SetDefinedName)
  * [名前を取得する](workbook.md#GetDefinedName)
  * [定義された名前を削除](workbook.md#DeleteDefinedName)
  * [アプリケーションのプロパティを設定する](workbook.md#SetAppProps)
  * [アプリケーションのプロパティを取得する](workbook.md#GetAppProps)
  * [ブックのプロパティを設定する](workbook.md#SetDocProps)
  * [ブックのプロパティを取得する](workbook.md#GetDocProps)
* [ワークシート](sheet.md)
  * [列の可視性設定](sheet.md#SetColVisible)
  * [列幅の設定](sheet.md#SetColWidth)
  * [行の高さを設定](sheet.md#SetRowHeight)
  * [行の表示設定](sheet.md#SetRowVisible)
  * [ワークシート名を取得する](sheet.md#GetSheetName)
  * [列の可視性を取得する](sheet.md#GetColVisible)
  * [列幅を取得](sheet.md#GetColWidth)
  * [行の高さを取得する](sheet.md#GetRowHeight)
  * [行の可視性を取得する](sheet.md#GetRowVisible)
  * [ワークシートインデックスを取得](sheet.md#GetSheetIndex)
  * [ワークシートマップを取得する](sheet.md#GetSheetMap)
  * [ワークシートリストを取得する](sheet.md#GetSheetList)
  * [ワークシート名を設定](sheet.md#SetSheetName)
  * [ワークシートのプロパティを設定する](sheet.md#SetSheetPrOptions)
  * [ワークシートのプロパティを取得する](sheet.md#GetSheetPrOptions)
  * [列を挿入](sheet.md#InsertCol)
  * [行挿入](sheet.md#InsertRow)
  * [重複行を追加](sheet.md#DuplicateRow)
  * [行を複製](sheet.md#DuplicateRowTo)
  * [行のアウトラインを作成する](sheet.md#SetRowOutlineLevel)
  * [列のアウトラインを作成する](sheet.md#SetColOutlineLevel)
  * [行のアウトラインを取得する](sheet.md#GetRowOutlineLevel)
  * [列のアウトラインを取得](sheet.md#GetColOutlineLevel)
  * [列イテレータ](sheet.md#Cols)
  * [行イテレータ](sheet.md#Rows)
  * [検索シート](sheet.md#SearchSheet)
  * [シートを保護する](sheet.md#ProtectSheet)
  * [無防備シート](sheet.md#UnprotectSheet)
  * [列を削除](sheet.md#RemoveCol)
  * [行を削除](sheet.md#RemoveRow)
  * [行の値を設定](sheet.md#SetSheetRow)
  * [改ページを挿入](sheet.md#InsertPageBreak)
  * [改ページを削除](sheet.md#RemovePageBreak)
* [セル](cell.md)
  * [セル値設定](cell.md#SetCellValue)
  * [ブール値設定](cell.md#SetCellBool)
  * [既定の文字の種類の値を設定する](cell.md#SetCellDefault)
  * [実数を設定する](cell.md#SetCellInt)
  * [文字列値の設定](cell.md#SetCellStr)
  * [セルスタイルの設定](cell.md#SetCellStyle)
  * [ハイパーリンクの設定](cell.md#SetCellHyperLink)
  * [セルのリッチテキストを設定する](cell.md#SetCellRichText)
  * [リッチテキスト形式を取得する](cell.md#GetCellRichText)
  * [セル値取得](cell.md#GetCellValue)
  * [セルタイプを取得します](cell.md#GetCellType)
  * [列ごとにすべてのセル値を取得する](cell.md#GetCols)
  * [行ごとにすべてのセル値を取得する](cell.md#GetRows)
  * [ハイパーリンクを取得](cell.md#GetCellHyperLink)
  * [スタイルインデックスの取得](cell.md#GetCellStyle)
  * [セルを結合](cell.md#MergeCell)
  * [セルの結合を解除](cell.md#UnmergeCell)
  * [セルを結合する](cell.md#GetMergeCells)
  * [コメント追加](cell.md#AddComment)
  * [コメントを得る](cell.md#GetComments)
  * [セル式の設定](cell.md#SetCellFormula)
  * [セル式を取得する](cell.md#GetCellFormula)
  * [セル値を計算する](cell.md#CalcCellValue)
* [グラフ](chart.md)
  * [グラフを追加する](chart.md#AddChart)
  * [グラフシートを作成する](chart.md#AddChartSheet)
  * [2D エリアチャート](chart/area.md)
  * [2D 積層型エリアチャート](chart/areaStacked.md)
  * [2D 100％ 積み上げ面グラフ](chart/areaPercentStacked.md)
  * [3D エリアチャート](chart/area3D.md)
  * [3D 積み上げ面グラフ](chart/area3DStacked.md)
  * [3D 100％ 積み上げ面グラフ](chart/area3DPercentStacked.md)
  * [2D クラスタ棒グラフ](chart/bar.md)
  * [2D 積み上げ棒グラフ](chart/barStacked.md)
  * [2D 100％ 積み上げ棒グラフ](chart/barPercentStacked.md)
  * [3D クラスター棒グラフ](chart/bar3DClustered.md)
  * [3D 積み上げ棒グラフ](chart/bar3DStacked.md)
  * [3D 100％ 積み上げ棒グラフ](chart/bar3DPercentStacked.md)
  * [3D 円グラフクラスタ付き棒グラフ](chart/bar3DConeClustered.md)
  * [3D 円グラフ積み上げ棒グラフ](chart/bar3DConeStacked.md)
  * [3D 100% 円グラフグラフ](chart/bar3DConePercentStacked.md)
  * [3D ピラミッド クラスタ化棒グラフ](chart/bar3DPyramidClustered.md)
  * [3D ピラミッド積み上げ棒グラフ](chart/bar3DPyramidStacked.md)
  * [3D 100% ピラミッド積み上げ棒グラフ](chart/bar3DPyramidPercentStacked.md)
  * [3D 円柱クラスタ化棒グラフ](chart/bar3DCylinderClustered.md)
  * [3D 円柱積み上げ棒グラフ](chart/bar3DCylinderStacked.md)
  * [3D 100% 円柱積み上げ棒グラフ](chart/bar3DCylinderPercentStacked.md)
  * [2D クラスター縦棒グラフ](chart/col.md)
  * [2D 積み上げ縦棒グラフ](chart/colStacked.md)
  * [2D 100％ 積み上げ縦棒グラフ](chart/colPercentStacked.md)
  * [3D クラスター縦棒グラフ](chart/col3DClustered.md)
  * [3D 縦棒グラフ](chart/col3D.md)
  * [3D 積み上げ縦棒グラフ](chart/col3DStacked.md)
  * [3D 100％ 積み上げ縦棒グラフ](chart/col3DPercentStacked.md)
  * [3D 円グラフグラフ](chart/col3DCone.md)
  * [3D 円グラフクラスタ化縦棒グラフ](chart/col3DConeClustered.md)
  * [3D 円グラフ積み上げ縦棒グラフ](chart/col3DConeStacked.md)
  * [3D 100% 円グラフ積み上げ縦棒グラフ](chart/col3DConePercentStacked.md)
  * [3D ピラミッド縦棒グラフ](chart/col3DPyramid.md)
  * [3D ピラミッド クラスタ化縦棒グラフ](chart/col3DPyramidClustered.md)
  * [3D ピラミッド積み上げ縦棒グラフ](chart/col3DPyramidStacked.md)
  * [3D 100% ピラミッド積み上げ縦棒グラフ](chart/col3DPyramidPercentStacked.md)
  * [3D 円柱縦棒グラフ](chart/col3DCylinder.md)
  * [3D 円柱クラスタ化縦棒グラフ](chart/col3DCylinderClustered.md)
  * [3D 円柱積み上げ縦棒グラフ](chart/col3DCylinderStacked.md)
  * [3D 100% 円柱積み上げ縦棒グラフ](chart/col3DCylinderPercentStacked.md)
  * [ドーナツチャート](chart/doughnut.md)
  * [折れ線グラフ](chart/line.md)
  * [円グラフ](chart/pie.md)
  * [3D 円グラフ](chart/pie3D.md)
  * [レーダーチャート](chart/radar.md)
  * [散布図](chart/scatter.md)
  * [3D サーフェス チャート](chart/surface3D.md)
  * [3D ワイヤフレーム サーフェス チャート](chart/wireframeSurface3D.md)
  * [輪郭グラフ](chart/contour.md)
  * [ワイヤフレーム輪郭グラフ](chart/wireframeContour.md)
  * [バブルチャート](chart/bubble.md)
  * [3D バブル チャート](chart/bubble3D.md)
  * [チャートを削除](chart.md#DeleteChart)
* [イメージ](image.md)
  * [図を挿入する](image.md#AddPicture)
  * [画像を取得](image.md#GetPicture)
  * [画像を削除](image.md#DeletePicture)
* [形状](shape.md)
* [スパークライン](sparklines.md)
* [スタイル](style.md)
  * [スタイルの作成](style.md#NewStyle)
  * [枠](style.md#border)
  * [色塗り](style.md#shading)
  * [パターン塗りつぶし](style.md#pattern)
  * [アライメント](style.md#align)
  * [フォントの下線](style.md#underline)
  * [デジタルカスタムフォーマット](style.md#number_format)
  * [列のスタイル設定](style.md#SetColStyle)
  * [行スタイルを設定する](style.md#SetRowStyle)
  * [既定のフォントを設定する](style.md#SetDefaultFont)
  * [デフォルトのフォントを取得する](style.md#GetDefaultFont)
* [ストリーミング書き込み](stream.md)
  * [ストリームライターを取得する](stream.md#NewStreamWriter)
  * [ストリームにシート行を書き込む](stream.md#SetRow)
  * [ストリーミングするテーブルを追加する](stream.md#AddTable)
  * [ストリームでマージセル](stream.md#MergeCell)
  * [ストリームの列幅を設定する](stream.md#SetColWidth)
  * [エンディングストリーム](stream.md#Flush)
* [データ](data.md)
  * [データ検証を追加する](data.md#AddDataValidation)
  * [データ検証の削除](data.md#DeleteDataValidation)
* [ピボットテーブル](pivot.md#PivotTable)
  * [ピボットテーブルを作成する](pivot.md#AddPivotTable)
* [ツール機能](utils.md)
  * [テーブル作成](utils.md#AddTable)
  * [自動フィルタ](utils.md#AutoFilter)
  * [セルキャッシュをクリア](utils.md#UpdateLinkedValue)
  * [セル名の分割](utils.md#SplitCellName)
  * [結合セル名](utils.md#JoinCellName)
  * [列名を番号に](utils.md#ColumnNameToNumber)
  * [名前の列番号](utils.md#ColumnNumberToName)
  * [座標に対するセル名](utils.md#CellNameToCoordinates)
  * [セル名に対する座標](utils.md#CoordinatesToCellName)
  * [条件付き書式スタイルの作成](utils.md#NewConditionalStyle)
  * [条件付き書式の設定](utils.md#SetConditionalFormat)
  * [条件付きフォーマットを削除](utils.md#UnsetConditionalFormat)
  * [設定ペイン](utils.md#SetPanes)
  * [カラー値計算](utils.md#ThemeColor)
  * [RGBおよびHSLカラースペースカラー値変換](utils.md#RGBToHSL)
  * [HSLとRGBカラースペースカラー値変換](utils.md#HSLToRGB)
  * [ファイルライター](utils.md#FileWriter)
  * [VBA プロジェクトの追加](utils.md#AddVBAProject)
  * [Excel の日付を時刻に変換する](utils.md#ExcelDateToTime)
  * [文字トランスコーダー](utils.md#CharsetTranscoder)
* より多くの例
  * [カレンダー](example/calendar.md)
  * [依存ドロップリスト](example/dependentDropList.md)
  * [マルチセレクトドロップリスト](example/multiselectDropList.md)
* [定数](constants.md)
* [変数](variables.md)
* [パフォーマンスデータ](performance.md)
* [参加貢献](contribution.md)
* バージョン履歴
  * [v2.5.0 (2022-01-03)](releases/v2.5.0.md)
  * [v2.4.1 (2021-08-02)](releases/v2.4.1.md)
  * [v2.4.0 (2021-04-19)](releases/v2.4.0.md)
  * [v2.3.2 (2021-01-04)](releases/v2.3.2.md)
  * [v2.3.1 (2020-09-23)](releases/v2.3.1.md)
  * [v2.3.0 (2020-08-06)](releases/v2.3.0.md)
  * [v2.2.0 (2020-05-11)](releases/v2.2.0.md)
  * [v2.1.0 (2020-02-10)](releases/v2.1.0.md)
  * [v2.0.2 (2019-10-09)](releases/v2.0.2.md)
  * [v2.0.1 (2019-07-01)](releases/v2.0.1.md)
  * [v2.0.0 (2019-05-02)](releases/v2.0.0.md)
  * [v1.4.1 (2019-01-01)](releases/v1.4.1.md)
  * [v1.4.0 (2018-08-14)](releases/v1.4.0.md)
  * [v1.3.0 (2018-05-13)](releases/v1.3.0.md)
  * [v1.2.0 (2017-12-01)](releases/v1.2.0.md)
  * [v1.1.0 (2017-08-17)](releases/v1.1.0.md)
