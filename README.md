# Shortly

Shortly is a serverless pastebin service. Everything happens on the client side, and the data is stored in the URL.

## How it works

Data is compressed using the deflate algorithm, then base64 encoded to ensure it can be stored safely in a URL. It is then set as the `window.location.hash` of the current page.

You can view an example [here](http://www.intrepide-prod.com/shortly/index.html?d=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4&l=html&t=tomorrow) and another [here](http://www.intrepide-prod.com/shortly/index.html?d=wqVWS2/DmzAMPmfCv0LDg8K6Wm5SwqcZwoYBXRAUw6vCtkMPwrvCrFsvQQbCqDZjG1HDrEDCksOTBm3DvsO7SMOJdsOswrpNw7Y4w4TCpiTDssOjQ8Okw6fDsHnCkcKFJsONM8Ouw7ceXsO1wo7DuG7DjXDDnVsLw4UgSk3CrsOYwoTCiRACWnAvw41WwoU5wp3CpyAjw48fwqPCnsOTCTTCmB8JLMKBe8KoOzQkDsODRMOlS2jCqcOFYMKuQWvDq8KGbMK+w6VRacKyRGlow6DDnjh9cn8rNHx4P2BhAsOhwqJ8w6liOWARw4zCpTAQDRhkIcOawqFgw6Miw4NKC8Kjwq4zw5JGwqVZw6zDssKyw4hhYsOxFMOawpENGi1Qw7/DjMOKc8OMwpjCpwjDiFpmwqhDwpVwe8OTdDYuNxfCrD8hwqggTMKEw7rCjMOBfDLDvMOMZyfChMORZyPCm0xvSw8FwqZQGcO5Zm/DmcOIOsObw5LDo8KIe2/CtFjDg8OpbWFMwp55fhDDijRcPMK9wpDCnk0RQ8OYwpXDskbDiALCuHNRw5UEFcK+wovCuy9uFcKUwrvDnMOaOkVXVVTCu8K0QmByJ8OwCsOBL0vCgnVkwpPCusOqw5zDmcK5w4PCssOseFzCosO1wp3Cnj3CvEvCsyjCvwtkHgoKH8KVwrBrIsK4DxLCs8KUF8ORw4RDw60KwqDDj8K8Y2l3wqgKUmRxIWJswplgLSTDpk3Dh8KmPsK2XVXCncK5wqTDs8KwWEJmwqgYXyXCkHjCucK5worCuMK3TsOhDjXCtcOZSCxCwqpXUmwowpBbwoxqw6FZW0J0w51cKMKJwroIwoEXR8OgBcKgw6rCkyzDrG3DucOVdVXCkcOgwp1nMXRuasOPTDzCm8KLw59Gb8KUYcK/woMDw5PDtFJZG8Ouw5I5w6PCiMOyU8OJG8KhNMO3wqdew6TDjUonw79Tw5xdwoN0w5DDm01YKgYaWx7DuMOZwoDDsWpHQhbCm8KEwp3CsnfDlAcjw7bDuMOIw47DocK8w53CnCvChMKFwqvDjMOwNkwHYlQzRcK1w5dAdMKQVAkHw7t6w5LDrcO6wooEDjTCjXfCjcKEZxJkCBbDp8KGwoXCuVLDhcKKwobDsiN3dWnCtMKGG8OefRYldzDCkBpKw7/CjSkvw4d3wo4cWw5wc0JrwrZowpBBwpo5MmgPw7o/DEI3wo0Gwr9UZ8KhBMKhwq5BQsOZwrk1EW7Cn8OtO1PDt8OdwoHDqcOpwprDrcKnwoJqw5LCtA0FwqIrw6LCosKaw60PwppVZcOowrgdwr/CmMKKfMKaw4ofw4xpF2F/eMKNwpnDvsOLw4TDmmzDsExuwrLDjsKNOGLCiyQkwqTDpMOYwqMawpcVE8K1bChZw7rCrMOiTyPDnAN9w5Zowo3Do2l0wrfChcKCRMOBPFDCgMK8woHDgzrCnF4cw4/DunzDumvCgi9/woLDgsOxw6zDhB/DhsOpYMO3AV8OFsKwGcOYcMOrfyd6wop7M0TCt8ObYxdtw7XCkcKlc8KMw7032&l=javascript&t=eclipse).

Different browsers have different limits of the total URL length, however around 2000 characters seems to be the recommended safe maximum. At the moment there is currently nothing to enforce the limit, however a checksum is added to check that we get all the data.

You may be thinking that these really long urls are an issue, but that isn't the case. Testing [bit.ly](http://bit.ly/) and [t.co](http://t.co/) with these urls worked without issues. You could even chain them together in order to deal with longer data...

## Attribution

This uses the following libraries:

* [jQuery](http://jquery.com/)
* [js-base64](https://github.com/dankogai/js-base64)
* [js-deflate](https://github.com/dankogai/js-deflate)
* [ace](https://github.com/ajaxorg/ace-builds/)

## Get Involved

Fork, commit, send pull request, drink beer.

## Press

* [Shortly: a Serverless Pastebin Service - All Data is Stored in the URL](https://news.ycombinator.com/item?id=5696127) (2013)
* [Show HN: Shortly, a serverless pastebin](https://news.ycombinator.com/item?id=3834643) (2012)
* [Korben: Shortly – Un clone de pastebin sans base de données](http://korben.info/shortly-un-clone-de-pastebin.html) (2013)

## License

Remake by hmsintrepide

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/InteractiveResource" property="dct:title" rel="dct:type">shortly</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/lucaspiller/shortly" property="cc:attributionName" rel="cc:attributionURL">Luca Spiller</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike 3.0 Unported License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/lucaspiller/shortly" rel="dct:source">github.com</a>.<br />Permissions beyond the scope of this license may be available at <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/lucaspiller/shortly" rel="cc:morePermissions">https://github.com/lucaspiller/shortly</a>.