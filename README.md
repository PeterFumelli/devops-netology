# В файле .gitignore указаны следующие файлы и части названий файлов, которые будут проигнорированы при пуше

 • Служебные файлы Terraform:

 • .terraform/ — директория, в которую Terraform сохраняет рабочее состояние, загрузку провайдеров и другие временные данные. Она не должна попадать в репозиторий.

 • Файлы состояния инфраструктуры:
    *.tfstate и *.tfstate.backup — содержат текущее состояние инфраструктуры, включая IP-адреса, идентификаторы ресурсов и другую чувствительную информацию. Эти файлы не должны попадать в Git, чтобы избежать утечки данных и конфликтов между разработчиками.

 • Файлы конфигурации переменных:
    crash.log, terraform.tfvars, *.tfvars.json — могут содержать чувствительные переменные (например, токены, пароли). Эти файлы добавляются в .gitignore, чтобы не публиковать секреты.

 • Журналы ошибок и отладочные логи:
   crash.log — лог аварийных завершений Terraform.
