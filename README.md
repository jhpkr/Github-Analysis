Welcome!

This project explores publicly available GitHub repositories and commits history data (~1.36 TB) to analyze the effects of TuringBots and similar AI tools on Software Engineers and Data Scientists.
5 different data sets are used for the analysis: 
- Commits: Each commit has metadata such as the author, committer, commit date, SHA, parent commit(s), and commit message.
- Files: Contains metadata about the files in the repositories such as the file path, the mode, and the blob ID which links back to the content.
- Licenses: Contains information on the licenses used by repositories.
- Language: Contains information on the languages used by repositories.
- Contents: Provides contents of the files on the repositories.
**PySpark** was used for this analysis.

For this analysis, I have looked into the timeline of the data, which programming languages were most frequently used throughout the times, distribution of the most popular licenses, and most popular and rapidly growing repositories, and analyzed any trends that would point to the rise of AI.

### Bottom Line
- Although there are some trends hinting to the question of whether or not the TuringBots will provide meaningful improvement, further data collection processes and additional measures are required to determine whether TuringBots will replace software engineers.
- More data needs to be collected to continue tracking the popularity of Generative AI and its impact on the efficiency of Software Engineers.

### Timeline
![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/8b2dc8d3-3fd0-418c-a837-ac8a5e80fe6f)

The figure above shows the number of commits made throughout the time. Data cleaning and filtering were Required to make the data less noisy as some peaks shown in the figure were not considered as 'real events.' For example, one company made over 200,000 commits in one second. In addition, dates that were lower than 2008 and greater than the present year (2023) were removed. 

![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/bcf75f28-d8e1-4337-9155-be26a95ca8af)

The number of commits reached a peak in around 2016 then dwindles to previous levels from 2018. In 2022, GitHub announced that **they have experienced 27% growth in new developers with a 20% YoY growth in new repositories**. Therefore, it is interesting to note the decline in the number of commits starting from the end of 2017. Perhaps, the growth was mostly due to the contributions from private repositories or the graph suggests a data collection issue. Throughout the timeline, there are several sizeable spikes. Upon further inspection of the spikes that are currently being shown in the figure, they considered **‘real’ events as determined by the unique messages during the specific timeframe.**

### Most Popular Programming Languages

![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/4a544852-50d9-4c43-a971-46cbde6a598c)

Found the most popular commits by combining the Language and Commits table. Shell and Python remain to be the most used languages throughout the years. C and C++ phased out throughout the years and were replaced with HTML, JavaScript, and MakeFile.

### Most Popular Licenses
![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/b75d0870-f455-4449-97cc-42074f0c4989)

JavaScript, Java, and Shell are the languages associated with the top 3 licenses. Different Machine Learning and AI-related repositories are licensed under different licenses. For example, the TensorFlow repository is licensed under Apache 2.0 while Scikit is licensed under the BSD license. Therefore, it is difficult to highlight any licenses that are specifically for data-science. 

### Most Popular Repositories
![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/9560e4c6-40cf-41db-b5ba-f6f23aafb56c)
Looking at the most popular repositories, there were several important repositories: Chromium is an open-source project that aims to build a safer way to experience the web developed by Google. CloudFoundry is similar to Kubernetes where it allows developers to build, deploy, and run containerized applications. Powerpc is related to performance computing created by the Apple – IBM – Motorola alliance

### Most Rapidly Growing Repositories
![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/19122691-7c50-479b-b465-90fc1f2b6c1b)
The percentage increase from 2021 to 2022 was calculated to determine the fastest growing repository. For this analysis, the year 2022 was chosen as it was thought to maximize the chance of finding more machine learning or generative AI projects. The most notable repository in this analysis is the Google/Horologist which is Google’s opensource repository for Wear OS (smartwatch). Upon researching the other repository names, there were not any common technologies in common with one another. 

### Exploration into most popular GitHub Committers:
The most prolific committer are bots not associated with Big-tech. 

![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/9a2e082b-3c28-4898-80da-de8d424b3baf)

The most prolific committer is GitHub followed by Gerrit Code Review and Commit Bot. Given that most of the commits are coming from GitHub, it is difficult to determine whether the commits are being made from those who are associated with Big-Tech Companies. The first human committer is Curt Clifton who is a SwiftUI(mobile application development tool) frameworks engineer at Apple followed by James Michael DuPont who is a software developer not associated with any Big-tech companies. The rest of the human committers are also software engineers but they do not seem to be associated with any big-tech companies. 

### Text Duplication Analysis
MinHashLSH is an NLP technique to determine whether two bodies of text are similar based on a measurement called the Jaccard Distance. Performing MinHashLSH within subjects show that most messages are unique. 

![image](https://github.com/jhpkr/Github-Analysis/assets/106620040/7f2e13eb-1157-41d0-9deb-ec4795f32c07)

Had there been a significant number of duplicates, there may be some evidence that committers are directly copy and pasting their code without much thought.



















