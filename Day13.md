**Elastic Stack (ELK)**



It is used for log analysis and investigations. Although, it is not a traditional SIEM, many SOC teams use it like one because of its data searching and visualizing capability.

Some components behind ELK are:



**1. Elasticsearch**

The first component, Elasticsearch , is a full-text search and analytics engine for JSON-formatted documents. It stores, analyzes, and correlates data and supports a RESTful API for interacting with it.



**2. Logstash**

Logstash is a data processing engine that takes data from different sources, filters it, or normalizes it, and then sends it to the destination, which could be Kibana or a listening port. A configuration file is divided into three parts, as shown below.



&#x20;   The Input part is where the user defines the source from which the data is being ingested.

&#x20;   The Filter part is where the user specifies the filter options to normalize the log ingested above. 

&#x20;   The Output part is where the user wants the filtered data to be sent. It can be a listening port, Kibana Interface, Elasticsearch database, or file. 



**3. Beats**

Beats are host-based agents known as data-shippers that ship/transfer data from the endpoints to Elasticsearch . Each beat is a single-purpose agent that sends specific data to Elasticsearch .



**4. Kibana**

&#x20;Kibana is a web-based data visualization tool that works with Elasticsearch to analyze, investigate, and visualize data streams in real time. It allows users to create multiple visualizations and dashboards for better visibility. There is more on Kibana in the following tasks.

How they work together:



Now that we have learned about all the components of the Elastic Stack, let's see how these components work together step-by-step:



&#x20;is a web-based data visualization tool that works with to analyze, investigate, and visualize data streams in real time. It allows users to create multiple visualizations and dashboards for better visibility. There is more on in the following tasks.

How they work together:



Now that we have learned about all the components of the Elastic Stack, let's see how these components work together step-by-step:



&#x20;   Beats collect data from multiple agents. For example, Winlogbeat collects Windows event logs, and Packetbeat collects network traffic flows.

&#x20;  Logstash collects data from beats, ports, or files, parses/normalizes it into field value pairs, and stores them into Elasticsearch.

&#x20; Elasticsearch  acts as a database used to search and analyze data.

&#x20; Kibana  is responsible for displaying and visualizing the data stored in Elasticsearch . The data stored in Elasticsearch can easily be shaped into different visualizations, time charts, infographics, etc., using Kibana.



Today, I learned how to use ELK and how in the future as a SOC analyst, it will be one of the widely used tool I would use.

