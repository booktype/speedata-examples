# Book design

Standard Truetype fonts for Latin languages are supported. A page layout with 
left and right footers can be achieved with:

```
 <Case test="sd:even(sd:current-page())">
``` 

CMYK colours can be defined for consistent use throughout the layout, 
for example:

```
 <DefineColor name="separator-first" model="cmyk" c="0" m="0" y="0" k="70"/>
```

Master pages can be defined with:

```
  <Pagetype name="separator" test="$chaptertype = 'separator'">
```

and selected in the layout with:

```
 <SetVariable variable="chaptertype" select="'separator'" />
```

Where the master page changes, a new page can be forced with:

```
 <NewPage />
```

Background PDFs can be used in pages.

## Bleeds for litho PDF

Bleeds are supported by using negative position numbers when placing PDF files, 
PNG or JPEG images on a page. 

Images can also specify a solid background colour (if previously defined with 
DefineColor) which fills the bleed area:

```
 <PlaceObject column="-3mm" row="-3mm" background="full" backgroundcolor="separator-background">
   <Image file="globe.pdf" width="146mm" height="221mm"/>
 </PlaceObject>
```

Transparent PDF images can be layered over the background image, as long as 
they are placed later in the layout file (first object placed is the bottom 
layer):

```
 <PlaceObject column="100mm" row="100mm">
   <Image file="year.pdf" width="46mm" height="100mm"/>
 </PlaceObject>
```
