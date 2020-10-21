#This encryptor is for encrypting sentences/paragraphs with the key idea
#that each letter will be assigned a new letter. Symbols or capital letters will
#be retained.

import random

def generator():
    enckey="abcdefghijklmnopqrstuvwxyz"
    a=list(enckey)
    random.shuffle(a)
    c=''
    for i in a:
        c+=i
    c=c+a[0]
    return c


def senc(a,enckey=generator()):
    b=list(a)
    for i in range(0,len(a)):
        for j in range(0,27):
            if b[i]==enckey[j]:
                b[i]=enckey[j+1]
                break
    c=''
    for i in b:
        c+=i
    print("Encrypted text:",c,"\nEncryption Key:",enckey)

def sdec(a,enckey=0):
    if enckey==0:
        return "please enter encryption key"
    else:
        b=list(a)
        enckey=enckey+enckey[0]
        for i in range(0,len(a)):
            for j in range(1,27):
                if b[i]==enckey[j]:
                    b[i]=enckey[j-1]
                    break
        c=''
        for i in b:
            c+=i
        print(c)
    
def encrypt():
    a=str(input("Enter text to be encrypted: "))
    b=str(input("Enter encryption key (optional, press enter to skip): "))
    if b=='' or None:
        senc(a)
    else:
        senc(a,b)

def decrypt():
    a=str(input("Enter text to be decrypted: "))
    b=str(input("Enter encryption key (Required): "))
    sdec(a,b)

while True:
    a=str(input(("Write encrypt or decrypt to proceed: ")))
    if a=="encrypt":
        encrypt()
    elif a=="decrypt":
        decrypt()
