# Introducción

The Binding of Isaac utiliza Lua como su lenguaje de scripting para el modding del juego. Lua es un lenguaje ligero, de alto nivel e integrado conocido por su facilidad de aprendizaje comparado con otros lenguajes.

Antes de lanzarse a la creación de nuevo contenido, es importante aprender los fundamentos de Lua y de la programación en general. Lanzarse hacia el modding sin conocimiento previo de Lua será extremadamente desafiante. Si ya estás familiarizado con otros lenguajes, aprender Lua será mucho más sencillo.

# Creando el archivo Lua principal

Para que el código de tu mod se ejecute, necesitas un archivo Lua principal:
1. En tu carpeta del mod, crea un archivo llamado `main.lua` (¡Distingue entre mayúsculas y minúsculas!). Este archivo será ejecutado cuando el juego cargue tu mod
2. Abre la carpeta de tu mod en tu IDE

# Hola Mundo

>ℹ️ **Escribe el mod por tu cuenta!**
>Para un mejor entendimiento, recomendamos que escribas manualmente los fragmentos de código en tu IDE en vez de copiar y pegar.

En tu `main.lua`, escribe lo siguiente:.

```lua
print("¡Hola Mundo!")
```

No te preocupes por el significado de esto. Por el momento, guarda el archivo. ¡El siguiente paso es correrlo!

A difrerencia de los recursos como sprites y animaciones, recargar archivos de Lua no necesita reiniciar el juego, la consola de desarrollo te da un comando para recargar los archivos Lua de tu mod:

1. Abre la consola de desarrollo.
2. Escribe `luamod MOD_FOLDER_NAME`, reemplaza "MOD_FOLDER_NAME" con el nombre de la carpeta de tu mod (distingue entre mayúsculas y minúsculas). Por ejemplo, si el nombre de la carpeta de tu mod es "tutorial-mod", deberás ejecutar `luamod tutorial-mod`.

Al ejecutar el comando, deberás ver "¡Hola Mundo!" impreso en la consola. ¡Felicidades por ejecutar tu primer script de Lua!

# Un vistazo a las impresiones

La función `print` es usada para plasmar texto en la consola de desarrollo, puedes plasmar cualquier mensaje que quieras

```lua
print("¡Adiós!")
```

Es muy importante encerrar el texto usando comillas. No ahcerlo puede provocar errores de sintaxis o comportamiento inesperado

# Como son ejecutados los archivos Lua

Cuando un archivo lua es ejecutado, cada línea de código es ejecutado secuencialmente desde arriba hasta abajo. Por ejemplo, en el siguiente script de Lua:

```lua
print("¡Hola Mundo!")
print("¡Adiós!")
```

"¡Hola Mundo!" se plasmará primero, seguido de "¡Adiós!"

# Casos de uso de Print

Aunque se presente como algo simple, `print` es una herramienta de depuración poderosa. Se puede usar para:
  - Revisar si una porción de tu código está siendo ejecutada.
  - Plasmar ciertos valores o variables (serán revisadas en un capítulo posterior) para tener mayor entendimiento sobre tu código.

> ℹ️ **¿Qué hay de los otros métodos de depuración?**
> Aunque otros métodos de depuración como los breakpoints existen, no están disponibles en el modding de Isaac. De esta forma, `print` y la consola de desarrollo serán tus mejores amigos

# Cuestioonario

¡Es hora de un cuestionario rápido! Este será algo pequeño debido a que no se cubrió mucho en esta sección.

1.) ¿Qué es Lua?

<details>
  <summary>Solución</summary>
  Lua es un lenguaje de scripting ligero, de alto nivel e incrustado.
</details>
<br>

2.) ¿Qué función es utilizada para plasmar texto en la consola?

<details>
  <summary>Solución</summary>
  `print`
</details>
<br>

3.) Escribe un script que plasme las siguientes líneas en orden:
 - ¡Hola!
 - ¿Cómo estás?
 - Estoy bien, gracias.

  <details>
  <summary>Solución</summary>

  ```lua
  print("¡Hola!")
  print("¿Cómo estás?")
  print("Estoy bien, gracias.")
  ```
</details>
<br>
