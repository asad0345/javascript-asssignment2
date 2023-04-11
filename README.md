
Question No:1
function add(num){
    return function(number) //closure function
    {
        return num + number;
    }
}

const add5 = add(5); //here we create a variable (add5) which store the function add(num) with the by passing value 5 to it 
const result = add5(30); //Call the add5 function with an argument of 30, and store the result in a variable

console.log(result); // The result will be 35 as output

Question No:2
function search(array,value){
    if(array.length===0){
        return false;
    }
    else if(array[0]===value){
        return true;
    }
    else{
        return search(array.slice(1),value)
    }
    
}

const array1=[1,4,6,8,9,3,5];

const value=+prompt("please enter a value to find in array ");

console.log(search(array1,value));

Question No:3
function addParagraph() {
    const newParagraph = document.createElement("p");
    const content = document.createTextNode("Pakistan is a land of incredible diversity, rich culture, and a fascinating history. With its breathtaking natural landscapes, bustling cities, and warm hospitality of its people, Pakistan has something to offer for everyone. From the mighty Himalayas to the serene beaches of the Arabian Sea, the country boasts a wide range of natural beauty that is simply awe-inspiring.");
    newParagraph.appendChild(content);
  
    document.body.appendChild(newParagraph);

  }                                                                           <body>

   
    <p>Click on the button to add new Paragraph</p>
    <button onclick="addParagraph()" style="font-size: medium;">Add Paragraph</button>
    
    
</body>

Question No:4
<ul id="myList">
      <li>Mangoe</li>
      <li>Apple</li>
      <li>Gavava</li>
    </ul>
    
    <button onclick="addNewListItem('New Item')">Add Item</button>
    
    <script>
      function addNewListItem(text) {
        const list = document.getElementById("myList");
        const newListItem = document.createElement("li");
        const content = document.createTextNode(text);
        newListItem.appendChild(content);
        list.appendChild(newListItem);
      }
    </script>
Question No:5
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>q5</title>
  
</head>
<body>
 
    
    <p id="myParagraph">This is a paragraph.</p>
    
    <button onclick="changeBackgroundColor(document.getElementById('myParagraph'), 'red')">Set Red Background</button>
    <button onclick="changeBackgroundColor(document.getElementById('myParagraph'), 'green')">Set Green Background</button>
    <button onclick="changeBackgroundColor(document.getElementById('myParagraph'), 'blue')">Set Blue Background</button>
    
    <script>
      function changeBackgroundColor(element, color) {
        element.style.backgroundColor = color;
      }
    </script>
  </body>
</html>
Question No:6

function saveObjectToLocalStorage(key, object) {
    localStorage.setItem(key, JSON.stringify(object));
  }
  
  // Example usage:
  const myObject = { name: "Zeeshan Hassan", age: 21 };
  saveObjectToLocalStorage("myKey", myObject);

Question No :7
function getObjectFromLocalStorage(key) {
    const objectString = localStorage.getItem(key);
    return JSON.parse(objectString);
  }
  const myObject = getObjectFromLocalStorage("myKey");
console.log(myObject); // Should log the object you saved earlier
Question No: 8
function saveToLocalStorage(obj) {
    // Save each property to localStorage
    Object.keys(obj).forEach(function(key) {
      localStorage.setItem(key, JSON.stringify(obj[key]));
    });
  
    // Retrieve the object from localStorage and return it as a new object
    var newObj = {};
    Object.keys(obj).forEach(function(key) {
      newObj[key] = JSON.parse(localStorage.getItem(key));
    });
    return newObj;
  }
