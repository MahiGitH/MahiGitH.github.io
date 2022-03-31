<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
  li:visited,
  li:focus,
  li:active {
    text-decoration: line-through;
     }
 body{
  margin: auto;
   }
  *{
  box-sizing: border-box;
   }
  h1 {
  text-align: center;
  }

ul li {
  position: relative;
  background: #eee;
  padding: 12px 8px 12px 40px;
  list-style-type: none;
  transition: 0.2s;
} 
  </style>
</head>
<body>
  <h1>To Do List</h1>
  <div id = 'myFirst' class="listdiv">
  <ul id="myToDo">
    <li class="rem">Pray</li>
    <li class="rem">Laundary</li>
    <li class="rem">Call Mom</li>
    <li class="rem">Practice JavaScript</li>
    <li class="rem">To Do List Assignment- Due Friday</li>
    <li class="rem">Go To Supermarket</li>
    <li class="rem">Meeting Classmates</li>
  </ul>
  </div>
  <div id="mydiv" class="inputdiv">
    <input type="text" id="myInput" placeholder="Enter your to do list">
    <button onclick="newToDoItem()" class ="addBtn">Add New To do List</button>
  </div>
  <script>
  // create new list item when the button is clicked and cleared out
 function newToDoItem() {
  var li = document.createElement("li");
  var inputValue = document.getElementById("myInput").value;
  var t = document.createTextNode(inputValue);
  li.appendChild(t);
  if (inputValue === '') {
    alert("You must write To Do List!");
  } else {
    document.getElementById("myToDo").appendChild(li);
  }
  document.getElementById("myInput").value = "";
  var button = document.createElement("BUTTON");
  var txt = document.createTextNode();
  button.className = "close";
  button.appendChild(txt);
  li.appendChild(button);
  for (i = 0; i < close.length; i++) {
    close[i].onclick = function() {
      var div = this.parentElement;
      div.style.display = "none";
    }
  }
}

document.querySelector('ul').addEventListener('click', function handleClick(event) {
 console.log(event.target);
 setTimeout (1000);
  event.target.remove();
 });
  </script>  
</body>
</html>
