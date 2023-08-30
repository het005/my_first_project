# my_first_project
it is my first project please currect me if i am  make mistake
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    h3 {
        text-align: center;
    }

    .container {
        border: 2px solid black;
        background-color: skyblue;
        margin: auto;
        justify-content: center;
        align-items: center;
        display: flex;
        flex-direction: column;
        width: 250px;
        border-radius: 25px;
    }

    .row {
        margin: 10px 10px;
    }

    .button {
        padding: 15px;
        border-radius: 15px;
        cursor: pointer;
    }

    .display input {
        padding: 5px 0px;
        margin: 0px;
        border: 2px solid black;
        font-size: medium;
    }
</style>

<body>
    <div class="container ">
        <h3>wellcome to my calculator</h3>
        <div class="display">
            <input type="text" name="text" id="text">
        </div>
        <div class="row">
            <button class="button">7</button>
            <button class="button">8</button>
            <button class="button">9</button>
            <button class="button">*</button>
        </div>
        <div class="row">
            <button class="button">4</button>
            <button class="button">5</button>
            <button class="button">6</button>
            <button class="button">/</button>
        </div>
        <div class="row">
            <button class="button">1</button>
            <button class="button">2</button>
            <button class="button">3</button>
            <button class="button">+</button>
        </div>
        <div class="row">
            <button class="button">0</button>
            <button class="button">.</button>
            <button class="button">-</button>
            <button class="button">=</button>
        </div>
        <div class="row">
            <button class="button">ac</button>
            <button class="button">c</button>
            <button class="button">00</button>
           
        </div>
    </div>
</body>
<script>
    let string = "";
    let button = document.querySelectorAll('.button');
    Array.from(button).forEach((button) => {

        button.addEventListener('click', (c) => {
            if (c.target.innerHTML =='=') {
                string = eval(string);
                document.querySelector('input').value = string;
            }
             else if (c.target.innerHTML =='c') {
                string = "";
                document.querySelector('input').value= string;
            }
             else if (c.target.innerHTML =='ac') {
                string = "";
                document.querySelector('input').value= string;
            }
            else{
                console.log(c.target);
                string  = string + c.target.innerHTML;
                document.querySelector('input').value = string;
            }
        });
    });

</script>

</html>
