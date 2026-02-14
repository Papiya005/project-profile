# project-profile
To make a simple and reliable project
Build  a simple todo list using html and javascript

<html>html code</html>
 <h1>Todo List</h1>
   <input type="text"placeholder="enter something">
   <button>Add</button>
   <ul>
    <li>Eat<button class="delete">delete</button></li>
    <li>Code<button class="delete">delete</button></li>
   </ul>

   // javascript code
let btn=document.querySelector('button');
let ul=document.querySelector('ul');
let li=document.querySelector('li');
let inp=document.querySelector('input');

// add the eventlistener
btn.addEventListener('click',function(){
  if(inp.value.trim()==="")
    return;
  console.log(inp.value);
  let item=document.createElement('li');
  item.innerText=inp.value;
  ul.appendChild(item);
  inp.value="";

  let delbtn=document.createElement('button');
  delbtn.innerText='delete';
  delbtn.classList.add('delete');
  item.appendChild(delbtn);
});
let delbtns=document.querySelectorAll('.delete');
for(delbtn of delbtns)
{
  delbtn.addEventListener('click',function(){
    console.log("element deleted");
   let parent =this.parentElement;
    parent.remove();
  })
}
   
   
