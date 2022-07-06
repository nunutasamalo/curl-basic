# curl-basic

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
