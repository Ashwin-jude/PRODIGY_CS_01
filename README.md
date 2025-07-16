a= input("enter the text")
b= int(input("enter the key"))
def encrypt(a,b):
    c=""
    for i in range (len (a)):
        if a[i].isalpha():
            if a[i].islower():
                c = c+ chr((ord(a[i])-ord("a")+b)%26+ord("a"))
            else :
                c = c+ chr((ord(a[i])-ord("A")+b)%26+ord("A"))   
    return c
def decrypt(a,b):
    return encrypt(a,-b)
d=encrypt(a,b)
print("encrypted text",d)
e=decrypt(a,b)
print("decrypted text",e)
