# Introducción

Antes de andentrarnos en el código, es menester el entender cómo crear un mod que el juego pueda cargar. Este capítulo te guiará sobre cómo crear un mod básico de reemplazo de recursos, como un reemplazo de sprite.

# Creando un mod

El proceso para crear un mod es bastante sencillo. 

1. **Navega hacia la carpeta de mods.** Para los usuarios de Steam, suele estar ubicada en `C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\mods`.
2. **Crea una nueva carpeta.** Dale un nombre claro y descriptivo para encontrarlo más fácil.
3. **Reinicia el juego si está activo.** El juego sólo cargará nuevos mods al iniciar.
4. **Abre el menu de mods.** Deberías ver tu mod recien creado en la lista.
5. **¡Felicidades!** ¡Creaste tu primer mod! Por el momento, no hace nada. Esto cambiará pronto.

# Activar la Consola de Desarrollo

La consola de desarrollo es una herramienta invaluable para los modders, permitiendo, entre otras cosas, recargar mods, spawnear objetos, etc. Para checar si está habilitada, empieza una partida y presiona la tecla `~` (Si se usa la distribución en españo, presiona la tecla `Ñ`). Si la consola aparece, puedes seguir, de otro modo, haz los siguientes pasos:

1. **Cierra el juego.** Esto es importante para evitar que los cambios se sobreescriban.
2. **Abre el archivo `options.ini`**. Por lo general se encuentra en `C:\Users\%username%\Documents\My Games\Binding of Isaac Repentance`.
3. **Busca la línea `EnableDebugConsole=0` y cámbialo a `EnableDebugConsole=1`.**
4. **Guarda el archivo e inicia el juego.** Ahora deberías poder acceder a la consola.

# Crear un mod de reemplazo de recursos 
Reemplazar recursos del juego con los tuyos es muy sencillo. Vamos a reemplazar el sprite del objeto The Sad Onion con como ejemplo:

1. **Crea tu sprite.** Puedes crear tu propio sprite o [usar este existente por Bajongo.](https://i.imgur.com/S3jHjdt.png)

>⚠️ **Advertencia**
> Guarda tu sprite como un **archivo .png con una profundidad de bit de 32.** De otra forma no se mostrará correctamente.

2. **Busca el sprite original.** Los recursos del juego están ubicados en las carpetas "resources" y "resources-dlc3" en el directorio del juego (`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\` para usuarios de Steam). "resources-dlc3" contiene recursos específicos de Repentance, mientras que "resources" contiene todo lo demás. Como The Sad Onion existe desde antes de Repentance, su sprite se encuentra en "resources". 
  * Navega hasta "resources" > "gfx" > "items" > "collectibles". Encontrarás el sprite de The Sad Onion llamado "collectibles_001_thesadonion.png". Recuerda su nombre y ubicación.

3. **Mirror the folder structure in your mod.**
 * Create a "resources" folder within your mod folder.
 * Inside "resources", create a "gfx" folder.
 * Inside "gfx", create an "items" folder.
 * Inside "items", create a "collectibles" folder.
 * Place your new Sad Onion sprite inside the "collectibles" folder and name it "collectibles_001_thesadonion.png".

3. **Imita la estructura de carpetas en tu mod.**
 * Crea una carpeta "resources" en la de tu mod.
 * Dentro de "resources", crea una carpeta "gfx".
 * Debtro de "gfx", crea una carpeta "items".
 * Dentro "items", crea una carpeta "collectibles".
 * COloca tu nuevo sprite de The Sad Onion dentro de la carpeta "collectibles" y renómbralo a "collectibles_001_thesadonion.png".

4. **Reinicia el juego si está corriendo.**

5. **Spawnea The Sad Onion usando el siguiente comando: `spawn 5.100.1`**
   
¡Voila! Acabas de crear tu primer mod de reemplazo de recursos

> ℹ️ **Solución de problemas**
> Si tu mod no aparece, reevisa la estructura de carpetas y los nombres de archivos por su precisón (¡Recuerda, distinguen entre mayúsculas y minúsculas). Otro mod podría estar anulando tu sprite, así que desactiva los mods que conflictúen.

# Reemplazando otros recursos 

Este proceso se aplica igualmente para otros sprites, música, efectos de sonido y animaciones. La única diferencia radida en el tipo de archivo de tu nuevo recurso y la estructura de carpetas que estás imitando

> **⚠️ Advertencia**
> Si estás tratando de añadir un sonido, estos requieren un encoding de 32-bit. Si no lo haces, estos sonarán como estática extremadamente ruidosa en el juego y lastimará tus oídos. ¡Ouch!

# Más usos de la consola de desarrollo

Si deseas aprender más sobre la Consola de Desarrollo y los comandos que esta posee, la Wiki de Isaac tiene [una página al respecto.](https://bindingofisaacrebirth.fandom.com/wiki/Debug_Console). Algunos comandos serán cubiertos a profundidad en secciones posteriores.
