1) Problem set for the box model:

debug
<div style="width: 300px; padding: 20px; border: 10px solid black;">
    Fix this box model error.
</div>

the problem in this code is box sizing property is no defined by default the box sizing property take value contain-box that will change the dimension of box while changing the property border box property like 
adding margin and padding so best way is to use the box sizing property value is border-box


question 3) create responsive box(output based question)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Box</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      
    }

    .box {
      width: 50vw; /* 50% of the viewport width */
      padding: 10px;
      border: 5px solid red;
      text-align: center;
      
    }
  </style>
</head>
<body>
  <div class="box">
    Box 
  </div>
</body>
</html>

question4) How does the Box Model influence layout when combined with Flexbox? Provide an example to demonstrate.
ans) flexbox properties can influence the box model like flex wrap property for container and the flex shrink, flex grow and flex base properties for the child container can adjust the size of the box according to the given value and justify content property of the flex that also influence the space/ margin between the differernt box That's how it influence

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Model with Flexbox</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .container {
      display: flex;
      justify-content: space-around;
      align-items: center;          
      height: 100vh;                
    
    }

    .box {
      width: 100px;
      padding: 20px;
      border: 5px solid red;
      margin: 10px;
      background-color: #fff;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3</div>
  </div>
</body>
</html>


2). Position: absolute,relative,fixed

question1) error based debugging

<div style="position:relative">
    <div style="position: absolute; top: 10px; left: 20px;">
        I should be positioned relative to my parent.
    </div>
</div>
before using the aboslute position we have to assign position like relative,fixed, absolute to its parent else it will take the root element as its parent and its position is static(root element)

quest2)  
ans)

question4) compare the position fixed with sticky and provide a use case for each
ans)
Sticky: sticky stick to the defined scroll position 
iniitally scrolls with the page but stick when you reach the specified position like top 100px it will stick after the 100px

3)css px rem and em %

debug

:root {
    font-size: 16px;
}
.box {
    width: 2em;
    height: 2em;
}

use only one from em or rem because em taking reference to its parent component and rem taking reference to its root component which is html so they are taking different for the height and width this is not the good practice so used either parent component reference or rem 

question4) how do rem and em interact differently in nexted elemnts
ans) use only one from em or rem because em taking reference to its parent component and rem taking reference to its root component which is html so they are taking different for the height and width this is not the good practice so used either parent component reference or rem 





















