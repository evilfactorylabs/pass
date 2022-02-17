# pass

Every credentials used by evilfactorylabs are here using [`pass(1)`](https://www.passwordstore.org/) as a password manager, so you need to have
one if you haven't installed it.

Also, you need a [`pass-otp`](https://github.com/tadfisher/pass-otp) extension to generate the TOTP code, go install it!

The GPG signature used is `07EFAC00F86F1434` where the public key can be accessed [here](https://github.com/anakmagang.gpg).

## Quick Start

### Get password for evilfactorylabs Twitter

```bash
pass get Twitter/evilfactorylabs | pbcopy
```

### Get OTP code for evilfactorylabs Twitter


```bash
pass otp OTP/Twitter/evilfactorylabs | pbcopy
```

That's it.

## Tips

All commits must be signed. Plus if you have multiple git accounts on your machine, you can use this as a trick:

```
[includeIf "gitdir:~/.password-store/"]
  [user]
    name = evilfactorylabs
    email = contact@evilfactorylabs.org
    signkey = 15FB567DCBFA1A6C75DC6F9107EFAC00F86F1434
```

If you currently use `pass` as your primary password manager too, maybe you use this approach:

```
[includeIf "gitdir:~/.password-store/evilfactorylabs"]
  [user]
    name = evilfactorylabs
    email = contact@evilfactorylabs.org
    signkey = 15FB567DCBFA1A6C75DC6F9107EFAC00F86F1434
```

Where `~/.password-store/evilfactorylabs` is symlinked to somewhere...
