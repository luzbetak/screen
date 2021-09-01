Linux Screen 
============


### vi .screenrc
source $HOME/.screenrc-settings-default
source $HOME/.screenrc-windows-default

### vi .screenrc-settings-default
# Use a login shell (.bash_profile is read)
shell -bash
startup_message off
defscrollback 5000
autodetach on
logfile "$HOME/var/log/screen/%Y%m%d-%t"
hardstatus alwayslastline
backtick 101    999999  999999  perl -e 'print( join q[.], (split /\./, $ENV{HOSTNAME})[0..1] );'

### Redhat Screen Configuration 
hardstatus string '%{= kG}[ %{G}%101` %{g}][%= %{= kw}%?%-Lw%?%{r}(%{W}%n*%f %t%?(%u)%?%{r})%{w}%?%+Lw%?%?%= %{g}][%{B} %Y%m%d %{W}%c %{g}]'

### vi .screenrc-windows-default
screen -t root  0
screen -t httpd 1
screen -t edit1 2
screen -t edit2 3
screen -t mysql 4 
screen -t local 5 

### Kill screen session
screen -S 44226.kevin -X quit

