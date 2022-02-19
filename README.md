# password-hashcat
Documentation of the steps to run Hashcat on Ubuntu 20.04 terminal for cracking passwords with MD5 encryption.
----------------------------------------------------------------------------------------

1. Installing Hashcat
    • on the terminal, run: sudo apt-get install hashcat
2. Creating directories
    • create a main directory that would contain the project files: mkdir gshc
    • create a sub-directory that would have wordlists, output & input files: mkdir skull
3. Downloading requirements:
    • wordlist used: rockyou.txt from skullsecurity
    • input file used: password_dump.txt
                       gshc/skull$ cat password_dump.txt displays the file
                       modified to target_hash.txt; having only hashes
                       
    • output file: blank text file created to which output will be written (output.txt)
4. Running Hashcat
    • to crack the hashes, the following command was used:
        gshc/skull$ sudo hashcat -m 0 target_hash.txt -o output.txt rockyou.txt
    • the output was written to the output.txt file, which was displayed using:
        gshc/skull$ sudo cat output.txt
    
