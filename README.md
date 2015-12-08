#graph-chooser

##### A treemap to guide what graph to use based on what variables you have

## Background

I'm working on a guide of what graph to use to plot your data. I'm not a statistician so I get confused when reading guides for what graphs to pick made my statisticans. They're all about intent. "What information specifically do you want to extract from the data?", "What message are you trying to convey?", "Are you looking for a relationship or a composition?", etc. 

More often I just find myself with a bunch data and want to visualize it. Graphing it helps me understand it better. There's no other ulterior motive or goal. I just have a table and need to know how to represent it based soley on the data. So I'm creating this for myself and others like me.

## Data organization/structure

I got stuck with the following scenario when first starting this project: I could take the same data and structure it differently, resulting in me not being sure how many and what kind of variables an item had. 

For instance, I look at this table and think: There are four variables, one categorical and three numerical.



| Season | Sales | Expenses | Profit |
|--------|-------|----------|--------|
| Winter |  1000 |  400     |    200 |
| Spring |  1170 |  460     |    250 |
| Summer |  660  |  1120    |    300 |
| Fall   |  1030 |  540     |    350 |

But I rearrange that table, with the exact same data, and suddenly it has three variables, two categorical and one numerical. 


| Season | Type    | Dollars  |
|--------|---------|----------|
| Winter |Sales    | 1000     |
| Winter |Expenses | 400      |
| Winter |Profit   | 250      |
| Spring |Sales    | 1170     |
| Spring |Expenses | 460      |
| Spring |Profit   | 250      |
| Summer |Sales    | 660      |
| Summer |Expenses | 1120     |
| Summer |Profit   | 300      |
| Fall   |Sales    | 1030     |
| Fall   |Expenses | 540      |
| Fall   |Profit   | 350      |


The difference here is between [**wide and narrow**](https://en.wikipedia.org/wiki/Wide_and_narrow_data) data. For the purposes of this guide, everything will be in regards to the **narrow** structure (called **long** in R).


[Live (unsynchronized) version here](crclayton.com/projects/graph-chooser/index.html)

![Example](Example.png)

## Example Images

These should be `400x400` `.PNG` files. I want to keep them square and I want to keep them small so they load quick. Time lags look really bizarre. 

Where possible, use highcharts to get the image so the examples have a consistent appearance.

They must have the same filename (not including the extension) as their name in the data.json name attribute. The extension must be all lower case.

Ex. `{ "name": "Example graph name" }` must have an image in the `img` directory called `Example graph name.png`

## Questions

These should be consistent and exclusively about the data.

1. How many variables?

2. Numerical or categorical?

3. Are numerical variables discrete or continuous?

4. Are categorical variables ordinal or nominal?