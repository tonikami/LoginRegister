>?php
    $con = mysql_connect("localhost","my_user","my_password","my_db");
	
	
	$username = $_POST[username];
	$password = $_POST[password];
	
	
	$statement = mysql_prepare($con,"SELECT * FROM User WHERE username = ? AND password = ?");
	mysql_stmt_bind_param($statement,"ss",$username,$password);  
	mysql_stmt_execute = ($statement);
	
	mysql_stmt_store_result($statement);
	mysql_stmt_bind_result($statement,$userID ,$name, $username,$email,$password,$ContactNo);
	
	$user = array[];
	while(mysql_stmt_fetch($statement)){
		
		$user[name] = $name;
		$user[username] = $username;
		$user[email] = $email;
		$user[password] = $password;
		$user[ContactNo] = $ContactNo;
		
	}
	
	echo json_encode($user);
	
	mysql_stmt_close($statement);
	
	mysql_close($con);
?>
