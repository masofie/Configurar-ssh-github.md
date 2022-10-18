# Configuración SSH para Git/GitHub desde una Máquina Virtual

## ¿ Qué es SSH ?

El SSH , es un protocolo de acceso remoto que es utilizado mediante un canal seguro y que toda información esta cifrada .

El puerto estándar que utiliza es el 22 , para comunicarse remotamente desde una màquina .

Si quieres buscar mas información sobre SSH puedes buscar en el siguiente enlace .

**Enalce:** (**https://es.wikipedia.org/wiki/Secure_Shell**)


## Generar Clave SSH 

### Paso 1 

Abrir terminal y ejecutamos el siguiente comando para crear las claves . Y ejecutamos el siguiente comando :

Primero nos colocamos en nuestro home y hacemos un 

**`pwd** 

Y después ejecutamos el siguiente comando para crear las claves 

**`ssh-keygen -t ed25519 -C "tu correo electrónico"`**

![1.png](./img/1.png)

### Paso 2 

Para ejecutar el siguiente comando , si estamos en fish . Tenemos que volver a bash y ejecutar el siguiente comando para inicial el agente ssh .

![2.png](./img/2.png)

### Paso 3 

Agregamos clave privada , para eso utilizamos este comando 

**`ssh-add ~/.ssh/id_ed25519`**

![3.png](./img/3.png)

## Añadiendo clave SSH en Git 

Para añadir la clave que acabas que crear en GitHUb, primero hay que copiar la clave para después pegrala y para eso utilizamos este comando .

Siempre vamos a subir la clave pública 

**`cat ~/.ssh/id_ed25519.pub`**