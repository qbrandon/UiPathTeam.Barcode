# UiPathTeam.Barcode

### Links

Component on UiPath Marketplace https://marketplace.uipath.com/listings/470

### Description

This is an activity package exposing 3 activities:
* Decode Image: will decode a barcode embedded inside an image (`UiPath.Core.Image` instance) into a string
* DecodeMuultiple Image: will decode multiple barcodes embedded inside an image (`UiPath.Core.Image` instance) into an array of string
* Encode String: will encode an input string into the desired barcode format

The underlying library used to handle the barcode processing is ZXing (https://github.com/zxing/zxing)

About `Encode String`
1. The formats available are described here: https://zxing.github.io/zxing/apidocs/com/google/zxing/BarcodeFormat.html
2. The `PureBarcode` argument allows the developer to choose whether the human readable data should be embedded below the barcode or not.
Please note that this argument may not apply to some code types, such as `QR_CODE`, in which case the `PureBarcode` value will be ignored.

### Setup

Please make sure that your Studio or Robot have access to the nuget.org feed (where the ZXing nupkg is hosted)
For the record here is the URL: https://api.nuget.org/v3/index.json

As for Marketplace itself, please refer to the following FAQ: https://docs.uipath.com/marketplace/docs/faq-integration-with-uipath-studio

Once the package intalled via the Package Manager in your specific project, you should see the activties be available in the Activity panel, under the UiPathTeam category.
