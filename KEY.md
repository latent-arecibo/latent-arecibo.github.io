# Key

OpenPGP public key of Latent Arecibo.

- Fingerprint: `DB73 6505 A91D 8D0B 1FA4  0BD4 9324 8BA7 1765 4E95`
- Primary key: Ed25519, for signing. Subkey: Curve25519, for encryption.
- Created on 2026-10-15. No expiry date, so the key still works if you read this years from now.
- The same key as a file: `latent-arecibo.asc` (https://latent-arecibo.github.io/latent-arecibo.asc)

This key is used to:

- receive private messages: encrypt your message with it and paste the encrypted text in an issue;
- prove authorship: the author of Latent Arecibo can sign any statement with the matching private key.

## Send a private message

```
curl -s https://latent-arecibo.github.io/latent-arecibo.asc | gpg --import
gpg --encrypt --armor --recipient DB736505A91D8D0B1FA40BD493248BA717654E95 message.txt
```

Then paste the content of `message.txt.asc` in an issue. Any OpenPGP tool works, not only GnuPG.

## Check a signature

`README.md.asc` is a detached signature of `README.md`.

```
gpg --verify README.md.asc README.md
```

If the fingerprint in the result matches the one above, the text is the author's.

## Public key

```
-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEatD8jxYJKwYBBAHaRw8BAQdAsOhIJyZtfgrbS62toePIS+lMYFUu3Ekbh6Yr
51Z+vM60MUxhdGVudCBBcmVjaWJvIChodHRwczovL2xhdGVudC1hcmVjaWJvLmdp
dGh1Yi5pbymIrwQTFgoAVxYhBNtzZQWpHY0LH6QL1JMki6cXZU6VBQJq0PyPGxSA
AAAAAAQADm1hbnUyLDIuNSsxLjEyLDAsMwIbAwULCQgHAgIiAgYVCgkICwIEFgID
AQIeBwIXgAAKCRCTJIunF2VOlXPIAP0bL2v6Dr4muXcw7S0HPQxLDDZeKwyPSQ53
vUIb4rtcuQD/Qiz/2Fs/o9KDkclzM3KvnqBEOc02c2PdqhyOyxj46Q24OARq0PyQ
EgorBgEEAZdVAQUBAQdAh8XaYkljmTMvh4rAP+rrGwes7NotugOXw/BPFkq7YTMD
AQgHiJQEGBYKADwWIQTbc2UFqR2NCx+kC9STJIunF2VOlQUCatD8kBsUgAAAAAAE
AA5tYW51MiwyLjUrMS4xMiwwLDMCGwwACgkQkySLpxdlTpX+AAD/aL/s4DaPtW4+
AnMNn98zdWXYorKL0iNnLvw1h19feW8A/2ZI8EP7KwOccXJ//e7OCL5ROeLzyPkU
ce2FaRnp2jsB
=keD/
-----END PGP PUBLIC KEY BLOCK-----
```
