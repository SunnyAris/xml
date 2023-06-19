XML Attributes Must be Quoted
Attribute values must always be quoted. Either single or double quotes can be used.

For a person's gender, the <person> element can be written like this:

<person gender="female">
or like this:

<person gender='female'>
If the attribute value itself contains double quotes you can use single quotes, like in this example:

<gangster name='George "Shotgun" Ziegler'>
or you can use character entities:

<gangster name="George &quot;Shotgun&quot; Ziegler">


XML Elements vs. Attributes
Take a look at these two examples:

<person gender="female">
  <firstname>Anna</firstname>
  <lastname>Smith</lastname>
</person>
<person>
  <gender>female</gender>
  <firstname>Anna</firstname>
  <lastname>Smith</lastname>
</person>
In the first example, gender is an attribute. In the last example, gender is an element. Both examples provide the same information.

There are no rules about when to use attributes or when to use elements in XML.

Avoid XML Attributes?
Some things to consider when using attributes are:

attributes cannot contain multiple values (elements can)
attributes cannot contain tree structures (elements can)
attributes are not easily expandable (for future changes)