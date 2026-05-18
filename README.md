
# 🚀 Sistema Automatizado de Alerta e Governança de Prazos

Este repositório contém a arquitetura da automação desenvolvida para garantir o cumprimento de prazos e o acompanhamento proativo de registros de um aplicativo corporativo, integrando o **Power Automate** e o **SharePoint**.

---

## 📊 Impacto de Negócio Registrado
* **Mitigação de Riscos:** Redução drástica na perda de prazos operacionais através de alertas preventivos diários.
* **Proatividade:** Substituição da checagem manual por um modelo de acompanhamento 100% ativo e automatizado.
* **Engajamento do Usuário:** Melhoria na experiência do usuário (UX), que passou a ter visibilidade clara das suas pendências diárias diretamente na caixa de entrada.

---

## 📄 O Desafio (Cenário Antigo)
Após a implantação de um aplicativo em **Power Apps (Canvas App)** para a gestão de demandas, os dados passaram a ser salvos de forma estruturada em listas do **SharePoint**. No entanto, o processo enfrentava um desafio de engajamento:
1. **Dependência de Ação Manual:** Não havia um mecanismo de alerta ativo. Para identificar quais registros estavam próximos do vencimento, o usuário precisava lembrar de acessar o aplicativo rotineiramente para consultar as datas de acompanhamento.
2. **Risco de Atrasos:** Em rotinas intensas, essa checagem manual deixava de ser priorizada, o que resultava em prazos perdidos e gargalos operacionais.

---

## 🛠️ A Solução Desenvolvida (Cenário Atual)
Para garantir a governança e a eficiência dos prazos, foi desenvolvida uma camada de automação em segundo plano utilizando o **Power Automate**:

### ⚙️ Arquitetura da Automação (Power Automate)
* **Gatilho de Recorrência (Scheduled Cloud Flow):** O fluxo executa de forma 100% autônoma, configurado para disparar todos os dias, pontualmente às **10:00 AM**.
* **Integração e Filtragem de Dados:** O fluxo realiza uma consulta na base de dados do **SharePoint**, aplicando filtros para identificar os registros com datas de acompanhamento críticas para o período.
* **Notificação Direta:** O sistema consolida as informações essenciais da pendência e dispara um e-mail de alerta diretamente para o usuário responsável pela demanda.

---

## 📸 Demonstração Visual

### Arquitetura do Fluxo (Power Automate)
<img width="1174" height="364" alt="automate_notificacao" src="https://github.com/user-attachments/assets/7a9228d7-9d9a-42ec-905e-98ef2e878d6b" />


### Notificação de Alerta Recebida pelo Usuário
<img width="640" height="608" alt="alerta_prazo" src="https://github.com/user-attachments/assets/408d6278-bdf8-4e2c-b47c-57aa751197d6" />


---

## ⚡ Diferenciais Técnicos

* **Otimização de Performance:** Uso de queries eficientes para buscar no SharePoint apenas os dados estritamente necessários para o dia atual, evitando processamento desnecessário e lentidão.
* **Planejamento de UX:** O disparo às 10h da manhã foi estrategicamente planejado para coincidir com o momento em que os usuários já organizaram as primeiras demandas do dia e podem priorizar as pendências urgentes alertadas pelo fluxo.

---

## 📂 Arquivos do Repositório
O arquivo de exportação original do fluxo do Power Automate (`.zip`) está disponível na raiz deste repositório para fins de análise técnica da estrutura de blocos e conectores.
