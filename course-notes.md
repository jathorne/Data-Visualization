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

2D > 3D for perception and understanding - can view all data at once and compare more easily and quickly (artery/heart attack example)

Simply visualizations are better

Gesalt Laws
- Proximity - elements close to each other are perceived as the same group
- Similarity - elements that look alike are organized together
- Figure + Ground - perceive object and surface
- Continuity - colinear and direction are grouped together
- Closure - we can complete unfinished objects - ignore gaps and complete contour lines
- Simplicity - figures are seen as their simple elements instead of complicated shapes

Think about what you're going to leave out of your chart as well as what you're going to put in

Chart Junk (Tufte) - "anything that is not part of the minimum set of visuals necessary to communicate the information understandably"
- Heavy/dark grid lines
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
