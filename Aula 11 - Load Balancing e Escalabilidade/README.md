# Aula 11 - Load Balancing e Escalabilidade

## 1. O problema da escalabilidade

**Por que escalar?**  
Sistemas digitais precisam suportar crescimento de usuários, dados e processamento. Escalar é garantir desempenho, disponibilidade e resiliência.

---

## 2. Técnicas de Escalabilidade

### **Vertical (Scale Up)**
- Aumenta recursos (CPU, memória, disco) de um servidor.
- **Limite:** Hardware físico, downtime para upgrade.
- **Indicado para:** Sistemas legados, bancos de dados monolíticos.

### **Horizontal (Scale Out)**
- Adiciona mais servidores/nós ao sistema.
- **Escalabilidade “infinita”** (ex: web, microserviços).
- **Desafio:** Manter estado e consistência.
- **Para arquitetos:** Use arquitetura stateless sempre que possível.

---

## 3. Load Balancing (Balanceamento de carga)

### **O que é?**
Distribui requisições entre múltiplos servidores, evitando sobrecarga e aumentando disponibilidade.

### **Tipos**
- **Layer 4 (TCP/UDP)**
  - Balanceia conexões de rede.
  - Exemplo: HAProxy, AWS NLB.
- **Layer 7 (HTTP/HTTPS)**
  - Analisa e distribui pelo conteúdo das requisições.
  - Exemplo: NGINX, AWS ALB.

### **Algoritmos**
- **Round Robin:** Sequencial, simples e eficiente.
- **Least Connections:** Para cargas desbalanceadas.
- **Weighted:** Permite dar mais carga a servidores mais potentes.
- **IP Hash:** Mantém afinidade do cliente com o mesmo servidor (sticky session).

### **Ferramentas**
- Open source: NGINX, HAProxy, Traefik, Envoy.
- Cloud: AWS ELB/ALB/NLB, Google Cloud Load Balancing, Azure Load Balancer.

---

## 4. Alta Disponibilidade e Resiliência

- **Health checks:** Verifica automaticamente se servidores estão ativos.
- **Failover:** Redireciona tráfego em caso de falha.
- **Escalabilidade automática:** Auto-scaling groups em nuvens públicas.

---

## 5. Gerenciamento de Estado e Sessões

- **Stateless:** Cada requisição é independente; facilita escalabilidade.
- **Stateful:** Sessões de usuário precisam ser compartilhadas (ex: Redis, Memcached).

---

## 6. Práticas avançadas

- **Blue/Green Deployment:** Deploy sem downtime, testando nova versão em paralelo.
- **Canary Release:** Liberação gradual de novas versões.
- **Global Load Balancing:** Multi-região, roteamento geográfico.
- **Observabilidade:** Monitoramento, tracing distribuído, dashboards (Prometheus, Grafana, Jaeger).

---

## 7. Desafios comuns

- **Single point of failure:** Load balancer deve ser redundante.
- **Escalabilidade de bancos de dados:** Uso de sharding, replicação, caching.
- **Custo:** Tráfego entre regiões pode ser caro.

---

## 8. Perguntas-chave

- Como garantir zero downtime durante upgrades?
- Como lidar com session stickiness em aplicações críticas?
- Quando usar balanceamento L4 versus L7?

---

## 9. Para arquitetos

- Avalie impacto de latência, throughput e failover.
- Considere o uso de service mesh (ex: Istio) para balanceamento interno.
- Implemente mecanismos de auto-healing.

---

## 10. Referências

- Patterns: Bulkhead, Circuit Breaker, Retry, Timeout
- AWS Well-Architected Framework: Reliability Pillar

---