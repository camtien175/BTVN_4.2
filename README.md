# BTVN_4.2
def btvn4_2(plaintext, k):
    ciphertext = ""
    k = k % 26 
    for ch in plaintext:
        if ch.isalpha(): 
            base = ord('A') if ch.isupper() else ord('a')
            enc = chr((ord(ch) - base + k) % 26 + base)
            ciphertext += enc
        else:
            ciphertext += ch  
    return ciphertext
if __name__ == "__main__":
    P = "TranThiCamTien"  
    k = 48  
    C = btvn4_2(P, k)
    print("Plaintext :", P)
    print("Key       :", k % 26)
    print("Ciphertext:", C)
