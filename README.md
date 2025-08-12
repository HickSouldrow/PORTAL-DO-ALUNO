## Instalação Automática

Você pode configurar o projeto automaticamente com o script abaixo (Linux ou Git Bash no Windows):

#!/bin/bash
# =========================
# Script de Setup do Projeto Laravel
# =========================

Iniciando configuração do projeto Laravel

# 1. Clonar repositório
Clonando repositório
"git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git"
cd SEU_REPOSITORIO || exit

# 2. Instalar dependências PHP
Instalando dependências PHP
"composer install"

# 3. Instalar dependências Node.js
Instalando dependências Node.js
"npm install"

# 4. Copiar e configurar .env
Configurando arquivo .env
"cp .env.example .env"

# 5. Configuração de banco no .env
's/DB_DATABASE=.*/DB_DATABASE=alunos/' .env
's/DB_USERNAME=.*/DB_USERNAME=root/' .env
's/DB_PASSWORD=.*/DB_PASSWORD=/' .env


# 7. Criar migration da tabela alunos
Criando migration da tabela alunos
"php artisan make:migration create_alunos_table"
<img width="601" height="174" alt="image" src="https://github.com/user-attachments/assets/b823fc9f-f5f3-4dd9-92fe-30ca23d03000" />

# 8. Rodar migrations
Rodando migrations
"php artisan migrate" ou "php artisan migrate:fresh"
<img width="603" height="266" alt="image" src="https://github.com/user-attachments/assets/db214f7e-d600-4547-a3ca-9727f5e820cc" />

# 9. Rodar build front-end
Rodando npm run dev
"npm run dev"
<img width="368" height="283" alt="image" src="https://github.com/user-attachments/assets/6898f0ae-49f5-4f44-be76-b909935d6b49" />


# 10. Rodar servidor Laravel
Iniciando servidor Laravel
"php artisan serve"
<img width="680" height="245" alt="image" src="https://github.com/user-attachments/assets/e6e3b179-9e01-42b2-9893-961717ba0de9" />

