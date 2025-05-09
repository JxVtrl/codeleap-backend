# CodeLeap Backend

Backend do desafio fullstack da CodeLeap, feito com **Django** e **Django REST Framework**.  
Fornece uma API RESTful para gerenciar posts.

---

## 🧰 Tech Stack

- Python 3.8+
- Django 5+
- Django REST Framework
- django-cors-headers
- SQLite (padrão, pode ser trocado por outro banco)

---

## 🚀 Como rodar localmente

### 1. Clone o repositório

```bash
git clone https://github.com/Jxvtrl/codeleap-fullstack-test.git
cd codeleap-fullstack-test/backend
```

### 2. Crie o ambiente virtual

Linux/macOS:
```bash
python3 -m venv venv
source venv/bin/activate
```
Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```
Ou, se preferir instalar manualmente:
```bash
pip install django djangorestframework django-cors-headers
```

### 4. Rode as migrações

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Inicie o servidor de desenvolvimento

```bash
python manage.py runserver
```

O servidor estará disponível em:  
[http://127.0.0.1:8000/careers/](http://127.0.0.1:8000/careers/)

---

## 📡 Endpoints da API

| Método | Endpoint           | Descrição                |
|--------|--------------------|--------------------------|
| GET    | /careers/          | Listar todos os posts    |
| POST   | /careers/          | Criar um novo post       |
| PATCH  | /careers/<id>/     | Atualizar título/conteúdo|
| DELETE | /careers/<id>/     | Deletar um post          |

---

## 📦 Exemplos de payload

**Criar post (POST /careers/):**
```json
{
  "username": "joao",
  "title": "Meu post",
  "content": "Olá mundo!"
}
```

**Atualizar post (PATCH /careers/<id>/):**
```json
{
  "title": "Título atualizado",
  "content": "Conteúdo atualizado"
}
```

---

## ⚙️ CORS (para desenvolvimento)

Para permitir requisições do frontend, o CORS está liberado para todas as origens:

```python
# No settings.py
CORS_ALLOW_ALL_ORIGINS = True
```

