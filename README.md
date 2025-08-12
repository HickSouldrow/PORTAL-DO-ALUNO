## Instalação Automática

Você pode configurar o projeto automaticamente com o script abaixo (Linux ou Git Bash no Windows):

#!/bin/bash
# =========================
# Script de Setup do Projeto Laravel
# =========================

echo "Iniciando configuração do projeto Laravel..."

# 1. Clonar repositório
echo "Clonando repositório..."
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
cd SEU_REPOSITORIO || exit

# 2. Instalar dependências PHP
echo "Instalando dependências PHP..."
composer install

# 3. Instalar dependências Node.js
echo "Instalando dependências Node.js..."
npm install

# 4. Copiar e configurar .env
echo "Configurando arquivo .env..."
cp .env.example .env

# 5. Configuração de banco no .env
sed -i 's/DB_DATABASE=.*/DB_DATABASE=alunos/' .env
sed -i 's/DB_USERNAME=.*/DB_USERNAME=root/' .env
sed -i 's/DB_PASSWORD=.*/DB_PASSWORD=/' .env


# 7. Criar migration da tabela alunos
echo "Criando migration da tabela alunos..."
php artisan make:migration create_alunos_table
<img width="601" height="174" alt="image" src="https://github.com/user-attachments/assets/b823fc9f-f5f3-4dd9-92fe-30ca23d03000" />

# 8. Rodar migrations
echo "Rodando migrations..."
php artisan migrate ou php artisan migrate:fresh
<img width="603" height="266" alt="image" src="https://github.com/user-attachments/assets/db214f7e-d600-4547-a3ca-9727f5e820cc" />

# 9. Rodar build front-end
echo "Rodando npm run dev..."
npm run dev &
<img width="368" height="283" alt="image" src="https://github.com/user-attachments/assets/6898f0ae-49f5-4f44-be76-b909935d6b49" />


# 10. Rodar servidor Laravel
echo "Iniciando servidor Laravel..."
php artisan serve
<img width="680" height="245" alt="image" src="https://github.com/user-attachments/assets/e6e3b179-9e01-42b2-9893-961717ba0de9" />

