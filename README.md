# Proyecto Interciclo Base De Datos

## Integrantes
1.  Adrian Lazo
2.  Rafael Prieto
3. John Serrano
4. Matias Sinchi

### Creación de nuevo usuario

- Debemos entrar a la terminal de ==SQL Plus==

![aplicacion a entrar](capturas/SQLPlus.png)

```bash
/as sysdba
```
```bash
ALTER SESSION SET "_ORACLE_SCRIPT"= TRUE;
```
- Ingresamos el comando para poder crear el usuario
```bash
CREATE USER proyecto1 IDENTIFIED BY "123"
```
- El siguente comando son los valores que le daremos al usuario
```bash
DEFAULT TABLESPACE "USERS"
TEMPORARY TABLESPACE "TEMP";
```
- le damos un espacio ilimitado por si las dudas
```bash
ALTER USER proyecto1 QUOTA UNLIMITED ON USERS;
```
- creamos una session para el usuario
```bash
GRANT CREATE SESSION TO proyecto1;
```
- y le damos los ultimos atributos al proyecto
```bash
GRANT "RESOURCE" TO proyecto1; 
ALTER USER proyecto1 DEFAULT ROLE "RESOURCE";
```