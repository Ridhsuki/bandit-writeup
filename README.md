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
   
2. Masukan password `bandit0`.
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

   Password untuk level 1 `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`.
___
## Level 1 → Level 2

original link: [level1](https://overthewire.org/wargames/bandit/bandit1.html)

1. Login ke ssh dengan command berikut.

   ```
   ssh bandit1@bandit.labs.overthewire.org -p 2220
   ```
   
2. Masukan password `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
3. Temukan password. Clue: The password for the next level is stored in a file called `-` located in the home directory.

   - `cat ./-` untuk melihat isi dari file `-` yang merupakan password untuk next level.
  
   **Preview**
      ```bash
      bandit1@bandit:~$ ls -a
      -  .  ..  .bash_logout  .bashrc  .profile
      
      bandit1@bandit:~$ cat ./-
      263JGJPfgU6LtdEvgfWU1XP5yac29mFx

      bandit1@bandit:~$ 
      ```

   Password untuk level berikutnya `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`.
___

## Level 2 → Level 3

original link: [level2](https://overthewire.org/wargames/bandit/bandit3.html)

1. Login ke ssh dengan command berikut.

   ```
   ssh bandit2@bandit.labs.overthewire.org -p 2220
   ```

2. Masukan password `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`
3. Temukan password. Clue: The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

   - `cat ./--spaces\ in\ this\ filename-- ` untuk melihat isi dari file `--spaces in this filename--` yang merupakan password untuk level berikutnya.
  
   **Preview**
      ```bash
      bandit2@bandit:~$ ls -a
      .  ..  .bash_logout  .bashrc  .profile  --spaces in this filename--
      
      bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename-- 
      MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
      
      bandit2@bandit:~$ 
      ```

   Password untuk level berikutnya `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`
___

## Level 3 → Level 4

original link: [level3](https://overthewire.org/wargames/bandit/bandit4.html)

1. Login ke ssh dengan command berikut.

   ```
   ssh bandit3@bandit.labs.overthewire.org -p 2220
   ```
2. Masukan password `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`.
3. Temukan password. Clue: The password for the next level is stored in a hidden file in the **inhere** directory.

   - `cd inhere/` untuk masuk ke directory `inhere`.
   - `cat ./...Hiding-From-You` untuk melihat isi dari file `./...Hiding-From-You` yang merupakan password untuk level berikutnya.

   **Preview**
      ```bash
      bandit3@bandit:~$ ls -a
      .  ..  .bash_logout  .bashrc  inhere  .profile
      
      bandit3@bandit:~$ cd inhere/
      
      bandit3@bandit:~/inhere$ ls -a
      .  ..  ...Hiding-From-You
      
      bandit3@bandit:~/inhere$ cat ./...Hiding-From-You 
      2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
      
      bandit3@bandit:~/inhere$ 
      ```

   Password untuk level berikutnya `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`.
___

## Level 4 → Level 5

original link: [level4](https://overthewire.org/wargames/bandit/bandit5.html)
___
## Password untuk login
| Level | Password |
|-----|-----|
| bandit0 | `bandit0` |
| bandit1 | `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If` |
| bandit2 | `263JGJPfgU6LtdEvgfWU1XP5yac29mFx` |
| bandit3 | `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx` |
| bandit4 | `` |
|  |  |


___
Other Resources:
- https://axcheron.github.io/writeups/otw/bandit/
