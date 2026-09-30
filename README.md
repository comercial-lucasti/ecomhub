<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:2b2b2b,100:E0B101&text=EComHub&fontColor=ffffff&fontSize=60&fontAlignY=38&desc=Central%20de%20opera%C3%A7%C3%A3o%20para%20e-commerce&descAlignY=62&descSize=20" alt="EComHub" />

**Uma plataforma única que substitui várias ferramentas pagas na operação diária de vendas online.**
Etiquetas, expedição, margem, estoque, reposição e IA, num só lugar e sem mensalidade de terceiros.

![Google Apps Script](https://img.shields.io/badge/Google%20Apps%20Script-2b2b2b?style=for-the-badge&logo=google&logoColor=E0B101)
![JavaScript](https://img.shields.io/badge/JavaScript-2b2b2b?style=for-the-badge&logo=javascript&logoColor=E0B101)
![Python](https://img.shields.io/badge/Python-2b2b2b?style=for-the-badge&logo=python&logoColor=E0B101)
![IA](https://img.shields.io/badge/IA%20Aplicada-E0B101?style=for-the-badge&labelColor=2b2b2b)
![Status](https://img.shields.io/badge/Em%20produ%C3%A7%C3%A3o-E0B101?style=for-the-badge&labelColor=2b2b2b)

</div>

---

> **Repositório de apresentação.** O código-fonte é **privado** e não é distribuído aqui. Esta página descreve o que a plataforma faz, como ela foi pensada e quais problemas ela resolve.

## O problema

Vender em vários marketplaces cria trabalho repetitivo e custo escondido: etiquetas montadas na mão, conferência de expedição em papel, planilhas de margem desatualizadas, ruptura de estoque e uma pilha de assinaturas de ferramentas que fazem cada uma só uma parte.

## A solução

O **EComHub** reúne essas rotinas em um único painel com login, conectado ao ERP da operação. Ele foi construído para **cortar custos recorrentes**, **reduzir erros de expedição** e **transformar dados soltos em decisão**, rodando inteiramente no ecossistema Google Workspace.

## Módulos

| Módulo | O que entrega |
|---|---|
| 🏷️ **Etiqueta Pronta · Mercado Livre** | Prepara as etiquetas de expedição em PDF diretamente no navegador do usuário |
| 🏷️ **Etiqueta Pronta · TikTok Shop** | Mesmo fluxo para o TikTok Shop, incluindo o tratamento do DANFE |
| ✅ **Conferência de expedição** | Confere o que sai de cada pedido e guarda o histórico das conferências |
| 💰 **Calculadora de margem** | Margem real por canal, com taxas configuráveis e ficha de custo por SKU |
| ⏱️ **Pedidos atrasados** | Lê os pedidos do ERP e destaca o que está perto de estourar o prazo de despacho, com atualização automática |
| 📊 **Relatório de meta** | Acompanhamento de metas, de acesso restrito a quem precisa ver |
| 📦 **Estoque e reposição** | Lê estoque, pedidos, kits e compras do ERP e sugere **quanto comprar**, com curva ABC |
| 🤖 **Assistente de IA (texto)** | Gera rascunhos de anúncios e respostas a compradores, usando o cadastro do produto |

## Diferenciais

- **Custo baixo:** roda em infraestrutura Google, sem servidor próprio e sem assinatura de ferramentas de terceiros.
- **Privacidade por padrão:** PDFs e dados de clientes são processados **somente no navegador** de quem usa; nada disso passa pelo servidor.
- **IA com cuidado:** o assistente remove dados pessoais (CPF, CNPJ, e-mail, telefone, CEP) e informações de custo e fornecedor **antes** de qualquer envio, tem limite diário de uso e registro de consumo.
- **Decisão, não só relatório:** a reposição calcula a quantidade sugerida de compra a partir do ritmo de vendas, do prazo, da segurança e das compras já em andamento.

## Segurança

| Camada | Como é tratada |
|---|---|
| Acesso | Login próprio, senhas armazenadas de forma criptografada e validade configurável por usuário |
| Sessão | Expira automaticamente, uma sessão ativa por usuário |
| Força bruta | Bloqueio temporário após tentativas seguidas erradas |
| Segredos | Chaves e tokens ficam fora do código, em armazenamento protegido da plataforma |
| Módulos sensíveis | O código de um módulo só é entregue depois do login correto |

## Qualidade

Os cálculos críticos são cobertos por testes automatizados:

| Área | Cobertura |
|---|---|
| Estoque e reposição | 509 verificações contra um cálculo independente, com testes de mutação (alterações deliberadas no código que os testes precisam detectar) |
| Assistente de IA | 28 verificações, incluindo a remoção de dados pessoais |

## Tecnologias

Google Apps Script · JavaScript · HTML/CSS · Google Sheets · Google Sites · Python (Google Colab) · APIs REST com OAuth 2 · LLMs via API

## Propriedade intelectual

O EComHub é software proprietário. **Todos os direitos reservados.** Não há licença de uso, cópia, modificação ou distribuição sem autorização escrita do autor (veja [LICENSE](LICENSE)).

## Contato

Interessado em uma demonstração ou em conversar sobre uma solução parecida para a sua operação? Fale comigo pelo [perfil](https://github.com/comercial-lucasti) ou pelo [LinkedIn](https://www.linkedin.com/in/comercial-lucas-t-i-0575013b3).
