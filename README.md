# ATVi-Atlantis

## Requisitos

- Node.js: v24.11.1 ou superior
- TypeScript: 4.x (instalado via npx)
- JavaScript: ES2016 (target de compilação)

## Como Executar

### 1. Instalar Dependências

```bash
npm install
```

### 2. Compilar TypeScript para JavaScript

```bash
npx tsc
```

### 3. Executar o Projeto

```bash
node js/teste/index.js
```

## Como Testar

### Usando cURL

#### Listar clientes
```bash
curl -X GET http://localhost:3000/clientes
```

#### Criar novo cliente
```bash
curl -X POST http://localhost:3000/clientes \
  -H "Content-Type: application/json" \
  -d '{
    "nome": "Pedro Silva",
    "nomeSocial": "Pedro",
    "dataNascimento": "1990-01-15",
    "endereco": {
      "rua": "Rua das Flores",
      "bairro": "Centro",
      "cidade": "São Paulo",
      "estado": "SP",
      "pais": "Brasil",
      "codigoPostal": "01000-000"
    }
  }'
```

#### Buscar cliente por ID
```bash
curl -X GET http://localhost:3000/clientes/1
```

#### Atualizar cliente
```bash
curl -X PUT http://localhost:3000/clientes/1 \
  -H "Content-Type: application/json" \
  -d '{
    "nome": "Pedro Silva Santos",
    "nomeSocial": "Pedro Santos"
  }'
```

#### Deletar cliente
```bash
curl -X DELETE http://localhost:3000/clientes/1
```

### Usando Insomnia

#### GET - Listar Clientes
- Método: `GET`
- URL: `http://localhost:3000/clientes`

#### POST - Criar Cliente
- Método: `POST`
- URL: `http://localhost:3000/clientes`
- Body (JSON):
```json
{
  "nome": "Maria Santos",
  "nomeSocial": "Maria",
  "dataNascimento": "1985-05-20",
  "endereco": {
    "rua": "Av. Paulista",
    "bairro": "Bela Vista",
    "cidade": "São Paulo",
    "estado": "SP",
    "pais": "Brasil",
    "codigoPostal": "01310-000"
  }
}
```

#### GET - Buscar Cliente por ID
- Método: `GET`
- URL: `http://localhost:3000/clientes/1`

#### PUT - Atualizar Cliente
- Método: `PUT`
- URL: `http://localhost:3000/clientes/1`
- Body (JSON):
```json
{
  "nome": "Maria Santos Silva",
  "nomeSocial": "Maria Silva"
}
```

#### DELETE - Remover Cliente
- Método: `DELETE`
- URL: `http://localhost:3000/clientes/1`

## Estrutura do Projeto

```
atv1-atlantis/
├── enumeracoes/
├── interfaces/
├── modelos/
├── teste/
├── js/
├── package.json
├── tsconfig.json
└── README.md
```

