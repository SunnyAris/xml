# XML
XML is a software- and hardware-independent tool for storing and transporting data.

## What is XML?
XML stands for eXtensible Markup Language
XML is a markup language much like HTML
XML was designed to store and transport data
XML was designed to be self-descriptive

    <note>
      <to>Tove</to>
      <from>Jani</from>
      <heading>Reminder</heading>
      <body>Don't forget me this weekend!</body>
    </note>

The XML above is quite self-descriptive:

It has sender information
It has receiver information
It has a heading
It has a message body
But still, the XML above does not DO anything. XML is just information wrapped in tags.

## The Difference Between XML and HTML

XML and HTML were designed with different goals:

- XML was designed to carry data - with focus on what data is
- HTML was designed to display data - with focus on how data looks
- XML tags are not predefined like HTML tags are

## XML Does Not Use Predefined Tags

The XML language has no predefined tags.

The tags in the example above (like <to> and <from>) are not defined in any XML standard. These tags are "invented" by the author of the XML document.

HTML works with predefined tags like `<p>, <h1>
, <table>,etc.`

With XML, the author must define both the tags and the document structure.