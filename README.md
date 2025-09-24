# 🚚 Gerenciador para Transportadora

![PHP](https://img.shields.io/badge/PHP-8.1+-777BB4?logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-9.x-FF2D20?logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-5.7+-4479A1?logo=mysql&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)
![Tests](https://img.shields.io/badge/tests-PHPUnit-blue)
![Build](https://img.shields.io/badge/build-passing-brightgreen)

Sistema web de gerenciamento para uma transportadora, desenvolvido em **PHP (Laravel)**.  
Fornece cadastro de clientes, controle de pedidos/entregas, autenticação de usuários e estrutura pronta para testes.


---

## 🔎 Visão geral
Este repositório contém uma aplicação Laravel com rotas, controllers, models, migrações e testes básicos (PHPUnit). Destina-se a ser uma base para operações de uma transportadora: cadastro de clientes, pedidos e rastreamento básico.

---

## 🧰 Tecnologias
- PHP (Laravel)
- Composer (dependências PHP)
- MySQL / MariaDB (banco de dados)
- Node.js + NPM (assets)
- Laravel Mix / Webpack (build front-end)
- PHPUnit (testes)

---

## 🚀 Requisitos locais
- PHP 8.0+ (recomendado 8.1+)
- Composer
- MySQL / MariaDB
- Node.js + NPM
- Extensões PHP comuns: pdo, mbstring, openssl, tokenizer, xml, ctype, json

---

## 🛠️ Instalação e execução (modo rápido)

1. Clone ou copie o projeto:
```bash
   git clone <url-do-repositorio>
   cd transportadora
```
2. Instale dependências PHP:
```bash
    composer install
```
3. Instale dependências de front-end e compile assets:
```bash
    npm install
    npm run dev    # ou `npm run build` para produção
```
4. Copie o .env e ajuste as variáveis:
```bash
    cp .env.example .env
```
-  Configure *DB_DATABASE*, *DB_USERNAME*, *DB_PASSWORD* e outras chaves (mail, app url, etc).
-  Se houver um *.env.bak* no repo, verifique seu conteúdo antes de usar.
5. Gere a chave da aplicação:
```bash
php artisan key:generate
```
6. Crie as tabelas no banco:
```bash
    php artisan migrate
```
- Se houver seeders configurados:
```bash
    php artisan db:seed
```
7. (Opcional) Crie link para a pasta de storage:
```bash
    php artisan storage:link
```
8. (Opcional) Crie link para a pasta de storage:
```bash
    php artisan serve
```
Acesse *http://localhost:8000.*

---

## ✅ Testes

Execute os testes com:
```bash
    php artisan test
    # ou
    ./vendor/bin/phpunit
```

## 🧭 Estrutura principal do projeto

- **app/Models** — Models (Clientes, Pedidos, etc.)
- **app/Http/Controllers** — Controllers (lógica das rotas)
- **database/migrations** — Migrações de banco de dados
- **database/seeders** — Seeders (dados iniciais)
- **resources/views** — Views (Blade templates)
- **routes/web.php** — Rotas web
- **public/** — Arquivos públicos (CSS, JS, imagens)

## ⚠️ Dicas e solução de problemas comuns

- **Permissões:** se arquivos em *storage* ou *bootstrap/cache* precisarem de permissão:
```bash
    sudo chown -R $USER:www-data storage bootstrap/cache
    sudo chmod -R 775 storage bootstrap/cache
```

- **Composer memory error:** se faltar memória ao instalar dependências:
```bash
    COMPOSER_MEMORY_LIMIT=-1 composer install
```

- **Erro de conexão com DB:** verifique host, porta, usuário e se o banco está rodando.
- **Assets não aparecem:** rode npm run dev e limpe cache do browser; em produção use npm run build.

## 🔐 Segurança / Produção

- Nunca versionar seu *.env* contendo credenciais.
- Use HTTPS em produção e configure *APP_ENV=production* e *APP_DEBUG=false*.
- Faça backups regulares do banco de dados.

## 🤝 Contribuição

Contribuições são bem-vindas:

1. Fork do repositório
2. Crie uma branch (*feature/nova-funcionalidade*)
3. Faça commits claros
4. Abra um Pull Request descrevendo a mudança

## 📄 Licença

Este projeto está licenciado sob a **MIT License** — veja o arquivo LICENSE no repositório.


