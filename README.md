# 7-FCC
<link href="https://fonts.googleapis.com/css?family=Khand:500" rel="stylesheet">
<link href="https://fonts.googleapis.com/css?family=Lobster+Two" rel="stylesheet">
# FCC-6-Responsive Web Design Challenges
Responsive Web Design Challenges Lesson Notes of OJKT
<!DOCTYPE: html>
<html>	
Lesson Notes of OJKT
<div id="page-wrapper">
<style>
		body, html {
  font-family: "Khand", sans-serif;
  background: lightgrey;
}

/*toolbar&title*/
#title {
	position: static;
	top: 0;
	right: 0;
	padding-left: 15vh;
	padding-right: 15vh;
	padding-bottom: 5vh;
	padding-top: 4vh;
  margin-top: 5px;
	margin-left: 1vw;
	margin-right: 0.3vw;
	color: black;
	background: repeating-linear-gradient(180deg, black 0px, cyan 40px, black 80px);
  font-size: 4vm;
	font-size: 5vh;
  font-family: font-family: 'Lobster Two', cursive;
	text-align: center;
	text-transform: uppercase;
}	
/*toolbar&title*/

/*footer*/
footer {
	position: static;
	bottom: 0;
	right: 0;
  margin-top: 10px;
	margin-left: 0px;
	padding-left: 10px;
	margin-right: 1px;
  background-color: #C0C0C0;
	border: 4px solid #000;
 	border-radius: 4px;
	color: darkgrey;
	font-size: 2vm;
	font-size: 2vh;
}
span {
    margin-right: 10px;
    display: flex;
    justify-content: flex-end;
    font-size: 0.9em;
    color: #eee;
}
/*footer*/

/*navlinks*/
  ul {
	position: fixed;
	Padding-top: 0vh;
	margin-top: 1vh;
	margin-left: 90vw;
	font-family: font-family: 'Lobster Two', cursive;
	text-transform: none;
	font-size: 3vm;
	font-size: 3vh;
		background-color: white;
		transform: rotate(-45deg);
		border: solid black 1vh;
		border-radius: 4vh;
}
#nav-link {
			padding-left: 0px;
			padding-right: 5px;
			color: red;
			font-size: 3vh;
    }
/*navlinks*/
/*grid*/
  .d1{background:LightSkyBlue;}
  .d2{background:LightSalmon;}
  .d3{background:PaleTurquoise;}
  .d4{background:LightPink;}
  .d5{background:PaleGreen;}
  
  .container {
    font-size: 40px;
    width: 100%;
    background: LightGray;
    display: grid;
  }
/*grid*/

/*media query*/
  .block1 {
    background: LightSkyBlue;
    grid-area: header;
  }
  
  .block2 {
    background: LightSalmon;
    grid-area: advert;
  }
  
  .block3 {
    background: PaleTurquoise;
    grid-area: content;
  }
  
  .block4 {
    background: lightpink;
    grid-area: footer;
  }
  
  .container2 {
    font-size: 1.5em;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 50px auto 1fr auto;
    grid-gap: 10px;
    grid-template-areas:
      "header"
      "advert"
      "content"
      "footer";
  }
  
  @media (min-width: 300px){
    .container2{
      grid-template-columns: auto 1fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
  }
  
 @media (min-width: 400px){
    .container2{
      grid-template-areas:
        "header header"
        "advert content"
        "footer footer";
    }
  }
/*media query*/
</style>

<header id="header"></header>
<head class="head">
		<h1 id=title><u>Introduction to the CSS Grid Challenges</u></h1>
	<div id="nav-bar">
			<ul>
				<strong><a class="nav-link" href="#header" id="nav-link">Jump to top</a></strong>
				<br>
			<strong><a class="nav-link" href="#footer" id="nav-link">Jump to bottom</a></strong>
		</ul>
	</div>
  </nav>
</head>
<hr>
	
<div>
	<p><u>Learning Objectives :</u><p>
    <ol>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Create Your First CSS Grid</a></li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Add Columns with grid-template-columns</a></li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Add Rows with grid-template-rows</a></li>
			<li><a class="nav-link" href="#Grid_Units">Use CSS Grid units to Change the Size of Columns and Rows</li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Create a Column Gap Using grid-column-gap</a></li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Create a Row Gap using grid-row-gap</a></li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Add Gaps Faster with grid-gap</a></li>
			<li><a class="nav-link" href="#Grid_Area">Use grid-column to Control Spacing</li>
			<li><a class="nav-link" href="#Grid_Area">Use grid-row to Control Spacing</li>
			<li><a class="nav-link" href="#Align_and_Justify">Align an Item Horizontally using justify-self</a></li>
			<li><a class="nav-link" href="#Align_and_Justify">Align an Item Vertically using align-self</a></li>
			<li><a class="nav-link" href="#Align_and_Justify">Align All Items Horizontally using justify-items</a></li>
			<li><a class="nav-link" href="#Align_and_Justify">Align All Items Vertically using align-items</a></li>
			<li><a class="nav-link" href="#Grid_Area">Divide the Grid Into an Area Template</li>
			<li><a class="nav-link" href="#Grid_Area">Place Items in Grid Areas Using the grid-area Property</li>
			<li><a class="nav-link" href="#CSS_Grids_columns_&_rows">Use grid-area Without Creating an Areas Template</a></li>
			<li><a class="nav-link" href="#Make_Life_Easy">Reduce Repetition Using the repeat Function</a></li>
			<li><a class="nav-link" href="#Make_Life_Easy">Limit Item Size Using the minmax Function</a></li>
			<li><a class="nav-link" href="#Flexible_Life">Create Flexible Layouts Using auto-fill</a></li>
			<li><a class="nav-link" href="#Flexible_Life">Create Flexible Layouts Using auto-fit</a></li>
			<li><a class="nav-link" href="#Media_Query">Use Media Queries to Create Responsive Layouts</a></li>
			<li><a class="nav-link" href="Inception_Grids">Create Grids within Grids</a></li>
   </ol>
<br><hr>
</div>

<div id="CSS_Grids_columns_&_rows">
	<h2>CSS Grids, columns & rows</h2>
	<p>display property with a value of grid is used to produce a grid like shown below. The number of parameters given to the <i>grid-template-columns</i> property indicates the number of columns in the grid, and the value of each parameter indicates the width of each column. The same with <i>grid-template-rows</i> eg. grid-template-columns: 50px 50px 50px; This will give your grid three columns that are 50px wide each.</p>
	<div class="container">
  <div class="d1">1</div>
  <div class="d2">2</div>
  <div class="d3">3</div>
  <div class="d4">4</div>
  <div class="d5">5</div>
	</div>
	<p>If <i>grid-gap</i> property has one value, it will create a gap between all rows and columns. However, if there are two values, it will use the first one to set the gap between the rows and the second value for the columns. e.g. <i>grid-gap:10px 20px;</i> means 10px between rows and 20px between columns.</p>
	<hr>
</div>

<div id="Grid_Area">
	<h2>Grid Area & spaces</h2>
		<p>Up to this point, all the properties that have been discussed are for grid containers. The grid-column property is the first one for use on the grid items themselves. eg: <i>grid-column: 1 / 3; grid-row</i> does the same thing but for the horizontal gaps.</p>
		<p>to save space and time we can change both rows and colum gaps and once with the grid property like this, <i>grid-gap</i>: 10px 20px; | with the grid-area property you can for example - <i>grid-area</i>: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at; e.g. <i>grid-area</i>: 1/1/2/4</p>
		<p>.item1 {<i>grid-area</i>: header;} This lets the grid know that you want the item1 class to go in the area named header. In this case, the item will use the entire top row because that whole row is named as the header area.</p>
	<hr>
</div>
	
<div id="Align_and_Justify">
	<h2>Align and Justify</h2>
	<p>justify-self property on a grid item. By default, this property has a value of stretch, which will make the content fill the whole width of the cell. This CSS Grid property accepts other values as well:</p>
	<ul>
		<li>start: aligns the content at the left of the cell,</li>
		<li>center: aligns the content in the center of the cell,</li>
		<li>end: aligns the content at the right of the cell.</li>
	</ul>
	<p>there's a way to align an item vertically as well. To do this, you use the align-self property on an item. This property accepts all of the same values as justify-self. e.g. <i>align-self:</i> end;</p>
	<p>Sometimes you want all the items in your CSS Grid to share the same alignment. You can use the previously learned properties and align them individually, or you can align them all at once horizontally by using justify-items on your grid container. This property can accept all the same values, the difference being that it will move all the items in our grid to the desired alignment. e.g. <i>justify-items</i>: center;</p>
	<p>Using the <i>align-items</i> property on a grid container will set the vertical alignment for all the items in our grid. used to move all the items to the end of each cell commonly.</p>
	<hr>
</div>
	
<div id="Grid_Units">
	<h2>Grid Units</h2>
	<p>Grid Units:</p>
	<div>
		<li> fr: sets the column or row to a fraction of the available space.</li>
		<li> auto: sets the column or row to the width or height of its content automatically.</li>
		<li> %: adjusts the column or row to the percent width of its container.</li>
	</div>
	<hr>
</div>
	
<div id="Make_Life_Easy">
	<h2>Make Life Easy</h2>
	<p>When you used grid-template-columns and grid-template-rows to define the structure of a grid, you entered a value for each row or column you created.<br> Lets say you want a grid with 100 rows of the same height. It isn't very practical to insert 100 values individually. Fortunately, there's a better way - by using the repeat function to specify the number of times you want your column or row to be repeated, followed by a comma and the value you want to repeat.<br>Here's an example that would create the 100 row grid, each row at 50px tall. <i>grid-template-rows</i>: repeat(100, 50px);</p>
	<p>You can also repeat multiple values with the repeat function, and insert the function amongst other values when defining a grid structure. Here's what I mean: grid-template-columns: repeat(2, 1fr 50px) 20px;</p>
	<p>There's another built-in function to use with grid-template-columns and grid-template-rows called minmax. It's used to limit the size of items when the grid container changes size. To do this you need to specify the acceptable size range for your item. e.g. <i>grid-template-columns</i>: repeat(3, minmax(90px, 1fr)); i incorporated the repeat function with the minmax so you can see how  it would work.</p>
	<hr>
</div>

<div id="Flexible_Life">
	<h2>Flexible Life</h2>
	<p>The repeat function comes with an option called auto-fill. This allows you to automatically insert as many rows or columns of your desired size as possible depending on the size of the container. You can create flexible layouts when combining auto-fill with minmax. <i>grid-template-columns</i>: repeat(auto-fill, minmax(60px, 1fr));</p>
	<p>auto-fit works almost identically to auto-fill. The only difference is that when the container's size exceeds the size of all the items combined, auto-fill keeps inserting empty rows or columns and pushes your items to the side, while auto-fit collapses those empty rows or columns and stretches your items to fit the size of the container.<br><strong>Note</strong><br>If your container can't fit all your items on one row, it will move them down to a new one.   grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));</p>
	<hr>
</div>
	
<div id="Media_Query">
	<h2><u>Media Query</u></h2>
	<div class="container2">
		<div class="block1">header</div>
		<div class="block2">advert</div>
		<div class="block3">content</div>
		<div class="block4">footer</div>
	</div>
	<hr>
</div>
	
<div id="Inception_Grids">
	<h2>Inception Grids</h2>
	<p>inception has nothing to do with nested objects but in coputer science it is known as recursion</p>
	<p>Turning an element into a grid only affects the behavior of its direct descendants. So by turning a direct descendant into a grid, you have a grid within a grid.<br>For example, by setting the display and grid-template-columns properties of the element with the item3 class, you create a grid within your grid.</p>
	<hr>
</div>
	
<footer id="footer">
		<ol>
			<i><a href="#">Privacy  .</a></i><br>			
      <i><a href="#">Terms  .</a></i><br>
      <i><a href="https://www.facebook.com/Active-Boardom-1433050133615965/?__tn__=kC-R&eid=ARDxFnA2JMu6bjlwqWvI3V1d0Rce9HdYBzDGGtJp0BhH-ueOlTAQbh0whATwwgFna9sm9jkboRpjWJnD&hc_ref=ARQaDkOV-XEkdyZItVQH9yuafF_narIIMZukBWJoaFoVgKTTBr5qBLQ1pDtdCP1cxF0&fref=nf&__xts__[0]=68.ARDYkTx9CsRT4OGTCvkO4FfhIcApAmkjQ-zBxaLHt1nqutrcdBfuonVlBKBXLg-l6giN-MiLriy2iHhYK3-uZ7l8efaHcYfOQPPUo3YknyBCljz10jZVwawd_JPGlqxxUxpaKdDVOc7vv4zQb1gvTtbiga9MLXcGfadpQU6YN_ZFZFBORq0wTJ2gjwQWf-hqAyErVWR_HM-_tje583zlZDxOBvyFSIb71aWN5zby5u-Ar3tr-Zn6BXKJ03w-KH30lCsYY8yrgpdS7DWA_-M3ogU_9pI9jGXFww4iDR6qmOdznSinEPP_J0pCY3maDJ4_2n1-a3Uq57kDKz4vC98">Contact  .</a></i> <!--contact-->
		</ol>
	    <span>&copy Copyright 2018, OJKT STYLES</span>
</footer>
	
</div>
