# Calculator-
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="logo1.png" type="image/icon type">
    <title>Calculator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background: #00bcd4;
            transition: all ease 0.4s;
        }

        div {
            margin-top: 21px;
        }

        button {
            margin-left: 14px;
            border-radius: 50px;
            width: 62px;
            height: 64px;
            font-size: 28px;
            border: 1px solid #efefef;
            font-weight: bolder;
        }

        #center {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        #display {
            height: 59px;
            width: 310px;
            text-align: end;
            font-size: 28px;
            padding-right: 12px;
            margin-left: 8px;
            border: 2px solid #efefef;
            border-radius: 11px;
            outline: none;
        }

        #calculator {
            background-color: blueviolet;
            padding-top: 15px;
            padding-left: 15px;
            border-radius: 15px;
            padding-right: 15px;
            transition: all ease 0.4s;
            padding-bottom: 25px;
        }

        p {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 40px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            color: rgb(3, 255, 234);
            font-weight: bolder;
            transition: all ease 0.4s;
            font-size: 31px;
        }

        #body {
            background: black;
            margin-right: 12px;
            height: 38px;
            width: 77px;
            transition: all ease 0.4s;
            border-radius: 50px;
        }

        header {
            height: 75px;
            position: absolute;
            width: 100%;
            /* background: white; */
            /* box-shadow: 0 0 12px -3px; */
            margin-top: -21px;
            display: flex;
            justify-content: flex-end;
            align-items: center;
        }

        #switch {
            background: white;
            height: 30px;
            margin-top: 4px;
            width: 30px;
            transition: all ease 0.4s;
            margin-left: 5px;
            border-radius: 50px;

        }
    </style>
</head>

<body id="boddy">
    <script>
        function seven() {
            a = document.getElementById("display")
            a.value += "7"
        }
        function eight() {
            a = document.getElementById("display")
            a.value += "8"
        }
        function nine() {
            a = document.getElementById("display")
            a.value += "9"
        }
        function plus() {
            a = document.getElementById("display")
            a.value += "+"
        }
        function four() {
            a = document.getElementById("display")
            a.value += "4"
        }
        function five() {
            a = document.getElementById("display")
            a.value += "5"
        }
        function six() {
            a = document.getElementById("display")
            a.value += "6"
        }
        function minus() {
            a = document.getElementById("display")
            a.value += "-"
        }
        function one() {
            a = document.getElementById("display")
            a.value += "1"
        }
        function two() {
            a = document.getElementById("display")
            a.value += "2"
        }
        function three() {
            a = document.getElementById("display")
            a.value += "3"
        }
        function star() {
            a = document.getElementById("display")
            a.value += "*"
        }
        function slash() {
            a = document.getElementById("display")
            a.value += "/"
        }
        function zero() {
            a = document.getElementById("display")
            a.value += "0"
        }
        function result() {
            a = document.getElementById("display")
            var b = eval(a.value)
            a.value = b
        }

        function cear() {
            a = document.getElementById("display")
            a.value = ""
        }
        function drk() {
            let a = document.getElementById("boddy");
            let b = document.getElementById("body");
            let c = document.getElementById("switch");
            let e = document.getElementById("para");
            let f = document.getElementById("calculator");
            if (a.style.background != "black") {
                a.style.background = "black"
                c.style.background = "black"
                f.style.background = "#161515"
                c.style.marginLeft = "42px"
                e.style.color = "white"
                b.style.background = "cyan"

            }
            else if (a.style.background == "black") {
                a.style.background = "#00bcd4"
                c.style.background = "white"
                e.style.color = "rgb(3, 255, 234)"
                b.style.background = "black"
                c.style.marginLeft = "5px"
                f.style.background = "blueviolet"

            }
        }
    </script>
    <header>
        <div id="body">
            <div id="switch" onclick="drk()"></div>
        </div>
    </header>
    <section id="center">
        <section id="calculator">
            <p id="para">Calculator</p>
            <input type="text" name="" readonly id="display">
            <div id="row1">
                <button onclick="seven()" value="7">7</button>
                <button onclick="eight()" value="8">8</button>
                <button onclick="nine()" value="9">9</button>
                <button onclick="cear()" value="AC" id="ac">AC</button>
            </div>
            <div id="row2">
                <button onclick="four()" value="4">4</button>
                <button onclick="five()" value="5">5</button>
                <button onclick="six()" value="6">6</button>
                <button onclick="plus()" id="plus" value=" + ">+</button>
            </div>
            <div id="row3">
                <button onclick="one()" value="1">1</button>
                <button onclick="two()" value="2">2</button>
                <button onclick="three()" value="3">3</button>
                <button onclick="minus()" value="-">-</button>
            </div>
            <div id="row4">
                <button onclick="slash()" value="/">/</button>
                <button onclick="zero()" value="0">0</button>
                <button onclick="result()" value="=">=</button>
                <button onclick="star()" value="*">*</button>

            </div>
        </section>
    </section>
</body>

</html>
