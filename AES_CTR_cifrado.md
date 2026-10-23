# Cifrado de texto con AES en modo CTR

```python
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes


def cifrar(texto):
    # Creamos una clave AES de 16 bytes
    clave = get_random_bytes(16)

    # Creamos el cifrador AES en modo CTR
    cipher = AES.new(clave, AES.MODE_CTR)

    # Convertimos el texto a bytes
    texto_bytes = texto.encode("utf-8")

    # Ciframos el texto
    texto_cifrado = cipher.encrypt(texto_bytes)

    return texto_cifrado


texto = input("Introduce el texto que quieres cifrar: ")

resultado = cifrar(texto)

print("Texto original:", texto)
print("Texto cifrado:", resultado)
print("Tamaño del texto original:", len(texto.encode("utf-8")), "bytes")
print("Tamaño del texto cifrado:", len(resultado), "bytes")
```
