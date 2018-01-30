<?php
    $hostname = test.cloud-ace.jp.;
    $username = takatori;
    $password = takatori;
    $dbname = "mysql";

    $connect = mysqli_connect($hostname, $username, $password);
    mysqli_select_db($connect,$dbname);

    $sql = "select * from user;";
    $sqlq = mysqli_query($connect, $sql); 
    while($row = mysqli_fetch_array($sqlq)){
      echo $row["User"];
    }
    mysqli_free_result($sqlq);
    mysqli_close($connect);
?>
