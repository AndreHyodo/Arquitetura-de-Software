# Aula 10 - Cloud Computing

## 1. Introdução e Conceitos Básicos

**O que é computação em nuvem?**  
É um modelo de entrega de recursos computacionais (servidores, armazenamento, redes, bancos de dados, serviços de análise, inteligência artificial etc.) pela internet, sob demanda, com escalabilidade automática e cobrança baseada no consumo.  
**Exemplo para iniciantes:** Usar o Google Drive para armazenar arquivos é computação em nuvem.

### **Evolução Histórica**
- Antes: Computação centralizada (mainframes), depois client-server, virtualização, até chegar à nuvem.
- Hoje: Nuvem é padrão para empresas de todos os portes.

---

## 2. Modelos de Serviço

### **IaaS (Infraestrutura como Serviço)**
- **Para quem:** Equipes de TI que querem controle sobre servidores e redes.
- **Responsabilidade:** Cliente gerencia SO, aplicações e dados.
- **Exemplo:** Amazon EC2, Azure VMs.
- **Dica avançada:** Ideal para arquiteturas que exigem flexibilidade máxima ou integração com sistemas legados.

### **PaaS (Plataforma como Serviço)**
- **Para quem:** Desenvolvedores que querem agilidade sem gerenciar infraestrutura.
- **Responsabilidade:** Cliente foca no código, provedor cuida do resto.
- **Exemplo:** Heroku, Google App Engine.
- **Tópico avançado:** Serverless é uma evolução do PaaS.

### **SaaS (Software como Serviço)**
- **Para quem:** Usuários finais e empresas que querem soluções completas.
- **Responsabilidade:** Cliente só gerencia usuários e dados.
- **Exemplo:** Salesforce, Office365, Gmail.
- **Para arquitetos:** Avalie integração via APIs e extensibilidade.

---

## 3. Tipos de Nuvem

- **Pública:** Compartilhada entre empresas/usuários (AWS, GCP, Azure).
- **Privada:** Dedicada a uma única organização (OpenStack, VMware).
- **Híbrida:** Combina nuvem pública e privada, permitindo estratégias como disaster recovery, burst ou segregação de dados sensíveis.
- **Multicloud:** Uso de múltiplos provedores para evitar dependência (“vendor lock-in”).

---

## 4. Vantagens e Benefícios

- **Escalabilidade e Elasticidade:** Adaptação instantânea à demanda.
- **Custo sob demanda:** Economia, sem gastos com ociosidade.
- **Alta disponibilidade e redundância:** Provedores oferecem SLAs robustos e replicação geográfica.
- **Automação:** Provisionamento, monitoramento e auto healing.

**Para arquitetos:**  
- Facilita DevOps, CI/CD, infraestrutura como código e microserviços.

---

## 5. Desafios e Riscos

- **Segurança:** Atenção à criptografia, controle de acesso, compliance (LGPD, GDPR, HIPAA).
- **Latência e desempenho:** Avalie zonas de disponibilidade e regiões.
- **Vendor lock-in:** Cuidado com dependências proprietárias.
- **Custos ocultos:** Tráfego de dados, licenças, recursos não provisionados corretamente.

---

## 6. Tendências Atuais

- **Serverless (FaaS):** Executa funções sem gerenciar servidores (ex: AWS Lambda, Azure Functions).
- **Containers e Orquestração:** Docker, Kubernetes, OpenShift.
- **Edge Computing:** Processamento próximo do usuário final.
- **Inteligência Artificial e Machine Learning como serviço.**

---

## 7. Boas Práticas

- **Escolha a nuvem e modelo de serviço adequado ao seu caso de uso.**
- **Automatize o provisionamento:** Use ferramentas como Terraform, Ansible, CloudFormation.
- **Implemente observabilidade:** Monitoramento, logs centralizados, alertas.
- **Planeje a segurança desde o design.**

---

## 8. Perguntas para Reflexão

- Quando migrar para a nuvem faz sentido?
- Como garantir portabilidade entre diferentes provedores?
- Quais workloads devem permanecer on-premises?

---

## 9. Para quem quer se aprofundar

- **Arquiteturas cloud-native:** 12-factor apps, microserviços, APIs.
- **Design para resiliência:** Chaos Engineering, circuit breaker, fallback.
- **Compliance:** Certificações e regulamentações para ambientes cloud.

---

## 10. Referências e Ferramentas

- AWS Well-Architected Framework
- Google Cloud Architecture Center
- Azure Architecture Center
- Ferramentas: Terraform, Kubernetes, Prometheus, Grafana

---