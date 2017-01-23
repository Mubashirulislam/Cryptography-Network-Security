# Caesar Cipher

The following program illustrates basic Caesar Cipher technique in C++.

### Program:

```c++
#include <iostream>
using namespace std;
void caesar_cipher(string text, int s, char c)
{
    //The following two lines changes the mode.
    if(c=='d')
        s=-s;
    string result = "";
    for (int i=0;i<text.length();i++)
    {
        if (isupper(text[i]))
            result += char(int(text[i]+s-65)%26 +65);
    else
        result += char(int(text[i]+s-97)%26 +97);
    }
    cout<<"Encryption: "<<result;
}
int main () {
   char mode;
   string msg,c;
   int key;
    cout<<"\nDo you wish to encrypt or decrypt the message";
    cout<<endl;
    cout<<"Press e for encryption and d for decryption: ";
    cin>>mode;
    cout<<"Please enter your message: ";
    cin>>msg;
    cout<<"Choose your key from 1-26: ";
    cin>>key;
    caesar_cipher(msg,key,mode);
   return 0;
}

```

### Output:

#### Encryption:

   ![Display an Image](https://github.com/Mubashirulislam/Cryptography-Network-Security/blob/master/Programs/Caesar%20Cipher/encryption.png)


#### Decryption:

 ![Display an Image](https://github.com/Mubashirulislam/Cryptography-Network-Security/blob/master/Programs/Caesar%20Cipher/decryption.png)
