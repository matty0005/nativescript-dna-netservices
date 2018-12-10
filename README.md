# NativeScript DNA NetServices

![nativescript-dna-netservices](https://raw.githubusercontent.com/DeepakArora76/nativescript-dna-netservices/master/dna-netservices.png)

NativeScript plugin for Bonjour/ZeroConf and network monitor. RxJS based APIs for Android and iOS. Easy to use APIs for service discovery, browsing and publication, and networking monitoring.

### Features

- Cross platform APIs for Android and iOS
- Service Discovery, Resolution, Browse, and Publication
- Monitor network availability
- WiFi and Cellular IP address retrieval

More about Bonjour/ZerConf can be found at:
[ Apple’s Bonjour implementation](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/NetServices/Introduction.html#//apple_ref/doc/uid/TP40002445-SW1 " Apple’s Bonjour implementation") and [Android mDNSResponder](https://github.com/andriydruk/RxDNSSD "Android mDNSResponder")

## Installation

From the command prompt go to your app's root folder and execute:

```javascript
tns plugin add nativescript-dna-netservices
```
This command automatically installs the necessary files, as well as stores **nativescript-dna-netservices** as a dependency in your project's package.json file.

## API

NativeScript DNA NetServices APIs are classified into the following services:
- **NetworkMonitorService**: Provides APIs for monitoring network availability and accessing device IP address
- **ZeroConfService**: Deals with service resolution and publication part of Bonjour/ZeroConf 
- **ZeroConfServiceBrowser**: Involves with service browsing part of Bonjour/ZeroConf

In the following sections, we will explore various APIs under various services.

### - NetworkMonitorService
JavaScript flavored version looks like:
```javascript
import { NetworkMonitorService } from "nativescript-dna-netservices";
```

JavaScript flavored version looks like:
```javascript
var NetworkMonitorService = require("nativescript-dna-netservices");
```

```javascript
NetworkMonitorService.getWiFiIpAddress()
.pipe(tap(ip => console.info(ip)))
.subscribe(ipAddr => {
  console.info(ipAddr)
});
```

## License

Apache License Version 2.0, January 2004
