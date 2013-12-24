designation-style
=================

osm2pgsql "style.lua" that causes the standard map style to render England/Wales access "designations" in preference to highway or tracktype.

The "standard" stylesheet contains rules for different sorts of tracks (tracktype), but doesn't contain rules for English/Welsh rights of way designations.

The changes here do the following:

1. Render any non-designated footway, bridleway or track as "path" (grey dashes in the "standard" style)
2. Render anything designated as "public_footpath" as a "footway" (dotted salmon)
3. Render anything designated as "public_bridleway" as a "footway" (dotted green)
4. Render anything designated as "restricted_byway" as a "grade4 track" (dashed and dotted brown).
5. Render anything designated as "byway_open_to_all_traffic" as a "grade3 track" (dashed brown)

These changes do mean that the the resulting database isn't any use for anything other than rendering, but they do allow designations to be displayed without any stylesheet changes.  Also, some information is lost in the process (e.g. track or steps vs path).

