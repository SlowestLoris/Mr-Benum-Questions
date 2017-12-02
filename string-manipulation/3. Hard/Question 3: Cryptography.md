# Cryptography
Research a simple `encryption or decryption` algorithm (For example, a Base64 Java encoder/decoder) , or make one up your own. Create a program that will prompt the user for a **string** and then **ask** the user if they want to encrypt or decrypt. Output the resulting string.

## Sample (DO NOT USE THIS)
The below example is an implemenation in java of a Base 64 Encoder. Note that the program does not meet all of the above expectations and is merely a sample.

### Base 64 Encoder
```java
import java.io.UnsupportedEncodingException;    
import javax.xml.bind.DatatypeConverter;
import java.util.Scanner;

public class test {

    public static void main(String[] args) throws UnsupportedEncodingException {
    	
    	Scanner sc = new Scanner(System.in);
    		
    	//Read a word from the user
    	System.out.println("Enter a word:");
        String str = sc.next();
        
        // encode data using BASE64
        String encoded = DatatypeConverter.printBase64Binary(str.getBytes());
        System.out.println("encoded value is \t" + encoded);

        // Decode data 
        String decoded = new String(DatatypeConverter.parseBase64Binary(encoded));
        System.out.println("decoded value is \t" + decoded);

    }

}
```
### Console
```
(comp) Enter a word:
(user) java
(comp) encoded value is 	amF2YQ==
(comp) decoded value is 	java
```