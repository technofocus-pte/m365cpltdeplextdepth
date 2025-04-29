# Lab 10: Implementieren einer Eingabeaufforderungsaktion für das Thema eines Quizgenerierungs-Agenten

## Übung 1: Verwenden natürlicher Sprache zum Erstellen eines Agenten

1.  Öffnen Sie einen Browser und melden Sie sich bei
    +++<https://copilotstudio.microsoft.com/+++> an und melden Sie sich
    mit den Anmeldeinformationen auf der Registerkarte "Ressourcen" an,
    wenn Sie sich noch nicht auf dieser Seite befinden.

![](./media/image1.png)

2.  Wenn Sie sich bereits auf der Copilot Studio-Seite befinden, klicken
    Sie auf **Home,** um zur Startseite zu gelangen.

![](./media/image2.png)

3.  Geben Sie auf der Startseite im Textbereich unter Beschreiben Sie
    Ihren Agenten, um ihn zu erstellen ein +++I want you to be a
    question and answering assistant that can answer common questions
    from users using the content of a website+++ und klicken Sie auf
    **Send**.

![](./media/image3.png)

4.  Möglicherweise wird ein Name für den Agent vorgeschlagen.
    Akzeptieren Sie es oder geben Sie Ihren eigenen Namen an.

5.  Geben Sie weitere Details zu den Funktionen des Agenten an, wie
    unten.

> +++help answer common product and support questions using the content
> of a website, and help answer HR questions from an uploaded file+++

6.  Geben Sie
    +++[www.microsoft.com+++](http://www.microsoft.com+++/) für die
    Website, die als Sknowledge-Quelle verwendet, wird an.

![](./media/image4.png)

7.  Wenn Sie mit den Anweisungen fertig sind, klicken Sie auf
    **Create,** um Ihren Agenten zu erstellen.

![](./media/image5.png)

8.  Der Agent wird erstellt und mit den Details geöffnet. Scrollen Sie
    durch die Seite, um zu verstehen, dass der Agent mit den Anweisungen
    erstellt wurde, die Sie dafür bereitgestellt haben.

![](./media/image6.png)

![](./media/image7.png)

9.  Klicken Sie auf das Symbol **Test**, um den Agenten zu testen. Geben
    Sie +++What is Copilot Studio+++ ein und drücken Sie **Enter**.

![](./media/image8.png)

10. Geben Sie +++What is the latest xbox model? +++ ein.

![](./media/image9.png)

Für die beiden oben genannten Schritte erhalten Sie vom Agenten eine
Antwort, die allgemein gehalten ist, da der Agent sein Allgemeinwissen
verwendet.

## Übung 2: Erstellen einer Eingabeaufforderungsaktion für ein Thema für generative Antworten

Aktionen können verwendet werden, um die Funktionen von Agenten zu
erweitern. Sie können Ihren Agenten in Microsoft Copilot Studio mehrere
Arten von Aktionen hinzufügen:

- **Prebuilt connector action**, die Power Platform-Konnektoren
  verwenden, um auf Daten aus anderen Systemen zuzugreifen, z. B.
  beliebte Unternehmensprodukte wie Salesforce, Zendesk, MailChimp und
  GitHub.

- **Custom connector action**, in der ein Konnektor für den Zugriff auf
  Daten von öffentlichen oder privaten APIs erstellt werden kann.

- **Power Automate cloud flow**, die Power Automate Cloud-Flows
  verwenden, um Aktionen auszuführen, Daten abzurufen und mit ihnen zu
  arbeiten.

- **AI Builder prompts**, die AI Builder und Natural Language
  Understanding verwenden, um die spezifischen Szenarien und
  Arbeitsabläufe in Ihrem Unternehmen zu adressieren.

- **Bot Framework skill**, die das Skillmanifest verwenden, das die
  Aktionen beschreibt, die der Skill ausführen kann, einschließlich
  seiner Eingabe- und Ausgabeparameter, der Endpunkte des Skills und der
  Dispatchmodelle für den Skill.

In dieser Übung erfahren Sie, wie Sie einem Themenknoten eine
Eingabeaufforderung zu einer Aktion hinzufügen.

1.  Wählen Sie in Ihrem Agent die Registerkarte **Topics** aus, wählen
    Sie **+ Add Topic** und wählen Sie **From a Blank**.

![](./media/image10.png)

2.  Geben Sie den Namen für das Thema wie folgt ein: +++Generate
    questions for a quiz+++. Wählen Sie den Hyperlink **Edit** unter
    Phrasen im Auslöser aus. Es müssen mindestens 5 Trigger-Phrasen
    eingegeben werden

> Fügen Sie die folgenden Phrasen nacheinander hinzu. Fügen Sie jede
> Phrase hinzu und wählen Sie die Option + aus, um den Auslöser
> hinzuzufügen.
>
> +++create a number of questions for a quiz based on a topic and format
> the quiz based on the instruction provided+++
>
> +++creates a quiz with a number of questions based on the topic
> provided and formats the quiz+++
>
> +++generate a quiz with a number of questions using the topic provide
> and format the questions+++
>
> +++creates questions for a quiz on a specific topic and format+++
>
> +++format a quiz by a number of questions based on the topic
> provided+++
>
> Wählen Sie oben rechts **Save** aus, um das Thema zu speichern.

![](./media/image11.png)

3.  Klicken Sie auf das +Symbol unterhalb des Trigger-Knotens. Wählen
    Sie die Schaltfläche **Add an action** und wählen Sie **New prompt
    (default AI model)** darunter aus.

![](./media/image12.png)

![](./media/image13.png)

4.  Das Dialogfeld Eingabeaufforderung wird angezeigt, und
    möglicherweise wird ein Flyout angezeigt, das Sie durch das
    Erstellen der Eingabeaufforderung führt. Wählen Sie **Next** aus, um
    den Guide zu durchlaufen.

5.  Wir erstellen eine Eingabeaufforderung, die Fragen für ein Quiz
    generiert. Geben Sie den Namen für die Eingabeaufforderung als
    +++Quiz Generator+++.

6.  Fügen Sie den folgenden Inhalt in das Eingabeaufforderungsfeld ein.

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++
>
> Erweitern Sie den Abschnitt **Input** und wählen Sie **+ Add input**.

![](./media/image14.png)

7.  Wählen Sie **Text** unter der Option **Add Input** aus.

![](./media/image15.png)

8.  Geben Sie den Namen als +++number+++ und geben Sie Beispieldaten
    ein, wie z.B. +++5+++. Wählen Sie **+ Add input** -\> **Text**, um
    die nächste Eingabe hinzuzufügen.

![](./media/image16.png)

9.  Geben Sie den Namen als +++topic+++ und geben Sie Beispieldaten ein,
    wie z.B. +++Science+++ und wählen Sie dann**+ Add
    input** -\> **Text**, um die nächste Eingabe hinzuzufügen.

\![\](./media/image16.png)

11. Geben Sie den Namen als +++format+++ und geben Sie Beispieldaten
    ein, wie z.B. +++bullet points+++

![](./media/image17.png)

12. Nachdem wir nun die Eingabenamen und Beispieldaten hinzugefügt
    haben. Als nächstes müssen die Eingaben in die Eingabeaufforderung
    eingefügt werden. Markieren Sie in der Eingabeaufforderung
    **\[numer\]** und wählen Sie **+ Add** und wählen Sie **number**
    unter **In your input** aus. Die Eingabe der Zahl wurde nun als
    Eingabe zur Eingabeaufforderung hinzugefügt.

![](./media/image18.png)

![](./media/image19.png)

13. Wiederholen Sie die gleichen Schritte für die verbleibenden
    Eingaben.

14. Sobald alle Eingaben zur Eingabeaufforderung hinzugefügt wurden,
    klicken Sie auf **Test Prompt** und beobachten Sie die
    Eingabeaufforderungsantwort.

![](./media/image20.png)

15. Wählen Sie **Save** aus, um die Eingabeaufforderung zu speichern.

![](./media/image21.png)

16. Der Knoten für die Eingabeaufforderungsaktion wird nun im
    Erstellungsbereich des Themas angezeigt. Als Nächstes müssen die
    Werte des Eingabeparameters definiert werden, damit der Agent sie
    ausfüllen kann. Wählen Sie das **Symbol \>**.

![](./media/image22.png)

17. Wählen Sie die Registerkarte **System** aus, und wählen Sie
    **Active.Text** als Eingabewert für die Aktion aus, um die gesamte
    Antwort des Benutzers zu verwenden und den Formatwert zu
    identifizieren.

![](./media/image23.png)

18. Wiederholen Sie dies für die verbleibenden Eingabeparameter der
    Eingabeaufforderungsaktion.

![](./media/image24.png)

19. Als nächstes müssen wir die Ausgabevariable der
    Eingabeaufforderungsaktion definieren. Auf diese Weise kann weiter
    unten im Thema auf die Antwort verwiesen werden. Wählen Sie das
    Symbol **\>** aus, und wählen Sie auf der Registerkarte **Custom**
    die Option **Create New** aus, und benennen Sie die Variable als
    +++**VarQuizQuestionsResponse**+++.

![](./media/image25.png)

![](./media/image26.png)

20. Wählen Sie unter der Eingabeaufforderungsaktion das +Symbol aus, um
    einen neuen Knoten hinzuzufügen, und wählen Sie **Send a message**
    aus. Wählen Sie das Variablensymbol **{x}** aus.

![](./media/image27.png)

21. Wählen Sie die Variable **VarQuizQuestionsResponse.text** aus.
    Dadurch wird die text-Eigenschaft der Antwort auf die
    Eingabeaufforderungsaktion dem Knoten "Nachricht senden"
    hinzugefügt. Wählen Sie **Save** aus, um Ihr Thema zu speichern.

![](./media/image28.png)

22. Als nächstes müssen die Themendetails aktualisiert werden, die von
    Ihrem Agenten verwendet werden, um das Thema mit der Absicht des
    Benutzers zu verknüpfen, wenn der generative Modus aktiviert ist.
    Wählen Sie **Details** und geben Sie Folgendes ein.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on
      the number of questions, the topic and format provided by the
      user+++

> Wählen Sie **Save** aus, um Ihr Thema zu speichern.

![](./media/image29.png)

23. Jetzt muss die Einstellung **Generativer Mode** aktiviert sein,
    damit der Agent das Thema mit der Eingabeaufforderungsaktion
    aufrufen kann. Wählen Sie **Settings** für Ihren Agenten aus.

![](./media/image30.png)

24. Wählen Sie die Einstellung **Generative AI** aus, und wählen Sie
    **Generate (Preview)** aus, gefolgt von **Save**.

![](./media/image31.png)

25. Jetzt sind wir bereit, den Agenten zu testen. Wählen Sie im
    Testbereich das **Refresh** aus. Geben Sie dann die folgende Frage
    ein und beobachten Sie die Ausgabe.

+++Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

> ![](./media/image32.png)

![](./media/image33.png)

**Zusammenfassung**

In diesem Lab haben wir gelernt, wie man eine Eingabeaufforderungsaktion
für ein Thema erstellt, indem man eine benutzerdefinierte
Eingabeaufforderung erstellt und testet.

