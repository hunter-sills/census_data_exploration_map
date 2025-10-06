# Advanced Tableau Mapping: US Census Employment and Migration Data

This project explores US Census employment data across Georgia, North Carolina, and Tennessee using an advanced, interactive map built in Tableau. Inspired by the now-inactive New York Times "Mapping the 2010 U.S. Census" project, this exercise showcases the mastery of complex visualization techniques for highly granular data, demonstrating a strategic approach to balancing user experience with technical constraints.

## Project Goal and Technical Objectives

The primary goal of this project was to replicate a seamless, interactive, drill-down map experience in Tableau, allowing users to explore data from the state level down to individual census tracts. My objectives were to:
*   **Research Advanced Techniques:** Evaluate various Tableau features, including map layers, sheet-swapping, and dual-axis maps, for their suitability in creating a high-performance, multi-level map.
*   **Source and Prepare Complex Data:** Retrieve and process large census shapefiles and employment data via the Census API for 2018 and 2023.
*   **Implement an Advanced Visualization:** Construct a dynamic, drill-down map that maintains pan and zoom functionality across multiple geographic layers.

## Solution and Technical Trade-offs

During development, I discovered that achieving a seamless, high-performance user experience with custom, granular shapefiles required a specific architectural decision that came with trade-offs.

*   **Multi-Source Data Architecture:** To enable independent filtering and dynamic transitions between geographic layers, I implemented a multi-source data structure. Each geographic level (State, County, Census Tract) was powered by its own data source. This was the most effective approach for achieving the desired interactive map UX.
*   **Performance vs. Analysis:** While this architecture was crucial for the map, it inherently limited the workbook's ability to perform standard cross-data source calculations and filters. Adding supplementary analytics on top of this structure led to noticeable performance bottlenecks.
*   **Strategic Adaptations:** To address this, I made a conscious decision to prioritize the core mapping experience. For supplementary analysis, I created a separate, combined data source to provide basic population change metrics via BANs (Big-Ass Numbers), accepting the performance trade-off to provide additional context.

## Key Takeaways and Strategic Considerations

This project was a valuable lesson in balancing ambitious visualization goals with technical realities. The experience provided key insights into the capabilities and limitations of advanced mapping in Tableau, particularly for self-contained, desktop-based projects.

*   **Prioritizing User Experience:** When building with large datasets, a clear understanding of what the end-user needs is paramount. In this case, providing a fluid exploratory mapping experience was prioritized over a full suite of analytical calculations.
*   **Architectural Implications:** Every choice has consequences. While the multi-source design was necessary for my desired map functionality, it imposed limitations on other parts of the dashboard. I learned valuable lessons in data modeling and balancing goals with technical realities.
*   **Adaptation to Constraints:** I adapted to the project's technical constraints by using alternative visualization techniques (BANs) and prioritizing the core user experience.
*   **Future Enhancements:** Subscription-based versions of Tableau and continued software updates could present features that simplify this workflow. I will keep these potential enhancements in mind for future design choices and project planning.

## Broader Applications

The type of specialized data map that I’ve built has broad applications where a geographical view of data informs decisions:

*   **Targeted Marketing:** Visualizing sales or customer data at a granular level for strategic, location-based marketing campaigns.
*   **Operational Planning:** Enabling operational teams, such as law enforcement, to analyze patterns at a local level for optimal allocation of resources.
*   **Data Journalism:** Creating embedded, highly interactive visualizations for web articles that engage and inform a broad audience.

---

## How to Use This Dashboard
Download the .twbx file and open it with Tableau Desktop.

## View the Interactive Dashboard

Explore the finished, interactive dashboard on Tableau Public by clicking the link below.

[![Static image of my Tableau viz](https://public.tableau.com/static/images/6X/6XMPGZWJM/1_rss.png)](https://public.tableau.com/app/profile/hunter.sills/viz/census_data_exploration_map/Dash)

## Data and Resources

The final dashboard is packaged in the included '.twbx' file, which contains all necessary data and assets for viewing the project. The raw data files (48 CSVs) and custom shapefiles used for this analysis are not included in this repository due to their large size, and because the '.twbx' provides a complete, portable view of the final project. All source data was retrieved from the U.S. Census Bureau.

---

# Contact

Connect with me on [LinkedIn](https://www.linkedin.com/in/hunter-sills/) or email me at hunter.sills@protonmail.com.

Explore my other projects at https://github.com/hunter-sills.
