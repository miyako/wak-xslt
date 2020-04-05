wak-xslt
========

Wakanda XSLT module.

About
-----
* [libxslt](http://xmlsoft.org/libxslt/)/1.1.28
* [libxml2](http://xmlsoft.org)/2.9.2
* [libiconv](https://www.gnu.org/software/libiconv/)/1.14: Mac and Windows. On Linux, the native iconv.

**Note**: zlib dependency is disabled for simplicity. 

![obsolete-word-black-frame-word-obsolete-word-black-frame-d-rendering-123942590](https://user-images.githubusercontent.com/1725068/78463940-29122280-771e-11ea-8be8-a7830725403e.jpg)

Old Wakanda.

Example
-------
```js
var modulesFolder = FileSystemSync('Modules');
var xslt = require(modulesFolder.path + "xslt");

var xmlPath = application.getFolder().path + "Documents/sample.xml";
var xslPath = application.getFolder().path + "Documents/sample.xsl";

var options = {
	'params':{
		'param1':"'string'", 
		'param2':"xPath", 
		'param3':'123'
	}
};

xslt.apply(xmlPath, xslPath, options).console.stdOut.toString();
```
