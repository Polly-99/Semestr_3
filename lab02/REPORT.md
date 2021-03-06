## Laboratory work II

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**
 
## Tutorial

```bash
$ export GITHUB_USERNAME=Polly-99
$ export GIST_TOKEN=****************************************
$ alias edit=vi  #переопределяем команду
```

```bash
$ npm install -g gistup #устанавливаем gistup
```

```bash
#редактрируем файл .gistup.json
$ cat > ~/.gistup.json <<EOF
{
  "token": "${GIST_TOKEN}"
}
EOF
```

```bash
$ cd ~  #заходим в домашнюю директорию
$ mkdir -p workspace/labs/projects/  # создаем новые директории
$ mkdir -p workspace/labs/tasks/
$ mkdir -p workspace/labs/reports/
```

## Report

```bash
$ cd ~/workspace/labs/ # переходим в заданную директорию 
$ export LAB_NUMBER=02 # создаем переменную окружения
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER} #клонируем репозиторий
$ mkdir reports/lab${LAB_NUMBER} #создаем директорию
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md #копируем README.md в REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md #редактируем REPORT.md в редакторе vi
$ gistup -m "lab${LAB_NUMBER}" #создаем коммит в gist 
```
