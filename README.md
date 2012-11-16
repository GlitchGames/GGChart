GGChart
============

GGChart allows for easy creation of Google Image Charts for your Corona apps. 
The Google Image Chart API was deprecated in April 2012 however it should still
work. Info is here - https://developers.google.com/chart/image/

Basic Usage
-------------------------

##### Require the code
```lua
local GGChart = require( "GGChart" )
```

##### Create a line chart
```lua
local lineChart = GGChart:new
{
	type = "line",
	mode = "standard",
	title = "Random Line Chart",
	legend = "Green|Red",
	legendPosition = "b",
	dataColours = "008000,FF0000",
	data = "t:10,20,40,80,90,95,99|20,30,40,50,60,70,80",
	width = 320,
	height = 150,
	margins = { 20, 0, 0, 20 },
	x = 0,
	y = 300
}
```

##### Create a pie chart
```lua
local pieChart = GGChart:new
{
	type = "pie",
	title = "Android Distribution - Percent",
	legend = "3.9|6.3|31.4|57.6|0.8",
	legendPosition = "r",
	width = 320,
	height = 150,
	labels = "Android 1.5|Android 1.6|Android 2.1|Android 2.2|Android 2.3",
	data = "t:3.9,6.3,31.4,57.6,0.8",
	mode = "2d",
	dataColours = "C4DF9B|AFD377|9AC653|84BA2F|6FAD0C",
	scale = { 0, 100 },
	margins = { 20, 0, 0, 20 },
	x = 0,
	y = 130
}
```

##### Create a QR code
```lua
local qrCode = GGChart:new
{ 
	type = "qr",
	data = "Corona Rocks!",
	width = 100,
	margin = 1,
	background = "bg,s,FFFF00",
	errorCorrectionLevel = "L",
	x = 20,
	y = 20
}
```

##### Destroy one of the charts
```lua
lineChart:destroy()
lineChart = nil
```

Update History
-------------------------

##### 0.1
Initial release