# API-de-competição-de-crossfit-DIO
API-de-competi-o-de-crossfit-chamada-WorkoutAPI

# 🏋️ WorkoutAPI

Uma API de competição de Crossfit desenvolvida com **FastAPI**, unindo duas paixões: codar e treinar.  
Este projeto é simples, didático e serve como base para estudos de modelagem de dados, APIs REST e boas práticas com FastAPI.

---

## 🚀 Funcionalidades

- Cadastro de atletas
- Filtro por nome e CPF (Query Parameters)
- Relacionamento com centro de treinamento e categoria
- Customização de response
- Tratamento de exceção de CPF duplicado (IntegrityError)
- Paginação com `fastapi-pagination`

---

## 🧱 Estrutura de diretórios

```
.
├── main.py
├── models.py
├── crud.py
├── schemas.py
├── database.py
├── routers/
│   └── atleta.py
```

---

## 🛠️ Requisitos

- Python 3.9+
- Pip

Instale as dependências com:

```bash
pip install fastapi[all] sqlalchemy fastapi-pagination
```

---

## ▶️ Como rodar a API

1. Clone este repositório:

```bash
git clone https://github.com/lucianosaints/API-de-competi-o-de-crossfit-chamada-WorkoutAPI.git
cd API-de-competi-o-de-crossfit-chamada-WorkoutAPI
```

2. Rode a aplicação localmente:

```bash
uvicorn main:app --reload
```

3. Acesse a documentação:

- Swagger: [http://localhost:8000/docs](http://localhost:8000/docs)
- Redoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

---

## 🧪 Exemplos de uso

### POST /atletas

```json
{
  "nome": "João Silva",
  "cpf": "12345678900",
  "centro_id": 1,
  "categoria_id": 2
}
```

### GET /atletas?nome=joao&cpf=12345678900

Retorna atletas filtrados por nome e CPF com:

- nome
- centro_treinamento
- categoria

---

## ⚠️ Observações

- Ao cadastrar um atleta com CPF duplicado, a API retorna:
  - `status_code`: 303
  - `detail`: "Já existe um atleta cadastrado com o cpf: x"

---

## 📌 Autor

Desenvolvido por **Luciano Saints**  
Feito com ❤️, código e muito treino.
