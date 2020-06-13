<html>
    <head>
    <title>Home</title>
    <script>
		function fun(){
		var user = document.getElementById("un");
		var pass = document.getElementById("password");
		var a = /^[a-zA-z]{1}[a-zA-z0-9]/;
		var b = /^[a-zA-z1-9]{1}[a-zA-z0-9]/;
		
			if(user.value.length == "" && pass.value.length == ""){
			document.getElementById("show").innerHTML="Enter username";
			document.getElementById("show1").innerHTML="Enter password";
			}
			else if(user.value.length == ""){
			document.getElementById("show").innerHTML="Enter username";
			}
			else if(pass.value.length == ""){
			document.getElementById("show1").innerHTML="Enter password";
			}			
			else if(a.test(user.value) == true && b.test(pass.value) == true){
			document.getElementById("show").innerHTML="username saved";
			document.getElementById("show1").innerHTML="password saved";
			}
			else if(a.test(user.value) == false){
			document.getElementById("show").innerHTML="invalid format";
			}
			else{
			document.getElementById("show1").innerHTML="invalid format";
			}
		}
    </script>
</head>
    <body>

	 <table>

	<tr><td><input type="text"  id="un" placeholder="username"></td><td><p id="show"></p></td></tr>
	<tr><td><input type="password"  id="password" placeholder="password"></td><td><p id="show1"></p></td></tr>
	<tr><td><input type="button" value="Submit" onfocus="fun()"/></td></tr>
	
    </table>
</body>
</html>
