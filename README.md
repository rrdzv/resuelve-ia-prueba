# Prueba IA Resuelve

Nos da gusto que quieras ser parte de nuestro equipo, si quieres saber un poco más sobre Resuelve Ingeniería y el equipo puedes ver [aquí](https://github.com/resuelve/nuestro-equipo).

Este ejercicio es una oportunidad para que escribas un poco de tu código más limpio que nos muestre cómo solucionas un caso básico de negocio.

* Escribe el código como si fuera a producción
* Asume que tu código pasará por un extenso proceso de _code review_
* Puedes apoyarte en cualquier referencia que desees 
* Puedes usar Python o R para escribir tu código
* Recuerda documentar adecuadamente tu código
* Asegurate de dejar instrucciones claras de cómo ejecutar tu código como si fuera a desplegarse en producción

## Problema 1

Los DS que trabajan en Resuelve tienen entre sus varios objetivos la tarea de cuantificar la actividad de los usuarios. Y así llevar a los equipos al éxito. Una de las áreas más grandes que nos preocupa es el compromiso que tienen los usuarios con la marca. El conjunto de datos que te vamos a proporcionar contienen ejemplos de lo que solemos utilizar para resolver problemas reales.  Utilizando estos datos, tu conocimiento del negocio y potencialmente tus intereses, realiza lo siguiente

Para todos los usuarios que recibieron una notificación, ¿cuál es la diferencia en promedio en transacciones 7 días antes de que llegue la notificación vs. 7 días después de la notificación agrupado por país y grupo de edad.

Cómo ejecutar:
Ve a http://metabase.resuelve.io/ e inicie sesión con el
credenciales que te hemos enviado

1. Esto es Metabase, una herramienta de informes de código abierto. Es una alternativa gratuita a herramientas como Tableau, Looker, Microstrategy, PowerBI, etc.

2. Si te sientes confundido, puede leer su guía de inicio aquí:
https://metabase.com/docs/latest/getting-started.html.

ii. En la base de datos de `Data Warehouse`, tenemos tablas precargadas con datos inspirados en datos de la vida real que tomamos de nuestro día a día. Encontrarás el completo Descripción de los nombres y variables de la tabla al final del desafío.
También puede ver las tablas y el esquema de la base de datos en Metabase.

iii) Puedes usar la interfaz SQL de Metabase para probar SQL y generar diferentes
tipos de gráficos
iv. Crea una nueva "pregunta" y, una vez que estés satisfecho con tu consulta
y visualización, guarda tu pregunta como "ds_challenge-q1" en tu Colección personal

v. Siéntete libre de guardar más preguntas y jugar con Metabase si
deseas, pero solo se considerará lo que se incluyas en "ds_challenge-q1"
para evaluación

## Problema 2

Con el data set en el archivo "datos_prestamo.csv" tiene información de una empresa que otorga créditos. Hasta ahora, hay un grupo de personas (el equipo de crédito) que estudia registro a registro y decide si prestarle o no. Las variables que tenemos son:

* Fecha_registro: El día y hora que el usuario se registró en nuestro sitio web.
* Fecha_contacto: El día y hora que un asesor se comunicó con el cliente. Debe ser posterior a la Fecha de registro.
* Id: Identificador que se le asigna al cliente. Debe ser único.
* Genero: Hombre o mujer.
* Casado: Si está casado.
* Dependientes: Número de personas que dependen de su ingreso.
* Educacion: Graduado si tiene un título universitario o superior. No graduado en otro caso.
* Trabaja_para_el: Si es dueño del negocio o empresa en donde trabaja.
* Salario: Salario neto anual en pesos.
* Salario_pareja: Salario neto anual de la pareja en pesos.
* Credito_pedido: Crédito que solicito en miles de pesos.
* Plazo_prestamo: Plazo al que pidió su crédito en días (en cuántos días va a pagar).
* Hitorial_crediticio: 1 si tiene historial crediticio, 0 si no tiene.
* Area_vivienda: En qué tipo de área esta situada su casa.
* Estatus_prestamo: Si le otorgaron el crédito.
* Asesor_asignado: El nombre del asesor que atenderá al cliente si se le otorgó el crédito.

En el último mes, han llegado muchos más registros de los que puede atender el equipo de crédito. Alguien sugirió crear un modelo para poder decidir a quien prestarle.

* ¿Crees que sea una buena idea? ¿ Por qué?
* Si la respuesta fue sí, ¿qué tipo de probema es según los datos que tienes? (Supervisado o No Supervisado)
* Haz las transformaciones que necesites a los datos y desarrolla algún modelo.
* ¿Cómo sabes que es un buen modelo?

## El Dataset

1. devices.csv
una tabla de dispositivos asociados con un usuario
- marca: cadena correspondiente a la marca del teléfono
- user_id: cadena que identifica de forma exclusiva al usuario
2. users.csv
una tabla de datos de usuario
- user_id: cadena que identifica de forma exclusiva al usuario
- birth_year: número entero correspondiente al año de nacimiento del usuario
- país: cadena de dos letras correspondiente al país de residencia del usuario
- ciudad: dos cadenas correspondientes a la ciudad de residencia del usuario
- created_date: fecha y hora correspondiente a la fecha de creación del usuario
- user_settings_crypto_unlocked: entero que indica si el usuario ha desbloqueado el cifradomonedas en la aplicación
- plan: cadena que indica en qué plan está el usuario
- atributos_notificaciones_marketing_push: flotante que indica si el usuario ha aceptado recibirnotificaciones push de marketing
- atributos_notificaciones_marketing_email: flotante que indica si el usuario ha aceptado recibirnotificaciones de marketing por correo electrónico
- num_contacts: número entero correspondiente al número de contactos que el usuario tiene en Resuelve
- num_referrals: número entero correspondiente al número de usuarios referidos por el usuario seleccionado
- num_successful_referrals: número entero que corresponde al número de usuarios con éxitoreferido por el usuario seleccionado (significa con éxito los usuarios que realmente han instalado la aplicacióny pueden usar el producto)

3. notificaciones.csv
una tabla de notificaciones que ha recibido un usuario
- motivo: cadena que indica el propósito de la notificación
- canal: cadena que indica cómo se ha notificado al usuario
- estado: cadena que indica el estado de la notificación
- user_id: cadena que identifica de forma exclusiva al usuario
- created_date: fecha y hora que indica cuándo se envió la notificación
4. transacciones.csv
una tabla con las transacciones que realizó un usuario
- transaction_id: cadena que identifica de forma exclusiva la transacción
- transacciones_tipo: cadena que indica el tipo de transacción
- transacciones_currencia: cadena que indica la moneda de la transacción
- amount_usd: flotante correspondiente al monto de la transacción en USD
- transacciones_estado: cadena que indica el estado de una transacción
- COMPLETADO: la transacción se completó y se cambió el saldo del usuario
- RECHAZADA / FALLADA: la transacción se rechazó por algún motivo, generalmente corresponde asaldo insuficiente
- REVERTED: la transacción asociada se completó primero pero luego se revertió más tarde en el tiempo potencialmente debido a que el cliente se comunica con Resuelve
- ea_cardholderpresence: cadena que indica si el titular de la tarjeta estaba presente cuando la transacciónsucedió
- ea_merchant_mcc: flotante correspondiente al Código de categoría de comerciante (MCC)
- ea_merchant_city: cadena correspondiente a la ciudad del comerciante
- ea_merchant_country: cadena correspondiente al país del comerciante
- direction: cadena que indica la dirección de la transacción
- user_id: cadena que identifica de forma exclusiva al usuario
- created_date: fecha y hora correspondiente a la fecha de creación de la transacción

## ¿Llegaste aquí por casualidad?
Si llegaste aquí por casualidad y ya tienes la prueba resuelta, ¡manda tus resultados a edsuarez@resuelve.mx para revisarla y agendar una llamada!


