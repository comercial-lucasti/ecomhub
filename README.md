<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=130&color=0:2b2b2b,100:E0B101&section=header" alt="Banner EComHub" />

# EComHub

**Uma plataforma única que substitui várias ferramentas pagas na operação diária de vendas online.**
Etiquetas, expedição, fulfillment, devoluções, margem, estoque, reposição, alertas e IA, num só lugar e sem mensalidade de terceiros.

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

### Expedição

| Módulo | O que entrega |
|---|---|
| 🏷️ **Etiqueta Pronta · Mercado Livre** | Etiqueta + DANFE + faixa de SKU/quantidade em PDF no navegador, com **trava de segurança**: cada SKU é conferido com o pedido no ERP e o download só libera se tudo bater |
| 🏷️ **Etiqueta Pronta · TikTok Shop** | Mesmo fluxo para o TikTok Shop, incluindo o tratamento do DANFE |
| ⚡ **ZPL Turbo** | Converte etiquetas ZPL em PDF (térmica ou A4) direto no navegador, centenas de uma vez, remove repetidas |
| ✅ **Conferência de expedição** | Bipe por pacote: faltando, repetido, fora da coleta, com histórico |
| 🚚 **Contagem de despachos** | Quantos pedidos saem hoje por forma de envio, despachados × faltando, mensagem pronta para a equipe |
| ⏱️ **Pedidos atrasados e travados** | Destaca o que está perto de estourar o prazo e o que parou no meio do caminho (regras editáveis) |

### Fulfillment e devoluções

| Módulo | O que entrega |
|---|---|
| 📦 **Envios Full** | Checklist de cada envio para o fulfillment com fotos e vídeos por etapa, conferência SKU × quantidade, nota de remessa conferida no ERP e andamento em tempo real para a gestão |
| ↩️ **Conferência de devoluções** | Recebimento por SKU (bom, avariado, faltou), fotos obrigatórias organizadas por nota, estoque liberado × avariado sem lançamento duplicado |
| 📉 **Devoluções** | Taxa de devolução por SKU e por canal |

### Gestão

| Módulo | O que entrega |
|---|---|
| 💰 **Calculadora e margem por produto** | Margem real por canal com taxas por faixa de preço, frete e imposto; preço mínimo |
| 📦 **Estoque e reposição** | Ruptura, curva ABC e **quanto comprar**; gera as ordens de compra no ERP com prévia |
| 🔥 **Queima de estoque** | Produto parado, dinheiro parado e menor preço de promoção que ainda respeita a margem |
| 🧾 **Saúde do cadastro** | GTIN, peso e medidas, NCM, foto, descrição e custo: o que falta em cada produto |
| 📊 **Painel de vendas e meta** | Faturamento, pedidos, ticket e cancelamentos por canal; acompanhamento de meta (acesso restrito) |
| 🔔 **Notificações** | Alertas automáticos num espaço do Google Chat: resumo da manhã, atrasos, ruptura, compras atrasadas, pedido grande, fechamento do dia |
| 🤖 **Assistente de IA (texto)** | Rascunhos de anúncios e respostas a compradores a partir do cadastro do produto |

## Diferenciais

- **Custo baixo:** roda em infraestrutura Google, sem servidor próprio e sem assinatura de ferramentas de terceiros.
- **Privacidade por padrão:** PDFs e dados de clientes são processados **somente no navegador** de quem usa; nada disso passa pelo servidor.
- **IA com cuidado:** o assistente remove dados pessoais (CPF, CNPJ, e-mail, telefone, CEP) e informações de custo e fornecedor **antes** de qualquer envio, tem limite diário de uso e registro de consumo.
- **Rastreabilidade:** cada envio ao fulfillment e cada devolução guarda quem fez, quando, as fotos e os vídeos, para consultar meses depois.
- **À prova de erro na etiqueta:** a etiqueta só é liberada quando os produtos conferem com o pedido no ERP.
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
| Estoque e reposição | 512 verificações contra um cálculo independente, com testes de mutação (alterações deliberadas no código que os testes precisam detectar) |
| Etiquetas, ZPL e conferência de SKU | 45 verificações, incluindo listas com vários produtos no mesmo pacote |
| Envios Full, devoluções e contagem | 124 verificações, incluindo repetição segura de etapas (sem lançamento duplicado) |
| Painel, operação, compras, margem e notificações | 193 verificações |
| Assistente de IA | 30 verificações, incluindo a remoção de dados pessoais |

São **15 suítes e mais de 900 verificações** executadas a cada mudança.

## Tecnologias

Google Apps Script · JavaScript · HTML/CSS · Google Sheets · Google Drive · Google Chat · Google Sites · WebAssembly · Python (Google Colab) · APIs REST com OAuth 2 · LLMs via API

## Propriedade intelectual

O EComHub é software proprietário. **Todos os direitos reservados.** Não há licença de uso, cópia, modificação ou distribuição sem autorização escrita do autor (veja [LICENSE](LICENSE)).

## Contato

Interessado em uma demonstração ou em conversar sobre uma solução parecida para a sua operação? Fale comigo pelo [perfil](https://github.com/comercial-lucasti) ou pelo [LinkedIn](https://www.linkedin.com/in/comercial-lucas-t-i-0575013b3).
