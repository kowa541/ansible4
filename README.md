# ansible4
# Лабораторная работа П04: Базовый деплой Nginx с помощью Ansible

## Цель работы
Автоматизация установки веб-сервера Nginx и развертывания HTML-страницы на целевой виртуальной машине с использованием Ansible.

## Инфраструктура
- **Управляющая машина (ANSIBLE1):** Ubuntu, IP `10.0.2.4`
- **Целевая машина (ANSIBLE2):** Ubuntu, IP `10.0.2.3`, пользователь `runner`
- **Сеть:** VirtualBox NAT Network (NatLab)

## Структура проекта
- `inventory.ini` — файл инвентаризации с параметрами подключения (SSH-ключ, пользователь).
- `playbook.yml` — основной плейбук Ansible.
- `index.html.j2` — Jinja2-шаблон веб-страницы с использованием переменных (`ansible_hostname`, `ansible_date_time`).

## Выполнение
Запуск плейбука осуществляется командой:
ansible-playbook -i inventory.ini playbook.yml 

## Результаты
Плейбук успешно выполнен без ошибок (failed=0).
Nginx установлен, запущен и добавлен в автозагрузку.
Веб-страница успешно отдается по HTTP.

## Доказательства (Скриншоты)

<img width="895" height="441" alt="image" src="https://github.com/user-attachments/assets/6399c8a2-30e5-49cd-8c71-8702913bc602" />

<img width="612" height="331" alt="image" src="https://github.com/user-attachments/assets/8fa1836a-5079-411f-b7e5-bccc6fc14cfb" />

<img width="634" height="302" alt="image" src="https://github.com/user-attachments/assets/27f88b6b-1a07-445e-b54a-c13cb815acdc" />
