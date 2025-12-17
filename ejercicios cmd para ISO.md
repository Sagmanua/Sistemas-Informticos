SCRIPTS CMD PARA ISO
1. Crea una carpeta llamada "Proyectos" en el escritorio.
C:\Users\BohdanSydorenko>mkdir Proyectos


2. Mueve la carpeta "Proyectos" al directorio raíz de C:.
C:\Users\BohdanSydorenko\Documents>move "C:\Users\BohdanSydorenko\Documents\Proyectos" "C:\"
Se ha(n) movido         1 directorio(s).

3. Dentro de "Proyectos", crea tres carpetas: "DAW1", "DAW2" y "DAW3".

>mkdir C:\Proyectos\DAW1 C:\Proyectos\DAW2 C:\Proyectos\DAW3

4. Renombra la carpeta "DAW1" a "DAM1".

ren C:\Proyectos\DAW1 DAM1


5. Mueve "DAM1" a una nueva carpeta llamada "Backup" en C:.

C:\Proyectos>cd DAM1

C:\Proyectos\DAM1>mkdir Backup

6. Copia "DAW2" a "Backup".
C:\Proyectos\DAW2 C:\Backup\DAW2 /E /I

7. Elimina la carpeta original "DAW3".
rmdir /S /Q C:\Proyectos/DAW3
8. Crea un archivo vacío llamado "lista.txt" dentro de "Proyectos".


9. Renombra el archivo "lista.txt" a "alumnos.txt".
10.Mueve "alumnos.txt" a "C:\Backup".
11.Crea un usuario llamado "alumno1" con contraseña "1234".
12.Crea un grupo local llamado "estudiantes".
13.Añade el usuario "alumno1" al grupo "estudiantes".
14.Crea un usuario "adminclase" con contraseña "abcd1234".
15.Haz que "adminclase" sea administrador del sistema.
16.Cambia la contraseña de "alumno1" a "5678".
17.Lista todos los usuarios existentes en el sistema.
18.Lista todos los grupos locales existentes en el equipo.
19.Elimina el usuario "alumno1" del sistema.
20.Elimina completamente la carpeta "Backup".