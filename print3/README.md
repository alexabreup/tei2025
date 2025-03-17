# Projeto Integrador: **Anjos da Guarda**

## Descrição do Projeto
O **Anjos da Guarda** é um sistema inovador de proteção contra o esquecimento de pessoas e animais em veículos automotivos. Utilizando uma combinação de sensores avançados, conectividade Wi-Fi/Bluetooth, GPS e inteligência artificial (IA), o projeto tem como objetivo prevenir tragédias causadas pelo esquecimento de crianças ou animais dentro de veículos, garantindo alertas em tempo real para cuidadores.

Este projeto foi desenvolvido como parte do **Projeto SAGA SENAI DE INOVAÇÃO**, seguindo critérios rigorosos de avaliação que abrangem desde a justificativa e objetivos até a viabilidade técnica e comercialização.

---

## Funcionalidades Principais
1. **Detecção Multissensorial**:
   - Sensores de peso, movimento e temperatura para confirmar a presença de pessoas ou animais.
   - Algoritmo de votação para reduzir falsos positivos (mínimo 2 sensores ativos).

2. **Alertas Inteligentes**:
   - Notificações push via aplicativo móvel (Blynk/Firebase).
   - Alarme sonoro e visual no veículo.
   - Localização GPS em tempo real.

3. **Processamento de IA**:
   - Modelo TensorFlow Lite para detecção de presença via câmera (opcional).
   - Análise de anomalias em dados de sensores.

4. **Conectividade Avançada**:
   - Wi-Fi e Bluetooth 5.0 para comunicação com dispositivos externos.
   - Integração com GPS para fornecer informações de localização.

5. **Economia de Energia**:
   - Modo deep sleep para operação prolongada em standby.
   - Bateria de backup (LiPo) com circuito de carga.

---

## Componentes Principais
- **Microcontrolador**: ESP32-S3 (processamento, Wi-Fi, Bluetooth, NPU para IA).
- **Sensores**:
  - Peso: Células de carga + amplificador HX711.
  - Movimento: Sensor radar RCWL-0516.
  - Temperatura/Umidade: DHT22 ou sensor digital I2C.
  - Câmera: Módulo OV2640 (opcional para visão computacional).
- **Módulos Adicionais**:
  - GPS NEO-6M para localização.
  - Buzzer e LEDs para alarme local.
  - Fonte de energia: Regulador de tensão 12V → 3.3V e bateria de backup.

---

## Arquitetura do Sistema
1. **Hardware**: Integração de sensores, módulos e microcontrolador.
2. **Firmware**: Leitura de sensores, processamento de dados e envio de alertas.
3. **Aplicativo Móvel**: Interface para notificações push, visualização de dados e histórico de alertas.
4. **Nuvem**: Armazenamento de dados e análise remota via Firebase.

---

## Etapas de Desenvolvimento
### Fase 1: Hardware (2 semanas)
- Montagem do protótipo com ESP32-S3, sensores e módulos.
- Configuração de células de carga (HX711) e sensor radar.
- Integração opcional da câmera OV2640.

### Fase 2: Firmware (3 semanas)
- Implementação de leitura de sensores (peso, movimento, temperatura).
- Calibração para evitar falsos positivos.
- Configuração de Wi-Fi/Bluetooth e integração com GPS.

### Fase 3: Aplicativo Móvel (2 semanas)
- Desenvolvimento de funcionalidades:
  - Notificações push (OneSignal/Firebase).
  - Visualização de dados em tempo real.
  - Histórico de alertas e localização GPS.

### Fase 4: Testes e Otimização (2 semanas)
- Testes de precisão dos sensores em diferentes cenários.
- Validação de consumo de energia (modo deep sleep).
- Ajustes no algoritmo de votação e modelo de IA.

---

## Cronograma
| Fase              | Duração   | Entregáveis                  |
|--------------------|-----------|------------------------------|
| Hardware          | 2 semanas | Protótipo funcional          |
| Firmware          | 3 semanas | Código base com sensores/alertas |
| Aplicativo        | 2 semanas | Versão beta do app           |
| Testes            | 2 semanas | Relatório de validação       |

---

## Orçamento Estimado
| Item                  | Custo (USD) |
|-----------------------|-------------|
| ESP32-S3             | 15,00       |
| Sensores             | 25,00       |
| Módulo GPS           | 10,00       |
| Câmera OV2640        | 12,00       |
| Componentes diversos | 20,00       |
| **Total**            | **82,00**   |

---

## Desafios e Mitigações
1. **Consumo de Energia**:
   - Uso de modo deep sleep e bateria de backup.
2. **Falsos Positivos**:
   - Combinação de sensores + algoritmo de votação.
3. **Processamento de IA**:
   - Uso de modelos leves (TensorFlow Lite Micro).

---

## Resultados Esperados
- Detecção de presença em veículos com **98% de precisão**.
- Envio de alertas em até **30 segundos** após a detecção.
- Operação por **7 dias em standby** com bateria de backup.

---

## Vantagens do ESP32-S3
- **NPU (Unidade de Processamento Neural)**: Eficiência em tarefas de IA/ML.
- **Maior Memória**: 512 KB RAM e opções de memória flash expandidas.
- **Conectividade Avançada**: Bluetooth 5.0, BLE e Wi-Fi eficiente.
- **Segurança Aprimorada**: Criptografia AES, SHA, RSA e secure boot.
- **Suporte a Câmera**: Interface nativa para visão computacional.

---

## Documentação
A documentação completa do projeto está disponível no arquivo `DOCUMENTACAO_PROJETO_INTEGRADOR.docx`, incluindo:
- Canvas do projeto.
- Esquemas e diagramas eletroeletrônicos.
- Trechos de código e lógica implementada.
- Referências bibliográficas no padrão ABNT.

---

## Contribuições
Este projeto foi desenvolvido por alunos do **SENAI** como parte do **Projeto SAGA de Inovação**. Contribuições são bem-vindas! Para colaborar, siga as etapas abaixo:
1. Faça um fork deste repositório.
2. Crie uma branch para sua contribuição: `git checkout -b feature/nome-da-feature`.
3. Envie um pull request detalhando suas alterações.

---

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).

---

## Contato
Para mais informações, entre em contato com o grupo de desenvolvimento:
- Email: [alexabreuper@gmail.com]
- Email: [luisgustavo.l.p@hotmail.com]
- Email: [alemaoalff71@gmail.com]
---