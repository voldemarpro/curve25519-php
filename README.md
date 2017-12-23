# curve25519 php

Curve25519 library with Ed25519 signatures extension for PHP.

```php
$secureRandom = \openssl_random_pseudo_bytes(64);
$privateKey = curve25519_private($secureRandom);
$publicKey  = curve25519_public($private);

$secureRandom = \openssl_random_pseudo_bytes(64);
$agreement = curve25519_shared($privateKey, $publicKey);
$signature = curve25519_sign($secureRandom, $privateKey, $message);
$signatureValid  = curve25519_verify($publicKey, $message, $signature) == 0;
```

# Installation
## Linux and OS X

```
phpize
./configure
make
sudo make install
```

# License
MIT

