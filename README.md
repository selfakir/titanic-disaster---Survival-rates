# Titanic survival : Who were the luckiest ?


## Summary
Back in 1912, the largest passenger liner in service at the time, Titanic, with an estimated 2224 people on board, hit an iceberg and sunk. 68% of the passengers on board died. However, passengers were more likely to survive depending on their gender and  boarding class. This project aims to  visualize survival rates for different categories (gender, classà. So let's see who were the luckiest during this tragic event.
The visualization uses data for 891 passengers where females represented 35% and upper class passengers represented 24% of the total number of passengers in the dataset.

## Design

### Chart type selection
The objective is to compare survival rates for different categories. Since the beggining, the barchart seemed to be the best candidate even if I was tempted to use a pie chart.
The mine challenge was to  give intuitively an insight on both counts (survivors, deaths) and percentages (survival rates, death rates) on the same chart. 

### Percentages vs counts
First, I tried with counts and percentages separately. It was clear to me that I needed to use percentages (normalized data) in the y axis but I wanted to keep an eye on the numbers that were very disparate between classes and gender. How can I do that ? 
Well, for example I could use an interactive legend that will enable switching between two graphs, one for counts and one for percentages. Or, I could simply use the power of tooltip box containing numbers. I wanted to keep it simple so I opted for the tooltip alternative. Moreover, I wasn't satisfied with the tooltip rendering data columns name (Pclass, Survived,...). This is something I didn't want the viewer to see, I had to customize the rendered text in the tooltip anyway.

### Colors & Legend
The default colors weren't behaving as I expected. I had to modify them programatically. Pastel blue for men and Pastel pink for women. colors weren't enough to spot gender categories. So I needed a legend. But what if I only used some labels on the bottom of the bars ? This what I did.


### Axis layout
I decided to hide axis lines and titles because I think that the person who views the visualization would understand with or whitout the titles.

At this stage, I had my first sketch (index.html) and it was time to get some feedbacks.

The feedbaks concerned mainly the colors, the title, the lack/relevancy of data labels on the different chart bars, the x axis class names. After three iterations, I ended with the final visualization (index3.html).



## Feedbacks

I conducted interviews with 3 friends of mine. Many thanks to Ayoub, Youssef and Hanane.


### Feedback 1 (Ayoub)

"Ok I can undertsand that women and 1st class passengers were more lucky to survive but it is not straightforward at all maybe because of the color reprensenting the non-survival rate or because the chart lacks some data labels"

" class 3, class 2, class 1 are counter intuitive"

I added data labels reprensenting numbers for each bart (number of people who died VS number of people who survived) and changed the color for non-survival rates or death rates. 
I also updated the tooltip with survival/death rates. 
I modified the class names on the x Axis to lower, upper, medium class. The result was better and more intuitive. I guessed this was because classes names and survival rates are now moving up together. 
I also asked ayoub if the chart was better with or without axis lines. He suggested that it was better whit axis lines.

The result was index1.html.

### Feedback 2 (Youssef)

"The chart is about survival rate. Right ? well the first think I see are the number for people who survived/died."

I added data labels reprensenting numbers for each bart (number of people who died VS number of people who survived) and changed the color for non-survival rates or death rates. I also updated the tooltip with survival/death rates.
With youssef we tried different sizes for class names and also different number of ticks for the y Axis. We decided to increase the class names font size and decrease the number of ticks.

"The title is long and not engaging...A standard one"
I updated the title to "Titanic disaster : Who were the luckiest ?"

The result was index2.html.

### Feedback 3 (Hanane)

"Females were the most likely to survive. Upper class passengers were lucky."

"Can you try the same color for non survivors....a light one for both males and females"

We played with colors and ended up using a light gray for both males and females.

The final visualization was index3.html.



## Ressources

Online courses : Udacity data visualization course (D3 and dimple.js)

Titanic data set: https://www.kaggle.com/c/titanic-gettingStarted

dimple documentation : https://github.com/PMSI-AlignAlytics/dimple/wiki

dimple js examples: http://dimplejs.org/examples_index.html

colors: http://colors.findthedata.com/saved_search/Pastel-Colors

tooltip customization : http://stackoverflow.com/questions/25334677/override-d3-dimple-tooltips-with-chart-data

