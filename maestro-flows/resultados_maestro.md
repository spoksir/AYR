## 🛠️ Automação Maestro

Este documento descreve os três flows automatizados criados com **Maestro CLI** para a aplicação **AYR – Are You Ready?**. Para cada fluxo incluímos:

1. **Login - Flow**  
2. **Registo de Atividade - Flow**  
3. **Registo de Utilizador - Flow**  

---

### 1. Login - Flow

**Descrição e Resultados**  
Validar o fluxo completo de autenticação: onboarding → Skip → preenchimento de nr.Tlf + password → acesso ao menu principal.
Foi realizado com sucesso o flow.

:clapper:  [Resultado do fluxo em Vídeo](https://drive.google.com/file/d/1pFHPJTtZ8zzK9COZhKmIdonsuXbjBaaA/view?usp=drive_link)


**Descrição do Fluxo**  
```yaml
appId: com.ceiia.ayr
---

- launchApp:
    clearState: true

- waitForAnimationToEnd:
    timeout: 5000    

- assertVisible: "Value your"

- swipe:
    direction: left
    duration: 5000

- swipe:
    direction: left
    duration: 5000

- swipe:
    direction: left
    duration: 5000        

- tapOn:
    text: "SKIP"
    waitToSettleTimeoutMs: 500  

- tapOn:
    id: "com.ceiia.ayr:id/login_phone_til"

- inputText:
    text: "915451459"

- tapOn:
    id: "com.ceiia.ayr:id/login_password_til"   

- inputText:
    text: "Teste123*"    

- tapOn:
    text: "Next"   
    waitToSettleTimeoutMs: 5000        

- tapOn:
    text: "ACCEPT"
```

### 2. Registo de Atividade - Flow

**Descrição e Resultados**  
Validar o fluxo de registo de uma atividade: menu geral → escolher opção → iniciar percurso + finalizar percurso → sucesso.
Foi realizado com sucesso o flow sendo utilizado o comando "runFlow" para realizar o login com sucesso e seguir instruções para registo de atividade.

:clapper:  [Resultado do fluxo em Vídeo]()

**Descrição do Fluxo**  
```yaml
appId: com.ceiia.ayr
---
#- runFlow: login.yaml

- waitForAnimationToEnd:
    timeout: 10000    

- tapOn:
    id: "com.ceiia.ayr:id/action_iv"
    index: 0

- extendedWaitUntil:   
    visible: "Activity"
    timeout: 10000

- tapOn:
    id: "com.ceiia.ayr:id/start_activity_btn"

- extendedWaitUntil:  
    visible: "Stop"
    timeout: 20000

- tapOn:
    text: "Stop" 

- extendedWaitUntil:   
    visible: "End"
    timeout: 10000       

- tapOn:
    text: "End"     




```
### 3. Registo de Utilizador - Flow

**Descrição e Resultados**  
Validar o fluxo completo de registo de utilizador: onboarding → Skip → sign up + preenchimento dos campos → aceitar Terms & Conditions → Confirmação.
Foi automatizado parte do fluxo com sucesso mas não foi possível concluir devido à limitação de ser necessário registo com número de telefone e confirmação via SMS. Seria necessário explorar soluções

:clapper:  [Resultado do fluxo em Vídeo]()

**Descrição do Fluxo**  
```yaml
appId: com.ceiia.ayr
---

- launchApp:
    clearState: true

- waitForAnimationToEnd:
    timeout: 10000    

- assertVisible:
    id: "com.ceiia.ayr:id/videoView"

- swipe:
    direction: left
    duration: 5000

- swipe:
    direction: left
    duration: 5000

- swipe:
    direction: left
    duration: 5000        

- tapOn:
    text: "SKIP"
    waitToSettleTimeoutMs: 500  

- tapOn:
    id: "com.ceiia.ayr:id/sign_up_tv"
    waitToSettleTimeoutMs: 500

- tapOn:
    point: 50%,28%
    waitToSettleTimeoutMs: 500

- inputText:
    text: "Francisco"       

- tapOn:
    point: 50%,42%
    waitToSettleTimeoutMs: 500

- inputText:
    text: "Vieira"    

- tapOn:
    point: 50%,55%
    waitToSettleTimeoutMs: 500

- inputText:
    text: "franciscovieira88@gmail.com"   

- swipe:       
    direction: up

- assertVisible:
    id: "com.ceiia.ayr:id/next_btn"    
  
- tapOn:
    point: 67%,34%
    waitToSettleTimeoutMs: 500

- inputText:
    text: "915451459"   

- tapOn:
    point: 50%,53%
    waitToSettleTimeoutMs: 500

- inputText:
    text: "Teste123*" 

- tapOn:
    id: "com.ceiia.ayr:id/next_btn"
    waitToSettleTimeoutMs: 500  

- tapOn:
    point: "8%,59%"  

- tapOn:
    id: "com.ceiia.ayr:id/next_btn"        
   
- assertVisible: "There is already a user registered with this username. Please login."

- tapOn:
    id: "com.ceiia.ayr:id/btnNegative"
    waitToSettleTimeoutMs: 500




