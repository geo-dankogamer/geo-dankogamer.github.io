<!DOCTYPE html>
<html>
  <head>
    <title>Kliknutie na tlačidlo</title>
    <style>
      /* štýly pre tlačidlo */
      #click-btn {
        background-color: black;
        color: white;
        border: none;
        padding: 10px 20px;
        font-size: 16px;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <h1>Zostávajúce kliknutia: <span id="remaining-clicks">10</span></h1>
    <button id="click-btn" onclick="showText()">click</button>
    <p id="hidden-text">
      &#68;&#111;&#117;&#103;&#108;&#97;&#115;&#32;&#69;&#110;&#103;&#101;&#108;&#98;&#97;&#114;&#116;
    </p>
    <script>
      var remainingClicks = 10; // počet zostávajúcich kliknutí
      function showText() {
        remainingClicks--; // znížiť počet zostávajúcich kliknutí o 1
        document.getElementById("remaining-clicks").innerHTML = remainingClicks; // aktualizovať text s počtom zostávajúcich kliknutí
        if (remainingClicks === 0) {
          document.getElementById("hidden-text").innerHTML = "Douglas Engelbart"; // dekódovať text po 10 kliknutiach
        }
      }
    </script>
  </body>
</html>

