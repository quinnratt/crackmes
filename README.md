
# Reverse Engineering thefirsttest by JoeJoeJoe's

opening ghidra i was met with

```
undefined8 main(void)
{
int local_c;
puts("Welcome to your first test!");
puts("Please input the password:");
puts("WARNING: Please input password twice");
__isoc23_scanf(&DAT_00401235,&local_c);
if (local_c == 0x72abb3c9) {
}
puts("Well done, you are a master hacker!");
else {
}
}
puts("Wrong password, try agian!");
return 0;
```

this was my first crackme challenge i took
i was confused staring at it for a while


&DAT_0040123 didnt really matter
* 0x72abb3c9 did

i attempted entering it constantly in my terminal twice with no avail

```bash
~/crackmes,
λ  ./thefirsttest
Welcome to your first test!
Please input the password:
WARNING: Please input password twice
0x72abb3c9 0x72abb3c9               
Wrong password, try agian!
```

it was very easy as all i had to do was 
change the hexadecimal into decimal

```bash
~/crackmes,
λ  ./thefirsttest
Welcome to your first test!
Please input the password:
WARNING: Please input password twice
 1923855305
 1923855305
Well done, you are a master hacker!
```
<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/2a20bdb5-4c9b-411b-96ce-b7fd842c0a32" />
