# Самостоятельная работа
Реализация ci/cd конвейера, Инстументы: Jenkins + Nexus + SonarQube + Ansible + Vault.

Добавлен node_exporter на все VM, автоматическое развертывание через Ansible-playbook `./ansible/nodeExporter.yml`, сбор метрик в Prometheus `./userdata/prometheus.yml`
Добавлен (в процессе) установщик ELK + раскатка Filebeat по всем хостам

Автоматизация Компиляции из исходного кода, тестирования, развертывания артефакта на тестовый стенд, после финальной проверки SonarQube установка в прод.

## Виртуальные машины:
- jenkins (Jenkins, Ansible, Prometheus, Grafana)
- elk_stack (Elasticsearch, Logstash, Kibana, Node_Exporter (мониторинг), Filebeat(логироваине)
- nexus
- sonarqube
- backend
- ctfrontend
- cpfrontend

Весь Provision `./userdata/`

### Playbook установщик Prometheus
Добавлен установщик Prometheus 2.37 `./ansible install_prometheus_2.37.yml`

### Раскатка Node_exporter (сбор метрик в Prometheus) на все Хосты
`./ansible/nodeExporter.yml`

### Раскатка Filebeat (сбор логов в Elasticsearch) на все Хосты
`coming soon`

### Установщик ELK
`coming soon`