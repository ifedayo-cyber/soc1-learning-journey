**SPLUNK**



Splunk is one of the leading solutions in the market. It allows users to collect, analyze, and correlate network and machine logs in real time. Today, I learnt about the basics of Splunk and its functionalities, and how it provides better visibility of network activities and helps speed up detection.



Splunk has three main components: Forwarder, Indexer, and Search Head. These components work together to help us search and analyze the data. These components are explained below:



**Splunk Forwarder**

&#x20;Splunk Forwarder is a lightweight agent installed on the endpoint intended to be monitored, and its main task is to collect the data and send it to the Splunk instance. It does not affect the endpoint's performance as it takes a few resources to process. Some of the key data sources are:



&#x20;   Web server generating web traffic.

&#x20;   Windows machine generating Windows Event Logs, PowerShell, and Sysmon data.

&#x20;  Linux host generating host-centric logs.

&#x20;   Database generating DB connection requests, responses, and errors.



The forwarder collects data from the log sources and sends it to the Splunk Indexer





**Splunk Indexer**

Splunk Indexer plays the main role in processing the data it receives from forwarders. It parses and normalizes the data into field-value pairs, categorizes it, and stores the results as events, making the processed data easy to search and analyze. Now, the data, which is normalized and stored by the indexer, can be searched by the Search Head.



**Search Head**



Splunk Search Head is the place within the Search \& Reporting App where users can search the indexed logs, as shown below. The searches are done using the SPL (Search Processing Language), a powerful query language for searching indexed data. When the user performs a search, the request is sent to the indexer, and the relevant events are returned as field-value pairs.



At the end of the day, I did a practical using Splunk and a downloaded task file to analyze data.

