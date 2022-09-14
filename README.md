<!DOCTYPE html>
<html>
    <head>
        <title>color hexcode generator</title>
        <style>
            body{
                margin:0px;
                display:flex;
                justify-content:center;
                align-items:center;
                height:100vh;
                text-align:center;
            }
            div{
                background-color:darkgreen;;
                height:200px;
                width:400px;
                
                border-radius:5px;
                box-shadow: 2px 4px 8px rgba(0, 0, 0, 0.404);
                display:flex;
                justify-content: center;
                align-items:center;
                flex-direction: column;
                
            }
            #colorgenerator{
                margin:0px 20px;
                padding:8px 8px;
                border-radius:8px;
                font-size:20px;
                border:0;
                background-color:slateblue;
                color:white;
                font-family:cursive;
                font-weight:bold;
                cursor:pointer;
              
            }
            #colorhexcode{
                margin:20px 0px;
                color:white;
                font-size:20px;
                font-weight:bold;
                font-family:cursive; 
            }
            
        </style>
    </head>
    <body>
        <div>
            <button id="colorgenerator" onclick="setbg()">click me to generate a new color</button>
            <span id="colorhexcode"></span>
        </div>
        <script>
            let colorcode=document.getElementById("colorhexcode");
            let generator=document.getElementById("colorgenerator");
            let setbg=function(){
                let randomColor=Math.floor(Math.random()*16777215).toString(16);
                document.body.style.backgroundColor = "#" + randomColor;
                colorcode.innerHTML = "color hexcode is #"+ randomColor;
            };
            setbg();
            
        </script>
    </body>
</html>
