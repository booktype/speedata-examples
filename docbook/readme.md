# DocBook

This example layout is based on data in the DocBook 5.1 standardised format: http://docs.oasis-open.org/docbook/docbook/v5.1/docbook-v5.1.html

When a particular type of data may or may not be included, a conditional statement can be used inside a paragraph:

```
<Switch>
   <Case test="@role = 'graphic_design' and string(personname) != ''">
     <Value>Graphic design by: </Value><Value select="personname"></Value>
   </Case>
</Switch>
```

