# Curso de Docker en Platzi

Ésta es una aplicación de ejemplo para el curso de Docker de Platzi por Guido
Vilariño.

Encuentra más información en https://platzi.com, suscríbete al curso y aprende
a usar Docker de manera profesional.

Para hacer construcción del proyecto con build se debe ejecutar:

docker build -t platziapp .

docker run --rm -d -p 3000:3000 -v $(pwd):/usr/src platziapp 

para conectarlo a través de la misma red, debo crear una red con 

docker network create --attachable platziapp

para listarlo es docker network ls

para ponerlo en la red 

docker network connect red contenedor

para correr un nultiambiente lo realizamos con

docker build -t platziapp -f build/development.Dockerfile .
