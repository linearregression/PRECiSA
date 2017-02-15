PVS PRECiSA 
==

To check the symbolic certificate generated by PRECiSA in PVS, the directory
`PVS` has to be added to the Unix environment variable
`PVS_LIBRARY_PATH`.  Depending upon your shell, one of the following lines
has to be added to your startup script.  In C shell (csh or tcsh), put this line in
`~/.cshrc`, where `<precisadir>` is the absolute path to the PRECiSA
directory `PVS`:

~~~
setenv PVS_LIBRARY_PATH "<precisapvsdir>:$PVS_LIBRARY_PATH"
~~~

In Borne shell (bash or sh), put this line in either `~/.bashrc or ~/.profile`:

~~~
export PVS_LIBRARY_PATH="<precisapvsdir>/nasalib:$PVS_LIBRARY_PATH"
~~~

To re-prove the PVS PRECiSA development and the provided examples `CD2D_tau`
and `CPR`, type the following command in a Unix shell.

```
$ provethem all-theories
```

The output of that command is

```
PRECiSA                  [OK: 87 proofs]
CD2D_tau                 [OK: 57 proofs]
CPR                      [OK: 8 proofs]

*** Grand Total: 152 proofs / 152 formulas. Missed: 0 formulas.
```