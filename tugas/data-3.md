# Tugas 3: Mengolah data

## Objective

Create a timeline and a map using SPARQL that show the same twenty items that
you have created.

Ideally your dataset is the same dataset that was created in task 2.

You may need to create additional items and statements so that the same twenty items
appear in the timeline and on the map.

These presentations may include other items which you did not create.

## Background

Wikidata has a query service which can generate maps and timelines.

Wikidata Query Service is at https://query.wikidata.org/ .

The query to build the set is written in SPARQL.

When the columns of the result include a Point object, Wikidata Query Service
allows the data to be shown on a map.

When the columns of the result include a Date object, Wikidata Query Service
allows the data to be shown on a timeline.

The display type can be changed after the query is run.

The default output can be pre-selected with a comment, like

```
#defaultView:Timeline
```
or
```
#defaultView:Map
```

An example timline is

http://tinyurl.com/jrv757r

An example map is

http://tinyurl.com/yceuoqne

## Submission

Once you have built your query that fulfils the requirements,
create a page on Wikidata in your 'userspace' with the two queries.

Go to https://www.wikidata.org/wiki/User:your_username/BKSMA-task3
and click Create.

To prevent the wiki parser from breaking your syntax,
surround your query code with `pre` tags.

```
<pre>
your query code here
</pre>
```

Preview and save, and share the link with your mentor for assessment.

## References

- https://en.wikibooks.org/wiki/SPARQL
- https://en.wikibooks.org/wiki/SPARQL/Wikidata_Query_Service
- https://www.wikidata.org/wiki/Wikidata:SPARQL_tutorial
- https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service
