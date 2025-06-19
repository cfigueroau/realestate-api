¿Qué importancia tiene probar en múltiples entornos de Node.js?
Probar en diferentes versiones de Node.js nos permite asegurarnos de que nuestra API funciona correctamente sin importar el entorno donde se ejecute. A veces una función es válida en una versión, pero no existe o se comporta distinto en otra. Hacer estas pruebas evita errores cuando la aplicación se instala en servidores con versiones distintas a las que usamos durante el desarrollo.


¿Por qué es importante validar la salida de una API desde un workflow?
Validar la salida desde un workflow automático garantiza que todo esté funcionando como se espera, cada vez que alguien hace un cambio. Así evitamos subir código que "rompa" la API sin darnos cuenta. Nos da confianza de que lo que estamos publicando sigue cumpliendo con lo que los usuarios o sistemas esperan recibir.


¿Qué pasos podríamos agregar si fuéramos a hacer despliegue a producción?
Si quisiéramos desplegar a producción, podríamos agregar:
	• Un paso para compilar o construir el proyecto (si fuera necesario).
	• Validaciones adicionales como pruebas de integración o cobertura de código.
	• Un paso que se conecte a un servidor o servicio (como Render, Vercel, AWS o Heroku) y haga el deploy automático si todo salió bien.
	• Notificaciones a Slack, correo o Discord avisando que el deploy fue exitoso.


¿Qué limitaciones tiene GitHub Actions y cómo las enfrentaríamos?
Una limitación es que los runners gratuitos tienen un tiempo limitado y no todos los entornos están disponibles. También puede pasar que se nos acaben los minutos si el proyecto es muy grande o usamos muchos workflows.
Para enfrentarlo:
	• Podemos optimizar nuestros jobs y evitar pasos innecesarios.
	• Usar caching para acelerar tiempos de instalación.
	• Y si el proyecto crece, migrar a runners propios o pagar un plan de GitHub con más minutos.
