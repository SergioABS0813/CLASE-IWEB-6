# CLASE-IWEB-6
Modelado de Base de Datos

## Toda Tabla debe tener un id
<img width="260" alt="Captura de pantalla 2023-03-06 210203" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/a094ce9d-f6b8-4a68-8635-34136ed38175">

## Foreign Key (FK)
Cuando una columna de PK pasa a otra tabla se llama Foreign Key (FK).

<img width="801" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/0acbac81-c5de-4ca0-88f2-8817f5f33d39">

## Creación de una tabla en MySQL
Los datos que sean CAMPOS OBLIGATORIOS siempre tendrán la característica de ser NN (Not Null).

En el id de cada tabla es recomendable colocar NN y AI (Auto Incremental).
<img width="960" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/4f8a7856-8b5b-4099-af45-958e6de5dae8">

## Relación entre tablas
<img width="30" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/7c78b291-a5d0-473e-a99a-5c833884727c">

![image](https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/fb937db5-5661-4765-b522-7e4cbd9c401f)



## Relación Fuerte/Débil entre tablas
Se define relación Fuerte cuando la otra tabla es dependiente de la primera tabla (no tiene valor sin ella):

Fuerte: PK ------> PK (Línea Continua)

Se define Débil cuando la otra tabla es independiente de la primera tabla (tiene valor por sí sola y PK):

Débil:  PK ------> FK (Línea Discontinua)

## Relación 1:N (1 a muchos)
Por ejemplo 1 persona puede tener muchos celulares (1:N).

<img width="341" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/bcbec31b-dd35-4821-a862-82cfff7e1b3c">

Relación de 1:N (FUERTE)

<img width="339" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/b1550602-e3d1-4f4e-a459-411d2a28aa53">

Relación de 1:N (DÉBIL)

<img width="344" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/3f6801da-4ab9-49fa-b580-bec1db8f7da5">

## Colocación de la relación 1:N
Por ejemplo si queremos colocar que el idPersona vaya al Celular entonces la pata de gallo debe estar en el Celular

INCORRECTA COLOCACIÓN:

<img width="444" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/89cfb743-1145-46f5-afd5-076760508809">

CORRECTA COLOCACIÓN:

<img width="415" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/a2f8c9ae-63f3-419e-9c14-253e64308909">

## Distinción en Relaciones 1:N (si pueden o no ser null)

![image](https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/6dc4155f-c51f-4d7a-8339-f2ea943941f0)

## Relación 1:N (con un NULL posiblemente)
Clic en la propia tabla donde quieres hacer la modificación
en la columna desasignarle NN

![image](https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/f05dff41-c803-4385-b8d7-a97687ae2e97)

## Relacion N:M (muchos a muchos)
Crea una tabla nueva con 2 PK (de las 2 tablas relacionadas) de relación FUERTE, pero si queremos modificarlo solo damos clic en la línea de relación y modificamos Identifying Relationship


![image](https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/b7f5a7dd-6930-4020-bda0-f95978f86265)

Para este ejemplo pensamos en que un celular podría tener muchas fundas. Entonces el id de CelularPorPersona tiene que ir hacia la tabla fundas (Este id fue creado porque los pusimos a todos como FK ya que al hacer relación de 1:n entonces también la otra tabla tenia 3 campos FK)

Con estas modificaciones entonces nos queda así:


![image](https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/87e707c1-ffe6-4230-a2d2-c5b108cc9c69)

