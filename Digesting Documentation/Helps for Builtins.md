# Help for Builtins

 ## introduction
This Problem introduces builtins, which are built into the shell itself as opposed to manual pages which have a directory where they are stored at
 ## approach
- I start with `help` to find the command `challenge`
- follow it with `help challenge` to know details about challenge
- run `challenge --secret "cbqY8Muj" ` to retrieve the flag
 ## code
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@man~help-for-builtins:~$ help
GNU bash, version 5.2.32(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                                history [-c] [-d offset] [n] or history -anrw [filename]>
 (( expression ))                                            if COMMANDS; then COMMANDS; [ elif COMMANDS; then COMMAN>
 . filename [arguments]                                      jobs [-lnprs] [jobspec ...] or jobs -x command [args]
 :                                                           kill [-s sigspec | -n signum | -sigspec] pid | jobspec .>
 [ arg... ]                                                  let arg [arg ...]
 [[ expression ]]                                            local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                              logout [n]
 bg [job_spec ...]                                           mapfile [-d delim] [-n count] [-O origin] [-s count] [-t>
 bind [-lpsvPSVX] [-m keymap] [-f filename] [-q name] [-u >  popd [-n] [+N | -N]
 break [n]                                                   printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]                           pushd [-n] [+N | -N | dir]
 caller [expr]                                               pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMANDS ;;]... esa>  read [-ers] [-a array] [-d delim] [-i text] [-n nchars] >
 cd [-L|[-P [-e]] [-@]] [dir]                                readarray [-d delim] [-n count] [-O origin] [-s count] [>
 challenge [--fortune] [--version] [--secret SECRET]         readonly [-aAf] [name[=value] ...] or readonly -p
 command [-pVv] command [arg ...]                            return [n]
 compgen [-abcdefgjksuv] [-o option] [-A action] [-G globp>  select NAME [in WORDS ... ;] do COMMANDS; done
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o option] [-A act>  set [-abefhkmnptuvxBCEHPT] [-o option-name] [--] [-] [ar>
 compopt [-o|+o option] [-DEI] [name ...]                    shift [n]
 continue [n]                                                shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections]                        source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=value] ...] or declare -p>  suspend [-f]
 dirs [-clpv] [+N] [-N]                                      test [expr]
 disown [-h] [-ar] [jobspec ... | pid ...]                   time [-p] pipeline
 echo [-neE] [arg ...]                                       times
 enable [-a] [-dnps] [-f filename] [name ...]                trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                                              true
 exec [-cl] [-a name] [command [argument ...]] [redirectio>  type [-afptP] name [name ...]
 exit [n]                                                    typeset [-aAfFgiIlnrtux] name[=value] ... or typeset -p >
 export [-fn] [name[=value] ...] or export -p                ulimit [-SHabcdefiklmnpqrstuvxPRT] [limit]
 false                                                       umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last] or fc -s [pat=rep] [c>  unalias [-a] name [name ...]
 fg [job_spec]                                               unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done                until COMMANDS; do COMMANDS-2; done
 for (( exp1; exp2; exp3 )); do COMMANDS; done               variables - Names and meanings of some shell variables
 function name { COMMANDS ; } or name () { COMMANDS ; }      wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]                            while COMMANDS; do COMMANDS-2; done
 hash [-lr] [-p pathname] [-dt] [name ...]                   { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "cbqY8Muj".
hacker@man~help-for-builtins:~$ challenge --secret "cbqY8Muj"
Correct! Here is your flag!
pwn.college{cbqY8MujthMXQa09qtOuN96GdyZ.dRTM5QDLzgTN0czW}

```
