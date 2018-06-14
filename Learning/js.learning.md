> Value types: Number, String, Boolean, undefined, null

> Reference type: Object, Function, Array

> Array
```js
var array = ["a", "b", 1, 2]
typeof array        // Print the type of array
array.push(3)       // Add element at the end
array.pop()         // Remove the last elemwnt
array.unshift("a")  // Add element at the front
array.shift()       // Remove the first element
array.indexOf("a")  
```

> slice() return part of a array but does not modifie the real array. slice(strat, end)
```js
var arr = [1, 2, 3, 4, 5, 6]
var arr1 = arr.slice(2,4)   // Out: [3, 4]
```

> splice() remove a part of a array and modifie the real array. splice(start, num_of_element_to_remove)
```js
var arr = [1, 2, 3, 4, 5, 6]
var arr1 = arr.splice(2,2)   // Out: [3, 4]
```

> Array merge
```js
var a = [1, 2, 3]
var b = [4, 5, 6]
var merge = a.concat(b)   // out: [1, 2, 3, 4, 5, 6]
```

> Object
```js
obj = {
    name: "Karim",
    age: 23,
    print: function(){
        console.log("This is karim");
    }
}
```

> Factory function
```js
function createCircle(radius){
    return{
        radius,
        draw: function(){
            console.log("draw a cicle")
        }
    }
}
const circle = createCircle(2);
circle.draw();
```

> Constructor function
```js
// Constructor function
function Circle(radius){
    let defaultLocation = { x:0, y:0};     // Private member 
    let newPropDefine = 1;

    let getDefaultLocation = function(){   // Private method
        return defaultLocation;
    } 

    this.radius = radius,                  // Public member
    this.draw = function(){
        getDefaultLocation();
        console.log("Draw circle");
    }

    // Getter & Setter
    Object.defineProperty(this, 'newPropDefine', {
        get: function(){
            return newPropDefine;
        },
        set: function(newValue){
            newPropDefine = newValue
        }
    })
}
let cir = new Circle(2);
cir.draw();
cir.newPropDefine;
```
