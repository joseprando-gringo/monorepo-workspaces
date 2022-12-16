# Criar imagem web
```sh
docker build -t monorepo-web . -f Dockerfile-web
```

# Validar as dependências (Não deve ter axios)
```
docker run -it monorepo-web sh
cd node_modules
ls
```

# Criar imagem consumer
```sh
docker build -t monorepo-consumer . -f Dockerfile-consumer
```

# Validar as dependências (Não deve ter express)
```
docker run -it monorepo-consumer sh
cd node_modules
ls
```