# Aula 12 - Microsserviços

## 1. O que são microsserviços?

**Definição:**  
Arquitetura onde uma aplicação é composta por pequenos serviços independentes, cada um executando uma função de negócio específica, comunicando-se via rede (geralmente HTTP/REST, gRPC ou mensageria).

### **Por que migrar para microsserviços?**
- Agilidade no desenvolvimento e deploy.
- Escalabilidade granular.
- Isolamento de falhas.

---

## 2. Princípios fundamentais

- **Descentralização:** Cada serviço tem seu próprio repositório de código, ciclo de vida e banco de dados.
- **Autonomia:** Serviços são independentes para desenvolvimento, deploy e escala.
- **Comunicação via API:** Contratos bem definidos, geralmente REST, gRPC, GraphQL, ou eventos (event-driven).
- **Responsabilidade única:** Cada serviço deve ser pequeno e focado em um domínio.

---

## 3. Benefícios para times e negócios

- **Deploys independentes:** Menos risco e mais frequência.
- **Escalabilidade independente:** Só escale o que precisa.
- **Resiliência:** Falha de um serviço não compromete todo o sistema.
- **Organização por domínio:** Facilita alinhamento com áreas de negócio (DDD).

---

## 4. Desafios e Armadilhas

- **Complexidade operacional:** Mais serviços para monitorar, versionar e orquestrar.
- **Consistência de dados:** Cada serviço tem seu banco, exigindo estratégias de consistência eventual.
- **Gerenciamento de dependências:** Versionamento de APIs, backwards compatibility.
- **Observabilidade:** Logs, tracing e métricas precisam ser centralizados.

---

## 5. Tecnologias e Ferramentas

- **Containers:** Docker, Podman.
- **Orquestradores:** Kubernetes, Docker Swarm, OpenShift.
- **API Gateways:** Kong, Ambassador, NGINX, AWS API Gateway.
- **Mensageria:** RabbitMQ, Kafka, SQS.
- **Service Mesh:** Istio, Linkerd, Consul Connect.

---

## 6. Padrões e Estratégias

- **Service Discovery:** Registro e localização automática de serviços.
- **Circuit Breaker:** Previne falhas em cascata (resiliência).
- **Bulkhead, Retry, Timeout:** Padrões de tolerância a falhas.
- **Event Sourcing/Command Query Responsibility Segregation (CQRS):** Separação de comandos e consultas, baseadas em eventos.

---

## 7. Boas práticas

- **APIs bem documentadas:** Swagger/OpenAPI, gRPC proto files.
- **Automatize deploy e testes:** CI/CD, pipelines, testes integrados e de contrato.
- **Centralize logs e métricas:** ELK Stack, Prometheus, Grafana, Jaeger.
- **Planeje rollback e deploys seguros:** Blue/Green, Canary.
- **Pensamento evolutivo:** Comece pequeno, extraia serviços conforme o crescimento.

---

## 8. Exemplos práticos

- **E-commerce:** Serviço de catálogo, carrinho, pagamentos, pedidos, recomendação.
- **Bancos digitais:** Serviços de autenticação, extrato, transferências, notificações.

---

## 9. Perguntas-chave e Respostas

**Como dividir um monolito em microsserviços?**  
- Analise o domínio de negócio usando DDD (Domain-Driven Design) para identificar bounded contexts, extraia partes menos acopladas do sistema e crie APIs entre elas. Migre gradualmente, começando pelos módulos mais independentes e críticos.

**Quando não usar microsserviços?**  
- Em sistemas pequenos, equipes reduzidas, aplicações sem necessidade de alta escalabilidade ou disponibilidade, e quando o overhead de complexidade operacional supera os benefícios.

**Como garantir consistência e rastreabilidade?**  
- Utilize eventos para sincronização entre serviços, implemente sistemas de mensageria confiáveis, centralize logs e use ferramentas de tracing como OpenTelemetry e Jaeger para monitorar fluxos distribuídos.

---

## 10. Para arquitetos

- Avalie trade-offs de granularidade.
- Use DDD (Domain-Driven Design) para identificar bounded contexts.
- Invista em automação e cultura DevOps.

---

## 11. Referências

- Microservices.io (Martin Fowler, Chris Richardson)
- O’Reilly - Building Microservices (Sam Newman)

---