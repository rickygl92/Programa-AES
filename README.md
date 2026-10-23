# Programa-AES

1. ¿Qué ocurre si intentas cifrar el texto plano?
El programa convierte primero el texto plano a bytes mediante UTF-8 y después lo cifra utilizando AES en modo CTR. El resultado es un texto cifrado que no se puede leer directamente.

Si intentamos cifrar el texto sin convertirlo previamente a bytes, se produce un error.

2. ¿Cuál es el tamaño del texto cifrado resultante?
En el modo CTR, el texto cifrado tiene exactamente el mismo tamaño en bytes que el texto original codificado en UTF-8, ya que no necesita añadir relleno (padding).

Por ejemplo, si el texto original ocupa 20 bytes, el texto cifrado también ocupará 20 bytes.

3. ¿Qué diferencias hay en el tamaño del texto cifrado entre el modo de operación ECB y CTR?
La principal diferencia es que ECB trabaja con bloques completos de 16 bytes, mientras que CTR puede cifrar mensajes de cualquier longitud.

En ECB, si el mensaje no ocupa un múltiplo de 16 bytes, es necesario añadir relleno para poder cifrarlo. En cambio, CTR no necesita relleno y mantiene el mismo tamaño que el mensaje original en bytes.
