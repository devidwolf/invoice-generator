# **Invoice Generator**
A simple tool to generate invoices right from your browser by using its print API for PDF saving.

---

## **Features**
- complete manipulation of invoice items (edit, clone, delete, order)
- automatic calculations of item price and total price
- custom inline html (e.g. use hyperlinks for: [Web](https://example.com), [PayPal.Me](https://paypal.me), ```mailto:```, ```tel:```)
- switch between different languages
- useable offline

---

## **How to**

### use the toolbar
|button|action|
|:---:|---|
|PDF|call print dialog|
|🖩|calculate item position numbers, item prices and total price|

Working with the invoice item selected with the position input:

|button|action|
|:---:|---|
|copy|duplicate selected position|
|🗑️|delete selected position|
|↑|move selected position upwards|
|↓|move selected position downwards|

### save static invoice data
Some data like your address, contact as well as paying details are pretty much static, here is how you can save them, so you do not have to retype everything after a page refresh. To do so, update the JSON inside ```/languages/prefill.js``` to fit your needs.

### add and set translations
1. duplicate an existing translation file in ```/languages```
2. rename it, e.g. ```lang_en.js```
3. write actual translations in JSON-Format
4. update path of import statement in ```/js/lang.js``` to match the new filename

### adjust page format
By default sizes and layouts match paper format *DIN A4* and page margins follow *DIN 5008*. For other standards, change CSS root variables in ```/css/master.css``` to your preferred sizes for page dimensions and margins.

### modify logic for default invoice no. and dates
Per default the invoice number is the current UNIX timestamp and invoice as well as delivery date equal todays date, while the due date is 30 days in the future from today. All that can be modified in ```/js/init.js```.

---

## **Notes**
- best experience in Chromium based browsers (Chrome, Edge, Opera)
- recommended printing settings (Chromium):

|option|value|
|---|---|
|Paper size|A4|
|Margins|None|

---

## **thx vendors**
  - [jQuery](http://jquery.com)
  - [Flexbox Grid](http://flexboxgrid.com)
  - [normalize.css](https://necolas.github.io/normalize.css/)
  - [Material Icons](https://material.io/resources/icons/)
  - [stackoverflow](https://stackoverflow.com) for a lot of useful extensions in ```/js/utilities.js```
