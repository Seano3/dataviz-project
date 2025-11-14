# South Shore Population 

This project explores population changes across towns in the South Shore of Massachusetts from 2000–2023. What began as a simple line-chart exploration evolved into a fully interactive geographic visualization. This report documents the design process from early sketches to the final interactive map.

Final Visulazation:
[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/Map%20with%20polish.png)](https://vizhub.com/Seano3/4977b613915f4d03bfc6390f6a7240e6)


## Motivation
Population changes in small, neighboring towns often reflect larger regional patterns, such as economic shifts, housing development, demographic changes, or major local events. By comparing towns side-by-side, we can see not only how each individual population evolves but also how the rise or fall of one town may relate to changes in its neighbors.

This area was particularly intersiting to me beacue it is the area I grew up in so the events of the past 25 years are very fammilular to me. 

## Design Process 

### Early Sketches 

To begin the process I started sketching out my inital ideas for what I would want my visulazation to look like. 

![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/Sketch.png)

The left sketch shows population over time for three towns. The right shows year-over-year percentage change. While percent change can reveal dramatic differences, the raw population graph provides more complete context.

Initaly I did not have plans to create the map that can be seen in the final product. 

### Inital Prototype

My first goal was to make a population line plot for just one of the towns. For this, I chose the town of Cohasset, the town I grew up in. 

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/Prototype.png)](https://vizhub.com/curran/eab039ad1765433cb51aad167d9deae4)

After this I created another graph with 3 additional nearby towns

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/ManyTownsPop.png)](https://vizhub.com/Seano3/cb0574f1bf2a4d4990f6bde2f0d4c8fc)

Additionaly I alse created a % change graph using the same data

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/ManyTowns%25Change.png)](https://vizhub.com/Seano3/64cf3668cd254e7694512d93c9ff673a)

As I added more data, I found that percent change became increasingly crowded and less useful. Especially when towns had very different starting populations as some of the smaller one would get lost in the background.

### Transition to a Map Based Visulazation 

Because these are real geographic locations, I wanted to experiment with representing the towns as a map, with color indicating year-over-year change and text showing the current population.

Before committing to full shapes, I prototyped using simple boxes:

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/boxes.png)](https://vizhub.com/Seano3/dd8280e02083447087ab86f3dc94b14c)

I was excited about this idea becuase it clearly visulaized the percent change of each town without drowning some of them out. Planning for the future, I also added a legend that would highlight the town the user was hovering over to be able to quickley find it on the map. 

### Return of the Line Plots

I still belived the visulation of the line plot would be usefull for anyone wanting to read this graph. I came up with the idea to add more interactiblity by adding that if a user clicked on a town, a line plot for that town's population would appear. 

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/Interactiviblity.png)](https://vizhub.com/Seano3/4977b613915f4d03bfc6390f6a7240e6)

### Forming the Map

Much of the final development time was spent converting simple boxes into the actual geographic shape of the South Shore.

To accomplish this, I built a coordinate conversion tool cordConverter.html that let me translate points from a reference image into relative SVG coordinates. This made it possible to accurately place and scale each town on the final map.

I also added additional towns to fill in the map and polished the interactions further. 

[![image](https://raw.githubusercontent.com/Seano3/dataviz-project/refs/heads/master/Map%20with%20polish.png)](https://vizhub.com/Seano3/4977b613915f4d03bfc6390f6a7240e6)

### Results 
The final visualization is an interactive map of the South Shore, showing:

- population for each town
- Year-over-year percent change via color
- Clickable towns that reveal historical line charts
- Hover highlighting for quick identification
- Time slider allowing users to play back years of population change


### Future Plans 
- The ability to see two towns or more on the line plot
- Zoom/pan support