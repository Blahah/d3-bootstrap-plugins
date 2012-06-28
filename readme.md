# d3.js tooltip
js/css duo for bootstrap style tooltips.

Click [a gisted example](http://bl.ocks.org/2981335). 

## How does it work? 
Tooltip.js attaches event listeners to selections that go and display
bootstrap tooltips or popovers. 

An example of how to use it:
```javascript
    selection.tooltip(function(d,i){
        return {        
            content:{
                type: "tooltip" //Other option: popover
                text: d.title
                //For popovers
                content: svg //A d3 svg element
                title: "A title"
            },
            detection:{
                type: "shape" #Work in progress
            },
            placement:{
                type: "fixed"
                gravity: "right" //left,top,bottom
                position: [d.x,d.y] 
            },            
            mousemove: false
        };
    })
    
```
    
Viola! Tooltips! Popovers!
## Current TODOS
* Add in better defaults
* Get the animations going
* Write some tests. 
* Use it in production. 

## License

### Major components:
* d3.js: [License](https://github.com/mbostock/d3/blob/master/LICENSE)
* Bootstrap: [License](https://github.com/twitter/bootstrap/blob/master/LICENSE)

### Everything else:

Public domain. 
