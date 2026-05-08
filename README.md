# Pipeline de Análise Automática de Campanhas — Google Ads

Automação de análise de performance de campanhas Google Ads usando LLM via API.
O script lê um CSV exportado do Google Ads, envia os dados para o Gemini e 
recebe um diagnóstico em linguagem natural com recomendações de ajuste de orçamento.
O relatório é salvo em .txt e enviado automaticamente por email.

## O que o script faz

1. Lê e trata o CSV exportado do Google Ads
2. Seleciona as colunas relevantes para análise
3. Monta um prompt com contexto de negócio
4. Envia os dados para o Gemini via API
5. Salva o relatório gerado em arquivo .txt
6. Envia o relatório por email automaticamente

## Tecnologias usadas

- Python
- Pandas
- Google Gemini API (google-genai)
- smtplib

## Como usar

1. Exporte o relatório de campanhas do Google Ads em CSV
2. Configure as variáveis no topo do script:
   - `GEMINI_API_KEY`: sua chave da API do Gemini (aistudio.google.com)
   - `NOME_CSV`: nome do arquivo exportado
   - `EMAIL_REMETENTE`, `EMAIL_SENHA`, `EMAIL_DESTINOS`: configurações de envio
3. Execute o script

## Configuração do email

O envio de email usa Gmail com senha de app.
Para gerar a senha de app: myaccount.google.com → Segurança → Senhas de app

## Exemplo de output

O script gera um relatório estruturado com:
- Campanhas recomendadas para aumento de orçamento
- Campanhas recomendadas para diminuição de orçamento  
- Campanhas para monitorar
- Conclusão geral com principais pontos de atenção# Automacao_com_IA
Pipelines de análises automáticas com LLM via API
