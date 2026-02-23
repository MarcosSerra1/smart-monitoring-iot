# 🚀 Smart Monitoring System — Plataforma IoT com Django

Sistema de monitoramento inteligente que simula sensores, recebe dados via API, armazena telemetria e exibe informações em um dashboard.

O projeto foi desenvolvido para aprendizado e portfólio, seguindo uma arquitetura real usada em sistemas de automação e IoT, com suporte futuro para integração com ESP32.

---

# 💡 Por que este projeto foi criado

Este projeto foi desenvolvido para simular um ambiente real de monitoramento industrial e automação, permitindo estudar comunicação entre dispositivos e servidores antes da integração com hardware real.

---

# 🧠 Objetivo do Projeto

Simular um ambiente de monitoramento de sensores onde é possível:

* Receber dados de dispositivos
* Armazenar telemetria
* Visualizar informações em dashboard
* Criar histórico de medições
* Preparar a infraestrutura para dispositivos reais (ESP32)

---

# 🏗️ Arquitetura do Sistema

```
┌──────────────┐
│ Simulador    │
│ (ESP32 futuro)│
└──────┬───────┘
       ↓
┌──────────────┐
│ Django API   │
└──────┬───────┘
       ↓
┌──────────────┐
│ Banco Dados  │
└──────┬───────┘
       ↓
┌──────────────┐
│ Dashboard    │
└──────────────┘
```

O simulador envia dados HTTP para a API, que salva no banco e disponibiliza para visualização.

---

# 📦 Estrutura do Projeto

```
smart-monitoring-iot/
├─ backend/           # API Django
├─ simulator/         # Simulador de sensores em Python
├─ docs/              # Documentação do projeto
├─ docker-compose.yml
└─ README.md
```

---

# ⚙️ Tecnologias Utilizadas

### Backend

* Python
* Django
* Django REST Framework

### Banco de Dados

* PostgreSQL / SQLite

### Frontend

* HTML
* JavaScript (Fetch API)

### Infraestrutura

* Docker

### Simulação

* Requests

---

# 🔌 Funcionalidades

✅ Recebimento de dados via API REST
✅ Armazenamento de telemetria
✅ Dashboard com visualização de dados
✅ Simulação de sensores
✅ Estrutura preparada para ingestão de dados em tempo real e expansão para múltiplos dispositivos

---

# 🧪 Simulador de Sensores

O projeto inclui um simulador em Python que envia dados aleatórios para a API, simulando um dispositivo IoT.

Exemplo de dados enviados:

```
{
  "temperature": 27.5,
  "humidity": 60
}
```

---

# 📊 Dashboard

O dashboard permite visualizar:

* Última leitura
* Histórico de dados
* Atualização automática
* Visualização de telemetria

---

# 🗺️ Roadmap

* [ ] API de ingestão de dados
* [ ] Simulador de sensores
* [ ] Dashboard básico
* [ ] Sistema de alertas
* [ ] Status online/offline
* [ ] Gráficos avançados
* [ ] Integração com ESP32
* [ ] Deploy em nuvem
* [ ] Integração com MQTT

---

# 🚀 Como rodar o projeto

## 1️⃣ Clonar o repositório

```
git clone https://github.com/MarcosSerra1/smart-monitoring-iot.git
cd smart-monitoring-iot
```

---

## 2️⃣ Backend

```
cd backend
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

---

## 3️⃣ Rodar simulador

Em outro terminal:

```
cd simulator
pip install -r requirements.txt
python send_data.py
```

---

# 📡 Endpoint da API

## Receber dados do sensor

POST /api/sensor-data/

Body JSON:

```
{
  "temperature": 25.3,
  "humidity": 55
}
```

---

# 🔮 Integração futura com ESP32

Quando o ESP32 estiver disponível, basta substituir o simulador pelo dispositivo real enviando requisições HTTP para a API.

Nenhuma alteração estrutural será necessária.

---

# 📚 Aprendizados com o projeto

O projeto demonstra a capacidade de projetar sistemas de telemetria completos, integrando backend, simulação de dispositivos e visualização de dados em uma arquitetura escalável.

---

# 👨‍💻 Autor

Marcos Gusmão

Estudante de Eletromecânica com foco em sistemas embarcados, automação e desenvolvimento backend para integração entre hardware e software.

---

# 📜 Licença

Este projeto está sob a licença MIT.
