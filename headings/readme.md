# Handle widows/orphans in columns

For proper widow and orphan handling in columns, paragraph headings 
(subheadings) also have to be taken into consideration. Otherwise a heading 
may appear in a previous column, separate from the body text it relates to.

Current XML export from Booktype uses one tag after another, so a subheading 
has no special relation with the following body text.

One solution with Speedata is to make the subheading an attribute of the body 
text paragraph, for example:

<C6BodyTextFirstPara subheading="Información general">La falta de un ganador claro en las elecciones presidenciales de abril y las acusaciones de fraude masivo y sistemático contra ambos candidatos en una segunda vuelta celebrada en junio mantuvieron el proceso electoral en punto muerto durante cinco meses.</C6BodyTextFirstPara>

However the InDesign template, if used, would have to be adjusted, assuming it 
can support this option.
