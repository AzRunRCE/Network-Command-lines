# Network-Command-lines
Momento about command lines

## Windows
- Run arbitary file on remote machine
  > PsExec.exe -d -i -u user -p password -c prog.exe \\IP_ADDRESS
  
- Admin share
  > IP_ADDRESS\c$
  
 - Run Elevated cmd
   > powershell.exe -Command "Start-Process cmd \"/k cd /d %cd%\" -Verb RunAs"
 - Get logged users (+ IP) of local network
   > for /l %%a in (0,1,256) do for /l %%v in (0,1,256) do echo *.*.%%a.%%v >> out.txt && QUERY USER /SERVER:*.*.%%a.%%v  >> out.txt
   > for /l %v in (0,1,256) do echo *.*.*.%v >> out.txt && QUERY USER /SERVER:*.*.*.%v  >> out.txt
   >
 - Remote shutdown computer
   > shutdown -i
 - Send message over network
   > msg * /server:IP_ADDRESS message
 
