# XML Tree Structure
XML documents are formed as element trees.

An XML tree starts at a root element and branches from the root to child elements.

## All elements can have sub elements (child elements):

```
<root>
  <child>
    <subchild>.....</subchild>
  </child>
</root> 
```

Self-Describing Syntax
XML uses a much self-describing syntax.

## A prolog defines the XML version and the character encoding:

```<?xml version="1.0" encoding="UTF-8"?>```
The next line is the root element of the document:

```<bookstore>```
The next line starts a ```<book>``` element:

```<book category="cooking">```
The ```<book>``` elements have 4 child elements: ```<title>```, ```<author>```, ```<year>```, ```<price>```.

```<title lang="en">Everyday Italian</title>
<author>Giada De Laurentiis</author>
<year>2005</year>
<price>30.00</price>
```
### The next line ends the book element:

```</book>```
You can assume, from this example, that the XML document contains information about books in a bookstore.




### Example: XML News
```
<?xml version="1.0" encoding="UTF-8"?>
<nitf>
  <head>
    <title>Colombia Earthquake</title>
  </head>
  <body>
    <headline>
      <hl1>143 Dead in Colombia Earthquake</hl1>
    </headline>
    <byline>
      <bytag>By Jared Kotler, Associated Press Writer</bytag>
    </byline>
    <dateline>
      <location>Bogota, Colombia</location>
      <date>Monday January 25 1999 7:28 ET</date>
    </dateline>
  </body>
</nitf>
```


## XML Documents Must Have a Root Element
XML documents must contain one root element that is the parent of all other elements:

```
<root>
  <child>
    <subchild>.....</subchild>
  </child>
</root>
```

### In this example <note> is the root element:
```
<?xml version="1.0" encoding="UTF-8"?>
<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>
```

### This line is called the XML prolog:

```<?xml version="1.0" encoding="UTF-8"?>```

UTF-8 is also the default encoding for HTML5, CSS, JavaScript, PHP, and SQL.

Note: The XML prolog does not have a closing tag! This is not an error. The prolog is not a part of the XML document.

The XML prolog is optional. If it exists, it must come first in the document.

To avoid errors, you should specify the encoding used, or save your XML files as UTF-8.

UTF-8 is the default character encoding for XML documents.

### All XML Elements Must Have a Closing Tag
In XML, it is illegal to omit the closing tag. All elements must have a closing tag:

```
<p>This is a paragraph.</p>
<br />
```

Opening and closing tags must be written with the same case:

```<message>This is correct</message>```

"Opening and closing tags" are often referred to as "Start and end tags". Use whatever you prefer. It is exactly the same thing.

## ! XML Elements Must be Properly Nested
In HTML, you might see improperly nested elements:

```<b><i>```This text is bold and italic```</b></i>```
In XML, all elements must be properly nested within each other:

```<b><i>```This text is bold and italic```</i></b>```
In the example above, "Properly nested" simply means that since the <i> element is opened inside the```<b>```element, it must be closed inside the ```<b>``` element.

### XML Attribute Values Must Always be Quoted
XML elements can have attributes in name/value pairs just like in HTML.

In XML, the attribute values must always be quoted:
```
<note date="12/11/2007">
  <to>Tove</to>
  <from>Jani</from>
</note>
```

To avoid this error, replace the ```"<"``` character with an entity reference:

```<message>salary &lt; 1000</message>```

### There are 5 pre-defined entity references in XML:

```
&lt;	<	less than
&gt;	>	greater than
&amp;	&	ampersand 
&apos;	'	apostrophe  or single quote (')
&quot;	"	Quote or double quote (“)
```

Comments in XML
The syntax for writing comments in XML is similar to that of HTML:

<!-- This is a comment -->

XML Stores New Line as LF
Windows applications store a new line as: carriage return and line feed (CR+LF).

Unix and Mac OSX use LF.

Old Mac systems use CR.

XML stores a new line as LF.



An XML breakfast menu

```
<?xml version="1.0" encoding="UTF-8"?>
<breakfast_menu>
  <food>
    <name>Belgian Waffles</name>
    <price>$5.95</price>
    <description>Two of our famous Belgian Waffles with plenty of real maple syrup</description>
    <calories>650</calories>
  </food>
  <food>
    <name>Strawberry Belgian Waffles</name>
    <price>$7.95</price>
    <description>Light Belgian waffles covered with strawberries and whipped cream</description>
    <calories>900</calories>
  </food>
  <food>
    <name>Berry-Berry Belgian Waffles</name>
    <price>$8.95</price>
    <description>Light Belgian waffles covered with an assortment of fresh berries and whipped cream</description>
    <calories>900</calories>
  </food>
  <food>
    <name>French Toast</name>
    <price>$4.50</price>
    <description>Thick slices made from our homemade sourdough bread</description>
    <calories>600</calories>
  </food>
  <food>
    <name>Homestyle Breakfast</name>
    <price>$6.95</price>
    <description>Two eggs, bacon or sausage, toast, and our ever-popular hash browns</description>
    <calories>950</calories>
  </food>
</breakfast_menu>
```