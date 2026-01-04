# parasplit
 Split wildcards.txt and Run parallelly

# Install
```
git clone https://github.com/rix4uni/parasplit.git && cd parasplit && chmod +x parasplit && cd .. && mv parasplit ~/bin
```

```
if ! grep -qxF 'export PATH="$HOME/bin/parasplit:$PATH"' ~/.bashrc ; then echo -e '\nexport PATH="$HOME/bin/parasplit:$PATH"' >> ~/.bashrc ; fi && source ~/.bashrc
```

```
parasplit -h
Usage: parasplit -j <number of jobs> -file <filename> <command template>
```

# Usage
This command split wildcards.txt in 5 files like this, then Running parallelly
```
split_01.txt
split_02.txt
split_03.txt
split_04.txt
split_05.txt
```

```
parasplit -j 5 -file wildcards.txt "findomain -f {} -q"
```
