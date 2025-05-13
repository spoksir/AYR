# AYR
Manual Testing and automation with Maestro to Android App: AYR - Are You Ready?

  <br><br>
  <h1 align="center">Plano de Testes</h1>
    
---
**App Version:** 2.9.17  
**Test Plan Version:** 1  
**Data:** 2025-05-14  
---
    
<br><br>
## 📋Objetivo 
  Este Plano de Testes foi elaborado para definir o objetivo, o âmbito, a estratégia, o ambiente, os critérios de entrada e saída, bem como informações sobre os artefactos a entregar e o cronograma. O projeto baseia-se num desafio técnico baseado na aplicação AYR - Are You Ready?
Serão verificadas as funcionalidades da aplicação quanto ao nível funcional, como a fluidez do onboarding, o fluxo de autenticação, o registo de atividades e GPS, navegação entre menus, operações na Wallet e gestão de perfil. Será testada também quanto ao nível não funcional para responsividade das transições, usabilidade (legibilidade da UI e contraste).

<br><br>
## :mag: Âmbito dos Testes
- :arrow_right:  **Cenário de Teste 1** - App Onboarding (Splash scrrens, Vídeo, até ao Login)
- :arrow_right:  **Cenário de Teste 2** - Login (Registo, Login, Recuperação de Password, tentativas falhadas)
- :arrow_right:  **Cenário de Teste 3** - Actions (Registo de atividades em Bike, scooter, etc., autorização GPS, créditos)
- :arrow_right:  **Cenário de Teste 4** - Show me more (Secção About, e Legal, links para páginas exteriores relevantes)
- :arrow_right:  **Cenário de Teste 5** - Avoided CO2 (Verificação do total acumulado de CO2 evitado)
- :arrow_right:  **Cenário de Teste 6** - Wallet (AYR Dots/Credits, movimentos, detalhes)
- :arrow_right:  **Cenário de Teste 7** - Profile (Foto do perfil, persistência, alteração password)

<br><br>
## :wrench: Abordagem
- :large_blue_circle: Testes Manuais Exploratórios
- :large_blue_circle: Testes Manuais Estruturados
- :large_blue_circle: Automação com Maestro
  * Criação de conta
  * Login com uma conta existente
  * Registar uma atividade na app

 <br><br>
## Critérios de Entrada e Saída
### Critérios de Entrada
- Aplicação AYR disponível (versão instalada)
- Casos de teste definidos

### Critérios de Saída
- Todos os casos de teste executados (manuais e automatizados)
- Todos os defeitos identificados reportados e registados
- Resultados documentados (Excel, Maestro e README no Github)

 <br><br>
## :books: Entregáveis
  - README.md
  - Maestro registo.yaml
  - Maestro login.yaml
  - Maestro registo_atividade.yaml
  - Tests_Ceiia.xlsx
  - TestPlan.md

<br><br>
## 📝 Cronograma
| Fase                             | Data Início       | Data Fim           |
|----------------------------------|-------------------|--------------------|
| Criação do Test Plan             | 2025-05-12 18:00  | 2025-05-13 20:30   |
| Criação de Test Cases            | 2025-05-13 09:00  | 2025-05-13 15:00   |
| Execução dos Test Cases          | 2025-05-13 15:00  | 2025-05-14 18:00   |
| Reporte de Bugs                  | 2025-05-14 09:00  | 2025-05-14 12:00   |
| Automação em Maestro             | 2025-05-14 13:00  | 2025-05-14 18:00   |



