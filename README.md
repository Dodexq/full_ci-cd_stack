# Самостоятельная работа
Реализация ci/cd конвейера, Инстументы: Jenkins + Nexus + SonarQube + Ansible + Vault.

Добавлен node_exporter на все VM, автоматическое развертывание через Ansible-playbook `/ansible/nodeExporter.yml`, сбор метрик в Prometheus `/userdata/prometheus.yml`

Автоматизация Компиляции из исходного кода, тестирования, развертывания артефакта на тестовый стенд, после финальной проверки SonarQube установка в прод.

## Виртуальные машины:
- jenkins
- nexus
- sonarqube
- backend
- ctfrontend
- cpfrontend

Весь Provision `./userdata/`