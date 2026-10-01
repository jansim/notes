

## introduction
- many interactive viz tools are being developed for exploratory data analysis and creation of both static as well as interactive data viz
- web technologies have emerged as one of the most popular platforms for these thanks to the ubiquity of browsers, portability and powerful libraries e.g. d3
- many visualizations often require data to be in a particular format or require transformations, even for exploratory plots
- indeed, typical data mining or data science workflows such as CRISP-DM or the data analysis life cycle described in veridical data science are circular altering back and forth between exploratory phases and data manipulation / preparation
- current data viz tools are usually quite focused on addressing specific needs and developed in isolation. They usually reinvent data loading workflows and lack options of manipulating, transforming or wrangling data. Supporting this is out of scope for them, but it leads to poor UX. This also has the downside that polished solutions such as the data loading workflow for e.g. rawgraphs require lots of time and effort to implement.
- abstracting away the data loading and handling will allow for viz tools to focus on viz instead and to separately develop smooth data loading flows as well as adding support for transformation
- this can also allow for easier integration into separate contexts such as a plugin for browser-based IDEs (e.g. VScode, Rstudio, postiron, ...), standalone apps (e.g. via tauri, electron), integration into websites, ...

## methodology
- developed a prototype using web technology, hosting tools in iframes
- dealing with the complexity of highly heterogeneous build pipelines
- data is passed to each tool, with option of passing data back in
- data is transformed to match the expectations of each tool

## conclusion
- prototype shows the feasability of this approach, but at very early stage. looking for input from the field with this paper to understand requirements
- many possiblities with new technologies such as duckdb for efficient data handling and flexible + efficient transformation via SQL
- a general solution could be helpful for integration in other contexts as well such as extensions for interactive notebooks, desktop applications (via e.g. Tauri or electron), ...
- issues exist, though, such as abandoned one-off tools
