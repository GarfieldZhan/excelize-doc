# Variables

```go
var (
    // ErrStreamSetColWidth defined the error message on set column width in
    // stream writing mode.
    ErrStreamSetColWidth = errors.New("must call the SetColWidth function before the SetRow function")
    // ErrColumnNumber defined the error message on receive an invalid column
    // number.
    ErrColumnNumber = errors.New("column number exceeds maximum limit")
    // ErrColumnWidth defined the error message on receive an invalid column
    // width.
    ErrColumnWidth = fmt.Errorf("the width of the column must be smaller than or equal to %d characters", MaxColumnWidth)
    // ErrOutlineLevel defined the error message on receive an invalid outline
    // level number.
    ErrOutlineLevel = errors.New("invalid outline level")
    // ErrCoordinates defined the error message on invalid coordinates tuples
    // length.
    ErrCoordinates = errors.New("coordinates length must be 4")
    // ErrExistsWorksheet defined the error message on given worksheet already
    // exists.
    ErrExistsWorksheet = errors.New("the same name worksheet already exists")
    // ErrTotalSheetHyperlinks defined the error message on hyperlinks count
    // overflow.
    ErrTotalSheetHyperlinks = errors.New("over maximum limit hyperlinks in a worksheet")
    // ErrInvalidFormula defined the error message on receive an invalid
    // formula.
    ErrInvalidFormula = errors.New("formula not valid")
    // ErrAddVBAProject defined the error message on add the VBA project in
    // the workbook.
    ErrAddVBAProject = errors.New("unsupported VBA project extension")
    // ErrMaxRows defined the error message on receive a row number exceeds maximum limit.
    ErrMaxRows = errors.New("row number exceeds maximum limit")
    // ErrMaxRowHeight defined the error message on receive an invalid row
    // height.
    ErrMaxRowHeight = errors.New("the height of the row must be smaller than or equal to 409 points")
    // ErrImgExt defined the error message on receive an unsupported image
    // extension.
    ErrImgExt = errors.New("unsupported image extension")
    // ErrMaxFileNameLength defined the error message on receive the file name
    // length overflow.
    ErrMaxFileNameLength = errors.New("file name length exceeds maximum limit")
    // ErrEncrypt defined the error message on encryption spreadsheet.
    ErrEncrypt = errors.New("not support encryption currently")
    // ErrUnknownEncryptMechanism defined the error message on unsupported
    // encryption mechanism.
    ErrUnknownEncryptMechanism = errors.New("unknown encryption mechanism")
    // ErrUnsupportedEncryptMechanism defined the error message on unsupported
    // encryption mechanism.
    ErrUnsupportedEncryptMechanism = errors.New("unsupported encryption mechanism")
    // ErrUnsupportedHashAlgorithm defined the error message on unsupported
    // hash algorithm.
    ErrUnsupportedHashAlgorithm = errors.New("unsupported hash algorithm")
    // ErrPasswordLengthInvalid defined the error message on invalid password
    // length.
    ErrPasswordLengthInvalid = errors.New("password length invalid")
    // ErrParameterRequired defined the error message on receive the empty
    // parameter.
    ErrParameterRequired = errors.New("parameter is required")
    // ErrParameterInvalid defined the error message on receive the invalid
    // parameter.
    ErrParameterInvalid = errors.New("parameter is invalid")
    // ErrDefinedNameScope defined the error message on not found defined name
    // in the given scope.
    ErrDefinedNameScope = errors.New("no defined name on the scope")
    // ErrDefinedNameduplicate defined the error message on the same name
    // already exists on the scope.
    ErrDefinedNameduplicate = errors.New("the same name already exists on the scope")
    // ErrCustomNumFmt defined the error message on receive the empty custom number format.
    ErrCustomNumFmt = errors.New("custom number format can not be empty")
    // ErrFontLength defined the error message on the length of the font
    // family name overflow.
    ErrFontLength = errors.New("the length of the font family name must be smaller than or equal to 31")
    // ErrFontSize defined the error message on the size of the font is invalid.
    ErrFontSize = errors.New("font size must be between 1 and 409 points")
    // ErrSheetIdx defined the error message on receive the invalid worksheet
    // index.
    ErrSheetIdx = errors.New("invalid worksheet index")
    // ErrUnprotectSheet defined the error message on worksheet has set no
    // protection.
    ErrUnprotectSheet = errors.New("worksheet has set no protect")
    // ErrUnprotectSheetPassword defined the error message on remove sheet
    // protection with password verification failed.
    ErrUnprotectSheetPassword = errors.New("worksheet protect password not match")
    // ErrGroupSheets defined the error message on group sheets.
    ErrGroupSheets = errors.New("group worksheet must contain an active worksheet")
    // ErrDataValidationFormulaLength defined the error message for receiving a
    // data validation formula length that exceeds the limit.
    ErrDataValidationFormulaLength = errors.New("data validation must be 0-255 characters")
    // ErrDataValidationRange defined the error message on set decimal range
    // exceeds limit.
    ErrDataValidationRange = errors.New("data validation range exceeds limit")
    // ErrCellCharsLength defined the error message for receiving a cell
    // characters length that exceeds the limit.
    ErrCellCharsLength = fmt.Errorf("cell value must be 0-%d characters", TotalCellChars)
    // ErrOptionsUnzipSizeLimit defined the error message for receiving
    // invalid UnzipSizeLimit and UnzipXMLSizeLimit.
    ErrOptionsUnzipSizeLimit = errors.New("the value of UnzipSizeLimit should be greater than or equal to UnzipXMLSizeLimit")
    // ErrSave defined the error message for saving file.
    ErrSave = errors.New("no path defined for file, consider File.WriteTo or File.Write")
    // ErrAttrValBool defined the error message on marshal and unmarshal
    // boolean type XML attribute.
    ErrAttrValBool = errors.New("unexpected child of attrValBool")
    // ErrSparklineType defined the error message on receive the invalid
    // sparkline Type parameters.
    ErrSparklineType = errors.New("parameter 'Type' must be 'line', 'column' or 'win_loss'")
    // ErrSparklineLocation defined the error message on missing Location
    // parameters
    ErrSparklineLocation = errors.New("parameter 'Location' is required")
    // ErrSparklineRange defined the error message on missing sparkline Range
    // parameters
    ErrSparklineRange = errors.New("parameter 'Range' is required")
    // ErrSparkline defined the error message on receive the invalid sparkline
    // parameters.
    ErrSparkline = errors.New("must have the same number of 'Location' and 'Range' parameters")
    // ErrSparklineStyle defined the error message on receive the invalid
    // sparkline Style parameters.
    ErrSparklineStyle = errors.New("parameter 'Style' must between 0-35")
)
```

Source relationship and namespace list, associated prefixes and schema in which it was introduced:

```go
var (
    SourceRelationship                      = xml.Attr{Name: xml.Name{Local: "r", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/officeDocument/2006/relationships"}
    SourceRelationshipCompatibility         = xml.Attr{Name: xml.Name{Local: "mc", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/markup-compatibility/2006"}
    SourceRelationshipChart20070802         = xml.Attr{Name: xml.Name{Local: "c14", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2007/8/2/chart"}
    SourceRelationshipChart2014             = xml.Attr{Name: xml.Name{Local: "c16", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2014/chart"}
    SourceRelationshipChart201506           = xml.Attr{Name: xml.Name{Local: "c16r2", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/drawing/2015/06/chart"}
    NameSpaceSpreadSheet                    = xml.Attr{Name: xml.Name{Local: "xmlns"}, Value: "http://schemas.openxmlformats.org/spreadsheetml/2006/main"}
    NameSpaceSpreadSheetX14                 = xml.Attr{Name: xml.Name{Local: "x14", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/spreadsheetml/2009/9/main"}
    NameSpaceDrawingML                      = xml.Attr{Name: xml.Name{Local: "a", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/main"}
    NameSpaceDrawingMLChart                 = xml.Attr{Name: xml.Name{Local: "c", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/chart"}
    NameSpaceDrawingMLSpreadSheet           = xml.Attr{Name: xml.Name{Local: "xdr", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing"}
    NameSpaceSpreadSheetX15                 = xml.Attr{Name: xml.Name{Local: "x15", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"}
    NameSpaceSpreadSheetExcel2006Main       = xml.Attr{Name: xml.Name{Local: "xne", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/excel/2006/main"}
    NameSpaceMacExcel2008Main               = xml.Attr{Name: xml.Name{Local: "mx", Space: "xmlns"}, Value: "http://schemas.microsoft.com/office/mac/excel/2008/main"}
    NameSpaceDocumentPropertiesVariantTypes = xml.Attr{Name: xml.Name{Local: "vt", Space: "xmlns"}, Value: "http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes"}
)
```
