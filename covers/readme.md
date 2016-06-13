# Covers for screen PDF

PDF files, PNG or JPEG images can be placed as front or back covers, depending 
on their place in the layout sequence:

```
 <SetVariable variable="chaptertype" select="'frontcover'"/>
   <PlaceObject column="0mm" row="0mm">
     <Image file="front_cover.pdf" width="140mm" height="215mm"/>
   </PlaceObject>
```

Vector text can be overlaid on the image, allowing for cover designs to be 
re-used with different translations.
