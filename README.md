
# Reverse Engineering thefirsttest by JoeJoeJoe's

[view joejoejoe's crackme](https://crackmes.one/crackme/6abc48c1ace07d1c3fbc4816)


## Writeup
opening ghidra i was met with

> the goal of the crackme is to turn the hexadecimal '0x72abb3c9`

```c
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


# [ghidra analysis]
<p align="center">
  <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/2a20bdb5-4c9b-411b-96ce-b7fd842c0a32" />
</p>

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

# [terminal review]
<img width="1366" height="768" alt="Untitled" src="https://github.com/user-attachments/assets/2852743c-e257-411a-aa6e-ca80aa8c3f63" />

