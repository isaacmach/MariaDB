# MariaDB Cluster on Kubernetes

Este repositório contém instruções e arquivos de configuração para implantar um cluster de três MariaDB no Kubernetes, garantindo alta disponibilidade e sincronização de dados entre os nós.

## Passos para Implantação

1. **Criação do Cluster Kubernetes:**
   - Configure um cluster Kubernetes usando um provedor de nuvem ou localmente.

2. **Implantação de Contêineres MariaDB:**
   - Use os manifestos Kubernetes ou gráficos Helm fornecidos neste repositório para implantar os contêineres MariaDB.
   - Certifique-se de definir réplicas, volume mounts e variáveis de ambiente conforme necessário.

3. **Configuração da Replicação MariaDB:**
   - Designe um nó como mestre e os outros como escravos.
   - Configure a replicação mestre-escravo nos nós MariaDB.

4. **Tratamento de Conexões de Clientes:**
   - Exponha o serviço MariaDB usando um Kubernetes Service do tipo LoadBalancer ou ClusterIP.
   - Configure um Ingress Controller para rotear as conexões de clientes para os nós disponíveis.

5. **Implementação de Verificações de Saúde e Failover Automático:**
   - Configure sondas de verificação de vida e prontidão para detectar a saúde dos nós MariaDB.
   - Configure políticas de reinicialização automática de pods ou redirecionamento de tráfego em caso de falha.

6. **Testes e Verificação:**
   - Realize testes para garantir que a configuração seja resiliente a falhas.
   - Verifique se os clientes podem se conectar e realizar operações mesmo após a falha de um nó.

7. **Monitoramento e Manutenção:**
   - Configure ferramentas de monitoramento, como Prometheus e Grafana, para acompanhar a saúde e o desempenho do cluster.
   - Realize manutenção regular, incluindo backups, atualizações e patches de segurança.
