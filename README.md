<!DOCTYPE html>
<html>
<head>
	<title>Registration form validation</title>
</head>
<script type="text/javascript">
	function validateform()
	{
		var x=document.forms["myform"]["name"].value;
		if(x=="")
		{
			alert("please fill your name!");
			return false;
		}
		if(x=NaN)
		{
			alert("name should not contain numbers");
			return false;
		}
		
		var y=document.forms["myform"]["email"].value;
		var atpos=y.indexOf("@");
		var dotpos=y.lastIndexOf(".");
		if(atpos<1||dotpos<atpos+2||dotpos+2>=y.length)
		{
			alert("please enter valid email address");
			return false;
		}

		var m=document.forms["myform"]["dob"].value;
		if(m=="")
		{
			alert("please fill date of birth");
			return false;
		}

		var addr=document.forms["myform"]["add"].value;
		if(addr=="")
			{
				alert("please fill address field");
				return false;
			}

		var p=document.forms["myform"]["mobile"].value;
		if(p.length<10)
		{
			alert("please enter valid phone number");
			return false;
		}
		if(p=="")
		{
			alert("please fill phome number");
			return false;
		}
		if(p!=NaN)
		{
			alert("mobile number should not contain alphabets");
			return false;
		}

	}
</script>
<body bgcolor="plum">
<form name="myform" method="post" onsubmit="return validateform()" bgcolor="pink">
	<table align="center" bgcolor="mistyrose" cellpadding="10px" cellspacing="2px" width="480px">
			<tr><td><font color="Red" align="center"><b>REGISTRATION FORM</b></font></td></tr>
		<tr>
			<td>Enter Your Name:</td>
			<td><input type="text" name="name"></td>
		</tr>
		<tr></tr>
		<tr>
			<td>Email id:</td>
			<td><input type="text" name="email"></td>
		</tr>
		<tr>
			<td>Date of Birth:</td>
			<td><input type="Date" name="dob"></td>
		</tr>
		<tr>
			<td>Gender:</td>
			<td><input type="radio" id="male" name="gender" value="male">male
			&nbsp;&nbsp;&nbsp;<input type="radio" id="female" name="gender" value="female">female</td></tr>
		<tr>
			<td>Address:</td>
			<td><textarea cols="16" rows="3" name="add" placeholder="enter address"></textarea></td>
		</tr>
		<tr>
			<td>Mobile Number:</td>
			<td><input type="text" name="mobile"></td>
		</tr>

		<tr>
			<td></td><td><button type="submit" align="center">register</button></td></tr>
	</table>
</body>
</html>
