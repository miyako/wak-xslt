wak-xslt
========

Wakanda XSLT module.

About
-----
* [libxslt](http://xmlsoft.org/libxslt/)/1.1.28
* [libxml2](http://xmlsoft.org)/2.9.2
* [libiconv](https://www.gnu.org/software/libiconv/)/1.14: Mac and Windows. On Linux, the native iconv.

**Note**: zlib dependency is disabled for simplicity. 

Example
-------
```
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
