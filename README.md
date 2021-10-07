# data-512-a1

The goal of this project is to examine the changes in desktop and mobile traffic that the Wikipedia website has had over the time period of January 2008 to August 2021. We will accomplish this by requesting API data, cleaning the data, and publishing a dataset. 

Link to license of the source data and a link to the Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

# The data was collected from the Legacy Pagecounts API and the Pageviews API. 

Link to Legacy Pagecounts API documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts

Link to Legacy Pagecounts API endpoint: https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end 

Link to Pageviews API documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

Link to Pageviews API endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

# In the final data file, we have 8 total columns:

year: The year the Wikipedia visit data was collected from

month: The month the Wikipedia visit data was collected from

pagecount_all_views: The number of desktop and mobile page counts aggregated together

pagecount_mobile_views: The number of mobile-specific page counts

pagecount_desktop_views: The number of desktop-specific page counts 

pageviews_all_views: The number of desktop and mobile page views aggregated together 

pageviews_mobile_views: The number of mobile-specific page views

pageviews_desktop_views: The number of desktop-specific page views

Special considerations with the data would be to pay attention to the type of data we are working with. The API calls will result on a JSON data structure and the analysis requires us to convert that data to a CSV. Taking special care to convert the data properly through data types is critical in this analysis. Furthermore, there should be no null values in our analysis, rather we should replace all our NaN values with 0. 
