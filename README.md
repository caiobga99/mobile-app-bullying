# 📱 Report Bullying

O **Report Bullying** é um aplicativo mobile desenvolvido com **React Native** e **Laravel** que permite aos usuários realizarem denúncias anônimas de bullying. As denúncias são processadas por uma API que utiliza o **ChatGPT** para analisar o relato e fornecer uma resposta automatizada de apoio e orientação.

---

## 🚀 Funcionalidades

- 📄 Envio de denúncias anônimas de bullying
- 🔒 Sistema de login e autenticação
- 🧠 Integração com a API do ChatGPT para respostas automatizadas
- 🗃️ Armazenamento seguro das denúncias no banco de dados
- 📬 Histórico de denúncias por usuário autenticado

---

## 🛠️ Tecnologias Utilizadas

### Backend
- [Laravel 10+](https://laravel.com/)
- [MariaDB](https://mariadb.org/)
- [Laravel Sanctum](https://laravel.com/docs/sanctum/) (para autenticação de API)
- Integração com OpenAI (ChatGPT)

### Frontend (Mobile)
- [React Native](https://reactnative.dev/)
- [Axios](https://axios-http.com/) para requisições HTTP
- [React Navigation](https://reactnavigation.org/)
- [AsyncStorage](https://react-native-async-storage.github.io/async-storage/) para login persistente

---

## ⚙️ Como Rodar o Projeto

### Pré-requisitos

- PHP >= 8.1
- Composer
- Node.js e npm
- Android Studio / Xcode (emulador ou dispositivo real)
- Laravel CLI (`laravel`)
- MariaDB ou MySQL
- Expo CLI (se estiver usando Expo)
- Conta na OpenAI com chave de API válida
- .ENV

---

### 📦 Backend (Laravel)

```bash
# 1. Clone o repositório
git clone https://github.com/seuusuario/report-bullying.git
cd report-bullying/backend

# 2. Instale as dependências
composer install

# 3. Copie o .env de exemplo e configure
cp .env.example .env

# 4. Configure suas variáveis de ambiente no .env:
# - DB_DATABASE
# - DB_USERNAME
# - DB_PASSWORD
# - OPENAI_API_KEY

# 5. Gere a chave da aplicação
php artisan key:generate

# 6. Rode as migrations
php artisan migrate

# 7. Inicie o servidor
php artisan serve

# 1. Navegue até a pasta do app mobile
cd ../mobile

# 2. Instale as dependências
npm install

# 3. Configure o arquivo de ambiente ou edite os endpoints no código (por ex. `BASE_URL` do backend)

# 4. Inicie o projeto com Expo ou React Native CLI
npm start
# Android
npm run android

# iOS (Mac apenas)
npm run ios
