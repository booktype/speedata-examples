# Two column Table of Contents

In Speedata Publisher, the table of contents is generated by creating attributes, which can then be placed like any other:

```
        <ForAll select="planetlisting">
          <Paragraph fontface="contents" textformat="text with indentation">
            <Value select="@name" />
            <Value> </Value>
            <Value select="@pagenumber" />
          </Paragraph>
        </ForAll>
```

This should mean that the design of the table of contents is not restricted to any particular format.