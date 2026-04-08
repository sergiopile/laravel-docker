# Laravel Docker — ACL & Benchmarking

Aplicação Laravel 10 com sistema de tickets de suporte, autenticação completa e controle de acesso.

## Sobre

Projeto Laravel com Docker para estudo de ACL (Access Control List) e benchmarking. Inclui sistema de tickets de suporte com CRUD completo, autenticação via Laravel Breeze, gerenciamento de perfil e verificação de email.

## Funcionalidades

- **Autenticação completa:** registro, login, reset de senha, verificação de email (Laravel Breeze)
- **Sistema de tickets:** CRUD completo com status (Open, Closed, Pending) usando Enums tipados
- **Gerenciamento de perfil:** editar, atualizar e excluir conta
- **Dashboard protegido:** acesso com autenticação + verificação de email
- **ACL:** controle de acesso por níveis de permissão

## Stack

| Camada | Tecnologia |
|--------|-----------|
| Backend | Laravel 10, PHP 8.1+ |
| Frontend | Blade, Tailwind CSS, Alpine.js |
| Banco | MySQL |
| Build | Vite 5, Docker (Laravel Sail) |
| Testes | PHPUnit 10, Mockery, FakerPHP |

## Como rodar

```bash
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate
npm run dev          # Vite dev server
php artisan serve    # Laravel server
```

## Estrutura

```
app/
├── Models/          # User, Support
├── Http/Controllers/ # Auth, Profile, Support
├── Enums/           # SupportStatus (Open, Closed, Pending)
database/
├── migrations/      # Schema (users, support, etc.)
routes/
├── web.php          # Rotas web
├── auth.php         # Rotas de autenticação
resources/views/     # Templates Blade
```
