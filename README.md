<!DOCTYPE html>
<html>
<head>
  <title>Roofing Cost Estimator</title>
</head>
<body>
  <h1>Roofing Cost Estimator</h1>
  <form>
    <h2>Roofing Materials</h2>
    <p>What's your roof sqft?: <input type="text" id="roofSqft"></p>
    <p>Perimeter of roof: <input type="text" id="perimeter"></p>
    <p>Valley length: <input type="text" id="valleyLength"></p>
    <p>Hip Length: <input type="text" id="hipLength"></p>
    <p>Ridge Length: <input type="text" id="ridgeLength"></p>
    <h2>Materials</h2>
    <p>Oakridge 1SQ: <input type="text" id="oakridge1sq"></p>
    <p>Ice & Water Shield 67LF: <input type="text" id="iceAndWaterShield67LF"></p>
    <p>Starter Strip Plus: <input type="text" id="starterStripPlus"></p>
    <p>Pro Armor Underlayment 10SQ: <input type="text" id="proArmorUnderlayment10SQ"></p>
    <p>Drip Edge: <input type="text" id="dripEdge"></p>
    <p>Pipe Boots: <input type="text" id="pipeBoots"></p>
    <p>Rain Diverter: <input type="text" id="rainDiverter"></p>
    <p>Hip & Ridge: <input type="text" id="hipAndRidge"></p>
    <h2>Vents</h2>
    <p>Drying Vent: <input type="text" id="dryingVent"></p>
    <p>Turtle Vent: <input type="text" id="turtleVent"></p>
    <p>Turbine Vent: <input type="text" id="turbineVent"></p>
    <p>Electric Vent: <input type="text" id="electricVent"></p>
    <p>Satellite Dish: <input type="text" id="satelliteDish"></p>
    <h2>Chimneys</h2>
    <p>Small Chimney: <input type="text" id="smallChimney"></p>
    <p>Medium Chimney: <input type="text" id="mediumChimney"></p>
    <p>Large Chimney: <input type="text" id="largeChimney"></p>
    <h2>Options</h2>
    <p>Options (0-9): <input type="text" id="options"></p>
    <button type="button" onclick="calculateCost()">Calculate Cost</button>
  </form>
  <p id="result"></p>

  <script>
    function calculateCost() {
      var roofSqft = parseFloat(document.getElementById("roof
 <script>   function calculateCost() {     var roofSqft = parseFloat(document.getElementById("roofSqft").value);     var oakridgeBundle = Math.ceil(roofSqft / 3);     var proArmor = Math.ceil(roofSqft / 10);     var roofingNail = Math.ceil(roofSqft / 10);     var perimeter = parseFloat(document.getElementById("perimeter").value);     var starterStripPlus = perimeter * 69.33;     var dripEdge = perimeter * 13.7;     var valleyLength = parseFloat(document.getElementById("valleyLength").value);     var iceAndWaterShield67LF = valleyLength * 66;     var hipLength = parseFloat(document.getElementById("hipLength").value);     var ridgeLength = parseFloat(document.getElementById("ridgeLength").value);     var hipAndRidge = Math.ceil((hipLength + ridgeLength) / 33);     var ridgeVent = Math.ceil(ridgeLength / 4);     var pipeBoots = parseFloat(document.getElementById("pipeBoots").value) * 13.25;     var dryingVent = parseFloat(document.getElementById("dryingVent").value) * 0;     var turtleVent = parseFloat(document.getElementById("turtleVent").value) * 22;     var turbineVent = parseFloat(document.getElementById("turbineVent").value) * 111.25;     var electricVent = parseFloat(document.getElementById("electricVent").value) * 144;     var satelliteDish = parseFloat(document.getElementById("satelliteDish").value) * 30;     var chimney = 0;     var chimneyOption = parseInt(document.getElementById("chimneyOption").value);     if (chimneyOption === 1) {       chimney = 250;     } else if (chimneyOption === 2) {       chimney = 350;     } else if (chimneyOption === 3) {       chimney = 450;     }     var options = parseFloat(document.getElementById("options").value) * 0;     var totalCost = oakridgeBundle * 37.14 + proArmor * 117 + roofingNail * 0 + starterStripPlus + dripEdge + iceAndWaterShield67LF + hipAndRidge * 77.65 + ridgeVent * 0 + pipeBoots + dryingVent + turtleVent + turbineVent + electricVent + satelliteDish + chimney + options;     document.getElementById("result").innerHTML = "Your total cost is: $" + totalCost.toFixed(2);   } 
 </script>
And here's the updated HTML code with the additional fields:
<h1>Roofing Cost Estimator</h1> <form>   <h2>Roofing Materials</h2>   <p>Roof Sqft: <input type="text" id="roofSqft"></p>   <p>Perimeter: <input type="text" id="perimeter"></p> 
 <p>Valley Length: <input type="text" id="valleyLength"></p> <p>Hip Length: <input type="text" id="hipLength"></p> <p>Ridge Length: <input type="text" id="ridgeLength"></p> <h2>Accessories</h2> <p>Pipe Boots: <input type="text" id="pipeBoots" value="13.25"></p> <p>Drying Vent: <input type="text" id="dryingVent"></p> <p>Turtle Vent: <input type="text" id="turtleVent" value="22"></p> <p>Turbine Vent: <input type="text" id="turbineVent" value="111.25"></p> <p>Electric Vent: <input type="text" id="electricVent" value="144"></p> <p>Satellite Dish: <input type="text" id="satelliteDish" value="30"></p> <h3>Chimney Options</h3> <p>Small Chimney: <input type="radio" name="chimney" value="250"></p> <p>Medium Chimney: <input type="radio" name="chimney" value="350"></p> <p>Large Chimney: <input type="radio" name="chimney" value="450"></p> <h2>Optional Upgrades</h2> <p>Upgrade Options: <input type="text" id="upgradeOptions"></p> <input type="button" value="Calculate Cost" onclick="calculateCost()"> </form> <div id="result"></div> 

