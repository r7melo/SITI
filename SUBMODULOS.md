# Uso de Submódulos no Projeto SITI

## O que são submódulos?

Submódulos são repositórios Git dentro de outro repositório.  
Eles permitem manter partes do projeto (ex: API e Web) separadas, mas integradas.

---

## Estrutura do Projeto

- `SITI/` (repositório principal)
  - `apps/api` → submódulo (SITI-API)
  - `apps/web` → submódulo (SITI-WEB)
  - `apps/db` → scripts do banco

---

## Clonando o projeto corretamente

```bash
git clone --recurse-submodules https://github.com/r7melo/SITI
```

Se já clonou sem submódulos:

```bash
git submodule update --init --recursive
```

---

## Atualizando o projeto

### Atualizar tudo

```bash
git pull --recurse-submodules
```

Usa exatamente os commits definidos no projeto principal

---

### Atualizar submódulos para versões mais recentes

```bash
git submodule update --remote --recursive
```

Puxa a versão mais nova das branches dos submódulos

OBS: pode quebrar o sistema

---

## Fluxo recomendado

1. Atualize o submódulo manualmente:

    ```bash
    cd apps/api
    git pull origin main
    ```

2. Volte para o projeto principal:

    ```bash
    cd ../..
    git add apps/api
    git commit -m "update api version"
    ```

Agora a versão do submódulo está controlada

---

## Boas práticas

- Não use `--remote` em produção automaticamente
- Sempre versione mudanças de submódulos
- Evite alterações diretas sem commit no repo principal

---

## Pergunta para refletir

Você quer:
- estabilidade → use versões travadas (fluxo recomendado para os devs)
- atualização constante → use `--remote`

