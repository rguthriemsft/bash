# Shell Tricks

#### Which Shell am I using?

```Bash
ps -p $$
```

[Source](https://linuxhandbook.com/shell-using/)

#### Color coding test output in shell

```Bash
# Print text in red
_error() {
  printf "\e[31mERROR: $@\n\e[0m"
}

# Print information in cyan
_information() {
  printf "\e[36m$@\n\e[0m"
}

# Print success message in green
_success() {
  printf "\e[32mSUCCESS: $@\n\e[0m"
}
```

[source](http://www.andrewnoske.com/wiki/Bash_-_adding_color)
