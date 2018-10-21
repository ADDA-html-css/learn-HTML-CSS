# Week 9 - Wrapping Up

## Objectives

## Agenda
- What's Next
- Preview JS
- Talk Domains
- Setting Up WP hosting

## Java Script Preview
- Share starter code

```
window.onload = function(){
  console.log('working');
   
  document.getElementById('todo').addEventListener('click', test);
}

function update (target) {
  alert('clicked');
  target.className = "done";
}

function clearAll(){
  console.log('clear');
  document.getElementById('todo').innerHTML = ""; 
}

function add(){
  var task = prompt('give me something to do');
  console.log(task);
  var item = document.createElement('li');
  item.innerHTML = task;
  document.getElementById('todo').append(item);
}

function test(event){
  event.target.className = 'done';
}
```
