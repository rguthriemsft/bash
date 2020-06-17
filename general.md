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
random_string() {
        # $1 The length of string to return
        echo $(head -30 /dev/urandom  | LC_CTYPE=c tr -dc 'a-z0-9' | fold -w $1 | head -n 1)
}

random_string 5
```

[source](https://www.saotn.org/bash-function-to-generate-a-random-alphanumeric-string/)

#### Tutorial on getopts

[source](https://www.shellscript.sh/tips/getopts/)
