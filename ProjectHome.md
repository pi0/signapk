
```
Usage: signapk (options) [command] (files)
commands:
  sign FILE         sign a .zip or .apk
  sign FILE1 FILE2  create a signed copy of FILE1 as FILE2
  cert FILE(s)      print cert info on FILE's signer
  certinfo FILE     print detailed cert info on FILE's signer
  cmp FILE          compare signer of FILE with default/selected cert
  cmp FILE1 FILE2   compare signer of FILE1 to signer of FILE2

options:
  -k, --key FILE    key to sign with
  -c, --cert FILE   cert to sign with
                    if -c or -k are not files then they are considered
                    aliases to builtins (ie -k testkey or -c platform)
  -f, --force       sign even if cert differs from original
  -t, --tmp DIR     use DIR for tempdir instead of '/cache'
  -d, --debug       output debugging
  -V, --version     print 'signapk v0.3.1'
exit codes:
  1: read error (file 1)                2: read error (file 2)
  3: write error                        4: ssl error
  5: zip write error                    9: key error
  8: sign: cert mismatch                10: cmp: cert mismatch
  128: script error                     255: user error
```