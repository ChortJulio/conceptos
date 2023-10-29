# NodeJS (midudev)
### https://www.youtube.com/watch?v=yB4n_K7dZV8&list=PLUofhDIg_38qm2oPOV-IRTTEKyrVBBaU7

## ¿Qué es?

- Entorno de ejecución de Javascript.
- Un sitio en donde se puede ejecutar Javascript.
- Se puede ejecutar en la terminal, en el backend, en el front, nintendo switch, etc.
- Es asíncrono con entrada y salida de datos.
- Salida orientada a EVENTOS. Utiliza un event loop.
- NodeJS utiliza V8. El mismo motor que utiliza Chrome. Cuando utilizamos NodeJS es como si usaramos el mismo motor de Chrome. Ojo, no el mismo entorno, sólo el mismo motor. Analogía con auto.

## Threads
- NodeJS difiere de otros lenguajes/frameworks es mono-hilo. Su sistema libera el proceso para hacer cosas asíncronas.
- Simula que hace múltiples cosas a la vez, aunque en realidad es sólo 1 a la vez.

## ¿Por qué aprender NodeJS?

1. Demanda del mercado: Linkedin, Yahoo, Ebay, etc. Cualquier compañía que conozcas utiliza NodeJS de alguna forma u otra. Hasta los comandos en la VSCode los utiliza. El STACK, MERN: MongoDB, React, NodeJS. Hasta NodeJS se utiliza a sí mismo. 
2. Se puede utilizar JS directamente. Ser productivo muy rápido.
3. Crear aplicaciones, utilidades, apis, servicios, scrapping, sin dificultad. No te limitás en nada.
4. Comunidad y ecosistemas INMESOS. Cuenta con npm. Posibilidades infinitas, personas, comunidades, artículos, gente con la que hablar de JS.
5. NodeJS es rápido, escalable y gratis (o casi gratis) de desplegar. No es lento y escala bastante bien. Consume un poco más memoria que otras soluciones, pero te permite escalar muy bien.

## Historia
- Se creó en 2009. Se unió en 2015 con otro proyecto y remotó el camino/senda. Ahora es totalmente de código abierto, sin una empresa detrás con 'agenda oscura'.

## Diferentes versiones o proyectos
- Puedo dockerizar todos mis proyectos.
- Utilizar administrador de versiones de node (nvm).
- Utilizar alternativa a nvm llamada fnm. Para hacer esto necesito previamente tener instalado 'Rust lang'. Cuento a continuación los pasos que tengo que hacer para instalarlo (es un problema de windows, si uso linux o mac puedo utilizar sin drama npm):
  - Habilitar e instalar WSL (ver WSL.md)
  - Ejecutar el siguiente comando en consola: curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  - Instalar fnm con el siguiente comando: curl -fsSL https://fnm.vercel.app/install | bash




