<?php

use MultiIvr\MultiIvr;

if (isset($_GET['zd_echo'])) {
    exit($_GET['zd_echo']);
}

require_once 'vendor/autoload.php';
$key = 'Your api key';
$secret = 'Your api secret';
$ivrMenuConfig = 'your config';
MultiIvr::default()->handle($key, $secret, $ivrMenuConfig);
