# Crie um agente declarativo poético com o Microsoft 365 Agents Toolkit

**Objetivo**

Um agente declarativo é uma versão personalizada do Microsoft 365
Copilot que permite aos usuários criar experiências personalizadas
declarando instruções, ações e conhecimentos específicos. Este guia
fornece informações sobre como criar um agente declarativo usando o
Microsoft 365 Agents Toolkit (uma evolução do Teams Toolkit).

Neste laboratório, você criará um agente declarativo poético.

## Exercício 1: Criar um agente declarativo

Neste exercício, você começará criando um agente declarativo básico a
partir do Visual Studio Code.

1.  Na VM, abra o **Visual Studio Code**.

2.  Selecione **Extensions** no painel esquerdo e digite +++Microsoft
    365 Agents Toolkit+++

![](./media/image1.png)

3.  Selecione o **Microsoft 365 Agents Toolkit** e selecione **Install**
    para instalar a extensão.

![](./media/image2.png)

4.  Selecione **Declarative Agent**.

![](./media/image3.png)

5.  Selecione **No Action** para criar um agente declarativo básico.

![](./media/image4.png)

6.  Selecione **Default folder** para armazenar a pasta raiz do projeto
    no local padrão.

![](./media/image5.png)

7.  Digite +++My Agent+++ como **Application Name** e pressione
    **Enter**.

![](./media/image6.png)

8.  Na nova janela do Visual Studio Code que é aberta, selecione
    **Microsoft 365 Agents Toolkit**.

![](./media/image7.png)

9.  Selecione **Provision** no painel **Lifecycle** e selecione **Sign
    in** no pop-up exibido para entrar na conta do Microsoft 365.

![](./media/image8.png)

10. **Sign in** usando as credenciais da aba **Resources** e feche a
    janela quando terminar.

![](./media/image9.png)

11. Agora, a criação básica do agente declarativo está concluída.

### Tarefa 1: Teste o agente

Nesta tarefa, testaremos o agente declarativo que criamos.

1.  Navegue até o aplicativo Copilot com o URL
    <https://m365.cloud.microsoft/chat>.

2.  No canto superior esquerdo, **selecione o** **ícone da conversation
    drawer**.

> ![](./media/image10.png)

3.  Selecione o agente declarativo **My Agent**.

> ![](./media/image11.png)

4.  Insira uma pergunta +++Hello! How can you help me?+++ para o seu
    agente declarativo e certifique-se de que ele responda com "Thanks
    for using Microsoft 365 Agents Toolkit to create your declarative
    agent!"

> ![](./media/image12.png)
>
> Neste exercício, criamos um agente declarativo básico e testamos sua
> funcionalidade.

## Exercício 2: Adicionar instruções

Neste exercício, começaremos a adicionar instruções ao agente
declarativo que criamos no exercício anterior e aprimorá-lo

1.  No Visual Studio Code, abra o arquivo **appPackage
    /instructions.txt** e substitua seu conteúdo pelo texto a seguir.

> <span class="mark">Você é um agente declarativo e foi criado com o
> Microsoft 365 Agents Toolkit. Você é especialista em criar
> poemas.</span>
>
> <span class="mark">Sempre que um usuário fizer uma pergunta, você
> **deve** transformar a resposta em um poema. O poema não **deve** usar
> markdown de citação e deve usar texto normal.</span>
>
> ![](./media/image13.png)

O conteúdo deste arquivo é inserido na propriedade instructions no
manifesto do agente durante o provisionamento.

2.  Selecione **Provision** no painel **Lifecycle** do Kit de
    ferramentas de agentes.

![](./media/image14.png)

3.  Verifique se o **provisioning** foi concluído **com sucesso**. Você
    verá uma mensagem no canto inferior direito do Visual Studio Code.

> ![](./media/image15.png)

4.  O agente declarativo usará suas instruções atualizadas depois que
    você recarregar a página.

5.  Atualize a página de chat, selecione **My Agent** e digite +++Do we
    have chocolate in our food catalog?+++

![](./media/image16.png)

6.  Observe que o agente dá uma resposta poética.

![](./media/image17.png)

7.  Agora, adicione iniciadores de conversa ao agente.

8.  Abra o arquivo **appPackage/declarativeAgent.json** e logo após o nó
    de instruções, adicione uma **vírgula,** pressione Enter e cole o
    código abaixo.

"conversation_starters": \[

        {

            "title": "Getting Started",

            "text": "How can I get started with Agents Toolkit?"

        },

        {

            "title": "Getting Help",

            "text": "How can I get help with Agents Toolkit?"

        }

    \]

![](./media/image18.png)

9.  Selecione **Provision** no painel Ciclo de vida do **Microsoft 365
    Agents Toolkit** e certifique-se de que o provisionamento seja
    concluído com sucesso.

10. Os iniciadores de conversa atualizados estarão disponíveis no seu
    agente declarativo depois que você **atualizar** a página.

11. **Atualize** a página do chat para verificar o mesmo.

![](./media/image19.png)

## Exercício 3: Adicionar conteúdo da web

Neste exercício, você adicionará a capacidade do agente de pesquisar
conteúdo da web.

1.  Abra o arquivo **appPackage/declarativeAgent.json** e adicione o
    array capabilities com o seguinte conteúdo.

> "capabilities": \[
>
> {
>
> "name": "WebSearch"
>
> }
>
> \]
>
> ![](./media/image20.png)

2.  Selecione **Provision** no painel Ciclo de vida do **Microsoft 365
    Agents Toolkit** e certifique-se de que o provisionamento seja
    concluído com sucesso.

> ![](./media/image21.png)
>
> O agente declarativo terá acesso ao conteúdo da web para gerar suas
> respostas depois que você recarregar a página.

3.  Pergunte ao agente: +++How can I build a declarative agent?+++ e
    observe que o agente responde a partir da web.

> ![](./media/image22.png)

## Resumo

Você aprendeu a criar o agente declarativo para o Microsoft 365 Copilot.
Você também aprendeu a aprimorar o agente criado com instruções e
conteúdo da web, além de testá-lo em cada etapa.
