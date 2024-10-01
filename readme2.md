# PŔACTICA 1 . COMANDOS DE DOCKER

Crea un novo repositorio público en git, coo nome da tarefa, clónao e engade un arquivo readme2.md en local que poña unha frase á túa elección.

Facendo uso de VScode, Docker e a imaxe de ubuntu da práctica anterior, describe no arquivo readme.md, cun formato claro, os pasos e comandos para:

**1. Descargar e comprobar que unha imaxe está no teu equipo**

Para descargar unha imaxe utilizamos o comando `docker pull ubuntu ` , e finalmente para comprobar que a temos no noso equipo, utilizamos o comando `docker images`.

**2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?**

Para crear un contenedor sen nome, utilizamos o comando `docker run -dit ubuntu`, onde podemos observalo co comando `docker ps -a`

**3. Crea un contenedor coo nome 'u1', cómo accedes a el?**

Para crear o contenededor, crease da misma forma que o anterior, pero engadindo '--name' e o nome que deseamos, é decir, `docker run -dit --name u1 ubuntu`, e para acceder a él podemos facendo click dereito ou co comando `docker exec -it u1 bash`, e xa entraremos no modo terminal deste contenedor.

**4. Comproba a súa ip e fai ping a google.com**

Para comprobar a ip, eu empreguei o comando `docker inspect u1 | grep "IPAddress `, onde saiume que teño a ip 172.17.0.2.
Para facer ping, simplemente empreguei o comando `ping google.com`

**5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?**

Como fixemos no apartado 3, crearemos o contenedor da misma forma pero cambiando o nome, 


**6. Se pechas as terminales, qué pasa coo contenedor?**

Como estes contendedores os iniciamos con `d`, neste caso seguiran en segundo plane, é dicir, seguiran executandose.

**7. Cánta memoria no disco duro ocupaches? usa docker para calculalo**

Para comprobar o espacio empregado, utilizamos o comando `docker system df`, no meu caso cando o empreguei tiña 3 imaxes que ocupaban 226 MB, e sete contendedores onde tres estaban activos, que ocupaban 42 MB.

**8. Cánta RAM ocupan os contenedores? Crea varios para calculalo**

Para comprobar a RAM ocupada, necesitamos empregar o comando `docker status` onde os contededores ocupaban 26,98 MiB.

**9. Cómo fixeches para clonar o repositorio**

Para clonar o repositorio, primero necesitaremos crealo en GitHub e copiar a URL, e a continuación empregar o comando `git clone https://github.com/aleexjusto/P1-ComandosdeDocker.git ` , neste caso ese é a miña dirección

**10. Cómo engades o arquivo readme2.md**

Para añadilo simplemente empregamos o comando `git add readme2.md`

**11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md**

Primeiro necesitamos gardar os cambios no documento, a continuación empregar o comando `git add readme2.md`, a continuación `git commit -m "P1" ` e finalmente subir o arquivo con `git push origin`.

**12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.**

Para comprobar as diferenzas, simplemente empregamos o comando `git diff origin/main` , onde main é o local.


