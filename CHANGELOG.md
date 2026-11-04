# Histórico de versões — Corrige Aí

Formato: [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) · versões em [SemVer](https://semver.org/lang/pt-BR/).
Versões `-rc.N` são de teste: saem como *pre-release* e só chegam a quem liga "Receber versões de teste" no app.
Cada versão tem o instalador, o `.sha256` e o `latest.yml` na página de [Releases](https://github.com/faustort/coai-instaladores/releases).

## [Não lançado]

### Novidades
- **Atualização automática:** o app baixa a versão nova sozinho e avisa "Atualização pronta para instalar". Ela é instalada quando você fecha o programa ou em Configurações › Atualizações › Reiniciar para atualizar.
- **GPT personalizado:** painel em três telas (configurar, corrigir, execução), com erros em português e previsão do lote; prévia da mensagem que será enviada, "Tentar de novo" por aluno, "Ver o que foi enviado" e "Ver parecer"; botão Parar.
- **Rubrica por gabarito:** modal "Conferir rubrica" na disciplina (gerar, editar, aprovar); o Gemini pode usar a rubrica aprovada no lugar do gabarito (opção desligada por padrão).

### Corrigido
- Uma rubrica aprovada não é mais sobrescrita pela extração automática.
- "Salvar alterações" e "Aprovar" funcionam também numa rubrica montada do zero.
- Em "uma conversa só", um trabalho que falha não contamina os seguintes.
- Tempo limite comum de resposta não pausa mais o lote por 6 horas; só o limite do provedor pausa.
- Trabalho preso em "em processamento" depois de Parar agora pode ser retomado.
- O diagnóstico não diz mais "deslogada" enquanto a página do Projeto ainda está carregando.

## [1.1.0-rc.3] — 2026-11-03 · versão de teste (pre-release)

Primeira versão publicada neste repositório, para testadores.

### Novidades
- **Meu jeito de corrigir:** tom, rigor e contexto por padrão geral ou por disciplina, instruções por modelo (Gemini, ChatGPT, DeepSeek), versões com diferenças em português e restaurar.
- **Conferir se a IA leu o roteiro** (2 etapas, opcional) no Gemini, ChatGPT e DeepSeek.
- **GPT personalizado:** opção de usar uma conversa só para o lote.
- **Modo oculto com sinal de vida:** etapa, relógio, pausa entre trabalhos e "Espiar" a página.
- **Limpar login** do portal e **Abrir no navegador** no menu do PDF.
- Relatório de saúde da IA em linguagem de professor.

### Corrigido
- O lote não morre mais no teto do lote; um erro em um trabalho vira "pulado" e o lote segue.
- Marcas de citação do Gemini/ChatGPT/DeepSeek são removidas antes de ler nota e parecer.
- A lista de trabalhos não fica mais desatualizada durante a leitura do portal.
- O prompt do Gemini não se contradiz mais com a Central.
