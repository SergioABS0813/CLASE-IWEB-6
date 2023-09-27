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

## Forward Engineer
Sirve para guardar el código SQL y transportarlo "guardarlo" en la base de datos

<img width="568" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/9910f335-0637-4398-8ae1-8f6bea84f88c">

<img width="660" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/cb986494-f437-4632-a1bc-8b03d05ade12">

<img width="663" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/e3bb5dbc-9c3f-41d1-9949-e31084773948">

<img width="506" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/ccc6b22a-67fd-4ae0-9dcb-8766e88bff7a">

Verificamos las tablas que se están exportando:

<img width="659" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/5ea9c1f2-6d6f-49c8-8722-a4b6798e5f85">

Siempre guardamos el código en SQL:

<img width="663" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/742a4a63-2e6d-4450-868c-9993672203ca">

<img width="310" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/062c45b7-ef93-48d1-a933-e9c860fa98e1">

Al final debe aparecer esta ventana:

<img width="664" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/a49cb759-126d-4239-8dee-a8e829a9a1d5">

## Reverse Engineer
Ir a Administration, luego clic en Data Import/Restore

<img width="695" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/42e2f0af-58b1-476a-ba64-4bcf739b22a4">

Darle a Import from Self y luego escoger el archivo .sql guardado:

<img width="742" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/ee3c1a4f-9c37-46ba-acab-49485f6d9f51">

Luego vamos a Import Progress, luego le damos a Start Import. Luego aparecerá así:

<img width="574" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/6165817d-dd61-4788-964a-ef6251cef5bc">

Ahora ya tenemos las tablas en código SQL, pero para verlo en mwb entonces realizamos reverse:

<img width="233" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/f329cfcd-f5af-4d99-ac69-3745aeed6407">

<img width="657" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/9376833e-f70d-4fa4-8f6f-16f276b3c9b0">

Luego le damos a todo next y finish

<img width="960" alt="image" src="https://github.com/SergioABS0813/CLASE-IWEB-6/assets/134556600/84487d24-bb20-4698-9df5-826f58139ea6">


