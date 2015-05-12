[Udacity](https://www.udacity.com/) Course on Data Visualization and D3.js

Visualization - explanatory
- Context - audience
- Appropriate visualization for audience
- Clutter - identify and eliminate non-value add
- Draw attention - use color, size, placement strategically to guide the viewer
- Story

Slope graphs - plot two data points in time, two groups, two points to compare change [Bachelor's Degree vs. Obesity example](http://vizwiz.blogspot.com/2013/01/alberto-cairo-three-steps-to-become.html)

[Anscombe's Quartet](http://en.wikipedia.org/wiki/Anscombe%27s_quartet) - always plot your data, don't rely of stas - power of visualization

* Ordered - size, oreintation, saturation
* Nominal - hue, shape, texture

Cleveland & McGill paper: Ranking of encondings (More Accurate to Less Accurate)

1. Position
2. Length
3. Angle Slope
4. Area
5. Volume
6. Color Density

Double encoding - using the same variable for both position and size or for x-position and color 

Opacity can make it easier to see where points overlap and to identify multiple points in a similar location

Example - [Facebook IPO Grpahic](http://www.nytimes.com/interactive/2012/05/17/business/dealbook/how-the-facebook-offering-compares.html?_r=0)
- Opacity allows you  to see the overlap
- Color and x-position are used for time
- Log-scale shows comparison 

In SVG/D3 (0,0) is at the top left of the plot/visual area so flip the bounds on the range for y when creating a scale so that it creates the mapped (0,0) in the lower left

Visual Encoding - building blocks of a graphic/visualization
- Parts of Speech : Sentences :: Visual Encodings : Charts

Commuinicate in the most effective manner 
- Simple solutions to solve problems

Visual Encodings + Data Type + Relationship = Chart Type

[Choosing a chart type](http://extremepresentation.typepad.com/files/choosing-a-good-chart-09.pdf)...
- Data type - continuous or categorical
- Dimension - 1D, 2D, 3D 
- Comparison of 2 variables, distribution of 1 variable, distribution of multipler variables, correlation
- Scatter - values are independent
- Line - points are connected - shoes trend and correlation/dependency


Geographic Chart Types
 - Choropleth = geographic + color
 - Cartogram = geographic + size
 - Dot map = geographic + shape
 
Pre-attentive Processing
 - We can instangly recognize things
 - Example - lots of numbers in a block - if they're all in black font, it's hard to count the number of 9s. However, if the 9s are highlighted in a colored font, it's easy to spot them.
 - 4 Attributes for Pre-attentive Processing
   - Color hue and intensity
   - Form
   - Movement
   - Spacial position
 - [Article: Tapping the Power of Visual Perception](http://www.perceptualedge.com/articles/ie/visual_perception.pdf)

Negative space  around or between shapes can be used effectively
- Example: [FedEx logo](http://www.fedex.com/us/) has an arrow in it between the E and the x
- Example - [Cholrea map by John Snow](http://en.wikipedia.org/wiki/John_Snow_%28physician%29#/media/File:Snow-cholera-map-1.jpg)

Think about eye movement across the page

Color
- Be careful with color
- "Get it right in black and white" - maybe you don't even need color
- Use medium hues or pastels (less vibrancy - softer feel + less eye strain)
- Avoid rainbow and bright colors
- Use color to highlight - facilitate understanding, make a point
- Don't just use it to use it and remove color where it's not making a point
- Be aware of color blindness
- [ColorBrewer](http://colorbrewer2.org/)
- [Article: Practical Rules for Using Color in Charts] (http://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf)

2D > 3D for perception and understanding - can view all data at once and compare more easily and quickly (artery/heart attack example)

Simply visualizations are better

[Gesalt Laws](http://jimsaw.com/design/gestalt.html)
- Proximity - elements close to each other are perceived as the same group
- Similarity - elements that look alike are organized together
- Figure + Ground - perceive object and surface
- Continuity - colinear and direction are grouped together
- Closure - we can complete unfinished objects - ignore gaps and complete contour lines
- Simplicity - figures are seen as their simple elements instead of complicated shapes

Think about what you're going to leave out of your chart as well as what you're going to put in

Chart Junk (Tufte) - "anything that is not part of the minimum set of visuals necessary to communicate the information understandably"
- Heavy/dark grid lines [Article: Grid Lines](http://www.perceptualedge.com/articles/dmreview/grid_lines.pdf)
- Unnecessary text
- Ornamenetet chart areas
- Pictures within graphs
- Shading or 3D

Data-Ink Ratio (Tufte) = Ink Used to Describe Data / Ink Used to Describe Everything Else
- High Ratio is good
- Remove labels when possible - heading may show enough
- Can even remove axes and encode the bars (or other visual) instead

Lie Factor (Tufte) = Size of Effect Shown in Graphic / Size of Effect Shown in Data
- Integrity of a graphic
- How well it actually represents the data
- Ideal is between 0.95 and 1.05
- Size of Effect = ( |Second Value - First Value| / First Value ) x 100

Grammar of Graphics Pipeline matches well with D3 chaining of transformations

Grammar of Graphidcs separates content/data from the medium/graphic/aesthetic

Designing a visualization is an iterative process that involves prototyping/sketching and redesigning

Narrative Structures
- Journalism - rigorous and empirical is the best
  - Quantitative and Rigorous & Empirical: [FiveThirtyEight](http://fivethirtyeight.com/features/what-the-fox-knows/)
  - Qualitative and Rigorous & Empirical: [Washington Post](http://www.washingtonpost.com/)
  - Quantitative and Anecdotal & Ad-Hoc - numbers out of context i.e. sports writers
  - Qualitative and Anecdotal & Ad-Hoc - no data or hard facts i.e. op-ed pieces

Correlation vs. Causation
- A and B vs. A implies B
- Need to be careful of presentation of results - don't want to allow reader/viewer to interpret causation from a correlation
- [Spurious Correlations](http://tylervigen.com/)

Traditional Journalism vs. Data Journalism
- Traditional
  - Static chart within a narrative
  - Narrative is focus, data is secondary
  - Linear narrative - sequence of events
  - Delivered in physical and static form
- Data 
  - Narrative built from the data
  - Data drives narrative - narrative is created by using the context of data
  - More complex and varied narrative 
  - Allow viewer/user to make conclusions in their own way
  - Delivered in interactive and dynamic form

Data visualization is really mostly about the data - finding data, parsing it, verifying the data, exploring it, etc. visualization is the final step

Best practices for visualizations
- Bar charts must have a 0 baseline [Example](http://flowingdata.com/2012/08/06/fox-news-continues-charting-excellence/)
- Don't Lie with Data - [Disinformation Visualization](https://visualisingadvocacy.org/blog/disinformation-visualization-how-lie-datavis)
- Pie charts can confuse the eye and are misleading - stacked bars can still show 100% for comparisons 
- Article: [Save the Pies for Dessert](http://www.perceptualedge.com/articles/visual_business_intelligence/save_the_pies_for_dessert.pdf)
- Article: [Misleading with Statistics](https://medium.com/i-data/misleading-with-statistics-c63780efa928)
- Make sure charts have clear units, informative labels, and context (title, etc.)
- Use juxtaposition/comparison to draw attention to the message
- Add interpretation/explanation to show what different highlighting/colors mean
- Think about how your audience might interpret or interact with the visualization

Bias in Data/Visualization
- Author Bias
  - "Designers and presenters of the visualization (knowing or unknowingly) misrepresent data through visual encodings or other design choices such as the chart type"
  - Design choices should "establish trust between the reader and the graphic" and "facilitate communication"
- Data Bias
  - Measurement errors, improper measurement, faulty device used for measurement, selection bias in questionnaire 
  - Basically, data errors or omissions
- Reader Bias
  - Reader's "preconceived notions or assumptions" 
  - "Consider your audience's background and familiarity with graphics when designing a data visualization"
 
Narrative Structures
- Article: [Narrative Visualization: Telling Stories with Data](http://vis.stanford.edu/files/2010-Narrative-InfoVis.pdf)
- Author Driven Narratives 
  - Linear flow between start and end
  - Predetermined narrative
  - Strong ordering
  - Heavy messaging
  - Need for clarity and speed
- Viewer Driven Narratives
  - Start then viewer chooses which way to go resulting in different endings for different viewers
  - Viewer gets to ask questions and explore
  - Viewer tells their own data story
  - "Choose your own adventure"
- Martini Glass Narrative
  - Start at the base and go through author driven single path 
  - Then the ending is an exploration of different paths
- What narrative to you want to build from the data? How do you want to do it?
  - Exploratory data analysis can help you find your message 



**Resources**
- [Edward Tufte](http://www.edwardtufte.com/tufte/)
- [Measure of America](http://www.measureofamerica.org/)
- [Plotly Blog](http://blog.plot.ly/)
- [Plotly Modern Data Blog](http://moderndata.plot.ly/)
- [The Functional Art](http://www.thefunctionalart.com/)
- [Visualising Data](http://www.visualisingdata.com/)
- [Flowing Data](http://flowingdata.com/)
- [Storytelling with Data](http://www.storytellingwithdata.com/)
- [A Tour through the Visualization Zoo](http://queue.acm.org/detail.cfm?id=1805128)
- [15 Data Visualizations That Will Blow Your Mind](http://blog.udacity.com/2015/01/15-data-visualizations-will-blow-mind.html)
- [Information Aesthetics](http://infosthetics.com/)
- [Visual Complexity](http://www.visualcomplexity.com/vc/)
- [Data Journalism Handbook](http://datajournalismhandbook.org/1.0/en/index.html)
- [Book: The Grammar of Graphics](http://www.amazon.com/The-Grammar-Graphics-Statistics-Computing/dp/0387245448)
- [Book: Information Visualization](http://www.amazon.com/Information-Visualization-Third-Edition-Technologies/dp/0123814642)
- [Graphic: Gay rights in the US](http://www.theguardian.com/world/interactive/2012/may/08/gay-rights-united-states)
- [Book: Creating More Effective Graphs](http://www.amazon.com/Creating-Effective-Graphs-Naomi-Robbins/dp/0985911123)
- [Book: Graph Design for the Eye and Mind](http://www.amazon.com/Graph-Design-Mind-Stephen-Kosslyn/dp/0195311841)

**Tools**
- [Tableau Public](https://public.tableau.com/s/)
- [RAW](http://raw.densitydesign.org/)
- [Chartio](https://chartio.com/)
- [D3](http://d3js.org/)
- [Dimple](http://dimplejs.org/)
