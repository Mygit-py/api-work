$url = "https://burpserver/api/apikey/v0.1/scan"
$scanNum = Read-Host "Enter scan number"
$apiURL = $url + "/" + $scanNum


$res = Invoke-RestMethod -Uri $apiURL -SkipCertificateCheck -Method Get

$scan = $res.issue_events

$fin = $scan.issue | select name,origin,path,severity,description

$fin | Export-Csv -Path "C:\foo\bar\Desktop\APItest.csv"
