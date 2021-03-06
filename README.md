## Evalúa tu trámite Puebla

[Licencia](/LICENSE)

### Deploy
Para utilizar el script de deploy con Chef se debe de correr:
`knife solo cook usuario@dominio`

Hay algunos prerrequisitos como:
- Verificar que en la carpeta `Deploy/data_bags/keys/secret.json` se encuentre la información correspondiente al
ambiente que se va a hacer deploy. [Ver archivo de ejemplo](https://github.com/civica-digital/urbem-puebla/blob/master/Deploy/data_bags/keys/secret.json.example)

- Verificar que `Deploy/nodes/dominio.json` donde el nombre de archivo `dominio` corresponde a la IP o al dominio
del ambiente objetivo. [Ver archivo de ejemplo](https://github.com/civica-digital/urbem-puebla/blob/master/Deploy/nodes/104.154.88.10.json)

- Si vas a agregar nuevas variables de entorno para el contenedor de Ruby, asegúrate de agregarlas en el `hash` de
`Deploy/site-cookbooks/urbem/libraries/creds_helper.rb`, además agregarlas en `docker/urbem-env.conf` para que se importen al
ambiente del contenedor.


#### Si es una instalación nueva
Asegurate de los prerrequisitos anteriores y utiliza el comando:

`knife solo bootstrap usuario@dominio`

Para más información de la implementación de estos scripts de deploy ver: [knife-solo](https://matschaffer.github.io/knife-solo/)

### Dependencias
- Ruby
- Rails
- Bootstrap sass
- Rspec
- Redis

Ver Gemfile para más información

### ¿Dudas?

Escríbenos a <equipo@codeandomexico.org>.

### Equipo

El proyecto ha sido iniciado por [Codeando México](https://github.com/CodeandoMexico?tab=members).
El core team:
- [Eddie Ruvalcaba](https://github.com/eddie-ruva)
- [Juan Pablo Escobar](https://github.com/juanpabloe)
- [Abraham Kuri](https://github.com/kurenn)
- [Noé Domínguez](https://github.com/poguez)
- [Abi Sosa](https://github.com/abisosa)
- [Miguel Morán](https://github.com/mikesaurio)

### Licencia

Creado por [Codeando México](https://github.com/CodeandoMexico?tab=members), 2013 - 2015.
Disponible bajo la licencia GNU Affero General Public License (AGPL) v3.0. Ver el documento [LICENSE](/LICENSE) para más información.
