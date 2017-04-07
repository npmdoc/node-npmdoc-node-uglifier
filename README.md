# api documentation for  [node-uglifier (v0.5.41)](https://github.com/zsoltszabo/node-uglifier)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-uglifier.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-uglifier) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-uglifier.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-uglifier)
#### Fully auto merging and uglifying a whole NodeJs project into one file with external files option. Thieves lose the module name and structure information, code runs faster. Makes deployement super easy!
Also now you can separate your dependencies!

[![NPM](https://nodei.co/npm/node-uglifier.png?downloads=true)](https://www.npmjs.com/package/node-uglifier)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-uglifier_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Zsolt Istvan Szabo",
        "email": "zsoltszabo317@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/zsoltszabo/node-uglifier/issues"
    },
    "contributors": [],
    "dependencies": {
        "fs-extra": "=2.0",
        "optparse": ">=0.x",
        "seedrandom": ">=0.x",
        "sugar": "=2.0.4",
        "uglify-js-harmony": "=2.6.2",
        "underscore": ">=1.5.2"
    },
    "description": "Fully auto merging and uglifying a whole NodeJs project into one file with external files option. Thieves lose the module name and structure information, code runs faster. Makes deployement super easy!\nAlso now you can separate your dependencies!",
    "devDependencies": {
        "express": "4.14.0",
        "nodeunit": "=0.10.2"
    },
    "directories": {},
    "dist": {
        "shasum": "2bdd0699eddcc417689f042439ce6dd614317b8f",
        "tarball": "https://registry.npmjs.org/node-uglifier/-/node-uglifier-0.5.41.tgz"
    },
    "engines": {
        "node": "> 0.6.0"
    },
    "gitHead": "f60dabe36ca86257b9b13ac5cf3d281d57cdce2f",
    "homepage": "https://github.com/zsoltszabo/node-uglifier",
    "keywords": [
        "obfuscate",
        "total",
        "whole",
        "project",
        "protect",
        "minify",
        "code protect",
        "uglify",
        "mangle",
        "compress",
        "automatic",
        "code separation",
        "separate dependencies",
        "sub project extraction"
    ],
    "main": "./index.js",
    "maintainers": [
        {
            "name": "arbitrager",
            "email": "zsoltszabo@web.de"
        }
    ],
    "name": "node-uglifier",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/zsoltszabo/node-uglifier.git"
    },
    "scripts": {
        "test": "node nodeunit.js ./lib_compiled/test/unitTest.js"
    },
    "url": "https://github.com/zsoltszabo/node-uglifier",
    "version": "0.5.41"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-uglifier](#apidoc.module.node-uglifier)
1.  object <span class="apidocSignatureSpan">node-uglifier.</span>ipaddr
1.  string <span class="apidocSignatureSpan">node-uglifier.</span>version

#### [module node-uglifier.ipaddr](#apidoc.module.node-uglifier.ipaddr)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>IPv4 (octets)](#apidoc.element.node-uglifier.ipaddr.IPv4)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>IPv6 (parts)](#apidoc.element.node-uglifier.ipaddr.IPv6)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>fromByteArray (bytes)](#apidoc.element.node-uglifier.ipaddr.fromByteArray)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>isValid (string)](#apidoc.element.node-uglifier.ipaddr.isValid)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>parse (string)](#apidoc.element.node-uglifier.ipaddr.parse)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>parseCIDR (string)](#apidoc.element.node-uglifier.ipaddr.parseCIDR)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>process (string)](#apidoc.element.node-uglifier.ipaddr.process)
1.  [function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>subnetMatch (address, rangeList, defaultName)](#apidoc.element.node-uglifier.ipaddr.subnetMatch)



# <a name="apidoc.module.node-uglifier"></a>[module node-uglifier](#apidoc.module.node-uglifier)



# <a name="apidoc.module.node-uglifier.ipaddr"></a>[module node-uglifier.ipaddr](#apidoc.module.node-uglifier.ipaddr)

#### <a name="apidoc.element.node-uglifier.ipaddr.IPv4"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>IPv4 (octets)](#apidoc.element.node-uglifier.ipaddr.IPv4)
- description and source-code
```javascript
function IPv4(octets) {
  var j, len, octet;
  if (octets.length !== 4) {
    throw new Error("ipaddr: ipv4 octet count should be 4");
  }
  for (j = 0, len = octets.length; j < len; j++) {
    octet = octets[j];
    if (!((0 <= octet && octet <= 255))) {
      throw new Error("ipaddr: ipv4 octet should fit in 8 bits");
    }
  }
  this.octets = octets;
}
```
- example usage
```shell
...

  IPv6.prototype.toIPv4Address = function() {
    var high, low, ref;
    if (!this.isIPv4MappedAddress()) {
      throw new Error("ipaddr: trying to convert a generic ipv6 address to ipv4");
    }
    ref = this.parts.slice(-2), high = ref[0], low = ref[1];
    return new ipaddr.IPv4([high >> 8, high & 0xff, low >> 8, low & 0xff]);
  };

  return IPv6;

})();

ipv6Part = "(?:[0-9a-f]+::?)+";
...
```

#### <a name="apidoc.element.node-uglifier.ipaddr.IPv6"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>IPv6 (parts)](#apidoc.element.node-uglifier.ipaddr.IPv6)
- description and source-code
```javascript
function IPv6(parts) {
  var i, j, k, len, part, ref;
  if (parts.length === 16) {
    this.parts = [];
    for (i = j = 0; j <= 14; i = j += 2) {
      this.parts.push((parts[i] << 8) | parts[i + 1]);
    }
  } else if (parts.length === 8) {
    this.parts = parts;
  } else {
    throw new Error("ipaddr: ipv6 part count should be 8 or 16");
  }
  ref = this.parts;
  for (k = 0, len = ref.length; k < len; k++) {
    part = ref[k];
    if (!((0 <= part && part <= 0xffff))) {
      throw new Error("ipaddr: ipv6 part should fit in 16 bits");
    }
  }
}
```
- example usage
```shell
...

ipaddr.fromByteArray = function(bytes) {
  var length;
  length = bytes.length;
  if (length === 4) {
    return new ipaddr.IPv4(bytes);
  } else if (length === 16) {
    return new ipaddr.IPv6(bytes);
  } else {
    throw new Error("ipaddr: the binary input is neither an IPv6 nor IPv4 address");
  }
};

ipaddr.process = function(string) {
  var addr;
...
```

#### <a name="apidoc.element.node-uglifier.ipaddr.fromByteArray"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>fromByteArray (bytes)](#apidoc.element.node-uglifier.ipaddr.fromByteArray)
- description and source-code
```javascript
fromByteArray = function (bytes) {
  var length;
  length = bytes.length;
  if (length === 4) {
    return new ipaddr.IPv4(bytes);
  } else if (length === 16) {
    return new ipaddr.IPv6(bytes);
  } else {
    throw new Error("ipaddr: the binary input is neither an IPv6 nor IPv4 address");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uglifier.ipaddr.isValid"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>isValid (string)](#apidoc.element.node-uglifier.ipaddr.isValid)
- description and source-code
```javascript
isValid = function (string) {
  return ipaddr.IPv6.isValid(string) || ipaddr.IPv4.isValid(string);
}
```
- example usage
```shell
...
  } catch (error) {
    e = error;
    return false;
  }
};

ipaddr.IPv4.isValidFourPartDecimal = function(string) {
  if (ipaddr.IPv4.isValid(string) && string.match(/^\d+(\.\d+){3}$/)) {
    return true;
  } else {
    return false;
  }
};

ipaddr.IPv6.isValid = function(string) {
...
```

#### <a name="apidoc.element.node-uglifier.ipaddr.parse"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>parse (string)](#apidoc.element.node-uglifier.ipaddr.parse)
- description and source-code
```javascript
parse = function (string) {
  if (ipaddr.IPv6.isValid(string)) {
    return ipaddr.IPv6.parse(string);
  } else if (ipaddr.IPv4.isValid(string)) {
    return ipaddr.IPv4.parse(string);
  } else {
    throw new Error("ipaddr: the address has neither IPv6 nor IPv4 format");
  }
}
```
- example usage
```shell
...
};

IPv4.prototype.range = function() {
  return ipaddr.subnetMatch(this, this.SpecialRanges);
};

IPv4.prototype.toIPv4MappedAddress = function() {
  return ipaddr.IPv6.parse("::ffff:" + (this.toString()));
};

IPv4.prototype.prefixLengthFromSubnetMask = function() {
  var cidr, i, j, octet, stop, zeros, zerotable;
  zerotable = {
    0: 8,
    128: 7,
...
```

#### <a name="apidoc.element.node-uglifier.ipaddr.parseCIDR"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>parseCIDR (string)](#apidoc.element.node-uglifier.ipaddr.parseCIDR)
- description and source-code
```javascript
parseCIDR = function (string) {
  var e, error, error1;
  try {
    return ipaddr.IPv6.parseCIDR(string);
  } catch (error) {
    e = error;
    try {
      return ipaddr.IPv4.parseCIDR(string);
    } catch (error1) {
      e = error1;
      throw new Error("ipaddr: the address has neither IPv6 nor IPv4 CIDR format");
    }
  }
}
```
- example usage
```shell
...
    throw new Error("ipaddr: the address has neither IPv6 nor IPv4 format");
  }
};

ipaddr.parseCIDR = function(string) {
  var e, error, error1;
  try {
    return ipaddr.IPv6.parseCIDR(string);
  } catch (error) {
    e = error;
    try {
      return ipaddr.IPv4.parseCIDR(string);
    } catch (error1) {
      e = error1;
      throw new Error("ipaddr: the address has neither IPv6 nor IPv4 CIDR format");
...
```

#### <a name="apidoc.element.node-uglifier.ipaddr.process"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>process (string)](#apidoc.element.node-uglifier.ipaddr.process)
- description and source-code
```javascript
process = function (string) {
  var addr;
  addr = this.parse(string);
  if (addr.kind() === 'ipv6' && addr.isIPv4MappedAddress()) {
    return addr.toIPv4Address();
  } else {
    return addr;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uglifier.ipaddr.subnetMatch"></a>[function <span class="apidocSignatureSpan">node-uglifier.ipaddr.</span>subnetMatch (address, rangeList, defaultName)](#apidoc.element.node-uglifier.ipaddr.subnetMatch)
- description and source-code
```javascript
subnetMatch = function (address, rangeList, defaultName) {
  var j, len, rangeName, rangeSubnets, subnet;
  if (defaultName == null) {
    defaultName = 'unicast';
  }
  for (rangeName in rangeList) {
    rangeSubnets = rangeList[rangeName];
    if (rangeSubnets[0] && !(rangeSubnets[0] instanceof Array)) {
      rangeSubnets = [rangeSubnets];
    }
    for (j = 0, len = rangeSubnets.length; j < len; j++) {
      subnet = rangeSubnets[j];
      if (address.match.apply(address, subnet)) {
        return rangeName;
      }
    }
  }
  return defaultName;
}
```
- example usage
```shell
...
  loopback: [[new IPv4([127, 0, 0, 0]), 8]],
  carrierGradeNat: [[new IPv4([100, 64, 0, 0]), 10]],
  "private": [[new IPv4([10, 0, 0, 0]), 8], [new IPv4([172, 16, 0, 0]), 12], [new IPv4([192, 168, 0, 0]), 16]],
  reserved: [[new IPv4([192, 0, 0, 0]), 24], [new IPv4([192, 0, 2, 0]), 24], [new IPv4([192, 88, 99, 0]), 24], [new IPv4([198, 51
, 100, 0]), 24], [new IPv4([203, 0, 113, 0]), 24], [new IPv4([240, 0, 0, 0]), 4]]
};

IPv4.prototype.range = function() {
  return ipaddr.subnetMatch(this, this.SpecialRanges);
};

IPv4.prototype.toIPv4MappedAddress = function() {
  return ipaddr.IPv6.parse("::ffff:" + (this.toString()));
};

IPv4.prototype.prefixLengthFromSubnetMask = function() {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
