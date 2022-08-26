# Самостоятельная работа
Реализация ci/cd конвейера, Инстументы: Jenkins + Nexus + SonarQube + Ansible + Vault.

Добавлен node_exporter на все VM, автоматическое развертывание через Ansible-playbook `./ansible/nodeExporter.yml`, сбор метрик в Prometheus `./userdata/prometheus.yml`

Добавлен (в процессе) установщик ELK + раскатка Filebeat по всем хостам

Автоматизация Компиляции из исходного кода, тестирования, развертывания артефакта на тестовый стенд, после финальной проверки SonarQube установка в прод.

## Виртуальные машины:
- jenkins (Jenkins, Ansible, Prometheus, Grafana, Node_Exporter, Filebeat)
- elk_stack (Elasticsearch, Logstash, Kibana, Node_Exporter, Filebeat)
- nexus (Nexus, Node_Exporter, Filebeat)
- sonarqube (sonarqube, Node_Exporter, Filebeat)
- backend (MariaDB, memcached, rabbitmq, Node_Exporter, Filebeat)
- ctfrontend (Tomcat, Node_Exporter, Filebeat)
- cpfrontend (Tomcat, Node_Exporter, Filebeat)

Весь Provision `./userdata/`

### Playbook установщик Prometheus
Добавлен установщик Prometheus 2.37 `./ansible install_prometheus_2.37.yml`

### Раскатка Node_exporter (сбор метрик в Prometheus) на все Хосты
`./ansible/nodeExporter.yml`

### Раскатка Filebeat (сбор логов в Elasticsearch) на все Хосты
`coming soon`

### Установщик ELK
`coming soon`