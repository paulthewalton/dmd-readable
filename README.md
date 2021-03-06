# Dmd Readable

> A plugin for dmd and jsdoc-to-markdown to provide more readable docs
>
> [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



<br><a name="About"></a>

### About
> Pass the plug-in name to [`jsdoc2md`](https://github.com/jsdoc2md/jsdoc-to-markdown) or [`dmd`](https://github.com/jsdoc2md/dmd):> > ```> jsdoc2md --plugin dmd-readable> ```> > This plugin (which was used to generate this readme) does a few things:> - removes global indexes (see below)> - places descriptions in block-quotes (Use @summary for descriptions without block quotes)> - adds more whitespace before headings> - changes the delimiter for multiple types in param tables to a comma> - adds alias output> > The removal of global indexes is now a setting in the [template](docs.hbs). If you are using your own template and you wish to retain this feature, add the following line to your template:> > ```> {{optionSet "global-index-format" "none"~}}> ```> > All options for global-index-format are "none", "grouped", "table", "dl". Other options and more info can be found [here](https://github.com/jsdoc2md/jsdoc-to-markdown/blob/master/docs/API.md#jsdoctomarkdown-).> > This plugin also provides the following helper functions:


<br><a name="package"></a>

### package(key) ⇒ <code>\*</code>
Reads info from the package.json file.

**See**: [docs.hbs](docs.hbs) for an example of how to use this function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | The package property you want returned |


<br><a name="changeCase"></a>

### changeCase(to, string) ⇒ <code>string</code>
Implements the library [change-case](https://github.com/blakeembrey/change-case).

**See**: _[docs.hbs](docs.hbs) for an example of how to use this function_  

| Param | Type | Description |
| --- | --- | --- |
| to | <code>string</code> | Shorthand or full name for the change-case function. |
| string | <code>string</code> | The string to modify |


<br><a name="prefixLines"></a>

### prefixLines(string, replacer) ⇒ <code>string</code>
Prefixes a string to the beginning of each line in the first string


| Param | Type | Description |
| --- | --- | --- |
| string | <code>string</code> | The string to modify |
| replacer | <code>string</code> | The string to prefix to each line |


<br><a name="findBy"></a>

### findBy(array, key, value) ⇒ <code>array</code>
Finds an object in an array with a matching key: value


| Param | Type | Description |
| --- | --- | --- |
| array | <code>array</code> | The array to search |
| key | <code>string</code> | The key to compare |
| value | <code>string</code> | The value to find |


<br><a name="replace"></a>

### replace(string, pattern, newString) ⇒ <code>string</code>
Calls string.replace


| Param | Type | Description |
| --- | --- | --- |
| string | <code>string</code> | The string to modify |
| pattern | <code>string</code> | The first arg for string.replace |
| newString | <code>string</code> | The second arg for string.replace |


<br><a name="isNew"></a>

### isNew(string) ⇒ <code>boolean</code>
Determines if the provided string is truthy and is different than the string provided the previous time this function was called


| Param | Type |
| --- | --- |
| string | <code>string</code> | 


<br><a name="debugValue"></a>

### debugValue(value) ⇒ <code>string</code>
Return the JSON string representation of a value.

**Author**: Paul Walton  

| Param | Type |
| --- | --- |
| value | <code>\*</code> | 


<br><a name="isSingular"></a>

### isSingular(value) ⇒ <code>boolean</code>
Check if value is not an array or is an array with length of 1.

**Author**: Paul Walton  

| Param | Type |
| --- | --- |
| value | <code>\*</code> | 


<br><a name="overview"></a>

### overview()
Overviews block

**Author**: Paul Walton  
