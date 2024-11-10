# overthewire
Write up for wargame Bandit
https://overthewire.org/wargames/bandit/

## Level 0 
ssh bandit0@bandit.labs.overthewire.org -p 2220 password:bandit0

## Level 0 -> 1
ssh bandit0@bandit.labs.overthewire.org -p 2220

ls -l
cat readme

Password=ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

## Level 1 -> 2
ssh bandit1@bandit.labs.overthewire.org -p 2220

ls -l

cat ./-

Password=263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## Level 2 -> 3
ssh bandit2@bandit.labs.overthewire.org -p 2220

ls -l

cat "spaces in this filename"

Password=MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## Level 3 -> 4
ssh bandit3@bandit.labs.overthewire.org -p 2220

ls- l

cd inhere

ls -a

cat "...Hiding-From-You"

Password=2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## Level 4 -> 5
ssh bandit4@bandit.labs.overthewire.org -p 2220

ls -l

cd inhere

ls -la

cat "./-file07"

Password=4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Level 5 -> 6
ssh bandit5@bandit.labs.overthewire.org -p 2220

ls -l

cd inhere

find . -type f -size 1033c

cat ./maybehere07/.file2

Password=HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## Level 6 -> 7
ssh bandit6@bandit.labs.overthewire.org -p 2220

cd ../..

find . -type f -size 33c -user bandit7 -group bandit6 2> /dev/null

cat ./var/lib/dpkg/info/bandit7.password

Password=morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## Level 7 -> 8
ssh bandit7@bandit.labs.overthewire.org -p 2220

grep 'millionth' data.txt 

Password=dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
