# password-hashcat
Documentation of the steps to run Hashcat on Ubuntu 20.04 terminal for cracking passwords with MD5 encryption.
----------------------------------------------------------------------------------------

1. **Installing Hashcat**
    
    • on the terminal, run: ` sudo apt-get install hashcat ` 
    
2. **Creating directories**
    
    • create a main directory that would contain the project files: ` mkdir gshc `
    
    • create a sub-directory that would have wordlists, output & input files: ` mkdir skull ` 
    
3. **Downloading requirements:**
    
    • wordlist used: rockyou.txt from skullsecurity
    
    • input file used: password_dump.txt
                       ` gshc/skull$ cat password_dump.txt `  displays the file
                       modified to target_hash.txt; having only hashes
                       
    • output file: blank text file created to which output will be written (output.txt)
    
4. **Running Hashcat:**
    
    • to crack the hashes, the following command was used:
        ` gshc/skull$ sudo hashcat -m 0 target_hash.txt -o output.txt rockyou.txt ` 
        
    • the output was written to the output.txt file, which was displayed using:
        ` gshc/skull$ sudo cat output.txt `

----------------------------------------------------------------------------------------

Input:

e10adc3949ba59abbe56e057f20f883e
25f9e794323b453885f5181f1b624d0b
d8578edf8458ce06fbc5bb76a58c5ca4
5f4dcc3b5aa765d61d8327deb882cf99
96e79218965eb72c92a549dd5a330112
25d55ad283aa400af464c76d713c07ad
e99a18c428cb38d5f260853678922e03
fcea920f7412b5da7be0cf42b8c93759
7c6a180b36896a0a8c02787eeafb0e4c
6c569aabbf7775ef8fc570e228c16b98
3f230640b78d7e71ac5514e57935eb69
917eb5e9d6d6bca820922a0c6f7cc28b
f6a0cb102c62879d397b12b62c092c06
9b3b269ad0a208090309f091b3aba9db
16ced47d3fc931483e24933665cded6d
1f5c5683982d7c3814d4d9e6d749b21e
8d763385e0476ae208f21bc63956f748
defebde7b6ab6f24d5824682a16c3ae4
bdda5f03128bcbdfa78d8934529048cf


Results Obtained:

e10adc3949ba59abbe56e057f20f883e:123456
25f9e794323b453885f5181f1b624d0b:123456789
5f4dcc3b5aa765d61d8327deb882cf99:password
fcea920f7412b5da7be0cf42b8c93759:1234567
25d55ad283aa400af464c76d713c07ad:12345678
e99a18c428cb38d5f260853678922e03:abc123
d8578edf8458ce06fbc5bb76a58c5ca4:qwerty
96e79218965eb72c92a549dd5a330112:111111
7c6a180b36896a0a8c02787eeafb0e4c:password1
6c569aabbf7775ef8fc570e228c16b98:password!
3f230640b78d7e71ac5514e57935eb69:qazxsw
f6a0cb102c62879d397b12b62c092c06:bluered
917eb5e9d6d6bca820922a0c6f7cc28b:Pa$$word1
