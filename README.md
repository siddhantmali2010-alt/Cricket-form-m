# Cricket-form-m
Yes
<html>
<script>
document.getElementById("playerForm")
.addEventListener("submit", function(e) {

e.preventDefault();

let name = document.getElementById("playerName").value;
let team = document.getElementById("teamName").value;
let jersey = document.getElementById("jersey").value;

let player = {
name: name,
team: team,
jersey: jersey
};

localStorage.setItem("player", JSON.stringify(player));

document.getElementById("result").innerHTML =
"Player Name: " + name +
"<br>Team: " + team +
"<br>Jersey Number: " + jersey;

alert("Player Details Saved Successfully!");

});
</script>

<body>
  
  <form id="playerForm">

<label>Player Name</label>
<input type="text" id="playerName" required>

<label>Team Name</label>
<input type="text" id="teamName" required>

<label>Jersey Number</label>
<input type="number" id="jersey" required>

<button type="submit">Submit</button>

</form>

<h2>Saved Player Details</h2>
<div id="result"></div>
    
 
  
  
  
  
  
  
  
</body>





</html>
