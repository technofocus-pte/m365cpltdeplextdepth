# Laboratório 6 - Amplie o Microsoft 365 Copilot Chat com um agente de RH criado usando o Microsoft Copilot Studio

**Objetivo**

Neste laboratório, você aprenderá a estender o Microsoft 365 Copilot
Chat com um Agente Declarativo criado no Microsoft Copilot Studio. Você
também aprenderá a adicionar uma ação personalizada ao agente criado.

Duração estimada – 45 minutos

## Exercício 1: Criando um ambiente Power Platform

Com a Power Platform, você pode criar diferentes ambientes e alternar
facilmente entre eles de acordo com suas necessidades. Um ambiente
armazena aplicativos, fluxos, dados, agentes, etc., e cada ambiente é
completamente isolado dos demais. Neste exercício, você criará um novo
ambiente dedicado no qual executará os exercícios e tarefas restantes.

1.  Abra um navegador e, usando suas credenciais de login na aba
    **Resources**, acesse
    [https://admin.powerplatform.com](https://admin.powerplatform.com/).

![](./media/image1.png)

2.  Selecione **Manage** e depois **+ New** em **Environments**.

![](./media/image2.png)

3.  Informe o Nome como +++ **Dev env** +++, selecione o **Type** como
    **Developer** e clique em **Next**. Selecione **Save** na tela **Add
    Dataverse**.

![](./media/image3.png)

![](./media/image4.png)

4.  O novo ambiente é criado e muda do estado **Preparing** para
    **Ready** quando estiver pronto.

![](./media/image5.png)

![](./media/image6.png)

## Exercício 2: Criando um agente para o Microsoft 365 Copilot Chat

Neste exercício, você criará um agente declarativo com o Microsoft
Copilot Studio e o hospedará no Microsoft 365 Copilot Chat.

1.  Faça login em <https://copilotstudio.microsoft.com/> usando as
    credenciais de login da aba **Resources**.

![](./media/image7.png)

2.  Selecione o ambiente **Dev env** que criamos no exercício anterior.

![](./media/image8.png)

3.  Para criar um agente declarativo para o Microsoft 365 Copilot Chat,
    você precisa primeiro navegar pela lista de agentes no Copilot
    Studio e depois selecionar o agente com o nome **Microsoft 365
    Copilot**.

4.  Selecione **Agents** na barra de navegação à esquerda e selecione
    **Copilot for Microsoft 365** na lista.

![](./media/image9.png)

5.  Uma nova seção do Microsoft Copilot Studio será aberta. A partir
    daí, selecione o comando **+ Add** para criar um novo agente para o
    Microsoft 365 Copilot Chat.

![](./media/image10.png)

6.  O Copilot Studio pede que você descreva em linguagem natural qual é
    o propósito do agente. Você pode definir os requisitos do seu
    agente. Cole o prompt abaixo para fazer isso.

> **+++You are an agent helping employees to find information about HR
> policies and procedures, about how to improve their career, and about
> how to define learning pathways.+++**

![](./media/image11.png)

7.  Quando solicitado pelo Copilot Studio, atribua o nome "Agentic HR"
    ao seu agente personalizado. Use o seguinte prompt.

+++Name it as Agentic HR+++

![](./media/image12.png)

8.  Em seguida, instrua o Copilot Studio a ter tarefas ou metas
    específicas com as seguintes instruções:

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![](./media/image13.png)

9.  Em seguida, defina um tom profissional para seu agente, fornecendo
    as seguintes informações:

**+++It should have a professional tone+++**

![](./media/image14.png)

10. Quando terminar de descrever seu agente, selecione o comando
    **Create** para criar o agente real.

![](./media/image15.png)

<img src="./media/image16.png"
style="width:6.26806in;height:3.09583in" />

## Exercício 3: Publicando o agente no Microsoft 365 Copilot Chat

1.  Selecione **Publish** na página de visão geral do agente.

![](./media/image17.png)

2.  Selecione **Publish** na tela **Publish agent**.

![](./media/image18.png)

> ![](./media/image19.png)

3.  Selecione **Copy** em **Share link** para copiar o link e depois
    selecione **Done**.

![](./media/image20.png)

4.  Abra uma nova aba e cole a URL copiada. Selecione **Add** para
    adicionar o **Agentic HR** à sua lista de agentes.

![](./media/image21.png)

![](./media/image22.png)

5.  Selecione **Skip** na tela de introdução.

![](./media/image23.png)

6.  O agente **Agentic HR** foi adicionado.

![](./media/image24.png)

## Exercício 4: Criar um site do SharePoint

1.  Em um novo navegador, navegue até
    +++https://m365.cloud.microsoft/chat/+++ Selecione **Apps** no
    painel esquerdo e selecione **SharePoint** quando os aplicativos
    forem carregados.

> ![](./media/image25.png)

2.  Selecione **+ Create site** na página do SharePoint.

![](./media/image26.png)

3.  Selecione **Communication Site** na página **Select the site type**.

![](./media/image27.png)

4.  Selecione um **Modelo** a ser usado.

![](./media/image28.png)

5.  Selecione **Use template**.

![](./media/image29.png)

6.  Digite **+++Contoso site+++** como **Site name** e selecione
    **Next.**

![](./media/image30.png)

7.  Na próxima tela, selecione **Create site**.

![](./media/image31.png)

8.  Depois de criado, anote a **URL** deste site.

![](./media/image32.png)

9.  Selecione **Documents** na barra de menu. Selecione **Upload -\>
    Files.**

![](./media/image33.png)

10. Selecione o arquivo **Sample-list-of-candidates.xlsx** de
    **C:\LabFiles** para ser carregado.

![](./media/image34.png)

## Exercício 5: Adicionando uma ação ao agente

Neste exercício, você adicionará uma ação personalizada ao agente que
criou. No Microsoft Copilot Studio, ao criar agentes para o Microsoft
365 Copilot Chat, você pode adicionar quatro tipos diferentes de ações:

- New prompt: permite consumir uma ação de IA criada usando um prompt
  escrito em linguagem natural.

- New Power Automate flow: permite consumir um fluxo do Power Automate.

- New custom connector: permite consumir um conector personalizado do
  Power Platform.

- New REST API: permite consumir uma API REST externa.

1.  Para adicionar uma nova ação, selecione **+ Add action** na seção
    **Actions** do painel de configuração do agente.

![](./media/image35.png)

2.  Selecione a opção **List rows present in a table** (Excel online) e
    selecione **Next.**

![](./media/image36.png)

![](./media/image37.png)

3.  Na tela **List rows present in a table**, forneça os detalhes abaixo
    e selecione **Add action**.

Name - +++List HR candidates+++

Description – +++List candidates for HR role+++

![](./media/image38.png)

![](./media/image39.png)

4.  Depois que a ação for adicionada, clique nela para abri-la e
    editá-la.

![](./media/image40.png)

5.  Selecione a seção **Inputs**.

![](./media/image41.png)

6.  Selecione **Set as a value** em **How will the agent fill this
    input** para cada argumento de entrada.

![](./media/image42.png)

7.  Selecione **Confirm** na caixa de diálogo de alteração das
    configurações de entrada.

![](./media/image43.png)

![](./media/image44.png)

8.  Forneça os valores abaixo para cada entrada.

**Location** – A URL do site da Contoso que você salvou no exercício
anterior.

Biblioteca de documentos – +++ **Documentos** +++

File – +++**Sample-list-of-candidates.xlsx**+++

Table – +++**Candidates_Table**+++

![](./media/image45.png)

![](./media/image46.png)

![](./media/image47.png)

9.  Depois que todas as atualizações estiverem concluídas, selecione
    **Save**.

![](./media/image48.png)

![](./media/image49.png)

10. Selecione **Publish** para publicar o agente.

![](./media/image50.png)

11. Selecione **Publish** novamente.

![](./media/image51.png)

12. **Copy** a URL e **abra** em um navegador.

![](./media/image52.png)

13. Desta vez, aparecerá a opção **Update now,** já que a atualização já
    foi adicionada. Selecione-a.

![](./media/image53.png)

14. Selecione **Open** quando estiver atualizado.

![](./media/image54.png)

15. Na tela do agente Agentic HR, envie a mensagem abaixo.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image55.png)

16. Na mensagem Data to be shared with Agentic HR, selecione a opção
    **Allow once**.

![](./media/image56.png)

17. Se for solicitado que você faça login, selecione a opção **Sign in
    to Agentic HR** e depois selecione **Connect** na próxima tela.

![](./media/image57.png)

![](./media/image58.png)

18. Selecione **Submit** quando estiver conectado.

![](./media/image59.png)

![](./media/image60.png)

19. Agora, reenvie a mensagem abaixo ao agente.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image61.png)

20. Você receberá então a lista solicitada

![](./media/image62.png)

![](./media/image63.png)

## Resumo

Neste laboratório, você aprendeu com sucesso como usar conectores
personalizados no Copilot Studio.
