# Домашнее задание к занятию 6 «Создание собственных модулей»

## Основная часть

Ваша цель — написать собственный module, который вы можете использовать в своей role через playbook. Всё это должно быть собрано в виде collection и отправлено в ваш репозиторий.

- Шаг 1. В виртуальном окружении создайте новый my_own_module.py файл.

- Шаг 2. Наполните его содержимым:

- Шаг 3. Заполните файл в соответствии с требованиями Ansible так, чтобы он выполнял основную задачу: module должен создавать текстовый файл на удалённом хосте по пути, определённом в параметре path, с содержимым, определённым в параметре content.

Внес правки.

- Шаг 4. Проверьте module на исполняемость локально.

<img width="908" height="127" alt="image" src="https://github.com/user-attachments/assets/849dde3d-38c8-4eee-98a4-c8d2183fc66d" />

- Шаг 5. Напишите single task playbook и используйте module в нём.
  
  <img width="570" height="212" alt="image" src="https://github.com/user-attachments/assets/e6fb2f9b-ba7a-455f-b32f-c50e0a1b52ba" />

- Шаг 6. Проверьте через playbook на идемпотентность.
  
  <img width="1102" height="299" alt="image" src="https://github.com/user-attachments/assets/9da548cf-ce60-4efc-8e31-843229e0bbb5" />

- Шаг 7. Выйдите из виртуального окружения.

- Шаг 8. Инициализируйте новую collection: ansible-galaxy collection init my_own_namespace.yandex_cloud_elk.

- Шаг 9. В эту collection перенесите свой module в соответствующую директорию.

  Перенес в /my_own_collection/my_own_namespace/yandex_cloud_elk/plugins/modules

- Шаг 10. Single task playbook преобразуйте в single task role и перенесите в collection. У role должны быть default всех параметров module.

  <img width="1110" height="90" alt="image" src="https://github.com/user-attachments/assets/344093f7-286a-4145-b27d-86f21dcde24b" />

- Шаг 11. Создайте playbook для использования этой role.

  [my_playbook](https://github.com/vladmgb/my_own_collection/blob/main/my_own_namespace/yandex_cloud_elk/my_playbook.yml)

- Шаг 12. Заполните всю документацию по collection, выложите в свой репозиторий, поставьте тег 1.0.0 на этот коммит.

  [README.md](https://github.com/vladmgb/my_own_collection/blob/main/my_own_namespace/yandex_cloud_elk/README.md)

- Шаг 13. Создайте .tar.gz этой collection: ansible-galaxy collection build в корневой директории collection.

  <img width="1019" height="104" alt="image" src="https://github.com/user-attachments/assets/c528a4d3-2cbe-4e90-ac06-78dcf0d79059" />

- Шаг 14. Создайте ещё одну директорию любого наименования, перенесите туда single task playbook и архив c collection.

- Шаг 15. Установите collection из локального архива: ansible-galaxy collection install <archivename>.tar.gz.

  <img width="1016" height="205" alt="image" src="https://github.com/user-attachments/assets/a307fce0-a27a-48d8-b867-a138f8e5ed44" />

- Шаг 16. Запустите playbook, убедитесь, что он работает.

<img width="1108" height="229" alt="image" src="https://github.com/user-attachments/assets/71816e63-6e54-4eed-85c3-30a977ce3fec" />


- Шаг 17. В ответ необходимо прислать ссылки на collection и tar.gz архив, а также скриншоты выполнения пунктов 4, 6, 15 и 16

  [Collection](https://github.com/vladmgb/my_own_collection/tree/main/my_own_namespace/yandex_cloud_elk)
  
  [архив](https://github.com/vladmgb/my_own_collection/blob/main/my_own_namespace/yandex_cloud_elk/my_own_namespace-yandex_cloud_elk-1.0.0.tar.gz)
