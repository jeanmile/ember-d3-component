Ember D3.js Component
==================

A graphic component for ember.js using d3.js

Installation
------------------

    bower install https://github.com/MythX/ember-d3-component.git
    
Include d3.js and ember-d3.js

    <script src="bower_components/ember-d3-component/dist/ember-d3.js"></script>

Usage
------------------

    {{ draw-chart width=1000 height=300 dataBinding='content' }}
    
Content example :

    {
        xAxis: {
          format: 'date',
          origin: false
        },
        yAxis: [{
          name: 'y1',
          color: 'black',
          legend: 'Legend 1',
          position: 'left'
        }],
        charts: [{
          type: 'bar'
          color: '#428BCA'
          yAxis: 'y1',
          data: [{
            keyD: your_key,
            valD: your_value
          }],
        }]
    }


Properties
------------------

General :

    xAxis: Object (required)
    yAxis: Array (required)
    charts: Array (required)

xAxis :

    format: String (date or numeric) (required)
    origin: Boolean (required)

yAxis :

    name: String (required)
    color: String (not required)
    legend: String (not required)
    position: String (left or right) (required)

Line-chart :

    type: 'line' (required)
    yAxis: String (required)
    data: Array (required)
    color: String (required)
    animation: Boolean (not required)
    
    
Bar-chart :

    type: 'bar' (required)
    yAxis: String (required)
    data: Array (required)
    color: String (not required) - For single color
    colors: Array (not required) - For multi-color, you need one color for one bar
    
Data : 

    [{
      keyD: key,
      valD: val,
     }]
    
    
