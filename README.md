# info5100

INFO 5100
Project Report 1


 
 
 


 Date:
10/06/2023
 
 
 
 
 
 
 
 
 
 
Team Member:
Kaylen Li(ql326@cornell.edu)
Ting-Min Lai(tl853@cornell.edu)
Yueyi Yang(yy2225@cornell.edu)
Xiaoyu Fan(xf234@cornell.edu)





0. Contribution
Kaylen Li: Contributed to data preprocessing, actively engaged in discussions regarding dataset selection and chart concepts, provided assistance with graphic design, and the completion of graphic 2.

Ting-min Lai: Actively participated in discussions regarding dataset selection and chart concepts, and made valuable contributions to graphic design, tasked with data cleaning and completion of graphic 1.

Xiaoyu Fan: Actively engaged in discussions regarding dataset selection and chart concepts, collaborated with Yueyi Yang on graphic design, took the lead in organizing meetings, played a key role in drafting the milestone report, and preparing the presentation.
.

Yueyi Yang: Actively participated in discussions regarding dataset selection and chart concepts, collaborated with Xiaoyu Fan on graphic design, and played a significant role in drafting the milestone report, designed web pages and fonts, as well as contributed to writing the final report and preparing the presentation.

1. Introduction

Youtube is a popular long-video platform all around the world and more and more people become youtubers. Hence, our group wants to analyze data in terms of the youtubers’ income. The report explains two questions we want to explore: 1. compare the extent to which the average income of youtubers in their home country is higher than per capita income of that country among youtubers from different countries to find the country in which the youtuber has the highest income based on per capita income of that country and 2. figure out which category is the most active and thus more profitable category based on the ratio of total views divided by number of subscribers. The data we use is Global Youtube Statistics 2023, so all the analysis and results reflect the data in 2023.

2. Graph1 
2.1 Introduction
Graphic1 is a world map used to compare the extent to which the average income of youtubers in their home country is higher than per capita income of that country among youtubers from different countries.


2.2 Design
First, we need to figure out how to measure the extent to which the income of a youtuber is higher than the per capita income of that country. We use the formula as shown below to calculate the extent.

Second, since we need to compare the datum above among different countries, we choose the world map as our diagram basis. Then the different countries in the map become the marks and the aligned positions and shapes of those countries are channels.
Third, since there are over fifty countries, it is not concise if we give each country a different color hue/luminance. Therefore, just like what other world map diagrams show, we decide to categorize the countries into six groups based on the extent to which the income of a youtuber is higher than the per capita income of that country. We use blue and red of different luminance levels to represent the data.

2.3 Implementation 
The first step is to import both youtuber data and average income data for each country. The second step is to clean the data, such as dropping some invalid or useless data. Next step is to construct a basic world map without any data display. Then d3.join is used to combine data and map display, after which the countries on the map would show different color hues.

2.4 Analysis and conclusion
Contrary to what we initially thought, youtubers in South and South-east Asia(India, Pakistan, Thailand, Malaysia, Philippines and Vietnam), North and North-east Asia(Russia, Japan, Korea), mediterranean regions( Italy, Turkey, Egypt and Iran) have a much higher income than average income of that country. Youtubers in Mexico, Chile, Germany have a higher income than the average income of that country. Youtubers in North America(US, Canada), Sweden, China and Saudi Arabia have a slightly lower income than the average income of that country. Youtubers in parts of Europe (British, France, Spain, Finland), parts of South America (Peru and Venezuela), Australia have a lower income than the average income of that country. Due to limitations of data, lots of countries, such as countries in Africa do not have data collection in 2023. To conclude, being a youtuber is a quite worthy job in South and South-east Asia. In most developed countries, being a youtuber does not earn more money than other people.

3. Graphic 2

3.1 Introduction
The objective of this graphic is to identify the categories of YouTube channels that have the potential to generate substantial profits using the prevailing YouTube income calculation algorithm. The research is presented under the title "Top U.S. YouTube Channels' Earnings By Channel Type".

In this analysis, we investigate the relationship between key metrics, specifically "Total Subscribers" on the x-axis and "Total Views" on the y-axis. Additionally, we utilize a sloped line within the visualization to represent the "Average Number of Views per Subscriber." This visualization aims to shed light on the earnings dynamics of various channel types on YouTube and provide insights into the factors that contribute to successful revenue generation.


3.2 Design
In our visualization, we employed a palette of thirteen distinct colors to represent thirteen unique Channel Types. We utilized circles as graphical elements to symbolize the annual earnings, with the circle's size directly correlating with the magnitude of earnings. Within each Channel Type category, we employed a series of three concentric circles, each with increasing radii (10, 20, and 40) and varying opacities (0.3, 0.5, and 1). These circles sequentially signify the following:

Average Lowest Yearly Earning Among Top U.S. Channels: Represented by the innermost circle with a radius of 10 and an opacity of 1.
Average Highest Yearly Earning Relative to Average Lowest Yearly Earning: Depicted by the middle circle with a radius of 20 and an opacity of 0.5.
Max Highest Yearly Earning Relative to Average Lowest Yearly Earning: Indicated by the outermost circle with a radius of 40 and an opacity of 0.3.
This visual encoding scheme provides a clear and intuitive representation of earnings data, allowing viewers to discern both the relative and absolute earnings of different channel types within the visualization.

3.3 Implementation
First, we cleaned the data, resulting in the creation of the file "youtube_us_type.csv". This file displayed the channel types for all regions in the United States, with a total of 13 types. Additionally, it presented the nine metrics for each channel type, as shown in Figure 1.


Next, we implemented the code, and the following are the steps:

Creating SVG Element and Basic Setup: The code begins by creating an SVG element to host the visualization and sets its width and height.

Defining CSS Styles: CSS styles are defined using the `<style>` tag, including styles for gridlines, text fonts, and colors, among others.

Defining Constants and Parameters: Multiple constants and parameters for the visualization are defined in the code, including mark annotations, color schemes, scales, and more. These parameters are used in the subsequent visualization process.

Creating Functions for Drawing Elements: The code defines several functions for creating various elements within the visualization, such as the title, labels, axes, gridlines, circles representing channels, and color annotations.

Loading and Processing Data: Data is loaded from a CSV file ('youtube_us_type.csv') using the `d3.csv` function from the D3.js library. The data is scaled for proper presentation within the visualization.

Drawing the Visualization: By invoking the previously defined functions, the code creates and renders visualization elements, including the title, labels, mark annotations, axes, gridlines, circles, and color annotations. These elements are data-driven and visually represent earnings data for YouTube channels.

Saving the SVG: Finally, the code defines the `saveSvg` function, enabling users to save the SVG visualization as an image file.

3.4 Analysis & Conclusion
In this code, the D3.js library is employed to construct an interactive visualization that presents earnings data for the most prominent YouTube channels in the United States, grouped by their channel types. The code encompasses a range of functions designed to generate visualization components, manage data loading and scaling, and ultimately generate the visualization itself. The primary objective of this visualization is to convey earnings data for diverse channel categories on YouTube in an informative and visually engaging manner. Users have the capability to interact with the visualization, facilitating a deeper understanding of the underlying data. This code serves as a valuable tool for data exploration and analysis in research reports.

By comparing the sizes of the circles in the final graph, it becomes evident that the "animals" channel type generates the highest earnings, while "nonprofit" earns the least. Simultaneously, we can observe that the "education" channel has the highest viewership, while the "tech" channel has the lowest. The "nonprofit" channel boasts the highest number of subscribers, whereas the "people" channel has the fewest subscribers.

By examining the positions of the circle centers, we can identify that eight channel types exceed the Average Number of Views per Subscriber, while five channel types fall below it. The "news" channel has the highest Number of Views per Subscriber, indicating that this type of content attracts a significant viewership beyond its subscriber base. However, most people do not actively subscribe to news channels, and this metric can rise significantly during major events, depending on whether significant news occurred during a given time period.

Similarly, the top-earning "animals" channels also draw in a substantial number of non-subscriber viewers. Interestingly, the "tech" channel exhibits an unusually low Number of Views per Subscriber, prompting speculation that some viewers may be compelled to follow the channel due to school assignments or a desire to learn about technology, but they do not regularly watch such content. This also raises the possibility of some tech channel creators engaging in the practice of purchasing subscribers.

Furthermore, by examining the sizes of the three concentric circles, we can observe that the "tech" and "news" channels' Max highest yearly earning relative to Average lowest yearly earning and Average highest yearly earning relative to Average lowest yearly earning are the closest. Additionally, it's worth noting an intriguing observation: true to its name, the "nonprofit" channel generates no profit, as evidenced by its Max highest yearly earning relative to Average lowest yearly earning and Average highest yearly earning relative to Average lowest yearly earning being the same.

4. Conclusion
For the world map diagram, being a youtuber is a quite worthy job in South and South-east Asia and North and North-east Asia. In most developed countries, being a youtuber does not earn more money than other people.
Based on the data from the “Top U.S. YouTube Channels' Earnings By Channel Type” graph, it's evident that the "Animals" channel type is the highest earner, while "Nonprofit" earns the least. "Education" attracts the most viewers, with "Tech" having the fewest. "Nonprofit" boasts the highest number of subscribers, while "People" has the fewest. "News" achieves the highest "Number of Views per Subscriber," suggesting broader appeal. "Tech" stands out with a remarkably low "Number of Views per Subscriber," potentially indicating non-organic growth.

A suggestion for people in the US: Create an Animal Youtube Channel to earn the most money! But make sure you do love animals instead of just making money out of them.






























































