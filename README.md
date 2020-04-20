<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src="https://github.com/Rocketseat/bootcamp-gostack-desafio-02/raw/master/.github/logo.png" width="300px" />
</h1>

<h3 align="center">
  BootCamp GoStack Desafio Final: FastFeet
</h3>

## Instruções

Clonar o projeto
```
git clone --recursive https://github.com/hgtpcastro/bootcamp-gostack-desafio-final.git
```
Atualizaçõe dos sub-módulos (back-end, front-end, mobile):
```
git submodule update --init --recursive
```

***

## Configurando o back-end

Vá para a pasta back-end  `cd back-end` , e rode o comando `yarn install`.

Renomeie o arquivo `.env.example` e faça as configurações necessárias, seguindo cada seção.

- PostgreSQL
```
docker run --name database -e POSTGRES_PASSWORD=[DB_PASS] -p 5432:5432 -d [DB_USER]
```

- Redis
```
docker run --name redisfastfeet -p 6379:[REDIS_PORT] -d -t redis:alpine
```

- Seed
```
yarn sequelize db:seed:all
```

Usuário administrador:
```
Email: fastfeet@admin.com
Password: 123456
```

- Migrations
```
yarn sequelize db:migrate
```

- Startar servidor
```
yarn dev
```

- Startas as queue (rode em um novo terminal)
```
yarn queue
```

## Configurando front-end
Vá para a pasta front-end `cd frontend`, e rode o comando `yarn install`.
Abra `src/services/api.js`, e atualize a variável `baseURL`, com as configurações do servidor.

- Startar a aplicação Web
```
yarn start
```

## Configurando mobile
Vá para a pasta mobile `cd mobile`, e rode o comando  `yarn install`.
Abra `src/services/api.js`, e atualize a variável `BASE_URL`, com as configurações do servidor.

- Build app for Android
```
react-native run-android
```

- Build app for Android
```
react-native run-android
```

- Start Metro server
```
yarn start
```
