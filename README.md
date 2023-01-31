# Calculadora

<html>
  <head>
    <style>
      .calculator {
        width: 400px;
        height: 500px;
        background-color: lightgray;
        border-radius: 20px;
        padding: 20px;
        text-align: center;
        box-shadow: 10px 10px 10px #888888;
      }
      input[type='text'] {
        width: 100%;
        height: 50px;
        font-size: 20px;
        text-align: right;
        margin-bottom: 20px;
      }
      button {
        width: 70px;
        height: 70px;
        font-size: 20px;
        margin: 10px;
        border-radius: 35px;
      }
    </style>
  </head>
  <body>
    <div class="calculator">
      <input type="text" id="display">
      <br>
      <button id="btn1">1</button>
      <button id="btn2">2</button>
      <button id="btn3">3</button>
      <button id="btnPlus">+</button>
      <br>
      <button id="btn4">4</button>
      <button id="btn5">5</button>
      <button id="btn6">6</button>
      <button id="btnMinus">-</button>
      <br>
      <button id="btn7">7</button>
      <button id="btn8">8</button>
      <button id="btn9">9</button>
      <button id="btnMult">x</button>
      <br>
      <button id="btnClear">C</button>
      <button id="btn0">0</button>
      <button id="btnEqual">=</button>
      <button id="btnDiv">÷</button>
    </div>
    <script>
      const display = document.querySelector("#display");
      const btns = document.querySelectorAll("button");

      btns.forEach(function (btn) {
        btn.addEventListener("click", function () {
          let btnVal = btn.innerHTML;
          if (btnVal === "C") {
            display.value = "";
          } else if (btnVal === "=") {
            display.value = eval(display.value);
          } else {
            display.value += btnVal;
          }
        });
      });
    </script>
  </body>
</html>
