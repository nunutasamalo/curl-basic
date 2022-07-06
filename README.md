# curl-basic
Trouble shoot connection with from terminal using curl
curl -v http://example.com -o saved
curl https://192.168.7.110:18030

 
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, $your_url);
curl_setopt($ch, CURLOPT_FAILONERROR, true); // Required for HTTP error codes to be reported via our call to curl_error($ch)
//...
curl_exec($ch);
if (curl_errno($ch)) {
    $error_msg = curl_error($ch);
}
curl_close($ch);

if (isset($error_msg)) {
    // TODO - Handle cURL error accordingly
}
