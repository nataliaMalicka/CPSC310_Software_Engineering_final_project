# CPSC310_Software_Engineering_final_project

I worked mostly on the backend of this project, building the query engine, and for front end, implementing the map and distance features on the UI in pacman flavour. The project is a custom database that supports filtering, aggregations, and sorting across two dataset types (course sections and campus rooms). Queries are parsed into a tree structure where leaf nodes handle comparisons (GT, LT, EQ, IS with wildcard support) and parent nodes handle boolean logic (AND, OR, NOT). The tree filters the dataset in a single recursive pass. When transformations are present, results are grouped by specified keys and reduced using aggregate operations (MAX, MIN, AVG, SUM, COUNT). Final results are projected onto the requested columns and sorted, with support for multi-key directional ordering. Validation runs throughout the pipeline to catch malformed queries and ensure only one dataset is referenced at a time.

The demo below showcases the UI functionality alongside its corresponding server requests and responses.

Built with TypeScript and Node.js. Query results are persisted to disk using fs-extra, and datasets are ingested from base64-encoded zip files processed with JSZip. The Decimal.js library is used for precision in aggregate calculations. The frontend UI was built with React. Testing was done with Mocha and Chai.

Note:
Completed as part of a course in Software Engineering.
Code not included in this repository intentionally to safeguard course content. 
    
<br>
<b>See video preview</b>:
<br>

<a href="https://youtu.be/CFxNFJkqrrk
" target="_blank"><img src="https://img.youtube.com/vi/CFxNFJkqrrk/maxresdefault.jpg" width="480" height="360" border="10" /></a>
