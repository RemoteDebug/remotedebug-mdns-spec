# Specification for RemoteDebug mDNS Devices

This is the specification for annnoncing RemoteDebug compatible devices over mDNS/Bonjour.

### Bonjour announcement:
```json
{
  name: "My Android phone", 
  type: "http", 
  subtype: "remotedebug"
  port: 9222,
  protocol: "tcp"
}
```

#### Addtional TXT-record for device meta-data:
```json
{
  device_type: "mobile",
  discover_url: "http://127.0.0.1:9222/json"
  runtime: "Chrome/37.0.2062.124",
  protocol_version: "1.1",
  user_agent: "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/37.0.2062.124 Safari/537.36"
}
```

## Properties

### device_type
`string` Describes the device type. Potential values: 

- mobile
- tv
- desktop
- service

### discover_url
`string` URL point to a HTTP JSON endpoint compliant too https://github.com/buggerjs/bugger-daemon#api  

### runtime
`string` runtime information. Typical named followed by version.

### protocol_version
`string` Protocol version

### user_agent 
`string` Browser/runtime user agent string

`




