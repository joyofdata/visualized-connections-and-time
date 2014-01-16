# inter-conn 0.0.0  
Tool for visualizing how entities are related in context of time.

## CSVs

Three CSV data sets:
- nodes
- links
- events

If you want to load the data from CSV files then the name of a file needs to contain the string "nodes", "links" or "events" depening on what data is contained.

### nodes:
- `id`: ID node can be referred to with. Also used as label in graph.
- `name`: Full name of nodes entity. Displayed in graph when you hover over a node.
- `type`: "human", "thing" or "firm". Determines color of node.
- `desc`: Description of node's entity shown in link info box.
- `src`: Sources for claims made.

### links:
- `idA`,`idB`: Nodes to be connected. Link is undirected.
- `type`: "guesswork" or "known" depending on reliability of information.
- `desc`: Description of the connection.
- `src`" Sources for claims made.

### events:
- `date`: Format is YYYY-MM-DD (13 January 2013 = 2013-01-13)
- `title`: Short title of event. Used in header of event displayed in the event info box.
- `desc`: Description of the event.
- `nodes`: IDs of involved nodes. Highlighted when hovering over header of event in event info box.
- `src`: Sources for claims made.

### the `src` field:
- `(http://www.example.org)`
- `(http://www.google.com)[search term 'test']`
- `['a book title' page 32]`
