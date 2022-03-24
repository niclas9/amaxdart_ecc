# Elliptic curve cryptography (ECC) in Dart

Elliptic curve cryptography lib for AMA based blockchain in Dart lang.

## Usage

A simple usage example:

```dart
import 'package:amadart_ecc/amadart_ecc.dart';

main() {
  // Construct the AMA private key from string
  AMAPrivateKey privateKey = AMAPrivateKey.fromString(
      '5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3');

  // Get the related AMA public key
  AMAPublicKey publicKey = privateKey.toAMAPublicKey();
  // Print the AMA public key
  print(publicKey.toString());

  // Going to sign the data
  String data = 'data';

  // Sign
  AMASignature signature = privateKey.signString(data);
  // Print the AMA signature
  print(signature.toString());

  // Verify the data using the signature
  signature.verify(data, publicKey);
}
```

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

## References

eosjs-ecc: https://github.com/EOSIO/eosjs-ecc

[tracker]: https://github.com/niclas9/amadart_ecc/issues
