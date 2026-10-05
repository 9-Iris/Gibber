# Gibber 1.0

Gibber is an easy to use encryption wrapper utilizing the AES-256 encryption.

## Highlights

* **AES-GCM** to prevent tampering of encrypted text.
* **256 Bits of entropy** preventing all brute force attacks.
* **Easy to learn** API with minimal boilerplate

## Quick start guide

```java

// Main.java

public class Main {

   public static void main(String[] args) throws Exception {
   
      // 1. Initialize a new 32 byte key using Gibber.key
      Gibber.Key secureKey = new Gibber.Key();
      System.out. println("Generated key: " + secureKey.toString());
      
      // 2. Initialize a Gibber using the new key
      Gibber cipher = new Gibber(secureKey);
      
      String plainText = "The quick brown fox jumps over the lazy dog.";
      String encrypted = cipher.encrypt(plainText);
      String decrypted = cipher.decrypt(encrypted);

   }

}
```






