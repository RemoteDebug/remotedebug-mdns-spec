# Specification for RemoteDebug MDNS Devices

This is the specification for annnoncing RemoteDebug compatible devices over MDNS/Bonjour.

Bonjour announcement:
```json
{
  name: "My Android phone", 
  type: "http", 
  subtype: "remotedebug"
  port: 9222,
  protocol: "tcp"
}
```

Addtional TXT-record for device meta-data:
```json
{
  name: "My device name",
  device_type: "mobile",
  runtime: "Chrome/37.0.2062.124",
  protocol_version: "1.1",
  user_agent: "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/37.0.2062.124 Safari/537.36"
}
```




`




