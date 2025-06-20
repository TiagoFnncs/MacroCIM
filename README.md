# Botão de Pânico Pessoal com Gatilho em Fone Bluetooth

Este repositório contém uma macro para o aplicativo **MacroDroid** que transforma um botão de mídia de um dispositivo Bluetooth (como um fone TWS) em um botão de pânico pessoal.

Quando acionada, a macro envia discretamente uma mensagem de ajuda e a sua localização atual para contatos pré-definidos.

## Funcionalidades

-   **Gatilho Discreto**: A macro é ativada com um único clique no botão de mídia do seu fone de ouvido.
-   **Condição de Segurança**: Só funciona se um dispositivo Bluetooth específico (nomeado "TWS" no arquivo original) estiver conectado, evitando acionamentos acidentais.
-   **Alerta por SMS**: Envia uma mensagem de texto customizável para um contato de emergência.
-   **Compartilhamento de Localização**: Envia a sua localização GPS atual para um segundo contato via SMS.
-   **Confirmação Visual**: Exibe uma notificação "Toast" (um pequeno pop-up) na tela com a mensagem "Enviado!" para confirmar que a ação foi executada.

## Fluxo da Macro

1.  **Gatilho**: O usuário pressiona uma vez o botão de mídia.
2.  **Verificação**: A macro verifica se o dispositivo Bluetooth com o alias "TWS" está conectado.
3.  **Ação (se a condição for verdadeira)**:
    -   Exibe a notificação "Enviado!".
    -   Envia a mensagem de texto `Oi amiga, preciso de ajuda, não estou me sentindo bem em casa.` para o número `+5561985019452`.
    -   Compartilha a localização atual por SMS com o contato salvo como "Deborah Loiola".

## Pré-requisitos

-   O aplicativo [MacroDroid](https://play.google.com/store/apps/details?id=com.arlosoft.macrodroid) instalado em seu dispositivo Android.
-   Permissões de **SMS** e **Localização** concedidas ao MacroDroid.

## Como Usar

1.  Baixe o arquivo `CIM.macro` deste repositório.
2.  No MacroDroid, vá em `Macros > Botão de Adicionar (+) > Importar Macro`.
3.  Navegue até o local onde salvou o arquivo `CIM.macro` e selecione-o.
4.  A macro será importada. Agora você **PRECISA** configurá-la.

## Configuração Obrigatória

Para que a macro funcione para você, é essencial alterar as seguintes informações:

1.  **Alterar o Dispositivo Bluetooth**:
    -   Abra a macro "CIM".
    -   Clique na primeira condição, que é um `Se (If)`.
    -   Clique na `Restrição: Bluetooth Conectado (TWS)`.
    -   Selecione o seu próprio fone de ouvido ou dispositivo Bluetooth na lista.

2.  **Alterar os Contatos de Emergência**:
    -   Na seção `Então (Then)`, clique na ação `Enviar SMS`. Altere o número `+5561985019452` para o número do seu contato de confiança e personalize a mensagem de texto.
    -   Clique na ação `Compartilhar Localização`. Selecione um contato da sua agenda para quem a localização deve ser enviada.

3.  **Salvar**: Após fazer as alterações, salve a macro no botão de "check" ou "salvar" no canto inferior direito.

## Aviso

Este é um projeto pessoal e uma ferramenta de conveniência. **Não confie nele como seu único método de segurança ou comunicação em uma emergência.** O funcionamento correto depende de múltiplas variáveis, como o sinal de GPS, a rede da operadora, as permissões do Android e o estado do aplicativo MacroDroid. Teste a macro exaustivamente após a configuração.
