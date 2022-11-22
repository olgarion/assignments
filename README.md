# assignments
a) One-way function (B. Schneier, Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition: https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003)
•	Easy to compute but hard (nearly impossible) to reverse
•	No secret parts so it can be public
•	It cannot be used for encryptions as-is because encrypted message cannot be decrypted
•	Trapdoor one-way function has a secret that helps to decode one way function which leaves us with the problem of sharing secrets between parties
•	One-way functions have a lot of use, e.g. checksum of downloaded file to validate that the file is original and not modified
‘A hash function is a function, mathematical or otherwise, that takes a variable-length input string (called a pre-image) and converts it to a fixed-length (generally 
smaller) output string (called a hash value).’(B. Schneier, Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition)
A one-way hash function is a hash function that works in one way only, it is easy to generate a hash value but it is hard to re-create the pre-image that leads to 
a particular values.
https://terokarvinen.com/2022/cracking-passwords-with-hashcat/

b) Crack this hash: 21232f297a57a5a743894a0e4a801fc3
Identify Hash Types of the 21232f297a57a5a743894a0e4a801fc3
![image](https://user-images.githubusercontent.com/117819595/203412715-bc057f65-8317-4f82-bffc-534aef1fe7d0.png)
I used hash type MD5 as in the exercise
$ hashcat -m 0 '21232f297a57a5a743894a0e4a801fc3' rockyou.txt -o solved
![image](https://user-images.githubusercontent.com/117819595/203412834-893e7dfe-a603-40d8-91d6-f1f709d48861.png)
![image](https://user-images.githubusercontent.com/117819595/203412852-4050336f-d945-4cf5-9cc4-bb96cf657e5f.png)
Password: admin
c) Crack this Windows NTLM hash: f2477a144dff4f216ab81f2ac3e3207d
Hash types:
![image](https://user-images.githubusercontent.com/117819595/203412944-23cf4b6c-c4bc-4643-8de8-a126c0ebbcf8.png)
I used hash type Double MD5 and I got exhausted:
![image](https://user-images.githubusercontent.com/117819595/203413007-10f2caaa-b86a-42eb-b0c0-09dfe748ded8.png)
Exhausted simply means hashcat has tried every possible password combination in the attack you have provided, and failed to crack 100% of all hashes given. 
In other words, hashcat has finished doing everything you told it to do – it has exhausted its search to crack the hashes. 
You should run hashcat again with a different attack/word list/mask etc. 
(https://hashcat.net/wiki/doku.php?id=frequently_asked_questions#i_may_have_the_wrong_driver_installed_what_should_i_do)
When I chose type NTLM: 1000 it got cracked:

![image](https://user-images.githubusercontent.com/117819595/203413151-567bd828-1efc-4da8-94c2-dd43e2e70b9a.png)

Password: monkey
d) Try cracking this hash and comment on your hash rate $2y$18$axMtQ4N8j/NQVItQJed9uORfsUK667RAWfycwFMtDBD6zAo1Se2eu . This subtask does not require actually cracking the hash, just trying it and commenting on the hash rate.

![image](https://user-images.githubusercontent.com/117819595/203413909-a40f47b9-edbd-4740-abef-0a80bb97a2cc.png)

It took 3 sec to crack

![image](https://user-images.githubusercontent.com/117819595/203414124-b8027dde-c42a-497b-bceb-eb3b933d4686.png)

I understand that it is the 2nd password it processed from the list.
f) Voluntary bonus: create some hashes of your own, then crack them with hashcat.
Generated at https://www.md5hashgenerator.com/
62a8119bc71653262e915983550b1885f80e2e3d

![image](https://user-images.githubusercontent.com/117819595/203414176-2c6a7a9d-fd8b-4ce9-8247-fc4991282f45.png)




