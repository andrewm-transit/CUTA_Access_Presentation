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

**Examples of Incorporating Access into Planning Projects**
