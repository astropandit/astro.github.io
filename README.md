# ananay-hosts
HTML
<nav class="navbar">  
  <div class="title">CWR</div>  
  <div class="ham" >  
  <span class="bar1"></span>  
  <span class="bar2"></span>  
  <span class="bar3"></span>  
  </div>  
  <ul class="nav-sub">  
   <li class="list-item"><a href="#" class="nav-link">Home</a></li>  
   <li class="list-item"><a href="#" class="nav-link">Blogs</a></li>  
   <li class="list-item"><a href="#" class="nav-link">About me</a></li>  
  </ul>  
 </nav>  

CSS
 *{  
  margin:0;   
  color:white;  
 }  
 .title{  
  cursor:pointer;  
 }  
 /*Properties for Nav-bar*/  
 .navbar{  
  display:flex;  
  top:0;  
  height:10vh;  
  justify-content:space-between;  
  align-items:center;   
  padding:0px 20px;  
  background:grey;  
 }  
 .nav-sub{  
  display:flex;  
  justify-content:space-between;  
 }  
 .list-item {  
  padding:10px;  
  list-style:none;  
 }  
 .nav-link{  
  color:inherit;  
  text-decoration:none;  
 }  
 /*Properties for Hamburger*/  
 .ham{  
  display:none;  
  padding:5px;  
  cursor:pointer;  
 }  
 .bar1,.bar2,.bar3{  
  display:block;  
  width:35px;  
  height:3px;  
  margin:5px auto;  
  background-color:#101010;  
  transition: 0.4s;  
 }  
 @media only screen and (max-width:768px){  
 *{  
   overflow:hidden;  
  }  
 .nav-sub{  
   position:absolute;   
   top:10vh;  
   right:0px;  
   flex-direction:column;  
   background-color:rgb(0,0,0,0.75);  
   border-radius:0px 0px 0px 20px;  
   transition:transform 0.3s ease-in;  
   transform:translate(100%);  
  }  
 .nav-change{  
   transform:translate(0%);  
  }  
 .ham{  
   display:block;  
  }  
 .change .bar1 {  
  transform: rotate(45deg) translate(8px,3px);  
 }  
 .change .bar2 {  
  opacity: 0;  
 }  
 .change .bar3 {  
  transform: rotate(-45deg) translate(8px,-3px);  
 }  
 } 
JAVASCRIPT
 const hamburger = document.querySelector(".ham");  
 const navsub = document.querySelector(".nav-sub");  
 hamburger.addEventListener('click', () => {  
  hamburger.classList.toggle("change")  
  navsub.classList.toggle("nav-change")  
 });
