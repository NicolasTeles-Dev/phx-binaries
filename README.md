# 📦 PHX Binaries

Repositório oficial que armazena os **binários compilados do PHP** usados pelo **PHX**, incluindo metadados, checksums e estrutura de distribuição via CDN.

Este repositório funciona como a "fonte de verdade" para instalação das versões disponíveis através do comando:

```bash
phx install <versão>
```

Assim, o PHX consegue baixar rapidamente o pacote já preparado, validar o SHA256 e extrair para uso imediato.

---

## 📁 Estrutura do Repositório

* **`versions.json`** — Arquivo central com:

  * versão
  * link para download
  * checksum SHA256
  * metadados adicionais

* **`/builds/`** *(opcional futuramente)* — diretório com artefatos gerados localmente ou para testes.

---

## ⚙️ Publicação dos Binários

Os binários disponibilizados aqui são gerados automaticamente pelo workflow do repositório **`phx`**, responsável por compilar e enviar cada pacote.

Após cada build:

1. O workflow faz upload do pacote `.tar.gz`
2. Atualiza o `versions.json`
3. A CDN do jsDelivr distribui o binário globalmente

Exemplo de acesso:

```
https://cdn.jsdelivr.net/gh/NicolasTeles-Dev/phx-binaries@main/versions.json
```

---

## 🤝 Contribuições

Você pode colaborar adicionando novas versões, ajustando metadados ou ampliando o suporte da estrutura. Sugestões úteis:

* Adicionar novas versões do PHP
* Aumentar suporte para ARM64, Alpine, musl
* Validar checksums
* Melhorar estrutura do `versions.json`
* Criar versões otimizadas com extensões adicionais

Pull Requests são bem-vindos.

---

## 🎯 Objetivo do Repositório

Manter uma base simples, rápida e confiável para distribuição dos binários PHP usados pelo **PHX**, facilitando o setup de ambientes PHP modernos em qualquer máquina.
