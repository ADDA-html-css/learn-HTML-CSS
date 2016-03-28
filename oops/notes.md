##ex 1
```css
/*mobile rules first*/
html{
	background-color: blue;
}

@media (min-width: 600px){
    /*override for a tablet*/
  html { 
	background: green; 
  }
}
```

##ex2
-start
```css

body{
	background-color: #eee;

	padding:0;
	margin: 0;
}



.box{
	display: block;
	width: 100%;
	height: 200px;
}


.one{
	background-color: #D88373;
}

.two{
	background-color: #BD1E1E;
}

@media (min-width: 600px){
  .box{
		display: inline-block;
		width: 50%;
		height: 400px;
		float:left;
	}
}
```

-next, change to this
```css

body{
	background-color: #eee;

	padding:0;
	margin: 0;
}



.box{
	display: block;
	width: 100%;
	height: 200px;

	text-align: center;
}


.one{
	background-color: #D88373;
}

.two{
	background-color: #BD1E1E;
}

h1{
	font-size: 5rem;
	margin:0;
}

@media (min-width: 600px){
  .box{
		display: inline-block;
		width: 50%;
		height: 400px;
		float:left;
	}

	html{
		font-size: 30px;
	}
}

@media (min-width: 900px){
  .box{
		display: inline-block;
		width: 50%;
		height: 400px;
		float:left;
	}

	html{
		font-size: 50px;
	}
}
```