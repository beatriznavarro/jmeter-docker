# Teste Distribuído JMeter 🚀🚀



![Teste Distribuído](https://github.com/beatriznavarro/jmeter-docker/blob/main/imagens/distributed.png?raw=true)



## Pré-requisitos:
- Docker
- Docker Compose

## 🛠 Como executar:

### Gerar a imagem:

```bash
docker build -t brnavarro/jmeterdistv1 .
```

### Subir os containers:

```bash
docker-compose up --scale server=2
```

### Executar o Teste de Performance:

```bash
jmeter -n -t sample.jmx -R jmeter-docker_server_1,jmeter-docker_server_2 -l results.jtl -e -o /resultsDash/
```
