# RSACore
RSACore For Python

A simple RSA library for python with built-in AES, which allows you to exchange encrypted data with an unlimited size.

Installation:

For Windows:
```bash
pip install rsacore
```
For Linux or MacOS:
```bash
pip3 install rsacore
```

Example:
```python
from rsacore import Core

RSA = Core()
RSA2 = Core()
RSA.SetPubKey(RSA2.GenKeys())
RSA2.SetPubKey(RSA.GenKeys())
msg = "Test msg"
data = RSA.Encrypt(msg.encode())
print(data)
data = RSA2.Decrypt(data)
print(data.decode())
```
