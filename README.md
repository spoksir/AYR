# AYR
Manual Testing and automation with Maestro to Android App: AYR - Are You Ready?

  <br><br>
  <h1 align="center">Read me</h1>
    
    
<br><br>
## 📋Descrição 
  Este repositório foi criado para execução de testes manuais e automação com maestro num projeto de desafio técnico de teste à aplicação AYR.

<br><br>
## :mag: Ferramentas necessárias
- :arrow_right:  **AYR APK Version: 2.9.17**
- :arrow_right:  **Maestro CLI**
- :arrow_right:  **Android Studio**
- :arrow_right:  **Excell**
- :arrow_right:  **GIT**


<br><br>
## :wrench: Preparar o ambiente
- :large_blue_circle: Clonar o Repositório: git clone https://github.com/spoksir/AYR.git 
- :large_blue_circle: Passo 2
- :large_blue_circle: Passo 3


 <br><br>
## Executar
### Testes Manuais
- Abrir testes-manuais/Tests_Ceiia.xlsx
- Alternar entre as folhas "Casos_Teste", "Casos_Teste_Execução", "Bugs")
- Drive com os artefactos: https://drive.google.com/drive/folders/1bdqV82YO4NmQ3JfHOc30Tgzv6vvlz2ac?usp=drive_link

### Testes Automatizados
- maestro test maestro-flows/registo.yaml
- maestro test maestro-flows/login.yaml
- maestro test maestro-flows/registo_atividade.yaml

 <br><br>
## :books: Estrutura do repositório
```text
AYR/
├── maestro-flows/               # Automação em Maestro
│   ├── registo.yaml             # TC-1-CT-4 + TC-2-CT-1
│   ├── login.yaml               # TC-2-CT-1
│   └── registo_atividade.yaml   # TC-3-CT-2
│
├── testes-manuais/              # Testes manuais e artefactos
│   ├── TestsCeiia.xlsx          # Abas: CasosTeste, CasosTeste_Execução, Bugs
│   └── TestPlan.md              # Plano de Testes em Markdown
│
└── README.md                    # Visão geral, como executar e estrutura
```

<br><br>
## :wrench: Dúvidas ou ajuda sobre o projeto
- :large_blue_circle: https://www.linkedin.com/in/fmlvieira/
