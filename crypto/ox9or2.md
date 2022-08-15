# OX9OR2

* The following lines tells us that the text is encrypted with the ```^``` operator: 
```python
def xor(msg, key):
    o = ''
    for i in range(len(msg)):
        o += chr(ord(msg[i]) ^ ord(key[i % len(key)]))
    return o
```

* The following lines in ```encryption.py``` tells us that the key is alphanumeric and is 9 digits long, and that the unencrypted text contains ```SHELL```. 
```python
assert key.isalnum() and (len(key) == 9)
assert 'SHELL' in msg
```

* The following program give us part of the key ```XORISC``` by doing the ```^``` operation on the known part of the flag and the encrypted text. 
```python
with open('message', 'r') as f:
    msg = ''.join(f.readlines()).rstrip('\n')
    shl = 'SHELL{'
    for i in range(len(msg)):
        print(chr(ord(msg[i]) ^ ord(shl[i % len(shl)])))
```

* Renaming ```encryption``` to ```message```, removing the ```assert``` statements and running ```encryption.py``` gives us the flag bar a few characters: ```SHELL{V>__1S_R3Xk_51BL3}```
* Assuming that the first part of the flag is ```X0R```, we get that the key is ```XORISCOOL```. 
* Running ```encryption.py``` with the new key gives us the final flag. 
