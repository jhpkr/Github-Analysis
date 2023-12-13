Welcome!

This project explores publicly available GitHub repositories and commit history data (~1.36 TB) to analyze the effects of TuringBots and similar AI tools on Software Engineers and Data Scientists.
There are 5 different data sets that are used for the analysis: 
- Commits: Each commit has metadata such as the author, committer, commit date, SHA, parent commit(s), and commit message.
- Files: Contains metadata about the files in the repositories such as the file path, the mode, and the blob ID which links back to the content.
- Licenses: Contains information on the licenses used by repositories.
- Language: Contains information on the languages used by repositories.
- Contents: Provides contents of the files on the repositories.
PySpark was used for this analysis.

For this analysis, I have looked into the timeline of the data, which programming languages were most frequently used throughout the times, distribution of the most popular licenses, most popular and rapidly growing repositories, and analyzed any trends in which would point to the rise of AI.
