# Insert data
Insert data into mysql database
 <?php 
	<?php
session_start(); 
$con = new mysqli("localhost","kashmirt_rashid","rashid123","kashmirt_fb"); //id757257_fyp FYP
             

	// initialize variables
	$name = "";
	$address = "";
	$id = 0;
	$update = false;

	if (isset($_POST['save'])) {
		$name = $_POST['name'];
		$age = $_POST['age'];
                $designation = $_POST['designation'];
		$organization = $_POST['organization'];

		mysqli_query($db, "INSERT INTO Psychologist (name, age, designation, organization) 
                VALUES ('$name', '$age','$designation', '$organization')"); 
		$_SESSION['message'] = "Address saved"; 
		header('location: info.php');
	}
  
  
