# Optimal-route search agent based on Beijing Subway sytem

## 1. Collect Beijing Subway system data

	+ Gaode(Chinese google map) offered the API for Beijing subway data, so we can directly request from this url: http://map.amap.com/service/subway?_1469083453978&srhdata=1100_drw_beijing.json

## 2. Clean and Extract Line and station data
	+ Get the information of Lines and format them with dict.
		* dict.keys() = the name of the line, e.g "S1"
		* dict.values() = a list compased of stations along this subway line
	+ Get the geographic information of stations and format them using dict
		* dict.keys() = the name of the station, e,g "金安桥"
		* dict.values() = a tuple of logitude and latitude

## 3. According to the line information, establish the site adjacency list
	e.g if the next stop of "金安桥” is "四道桥", then add "四道桥” to "金安桥“'s connections. At the end, we will get a dict reflects the adjecency relationships among these subway stations.

## 4. Visualize the subway system 
	Draw a map of beijing subway system based on the geospatial data of the stations and network connections of these stations. Here, we used the concept of graph in computer science field.

## 5. Build the seach Algorithm
	Based on the BFS algorithm and a search strategy of minimum distance, a search algorithm is developed.
