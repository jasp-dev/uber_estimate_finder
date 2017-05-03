<?php
$ch = curl_init();

curl_setopt($ch, CURLOPT_URL, "https://api.uber.com/v1.2/estimates/price?start_latitude=30.8452&start_longitude=75.6726&end_latitude=30.8913&end_longitude=75.8284");
curl_setopt($ch, CURLOPT_RETURNTRANSFER, TRUE);
curl_setopt($ch, CURLOPT_HEADER, FALSE);

curl_setopt($ch, CURLOPT_HTTPHEADER, array(
  "Authorization: Token API_TOCKEN",
  "Accept-Language: en_US",
  "Content-Type: application/json"
));


$data = curl_exec($ch);
$curl_error = curl_errno($ch);
$getserver= curl_getinfo($ch);
   

$json = json_decode($data, true);

curl_close($ch);

var_dump($data );

echo '<hr/>';
$value = $json['prices']['1']['high_estimate'];

echo $value;



?>
