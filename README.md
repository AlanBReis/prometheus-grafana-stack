# Stack de Monitoramento com Docker: Prometheus e Grafana

Este projeto configura uma stack completa de monitoramento e observabilidade usando Docker. Inclui Prometheus para coleta de métricas, Grafana para visualização, Loki para agregação de logs e Tempo para rastreamento distribuído.

## Funcionalidades

- **Prometheus**: Coleta métricas de vários serviços.
- **Grafana**: Visualiza métricas e logs em dashboards simples e personalizáveis.
- **Loki**: Agrega logs para consulta eficiente.
- **Tempo**: Lida com rastreamento distribuído para monitorar requisições entre serviços.
- **Promtail**: Encaminha logs para o Loki para armazenamento e consulta.

## Pré-requisitos

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

Certifique-se de que o Docker e o Docker Compose estejam instalados em sua máquina antes de continuar.

## Instruções de Configuração

1. Clone este repositório:

   ```bash
   git clone https://github.com/seuusuario/nome-do-repositorio.git
   cd nome-do-repositorio

   
2. Inicie os serviços usando o Docker Compose:  
    ```bash
    docker compose up -d
    
3. Acesse os seguintes serviços em seu navegador:
   * Grafana: http://localhost:3001 (Porta 3001)
   * Prometheus: http://localhost:9090 (Porta 9090)
   * Loki: http://localhost:3100 (Porta 3100)
   * Tempo: http://localhost:3200 (Porta 3200)

4. O Grafana está configurado por padrão para utilizar o Prometheus, Loki e Tempo como fontes de dados

## Configuração
Os seguintes serviços estão incluídos no arquivo docker-compose.yml:

* Prometheus: Executa na porta 9090 e está pré-configurado para coletar métricas.
* Grafana: Executa na porta 3001, pré-configurado com as fontes de dados (Prometheus, Loki e Tempo).
* Loki: Para agregação de logs, exposto na porta 3100.
* Tempo: Rastreamento distribuído, disponível na porta 3200.
* Alloy: Outro serviço para coleta de métricas.
* Shoehub, Orderservice, Paymentservice: Microserviços de exemplo para teste.

  
