# Reading Notes
### class 12


## Chart.js and canvas


- For setting up the chart the first thing that we need to do is download chart.js. Copy chart.min.js (min stands for minify). Create html page and import the script. 

- Create a canvas element in out HTML so that chart.js can draw out chart

``` <canvas id="buyers" width="600" height="400"></canvas> ```

- write the script that will retrieve the context of the canvas

```var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData); ```
 ```    
 - create the data with an object that contains labels for the base of the chart
 
```
 var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);
            // pie chart data
            var pieData = [
                {
                    value: 20,
                    color:"#878BB6"
                },
                {
                    value : 40,
                    color : "#4ACAB4"
                },
                {
                    value : 10,
                    color : "#FF8153"
                },
                {
                    value : 30,
                    color : "#FFEA88"
                }
            ];
            // pie chart options
            var pieOptions = {
                 segmentShowStroke : false,
                 animateScale : true
            }
            // get pie chart canvas
            var countries= document.getElementById("countries").getContext("2d");
            // draw pie chart
            new Chart(countries).Pie(pieData, pieOptions);
            // bar chart data
            var barData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                    {
                        fillColor : "#48A497",
                        strokeColor : "#48A4D1",
                        data : [456,479,324,569,702,600]
                    },
                    {
                        fillColor : "rgba(73,188,170,0.4)",
                        strokeColor : "rgba(72,174,209,0.4)",
                        data : [364,504,605,400,345,320]
                    }
                ]
            }
            // get bar chart canvas
            var income = document.getElementById("income").getContext("2d");
            // draw bar chart
            new Chart(income).Bar(barData);
            
```
## Canvas Api Usage
 
- canvas lookis like the img element but without src and alt attributes. 
 
- Canvas only has two attributes they are height and weight.
 
- The canvas can be resized with css.
 
- You can easily define fallback content if the browser dosent support it.
 
- Canvas requires a closing tag
 
- another example of rendering context
 
```
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
```

## Drawing shapes with canvas 

- The canvas is layed out in a grid. If the cavas is set to 150 * 150 pixesl then 1 pixel is equal to 1 unit on the gird. The origin of the grid is at the top left corner at coordinate(0,0). All elements are placed relative the origin.

- to draw a rectangel

```
fillRect(x, y, width, height)
Draws a filled rectangle.

strokeRect(x, y, width, height)
Draws a rectangular outline.

clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.

```

- <canvas> only supports two primitive shapes: rectangles and paths

- draws a rectangle
  
  
```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}

```

- moveTo() function Is like lifting a pen or pencil from one spot on a piece of paper and placing it on the next.

- to move from one positon and start drawing on different shapes

```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
     var ctx = canvas.getContext('2d');

    ctx.beginPath();
    ctx.arc(75, 75, 50, 0, Math.PI * 2, true); // Outer circle
    ctx.moveTo(110, 75);
    ctx.arc(75, 75, 35, 0, Math.PI, false);  // Mouth (clockwise)
    ctx.moveTo(65, 65);
    ctx.arc(60, 65, 5, 0, Math.PI * 2, true);  // Left eye
    ctx.moveTo(95, 65);
    ctx.arc(90, 65, 5, 0, Math.PI * 2, true);  // Right eye
    ctx.stroke();
  }
}

```

