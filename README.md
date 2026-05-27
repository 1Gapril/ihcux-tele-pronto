# TelePronto - Prototipagem de Baixa Fidelidade (IHC & UX)

## 👥 Integrantes
* *Cauã Mendes* - RA: 326141078
* *Fábio Henrique Zanini Ferreira* - RA: 326113387
* *Gabriel Ferreira de Souza* - RA: 325140970
* *Lucas Henrique Miranda* - RA: 325131396
* *Curso:* Análise e Desenvolvimento de Sistemas (ADS)
* *Instituição:* Centro Universitário UNA – Belo Horizonte
* *Matéria:* Interação Humano Computador e UX
* *Professor:* Daniel Henrique Matos de Paiva

## 🩺 Sobre o Projeto
O **TelePronto** é um aplicativo de saúde desenvolvido para o Hospital Universitário com foco em telemedicina para casos leves. O objetivo principal do design é transmitir calma, confiança e extrema simplicidade, eliminando ruídos visuais para atender usuários fragilizados, doentes ou da terceira idade.

---

## 👁️ Análise de Acessibilidade
Para mitigar os problemas de usuários com **visão turva**, **mal-estar** ou **dedos trêmulos**, aplicamos as seguintes diretrizes de IHC:
* **Áreas de Clique Generosas (Targets):** Todos os botões interativos possuem altura mínima de 48px a 64px e espaçamento (padding) de no mínimo 24px entre eles, evitando que dedos trêmulos cliquem no botão errado.
* **Tipografia e Contraste:** Uso de fontes sem serifa em tamanhos ampliados (mínimo de 18px para textos informativos e 24px para botões). O layout prioriza o alto contraste básico para leitura sob qualquer condição de luz.
* **Navegação Linear:** Evitamos menus complexos, hambúrgueres ocultos ou gestos de "arrastar" (swipe). A navegação é estritamente vertical e baseada em toques diretos.

---

## 🚀 Fluxo Crítico: Consulta de Urgência
O caminho do usuário para iniciar o atendimento médico imediato foi reduzido ao menor número de passos possível:
1. **Passo 1 (Home):** O usuário visualiza o botão gigante `[🚨 CONSULTAR AGORA]` logo ao abrir o app e realiza o primeiro toque.
2. **Passo 2 (Triagem Rápida):** Uma tela limpa pergunta o sintoma principal. O usuário seleciona uma opção em formato de lista vertical e clica em `[AVANÇAR]`.
3. **Passo 3 (Sala de Espera):** O sistema direciona o usuário imediatamente para a fila virtual, exibindo de forma explícita o tempo estimado e a posição na fila.

---

## 🛡️ Prevenção de Erros
Doentes ou idosos podem derrubar o celular ou clicar na tela por reflexo. Para evitar que a consulta seja encerrada por acidente:
* **Barreira de Confirmação:** O botão de encerrar chamada `[❌ DESCONECTAR]` exige uma confirmação dupla. Ao ser clicado, o sistema abre um pop-up centralizado ocupando a tela com a mensagem: *"Você tem certeza que deseja encerrar a consulta?"* com as opções explícitas `[Sim, Sair]` e `[Não, Continuar]`.
* **Distanciamento de Comandos:** O botão de desligar fica isolado no topo da interface ou distante dos botões de controle cotidianos (como o botão de tirar o som ou ativar câmera).

---

## ✨ Desafios Extras Implementados
* **Fluxo de Dependente:** Na tela *Home*, há um seletor rápido no topo com a foto/nome do usuário ativo. Ao clicar, abre-se uma gaveta simples para alternar o perfil para o modo "Infantil (Filho/Dependente)", alterando o contexto das consultas do aplicativo.
* **Modo Baixa Conexão:** Caso a oscilação da internet seja detectada na Sala de Espera ou Chamada, uma tarja amarela de aviso no topo da tela informa de forma clara: *"Internet fraca. Desligando o vídeo para priorizar o áudio com o médico."* O sistema faz o downgrade técnico sem interromper a comunicação do paciente.
