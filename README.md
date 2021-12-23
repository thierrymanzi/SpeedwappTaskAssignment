 # **Speedwapp Task Assignment using jquery**
 
 ### **Introduction**
 'This project is aim to return the position of widget in a tagerted element to return the following output in vertical and horizontal position:'
 
 * Top left
 * Top center
 * Top right
 * Center Left
 * Center center
 * Center bottom
 * Bottom left
 * Bottom center
 * Bottom bottom

 ---
 ---

 #### Flowchart image of explainations
 
 ![Explainations](thierrymanzi/SpeedwappTaskAssignment/functionality.png)
 
  #### To run the project visit 
 (https:speedwappassignment.herokuapp.com/)
  
  > Running our project 
  To run the project visit [Test Link](https:speedwappassignment.herokuapp.com/) or copy and paste  the URL [https://www.speedwappassignment.herokuapp.com](https://speedwappassignment.herokuapp.com/) in your browser(IEE,Mozilla Firefox,,Safari and Chrome,etc..) are supported.
  
  ### Project file structure
  ![project folder structure](SpeedwappTaskAssignment/structure.png)
  
  [Test Link](https:speedwappassignment.herokuapp.com/) or copy and paste  the URL [https://www.speedwappassignment.herokuapp.com](https://speedwappassignment.herokuapp.com/)
  
  ### Create a project folder and name it according to your favorite name
  
  `Our project has been developed using the following languages:`
  
  * HTML
 `Create a file and name it index.html' and paste the following code inside`
 
``` html 
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Speedwapp assignment Task</title>
    
<!--  Calling all css file located in our local folder of our project-->
    <link  type="text/css"  rel="stylesheet" href="css/style.css">
    <link type="text/css"   rel="stylesheet" href="jqueryui/jquery-ui.css" >
    <link type="text/css"   rel="stylesheet" href="jqueryui/jquery-ui.structure.css">
    <link  type="text/css" rel="stylesheet"  href="jqueryui/jquery-ui.theme.css">
    
<!--    calling all javascript files located in in our project sub folder-->
  <script type=text/javascript src="js/jquery.js"></script>
  <script type=text/javascript src="jqueryui/jquery-ui.js"></script>   

  <script>
        
// The start of jquery function to postion our widget
        
    $(function() {
            
      
        function position() {           //creation of function named position
        
         $(".position_widget").position({                                         

       my: $("#myHorizontalPositionID").val() +" " + $("#myVerticalPositionID").val(),  //vertical & horizontal of my position of our tagert element
          
       at: $("#atHorizontalPositionID").val()+ " " + $("#atVerticalPositionID").val(), 
          
       of: $("#parentDivID"),
          
             
collision: $("#collHorizontalPositionID").val() +" " + $("#collVerticalPositionID").val()

            });}
            

      $("select,input").on("click keyup change", position); //select element to change the positon in our target element

      $("#parentDivID").draggable({drag: position});            //A method that help us to drag the selected position

      position();  //calling posiion function
        });
        
//        The end of jquery function 
        
  </script>
</head>
   
    
<!--   the beggining of body tag -->
<body style="align=">
<!--  <h1>Position Widget using Jquery & Javascript</h1>-->
  <h1>POSITION WIDGET USING JQUERY & JAVASCRIPT</h1>
  <div class="height"> </div>

  <div id="parentDivID">
       <p>THIS THE PARENT TARGET ELEMENT</p>
    </div>

  <div class="position_widget" id="position_widgetId">
     <p>Change my position</p>
    </div>

    
<!--The beggining of our div with id optionDivID-->
  <div id="optionsDivID">

    <div class="selectDiv">
      <b>Select "my" positions :</b>
      <select id="myHorizontalPositionID">
        <option value="left">left</option>
        <option value="center">center</option>
        <option value="right">right</option>
      </select>
      <select id="myVerticalPositionID">
        <option value="top">top</option>
        <option value="center">center</option>
        <option value="bottom">bottom</option>
      </select>
    </div>
        
    <div class="selectDiv">
      <b>Select "at" positions :</b>
      <select id="atHorizontalPositionID">
        <option value="left">left</option>
        <option value="center">center</option>
        <option value="right">right</option>
      </select>
      <select id="atVerticalPositionID">
        <option value="top">top</option>
        <option value="center">center</option>
        <option value="bottom">bottom</option>
      </select>
           
    </div>
    <div class="selectDiv">
      <b>Select collision options:</b>
      <select id="collHorizontalPositionID">
        <option value="flip">flip</option>
        <option value="fit">fit</option>
        <option value="flipfit">flipfit</option>
        <option value="none">fit none</option>
      </select>
      <select id="collVerticalPositionID">
        <option value="flip">flip</option>
        <option value="fit">fit</option>
        <option value="flipfit">flipfit</option>
        <option value="none">none</option>
      </select>
    </div>
  </div>
<!--The end of our div with id optionDivID-->

    

    
</body>

<!--    The end of body tag-->
    
</html>

```
  * CSS
`Inside css folder create a css file and name it stye.css then copy and paste the following code.`

``` CSS
body{
/*    margin: 100px;*/
    max-width: max-content;
    margin: auto;
    background-color: darkgrey;
/*    background-image: url("spe.png");*/
/*    background: url("sp.png");*/

}

.height {
      height: 10px;
    }

h1{
width: 600px;
height: 20px;
padding: 20px;
margin: auto
border: 1px solid black;
background-color: #C4C1C1 ;
border: solid 2px darkgray;
border-radius: 10px;
text-align: center;
color: #4E4D4D;
font-family: sans-serif;
    font-size: 16px;
  }
    
#parentDivID {
width: 600px;
height: 400px;
padding: 15px;
border: 1px solid black;
background-color: #900C3F ;
border: solid 2px darkgray;
border-radius: 10px;
text-align: center;
color: black;
font-weight: bold;

}
    
.position_widget {
position: absolute;
display: block;
border-radius: 50%;
background-color: #ffc107;
text-align: center;
}
    
#position_widgetId {
width: 80px;
height: 80px;
    
}
    
#optionsDivID {
padding: 10px;
margin-top: 20px;
/*background-color:yellow;*/
width: 600px;
height: 100px;
padding: 15px;
background-color: #C4C1C1;
border: solid 2px darkgray;
border-radius:10%
}
    
.selectDiv {
padding-bottom: 20px;
}
    
select {
margin-left: 15px;
}

```
  * Javscript and JQuery and css 
`To enable jquery plugin library visit jqueryuicom to download the stable version click the follwowng link` 
 [jquery plugins library](<https://jqueryui.com/>) then unzip the folder and paste it in our local folddre of our project.
 
 ```JQuery plugins
 <link  type="text/css"  rel="stylesheet" href="css/style.css">
 <link type="text/css"   rel="stylesheet" href="jqueryui/jquery-ui.css" >
 <link type="text/css"   rel="stylesheet" href="jqueryui/jquery-ui.structure.css">
 <link  type="text/css" rel="stylesheet"  href="jqueryui/jquery-ui.theme.css">
 <script type=text/javascript src="js/jquery.js"></script>
 <script type=text/javascript src="jqueryui/jquery-ui.js"></script>   

 ```
  
  * php
  
  `In our root directory create php file as index.php` 
  `NB:We create this file for the purpose of enabling our project to run on Heroku free cloud 
  hosting as we known doesn't understand HTLM so we need call index.html in our php file.`
  
  `But this is option as long as you don't want to use Heroku`
  
  ```php
 <?php 
   include("index.html");
 ?>
  
  ````
  
  *json 
  ` Inside our root directory create a file as composer.json and paste the following code`
  `This file will enable our project to run on heroku cloud`
  
  ``` Json
  {}
  
  ```

  ### Project user interface
  
 ![speedwapp assignment](C:/Users/Admin/Desktop/Speedwapp_Task_Assignment/interfaceimage.png)
 
 
 ### Recommendation 
 For any input related to this assignment please share us  to know more.
 
 
 
 
 
   
  
   
  
  
  
