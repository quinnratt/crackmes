# Reverse Engineering: "thefirsttest" 
*By JoeJoeJoe's*

[🔗 View Challenge on Crackmes.one](https://crackmes.one/crackme/6abc48c1ace07d1c3fbc4816)

---

## 🔍 Overview
This was my first crackme challenge, and I was initially confused staring at it for a while.

> [!NOTE]
> The target hexadecimal value `0x72abb3c9` was the core piece of logic needed to bypass the check. The variable `&DAT_0040123` didn't end up mattering.

---

## 🛠️ Ghidra Analysis
Opening the binary in Ghidra revealed a straightforward integer comparison:

```c
undefined8 main(void)
{
    int local_c;
    puts("Welcome to your first test!");
    puts("Please input the password:");
    puts("WARNING: Please input password twice");
    __isoc23_scanf(&DAT_00401235,&local_c);
    
    if (local_c == 0x72abb3c9) {
        puts("Well done, you are a master hacker!");
    } else {
        puts("Wrong password, try agian!");
    }
    
    return 0;
}
