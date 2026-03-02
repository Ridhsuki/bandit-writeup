# bandit-writeup
Welcome to my bandit overthewire writeup as archive 

___
## Level 0 → Level 1

* original link 1: [level 0](https://overthewire.org/wargames/bandit/bandit0.html). (Getting Started).
* original link 2: [Level 0 → Level 1](https://overthewire.org/wargames/bandit/bandit1.html). (Find Password for next level).

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

original link: [Level 1 → Level 2](https://overthewire.org/wargames/bandit/bandit2.html).

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

original link: [Level 2 → Level 3](https://overthewire.org/wargames/bandit/bandit3.html).

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

original link: [Level 3 → Level 4](https://overthewire.org/wargames/bandit/bandit4.html).

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

original link: [Level 4 → Level 5](https://overthewire.org/wargames/bandit/bandit5.html).

1. Login ke ssh dengan command berikut.

   ```
   ssh bandit4@bandit.labs.overthewire.org -p 2220
   ```
   
2. Masukan password `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`.
3. Temukan password. Clue: The password for the next level is stored in the only human-readable file in the inhere directory.

   - `file ./-file*` untuk mengidentifikasi tipe atau format file.
  
   **Preview**
      ```bash
      bandit4@bandit:~$ ls -a
      .  ..  .bash_logout  .bashrc  inhere  .profile
      
      bandit4@bandit:~$ cd inhere/
      
      bandit4@bandit:~/inhere$ ls -a
      .  ..  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09

      bandit4@bandit:~/inhere$ file ./-file*
      ./-file00: data
      ./-file01: OpenPGP Public Key
      ./-file02: OpenPGP Public Key
      ./-file03: data
      ./-file04: data
      ./-file05: data
      ./-file06: data
      ./-file07: ASCII text
      ./-file08: data
      ./-file09: data
      
      bandit4@bandit:~/inhere$ cat ./-file07 
      4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
      
      bandit4@bandit:~/inhere$ 
      ```

   Password untuk level berikutnya `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`.
___

## Level 5 → Level 6

original link: [Level 5 → Level 6](https://overthewire.org/wargames/bandit/bandit6.html).

1. Login ke ssh dengan command berikut.

   ```
   ssh bandit5@bandit.labs.overthewire.org -p 2220
   ```

2. Masukan password `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`.
3. Temukan password.
    - Clue: The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
       - human-readable
       - 1033 bytes in size
       - not executable
     
    - `find . -type f -readable ! -executable -size 1033c` untuk mencari file berdasarkan kriteria tertentu.
      - `find` perintah utama untuk mencari file atau direktori.
      - `.` untuk menunjukan tempat direktori pencarian di mulai.
      -  `-type f` untuk mencari file bertipe biasa, bukan direktory.
      -  `-readable` untuk mencari file yang bisa di baca.
      -  `! -executable` untuk mencari file yang tidak bisa di eksekusi.
      -  `-sizw 1033c` untuk mencai dile yang ukuran nya 1033 bytes. `c` dibelakang angka berarti bytes (karakter).
  
    **Preview**
      ```bash
      bandit5@bandit:~$ ls -a
      .  ..  .bash_logout  .bashrc  inhere  .profile
      
      bandit5@bandit:~$ cd inhere/
      
      bandit5@bandit:~/inhere$ ls -a
      .            maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
      ..           maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
      maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
      
      bandit5@bandit:~/inhere$ find . -type f -readable ! -executable -size 1033c
      ./maybehere07/.file2
      
      bandit5@bandit:~/inhere$ cat ./maybehere07/.file2 
      HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

      bandit5@bandit:~/inhere$
      ```

   Password untuk level berikutnya `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`.

___
## Password untuk login
| Level | Password |
|-----|-----|
| bandit0 | `bandit0` |
| bandit1 | `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If` |
| bandit2 | `263JGJPfgU6LtdEvgfWU1XP5yac29mFx` |
| bandit3 | `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx` |
| bandit4 | `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw` |
| bandit5 | `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG` |
| bandit6 | `-` |
| bandit | `-` |
| bandit | `-` |
| bandit | `-` |
| bandit | `-` |
| bandit | `-` |



___
Other Resources:
- https://axcheron.github.io/writeups/otw/bandit/
- https://www.instagram.com/p/DVLGTlHjUsQ/?utm_source=ig_web_copy_link&igsh=NTc4MTIwNjQ2YQ==
