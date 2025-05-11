# Measuring Access with Open Data and Open Source Tools

Thanks for listening to my talk at CUTA. I've included the presentation and some examples in this repository if you want to revisit some of the slides. Below are some of the resources that I find helpful in my work.



### Sources of location data  
**OpenStreetMap**:  
- [OpenStreetMap.org](http://openstreetmap.org)  
  - [OSMnx](https://github.com/gboeing/osmnx): this is a Python library that's helpful for getting features to include in access measurement. It will also allow you to download OpenStreetMap networks as NetworkX graphs, which means you can use this package (and its dependencies) to do walking, biking, or driving access measurement without any additional tools. I use this approach for everything except transit analyses.
- [Overture Maps](https://overturemaps.org/): Overture Maps brings together data from OpenStreetMap, Microsoft, Meta, and others. This is probably the best (free) source for many types of location data, but it's more complicated to access. 

**Routing Tools**  
- [R5](https://github.com/conveyal/r5) and [Conveyal](https://conveyal.com/): R5 is open source, though Conveyal develops it primarily for their own software, which is a paid product.  
  - [r5py](https://github.com/r5py/r5py): this is a Python library allowing you to run R5 in a Python workflow. It's not officially supported by Conveyal, but has regular updates. This is my preference.  
  - [r5r](https://ipeagit.github.io/r5r/): this is the R library that allows access to R5. It is a great tool if you prefer to work in R.   
- [Valhalla](https://github.com/valhalla/valhalla): Valhalla is an actively developed and powerful tool, however running it is a bit more technical than running R5. You will have to set up a server or Docker container to run this an use the API to get results. This may be more complicated, but could have additional use cases beyond R5. You'll have to decide for yourself if running this will meet your needs. There are libaries that can  help incorporate this into a Python (or other) workflow. Third party providers can provide hosting/routing service if you choose to pay for a hosted version.  
- [routingpy](https://github.com/nilsnolde/routingpy): This Python library allows you to connect to multiple routing services, including Valhalla providers) but also Google Maps and others. These are not free to use, though this may be a good tool to incorporate into your workflow if you choose to connect with hosted routing platforms.

### Some Ways to Incorporate Access Measurement into Your Planning Projects
- Equity analyses - go beyond simply measuring what kind of service is near different communities and measure what those communities can get to. This can be in the form of looking at the time to closest destinations, cumulative opportunities, or other metrics. Results can be reported for different population groups or geographically.
- Service changes - quantify the impacts of your service changes across your service or in specific areas.
- Key performance indicators - set targets for providing minimum levels of access to community members and then ensure you are delivering that.
- Public engagement - use access metrics to communicate the value of projects to the community, decision-makers, community groups, and more. While service additions are easy to understand examples of changes in access, changes to network structure (e.g. towards a grid) and small improvements to travel time or reliability can drastically improve access. Improvements in one area of a network can have large positive (or negative) impacts in other areas. Understanding these impacts and communicating them to the public can help build buy in for projects.
- Building support for transit more broadly - transit provides immense benefit to the community. Communicating that value to community groups, stakeholders, elected officials, business groups, and others can include measures of access. For example, you could communicate with large employers how many community members are within a commute distance from their job sites or communicate the number of potential customers who could ride transit to a group of businesses in an area.

**Statistics Canada Proximity Measures Database**
If you're not able to start calculating access metrics for your projects, you can begin with work Statistics Canada produced nationwide. This data was updated most recently in 2023 and can help you to understand how your services met community demand when they were calculated. This can be a good baseline for you to begin to think about incorporating these types of measures into your work.

[Statistics Canada Spatial Access Measures](https://www150.statcan.gc.ca/n1/pub/27-26-0001/272600012023001-eng.htm)

**Further Reading**
See the examples folder for some products we've created in our projects. I've also included a Python notebook showing how you can create areas to route from if you're starting to experiment with the routing tools.  

To learn more about access measures in general, I recommend *Transport Access Manual: A Guide for Measuring Connection between People and Places* by The Committee of the Transport Access Manual. It's available online [here](https://transportist.org/transport-access-manual-a-guide-for-measuring-connection-between-people-and-places/).  

I'd love to learn more about how you have used these types of metrics in your work if you have examples you would share with me.

