# General

#### Multi-line string to file

```Bash
kernel="2.6.39"
distro="xyz"
cat >/etc/myconfig.conf <<EOL
line 1, ${kernel}
line 2, 
line 3, ${distro}
line 4 line
... 
EOL

cat /etc/myconfig.conf
```

#### Random number generation in bash

This outputs at max 4 bytes (the -N4 flag) signed decimal ints (-i) at no address (-An).

```Bash
od -An -N4 -i < /dev/urandom
```

[source](https://coderwall.com/p/s2ttyg/random-number-generator-in-bash)

#### Random alphanumeric string in bash (issues on MAc)

```Bash
random-string() {
        cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w ${1:-32} | head -n 1
}
```

[source](https://www.saotn.org/bash-function-to-generate-a-random-alphanumeric-string/)
