# Caesar_cipher_encryption
package Caesar_Cipher;

import java.util.*;
public class Caesarcipher_encryption{
    public static void main(String args[]) {
        Scanner Sc = new Scanner(System.in);
        System.out.println(" Enter the plaintext message : ");
        String plaintext = Sc.nextLine();
        System.out.println(" Enter the value by which each character in the plaintext message gets shifted:");
        int shift = Sc.nextInt();
        String ciphertext = "";
        char alphabet;
        for(int i=0; i < plaintext.length();i++) 
        {
         alphabet = plaintext.charAt(i);
         if(alphabet >= 'a' && alphabet <= 'z') 
            {             
             alphabet = (char) (alphabet + shift);		             
             if(alphabet > 'z') {		               
                alphabet = (char) (alphabet+'a'-'z'-1);
             }
             ciphertext = ciphertext + alphabet;
            }
            		           
            else if(alphabet >= 'A' && alphabet <= 'Z') {		            
             alphabet = (char) (alphabet + shift);    		                		            
             if(alphabet > 'Z') {		                
                 alphabet = (char) (alphabet+'A'-'Z'-1);
             }
             ciphertext = ciphertext + alphabet;
            }
            else {
             ciphertext = ciphertext + alphabet;   
            }
        
    }
    System.out.println(" ciphertext : " + ciphertext);
  }
}
