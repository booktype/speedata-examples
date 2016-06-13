# Support CJK text including Simplified Chinese

Supported: Partially

There appears to be no explicit option for CJK text. Sample text in Simplified
Chinese does not render at all when using PostScript outlines or TrueType 
collections. Errors include:

```
LuaTeX warning: lua-loaded font [9] (NotoSansCJKsc-Light) has no characters!
Error: Font 'wqy-zenhei.ttc' could not be loaded!
```

However, a TrueType font did work with Chinese text. The remaining issue was 
that the line breaking did not work as expected, probably because of the lack 
of spaces between Chinese characters.
