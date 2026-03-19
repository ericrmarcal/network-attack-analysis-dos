# 🛡️ Análise de Ataque à Rede: Inundação SYN (SYN Flood)

## 📝 Descrição
Este projeto detalha a investigação de uma interrupção de rede causada por um ataque de Negação de Serviço (DoS). O foco foi analisar como a exploração do "Three-way Handshake" do TCP pode esgotar os recursos de um servidor.

## 🔍 O que foi analisado:
* **Tipo de Ataque:** SYN Flooding.
* **Sintoma:** Erro de "Pausa na conexão" (Timeout) para usuários legítimos.
* **Identificação nos Logs:** Inundação de pacotes `SYN` vindos do IP `203.0.113.0` sem o correspondente pacote `ACK` final.



## ⚙️ Funcionamento Técnico (Exploração do Handshake)
O ataque interrompe o processo padrão de conexão:
1. **SYN:** O atacante envia a solicitação.
2. **SYN-ACK:** O servidor responde e reserva memória.
3. **Falta do ACK:** O atacante ignora a resposta, deixando a conexão "meio-aberta" até esgotar a memória do servidor.

## 🛡️ Medidas de Mitigação
No relatório, são discutidas formas de prevenir esse esgotamento, como o ajuste de timeouts de conexão e filtragem de IPs suspeitos.

## 📂 Documentação
* [Visualizar Análise Completa (PDF)](./Analisar-ataques-à-rede-de-computadores.pdf)
