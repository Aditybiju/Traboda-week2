# biOs -Traboda

**Challenge1: Multi-Encoder**
-----------------------------

**Challenge description** :

Its all about the base

**Flag:** inctfj{Y0u\_@re\_Qu1t3\_th3\_D3c0d3r}

**Approach:**

I solved using a python code.I opened the text file and found out that it is encoded.Then i opened the enc.py file and found out that the text file is encoded using hex and binary and also the the python code specified that it has been encrypted 5 times. So i imported two libraries binascii and base64 and used a python code . In that pthon code i used a for loop that has binascii.hexlify() and also base64.b64decode() and used print function to print the flag.binascii.hexlify() : It returns the hexadecimal representation of the binary data. It returns the decoded string.

**Challenge2: Base-Base-Base**
----------------------------------

**Challenge description:**

Have you heard of bases? I heard combination of those can be really cool!

**Flag** : inctfj{b4s3s\_4r3\_c00000000l}

**Approach:**

I opened the base.txt given and found it is encoded. It was encoded with base64 so decoded it using linux command:

echo&quot;text given&quot;|base64 --decode --;This actually decodes the base64 encryted text and after decoding i got a base32 encoded text.so i used the following command:

echo&quot; &quot;|base32 --decode --; This actually decodes the base32 encrypted text and after decoding it i got a hex encrypted text. So i used the folllowing command :

echo&quot; &quot;|xxd -p-r|base64--; This actually decodes the text and i got a base64 encoded text. And i decoded it to get the flag.

**Challenge3: Single byte Xor**
----------------------------------

**challenge description:**

Given a hex encoded string: 1314190e1c1001024a0825194e145d0e251849251f4e091316032518084a11491407 The above string has been Xored against a single character &#39;z&#39;. Decode it to a meaningful sentence and get the flag.

**Flag** : inctfj{x0r\_c4n&#39;t\_b3\_e4sily\_br0k3n}

**Approach:**

I opened the cipher text provided and found that it has been xored against a single character `z. we just need to xor it again with the same key t`o get the flag.

**Challenge4:**  **Naïve Cipher**
----------------------------------

**Challenge description:**

This Cipher is a very simple and common encryption method which forms part of the basis of cryptography. It simply shifts a string of letters a certain number of positions up or down the alphabet.

encoded string:`dixoae{oczz_ocz_hvnozm_ja_xvznzm_xdkczm}`

**Flag** : inctfj{thee_the_master_of_caeser_cipher}

**Approach:** So the text has been shifted with the key -5 by comparing the original flag to the text given .So we just decrypt it using this info.

**Challenge5: Angry Steve**
----------------------------------

**Challenge description**** :**

Jimmy found out about an embaraasing picture of his dad Steve. He believes that there is a text inside that file somwhere. But he is too scared to open and tamper with it as his father is a very short tempered man. Help Jimmy out!

**Flag**: inctfj{string5\_m4keth\_fl4gs}

**Approach** :

Opened the file angry.jpg and first i thought of checking the metadata but couldn&#39;t find anything. Then i used the folllowing command:

stringsangry.jpg|grep&quot;inctfj&quot;
 this command actually extracts all the printable character and grep finds the string specified. So after running this comand i got the flag.

**Challenge6: Mischief Kid**
----------------------------------

**Challenge description:**

Little Bart here is the biggest troublemaker in town. He is hiding the flag somewhere safe. Follow and bust out little Bart to get what you want!

**Flag** : inctfj{_4Ye_@aRr4mbB4_u_g0T_m3!}

**Approach:**

first used the command unzipmischief.jpg
so i found there are two files busted.png and flag.txt. First renamed flag.txt as flag.png and opened the file . But this file didn&#39;t have the flag. So downloaded ghex and used it to compare the magic numbers. So i found some numbers were missing from the busted.png file.so edited it to 89 50 4E 47 and opened busted.png and got the flag.

**Challenge7: Snow Man**
----------------------------------

Read the challenge name again! And yeah, everything you need is present in this file.

**Flag** : inctfj{h4h4_st3gsn0w_i5_c00000001}

**Approach:**

A text file was given .Then in the description a clue was given .So i went to biOs wiki page and came to know about stegsnow. Installed it and the password was provided in the text file as &quot;thisiseasy&quot;

and i used the following command:

stegsnow -C -p &quot;thisiseasy&quot; flag.txt ; this returned a base64 encoded text and i used the command :

echo&quot; &quot;|base64-d

this decoded the text and i got the flag.

**Challenge8: Con-The-Cat**
----------------------------------

**Flag** :inctfj{y0u_c4nt_s33_m3!!}

**Approach:**

A png file was provided . Used Ghex to look into the data . We can see multiple file signatures after the PNG which is of jpg.

Edited the data and saved the file to get an image which had the correct flag.
