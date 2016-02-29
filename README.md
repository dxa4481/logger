# logger
Simple javascript logging of fingerprint, IP address and user agent. This uses webRTC to grab internal, external, and IPv6 IP addresses, and it uses advanced finerprinting techniques including canvas fingerprinting to uniquely classify a user.

## Installation

```bash
    bower install logger.io
```

## Example usage

```javascript
  <script src="bower_components/fingerprintjs2/fingerprintjs2.js"></script>
  <script src="ip_scraper.js"></script>
  <script src="logger.js"></script>
  <script> sendInfo("/loggingEndpoint"); </script>
```

## Payload structure

POST /loggingEndpoint
```json
  {
      "internalIPs": ["10.175.1.6", "192.168.1.2"],
      "externalIPs": {
          "ipv4": ["208.167.254.27"],
          "ipv6": ["2605:6000:1018:c0d1:682f:b2d8:377f:f2b"]
      },
      "fingerprintHash": "2721d05774cddaa25b1df66d02c5a17b",
      "userAgent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.106 Safari/537.36"
  }
```
