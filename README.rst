Python XTEA

    This is an implementation of XTEA-Cipher in Python (eXtended Tiny Encryption Algorithm).

    XTEA is a blockcipher with 8 bytes blocksize and 16 bytes Keysize (128-Bit).
    The algorithm is secure at 2014 with the recommend 64 rounds (32 cycles). This
    implementation supports following modes of operation:
    ECB, CBC, OFB, CTR (buggy)


Example:

    >>> from xtea import *
    >>> key = " "*16  # Never use this
    >>> text = "This is a text. "*8
    >>> x = new(key, mode=MODE_OFB, IV="12345678")
    >>> c = x.encrypt(text)
    >>> text == x.decrypt(c)
    True
    
Note
   
    I does NOT guarantee that this implementation is secure. If there are bugs, tell me them. 
    Python 3 support is at work.
    My GPG/PGP key: 0CB97138 (full fingerprint: 8F93 4984 3BA7 4A1C E5F2  A1BA 1338 DFDE 0CB9 7138)