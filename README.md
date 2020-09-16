# Industrial App Store Power BI Connector

Intelligent Plant’s [Industrial App Store](https://appstore.intelligentplant.com) Power BI Connector enables Microsoft’s powerful analytics and visualizations to be applied to real time and historical process data. Seamlessly integrate plant and corporate data and share with any colleague on any device, enabling faster, better, real-time decision making. The Industrial App Store Power BI Connector connects to the Industrial App Store, while all data **remains** secure and safe on-premises. The plant data may be centralized in a corporate data lake or globally dispersed across many sites and historians. Either way, Industrial App Store Power Automate Connector brings it all together and delivers to your fingertips.

## Industrial App Store - What is it

Intelligent Plant developed the Industrial App Store which enables interaction with all the different historian data through a unified API. At start of May 2020 Intelligent Plant released an official, Microsoft certified Industrial App Store connector for Power Automate. No more hefty SQL queries or Excel document interrogations with no easy real-time update option or complicated architecture solutions, simply install Industrial App Store connect and out of the box you will be able to connect to Aspentech IP.21, OSIsoft PI, Honeywell Dynamo, OPC DA & HDA, Siemens and many more. This allows our customers to bring data from various sources into Microsoft Automate flows to deliver insights that weren’t possible before. Real-time updates prompt money-saving decisions by engineers that also increase plant safety and efficiency :fire:.

## Publications :newspaper:

* [Connecting industrial historians to Microsoft Power BI. One connector to get them all…](https://community.powerbi.com/t5/Community-Blog/Connecting-industrial-historians-to-Microsoft-Power-BI-One/ba-p/942200)
* [Power BI and Alarm & Event Bad Actors](https://community.powerbi.com/t5/Community-Blog/Power-BI-and-Alarm-amp-Event-Bad-Actors/ba-p/953020)
* [Alarm Analysis Dashboard design insights](https://community.powerbi.com/t5/Data-Stories-Gallery/Alarm-Analysis-Dashboard-design-insights/m-p/1091669)

## Getting started

### Get the connector

 The connector is certified and distributed by Microsoft with Power BI updates. Just click Get data and look for *Industrial App Store* data connector.

![Start Industrial App Store Connector](https://intelligentplant.com/datasheets/powerplatform/resources/ias-pp-start-connector.gif)

### Log in

Sign in using your Google, Linked In or your Microsoft credentials. If you have an organisation registered with the Industrial App Store you can use your organisation credentials (more infor [here](https://appstore.intelligentplant.com/wiki/doku.php?id=general:app_store_users "IAS - log in")).

During the log in process you can authorise Power BI to access your data sources or feel free to browse demo data source available by default for you to play around with.




## Supported actions (functions)

* **Tag Search**</br>Performs a tag search on the specified data source.

| Name        	| Required 	| Type   	| Description                                                      	| Default 	| Example 	  |
|-------------	|----------	|--------	|------------------------------------------------------------------	|---------	|------------ |
| Tag name    	| true     	| string 	| The name filter to use.                                          	| *       	| *LIC**    	|
| Page size   	| false    	| number 	| Page size for the results.                                       	| 20      	| *5*       	|
| Page number 	| false    	| number 	| The page number of the matching results that should be returned. 	| 0       	| *2*       	|

* **Get Snapshot**</br>Performs a snapshot (NOW) data query on a single data source.

| Name        	| Required 	| Type   	| Description                                                                                                                                                                                           	| Default 	| Example         	|
|-------------	|----------	|--------	|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------	|-----------------	|
| Tag Name(s) 	| true     	| string 	| Comma separated tag names to get data for.                                                                                                                                                            	| *n/a*   	| Sinusoid,LIC040 	|
| Display     	| false    	| option 	| Indicate whether to display numerical, string or both tag values. Some tags (digital) might indicate a status which has a more meaningful text value, e.g.OFF, representation than a numerical value, e.g. 0. 	| Numeric 	|                 	|

* **Get Data** :key:</br>Performs a historical data query.

| Name             	| Required 	| Type   	| Description                                                                                                       	| Default 	| Example                          	|
|------------------	|----------	|--------	|-------------------------------------------------------------------------------------------------------------------	|---------	|----------------------------------	|
| Tag Name(s)      	| true     	| string 	| Comma separated tag names to get data for.                                                                        	| *n/a*   	| Sinusoid,LIC040                  	|
| Start Date       	| true     	| string 	| Absolute or relative start time to use when performing the data query.                                            	| *n/a*   	| *-10d, 2018-01-15                	|
| End date         	| true     	| string 	| Absolute or relative end time to use when performing the data query.                                              	| *n/a*   	| *, *-1h, 2020-09-01T00:00:00     	|
| Function         	| true     	| option 	| Data function/aggregation to use when performing data query.                                                      	| *n/a*   	| Interp, Plot, Min, Max, Avg, Raw 	|
| Interval         	| false    	| string 	| The sample interval.                                                                                              	| *n/a*   	| 20s, 3h, 1d                      	|
| Number of Points 	| false    	| number 	| The maximum number of points to return per tag. Takes precedence over the *Interval* parameter if both specified. 	| *n/a*   	| 10, 150                          	|
| Display     	| false    	| option 	| Indicate whether to display numerical, string or both tag values. Some tags (digital) might indicate a status which has a more meaningful text value, e.g.OFF, representation than a numerical value, e.g. 0. 	| Numeric 	|                              	|

* **Get Processed** :key:</br>Perform aggregated or processed data query.

| Name             	| Required 	| Type   	| Description                                                                                                       	| Default 	| Example                          	|
|------------------	|----------	|--------	|-------------------------------------------------------------------------------------------------------------------	|---------	|----------------------------------	|
| Tag Name(s)      	| true     	| string 	| Comma separated tag names to get data for.                                                                        	| *n/a*   	| Sinusoid,LIC040                  	|
| Start Date       	| true     	| string 	| Absolute or relative start time to use when performing the data query.                                            	| *n/a*   	| *-10d, 2018-01-15                	|
| End date         	| true     	| string 	| Absolute or relative end time to use when performing the data query.                                              	| *n/a*   	| *, *-1h, 2020-09-01T00:00:00     	|
| Function         	| true     	| option 	| Data function/aggregation to use when performing data query.                                                      	| *n/a*   	| Interp, Plot, Min, Max, Avg, Raw 	|
| Interval         	| false    	| string 	| The sample interval.                                                                                              	| *n/a*   	| 20s, 3h, 1d |
| Display     	| false    	| option 	| Indicate whether to display numerical, string or both tag values. Some tags (digital) might indicate a status which has a more meaningful text value, e.g.OFF, representation than a numerical value, e.g. 0. 	| Numeric 	|                              	|

* **Get Plot** :key:</br>Performs a historical data query using *Plot* data function.

| Name        	| Required 	| Type   	| Description                                                                                                                                                                                                   	| Default 	| Example                      	|
|-------------	|----------	|--------	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------	|------------------------------	|
| Tag Name(s) 	| true     	| string 	| Comma separated tag names to get data for.                                                                                                                                                                    	| *n/a*   	| Sinusoid,LIC040              	|
| Start Date  	| true     	| string 	| Absolute or relative start time to use when performing the data query.                                                                                                                                        	| *n/a*   	| *-10d, 2018-01-15            	|
| End date    	| true     	| string 	| Absolute or relative end time to use when performing the data query.                                                                                                                                          	| *n/a*   	| *, *-1h, 2020-09-01T00:00:00 	|
| Intervals   	| false    	| string 	| The maximum number of points to return per tag.                                                                                                                                                               	| *n/a*   	| 20s, 3h, 1d                  	|
| Display     	| false    	| option 	| Indicate whether to display numerical, string or both tag values. Some tags (digital) might indicate a status which has a more meaningful text value, e.g.OFF, representation than a numerical value, e.g. 0. 	| Numeric 	|                              	|

* **Get Raw** :key:</br>Performs a historical data query using *Raw* data function.

| Name        	| Required 	| Type   	| Description                                                                                                                                                                                                   	| Default 	| Example                      	|
|-------------	|----------	|--------	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------	|------------------------------	|
| Tag Name(s) 	| true     	| string 	| Comma separated tag names to get data for.                                                                                                                                                                    	| *n/a*   	| Sinusoid,LIC040              	|
| Start Date  	| true     	| string 	| Absolute or relative start time to use when performing the data query.                                                                                                                                        	| *n/a*   	| *-10d, 2018-01-15            	|
| End date    	| true     	| string 	| Absolute or relative end time to use when performing the data query.                                                                                                                                          	| *n/a*   	| *, *-1h, 2020-09-01T00:00:00 	|
| Points   	| false    	| string 	| The maximum number of points to return per tag.                                                                                                                                                               	| *n/a*   	| 20s, 3h, 1d                  	|
| Display     	| false    	| option 	| Indicate whether to display numerical, string or both tag values. Some tags (digital) might indicate a status which has a more meaningful text value, e.g.OFF, representation than a numerical value, e.g. 0. 	| Numeric 	|                              	|

## Known limitations

Current limitations are mostly around the UI which are improving the usability and ease of access. These limitations ar emostly impsoed by Power Platform framework. Ongoing conversations with Microsoft support are being held to improve current available controls for develoeprs. 

## Using Alarm & Evnet meta tags :alarm_clock:

### A&E meta tags

The following meta tags are available for asset, tag, alarm identifier data aggregations (string before the meta tag will be used to match A&E data which will be used for analysis).
For example:

* `Oil Co/Osprey/KPI No ALM` - This will get number of alarms for *Oil Co/Osprey* asset.
* `Oil Co/Osprey/LIC040/KPI No ALM` - This will get number of alarms for *LIC040* tag.
* `Oil Co/Osprey/LIC040/HIHI/KPI No ALM` - This will get number of alarms for *LIC040 HIHI* tag.

> * \* KPI supports snapshot query (NOW value). Now value in AA defaults to **last event type message - 1m** (as start time) to **last event type message** (as end time). 
> * ** KPI supports trend query (value over time).
> * :triangular_flag_on_post: Indicates that KPI supports excluding empty aggregation buckets, for example if property `ExludeEmptyBuckets` set to true it won't take empty days when calculating averages. See examples for more info.

| KPI                                                   | UOM  | NOW*  | TREND** | Functions |
| ------------------------------------------------------|:----:|:-----:|:-------:|:---------:|
| `KPI avg no alm per 10m` :triangular_flag_on_post:<br/>*Mean average number of alarms per 10 minute buckets per selected interval in chosen period. NOTE: interval should be equal or greater than 10 minutes.* | count | Y | Y | |
| **KPI Avg No Alm per 1h** :triangular_flag_on_post:<br/>*Mean average number of alarms per 1 hour buckets per selected interval in chosen period. NOTE: interval should be equal or greater than 1 hour.*         | count | Y | Y | |
| **KPI Avg No Alm per 1d** :triangular_flag_on_post:<br/>*Mean average number of alarms per 1 day buckets per selected interval in chosen period. NOTE: interval should be equal or greater than 1 day.*           | count | Y | Y | |
| **kpi md avg no alm per 10m** :triangular_flag_on_post:<br/>*Median average number of alarms per 10 minute bucket, per interval for chosen period. NOTE: selected interval should be greater than 10 minutes.*    | count | Y | Y | |
| **kpi md avg no alm per 1h** :triangular_flag_on_post:<br/>*Median average number of alarms per 1 hour bucket, per interval for chosen period. NOTE: selected interval should be greater than 10 minutes.*        | count | Y | Y | |
| **kpi md avg no alm per 1d** :triangular_flag_on_post:<br/>*Median average number of alarms per 1 day bucket, per interval for chosen period. NOTE: selected interval should be greater than 10 minutes.*         | count | Y | Y | |
| **KPI avg max no alm per 10m** :triangular_flag_on_post:<br/>*Average highest alarm count in 10 minute bucket per selected interval in chosen period. NOTE: interval should be greater than 10 minutes*           | count | Y | Y | |
| **KPI Highest 10m**<br/>*Highest alarm count in 10 minute bucket per selected interval in chosen period. NOTE: interval should be greater than 10 minutes.*                                                       | count | Y | Y | |
| **KPI Highest 1h**<br/>*Highest alarm count in 1 hour bucket per selected interval in chosen period. Note: interval should be greater than 1 hour.*                                                               | count | Y | Y | |
| **KPI No Alm**<br/>*Alarm count per selected interval in chosen period.*                                                                                            | count | Y | Y | |
| **KPI No Int**<br/>*Intervention count per selected interval in chosen period.*                                                                                     | count | Y | Y | |
| **KPI No Dis**<br/>*Disable count per selected interval in chosen period.*                                                                                          | count | Y | Y | |
| **KPI % 10m > 5 Alm** :triangular_flag_on_post:<br/>*Percentage of 10 minute periods containing more than 5 alarms per selected interval in chosen period. NOTE: interval should be higher than 10 minutes.* | %     | Y | Y | |
| **KPI % 10m > 10 Alm** :triangular_flag_on_post:<br/>*Percentage of 10 minute periods containing more than 10 alarms per selected interval in chosen period. NOTE: interval should be higher than 10 minutes.*| %     | Y | Y | |
| **KPI % 1h > 30 Alm** :triangular_flag_on_post:<br/>*Percentage of 1 hour periods containing more than 30 alarms per selected interval in chosen period. NOTE: interval should be higher than 1 hour.*       | %     | Y | Y | |
| **KPI No 10m Accpt** :triangular_flag_on_post:<br/>*Count of number of 10 minute buckets with an acceptable number (0 or 1) of alarms per selected interval in chosen period. NOTE: interval should be higher than 10 minutes.* | count | Y | Y | |
| **KPI No 1h Accpt** :triangular_flag_on_post:<br/>*Count of number of 1 hour buckets with an acceptable number (<=6) of alarms per selected interval in chosen period. NOTE: interval should be higher than 1 hour.*           | count | Y | Y | |
| **KPI No 1d Accpt** :triangular_flag_on_post:<br/>*Count of number of 1 day buckets with an acceptable number (<=144) of alarms per selected interval in chosen period. NOTE: interval should be higher than 1 day.*           | count | Y | Y | |
| **KPI % Top 10 MFA**<br/>*Percentage contribution of top 10 most frequent alarms in period (bad actors) per selected interval in chosen period.*                                                                  | %     | Y | Y | |
| **KPI % Top 10 MFI**<br/>*Percentage contribution of top 10 most frequent interventions in selected period (bad actors) per selected interval in chosen period.*                                                  | %     | Y | Y | |
| **KPI Longest Flood**<br/>*Longest flood time span per selected interval in the chosen period.*                                                                                                                   | ms    | Y | Y | |
| **KPI % time in flood**<br/>*Percentage time spent in flood per selected interval in the chosen period.*                                                                                                          | %     | Y | Y | |
| **KPI Flood Count**<br/>*Flood count per selected interval for chosen period. NOTE: interval should be greater than 0 minutes.*                                                                                   | count | Y | Y | |
| **KPI avg % time > steady target (>1)**<br/>*n/a*                                                                                                                                                                 | %     | Y | Y | |
| **KPI avg % time > upset target (>10)**<br/>*n/a*                                                                                                                                                                 | %     | Y | Y | |

### Sequence of Events :bookmark_tabs:

It is possible to get A&E Sequence of Events data to Power BI. Use the following tag format when querying for this type of data:

```text
{Company}/{Plant}/Soe/{page-number}-{page-size}.{filter}
```

An example fo the above would be as follows:

```text
Oil Co/Osprey/Soe/0-30.tag=AI*
```

This will return all A&E messages where tag property matches ```AI*``` search string. Users can also add multiple filters on other fields e.g.:

```text
Oil Co/Osprey/Soe/0-30.tag=AI*&eventType=ALM
```

This will return all A&E messages where tag property matches ```AI*``` search string as well as the event type is an alarm.

List of available properties to filter on are:

| Property name        	| Description                                              	| Example                              	|
|----------------------	|----------------------------------------------------------	|--------------------------------------	|
| TimeStamp            	| Use start and end dates to retrieve specific date range. 	|                                      	|
| EventAddress         	|                                                          	| Oil Co/Osprey/28PALL3214/OFFNORM/ALM 	|
| FriendlyEventAddress 	|                                                          	| 28PALL3214/OFFNORM/ALM               	|
| Tag                  	| Tag name.                                                	| 28PALL3214                           	|
| TagDescription       	| Tag description.                                         	| Pressure controller.                 	|
| AlarmIdentifier      	| Alarm identifier.                                        	| OFFNORM, HI HI                       	|
| EventType            	| Event type.                                              	| ALM, RTN, INT, etc.                  	|
| Parameter            	| Event parameter.                                         	| OP                                   	|
| FromValue            	|                                                          	| RUNNING                              	|
| ToValue              	|                                                          	| STOPPED                              	|
| EngUnit              	| Engineering unit.                                        	| dgrC                                 	|
| Limit                	|                                                          	| 80                                   	|
| Value                	|                                                          	| 70                                   	|
| Priority             	|                                                          	| High                                 	|
| Shelved              	| Indicates whether the event is shelved.                  	| True                                 	|
| Suppressed           	| Indicates whether the event is suppressed.               	| False                                	|
| SrcMsg               	| Source message value.                                    	|                                      	|

### Bad Actor report

A bad actor report can also be obtained using meta tags.

| Tag Name      | Alarm Id  | Description               | Priority      | Unit      | Count     | Percentage    |
|-------------  |:----------|:--------------------------|-----------    |:----------|:----------|:--------------|
| 81LAHH1113    | OFFNORM   | 1st Stage Sep Oil/Wtr     | Warning       | Oil       | 851       | 5.36          |
| 31BAHH3383B   | OFFNORM   | --                        | Alert         | Red Unit  | 526       | 3.32          |
| 50UA1114      | HIHI      | Gen A Trouble             | Emergency     | Util      | 498       | 3.14          |

#### A number (list) of bad actors

To retrieve a list of bad actors use the following ofrmat

```text
{Company}/{Plant}/ALM BA report/{number-of-bad-actors}.{property-name}-a
```

Above table can be generated using the following meta tags.

| Tag name                            	| Alarm Id                                         	| Description                                     	| Priority                                  	| Unit                                  	| Count                                  	| Percentage                                  	|
|-------------------------------------	|--------------------------------------------------	|-------------------------------------------------	|-------------------------------------------	|---------------------------------------	|----------------------------------------	|---------------------------------------------	|
| Oil Co/Osprey/ALM BA report/3.tag-a 	| Oil Co/Osprey/ALM BA report/3.alarmIdentifier-a 	| Oil Co/Osprey/ALM BA report/3.tagDescription-a 	| Oil Co/Osprey/ALM BA report/3.priority-a 	| Oil Co/Osprey/ALM BA report/3.unit-a 	| Oil Co/Osprey/ALM BA report/3.count-a 	| Oil Co/Osprey/ALM BA report/3.percentage-a 	|

#### Specific bad actor

| Meta tag      |           |                           |               |           |           |               |
|-------------  |:----------|:--------------------------|-----------    |:----------|:----------|:--------------|
| Oil Co/Osprey/ALM BA report/1.tag | Oil Co/Osprey/ALM BA report/1.alarmIdentifier | Oil Co/Osprey/ALM BA report/1.tagdescription | Oil Co/Osprey/ALM BA report/1.priority | Oil Co/Osprey/ALM BA report/1.sourcehierarchy.unit | Oil Co/Osprey/ALM BA report/1.count | Oil Co/Osprey/ALM BA report/1.sourcehierarchy.percentage |
| Oil Co/Osprey/ALM BA report/2.tag | Oil Co/Osprey/ALM BA report/2.alarmIdentifier | Oil Co/Osprey/ALM BA report/2.tagdescription | Oil Co/Osprey/ALM BA report/2.priority | Oil Co/Osprey/ALM BA report/2.sourcehierarchy.unit | Oil Co/Osprey/ALM BA report/2.count | Oil Co/Osprey/ALM BA report/2.sourcehierarchy.percentage |
| Oil Co/Osprey/ALM BA report/3.tag | Oil Co/Osprey/ALM BA report/3.alarmIdentifier | Oil Co/Osprey/ALM BA report/3.tagdescription | Oil Co/Osprey/ALM BA report/3.priority | Oil Co/Osprey/ALM BA report/3.sourcehierarchy.unit | Oil Co/Osprey/ALM BA report/3.count | Oil Co/Osprey/ALM BA report/3.sourcehierarchy.percentage |

## Built With

Industrial App Store Connector was built using

* [Industrial App Store API](https://appstore.intelligentplant.com/wiki/doku.php?id=dev:app_store_developers "Intelligent Plant Industrial App Store Developers")
* [Power Query (informally known as "M")](https://docs.microsoft.com/en-us/previous-versions/mt270235(v=msdn.10)?redirectedfrom=MSDN)

## Contributing

Coming soon

## Useful links

* [Intelligent Plant](https://www.intelligentplant.com "Intelligent Plant")
* [Industrial App Store](https://appstore.intelligentplant.com "Industrial App Store")
* [Industrial App Store Wiki](https://appstore.intelligentplant.com/wiki "Industrial App Store wiki")
* [Intelligent Plant YouTube channel](https://www.youtube.com/channel/UCGWOUFOjAEk_QW9w1wWWPDw "Intelligent Plant YouTube channel")

## Support

For any questions please contact Intelligent Plant Ltd [here](https://www.intelligentplant.com/contactus "Intelligent Plant - Contact Us") or fire an email to support@intelligentplant.com.

## Authors

* Intelligent Plant team, Neil Lyall-Varnas.

## Acknowledgments

* Hat tip to anyone who contributed.
* Inspiration

![IAS Connector](https://www.intelligentplant.com/datasheets/powerplatform/resources/Welcome-Industrial-AppStore.png "Intelligent Plant = Industrial App Store")