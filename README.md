# SITI


O **SITI** é o repositório central do projeto, responsável por organizar a estrutura, documentação e integração entre os diferentes módulos do sistema.

Ele funciona como o ponto de entrada para entendimento da arquitetura geral, coordenação do desenvolvimento e orquestrador central de entrega do projeto para um servidor de produção.

---

## Estrutura do Projeto

```text
SITI/
└──apps/
   ├── web/           # Subdiretório do repositório SITI-WEB
   ├── api/           # Subdiretório do repositório SITI-API
   └── db/            # Inicialização do MySQL via Docker
```
---

## Como Trabalhar no Projeto


### Clone o repositório do respectivo ao time de desenvolvimento

- FrontEnd

    ```bash
    git clone https://github.com/r7melo/SITI-WEB
    cd SITI-WEB
    ```

- BackEnd

    ```bash
    git clone https://github.com/r7melo/SITI-API
    cd SITI-API
    ```

---

## Organização do Projeto

O repositório está estruturado para separar claramente:

- Documentação e arquitetura
- Backend
- Frontend
- Banco de dados

Isso permite desenvolvimento independente entre as partes, mantendo integração centralizada.

---

## Documentação

Toda a documentação do sistema deve ser mantida na pasta:

```bash
/docs
```

---

## Observações

- Sempre mantenha os submódulos atualizados
- Evite alterações diretas fora do escopo de cada módulo
- Utilize boas práticas de versionamento

---
