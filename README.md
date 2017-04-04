 <?php
        $db_host = "if0ck476y7axojpg.cbetxkdyhwsb.us-east-1.rds.amazonaws.com"; // 
        $db_name = "jhx6l5925zfhgbl7"; //nombre de base de datos
        $db_user = "e10pni5qya8ern0s"; //nombre de usuario
        $db_password = "wsc7z45iu649ipq7";  //contrase�a 
    
      $connection = mysqli_connect('if0ck476y7axojpg.cbetxkdyhwsb.us-east-1.rds.amazonaws.com', 'e10pni5qya8ern0s', 'wsc7z45iu649ipq7');
    
     mysqli_select_db($connection, $db_name) or die("Error al seleccionar la base de datos:".mysqli_error());
    @mysqli_query("SET NAMES 'utf8'");
   $sql_query = "SELECT * FROM alumno";
    $result = mysqli_query($connection, $sql_query);
    $rows = array();
while($r = mysqli_fetch_assoc($result)) {
  $rows[] = $r;
}
print json_encode($rows);
?>
