# bandit-writeup
Welcome to my bandit overthewire writeup as archive 

___
## Level 0 → Level 1

original link: [level0](https://overthewire.org/wargames/bandit/bandit0.html).

pada bandit level 0 sudah diberikan instruksi untuk login melalui ssh pada host dan port yang sudah disediakan, yaitu dengan ketentuan sebagai berikut.
- **username** = `bandit0`
- **password** = `bandit0`

maka yang perlu kita lakukan adalah sebagai berikut.
1. Login ke ssh dengan command berikut.

   ```
   ssh bandit0@bandit.labs.overthewire.org -p 2220
   ```
   
2. Masukan password `bandit0`
    <br>
    <div style="display: flex; flex-wrap: wrap; gap: 11px; justify-content: center; align-items: center;" align="center">
      <img alt="image" src="https://github.com/user-attachments/assets/67b0a847-2154-4ca3-9552-e37c5e3d130b" />
    </div>
    <br>
    
3. Temukan password untuk masuk ke level berikut nya.

   - `ls` untuk melihat isi dari directory saat ini.
   - `cat readme` untuk membaca isi dari file readme.

   **Preview**
      ```bash
      bandit0@bandit:~$ ls -a
      .  ..  .bash_logout  .bashrc  .profile  readme
      
      bandit0@bandit:~$ cat readme 
      Congratulations on your first steps into the bandit game!!
      Please make sure you have read the rules at https://overthewire.org/rules/
      If you are following a course, workshop, walkthrough or other educational activity,
      please inform the instructor about the rules as well and encourage them to
      contribute to the OverTheWire community so we can keep these games free!
      
      The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
      
      bandit0@bandit:~$ 
      ```

   Password `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
___
## Level 1 → Level 2

original link: level1
___
## Password
| Level | Password |
|-----|-----|
| bandit0 | `bandit0` |
| bandit1 | `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If` |

___
Other Resources:
- https://axcheron.github.io/writeups/otw/bandit/
