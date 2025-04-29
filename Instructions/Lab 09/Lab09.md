# Lab 09: Erstellen eines autonomen Agents zum Nachverfolgen neuer Dateien, die in OneDrive erstellt wurden

**Einleitung**

OneDrive For Business einer Organisation hat mehrere Dateien darin
erstellt, und es ist für den Administrator schwierig geworden, den
Überblick zu behalten.

**Ziel**

Erstellen Sie einen autonomen Agenten, um die Details der neu
hinzugefügten Datei in den Dateidetails-Tracker einzugeben. Dadurch wird
das Problem der Nachverfolgung der hinzugefügten Dateien behoben, und
der Dateidetail-Tracker enthält die Details aller neu erstellten
Dateien.

## Übung 1: Einrichten der Umgebung

### Aufgabe 1: Einrichten von OneDrive

1.  Öffnen Sie einen Browser, und navigieren Sie zu +++. **Melden Sie
    sich** mit den Anmeldeinformationen auf der Registerkarte
    **Resources** an.

![](./media/image1.png)

2.  Wählen Sie **OneDrive** aus dem linken Menü aus.

![](./media/image2.png)

3.  Klicken Sie auf das +-Symbol oben links und wählen Sie **Files
    upload**.

![](./media/image3.png)

4.  Wählen Sie die Datei **details.xlsx** aus **C:\LabFiles aus und**
    wählen Sie **Open**.

![](./media/image4.png)

5.  Sobald die Datei hochgeladen wurde, wird eine Erfolgsmeldung im
    Fenster angezeigt.

![](./media/image5.png)

6.  Klicken Sie im linken Menü auf **My files** und Sie können sehen,
    dass die neue Datei dort verfügbar ist.

![](./media/image6.png)

### Aufgabe 2: Aktivieren der Copilot Studio-Testversion

1.  Öffnen Sie in einem neuen Tab
    +++[https://copilotstudio.microsoft.com/+++](https://copilotstudio.microsoft.com/**+++).

2.  Melden Sie sich mit den **Anmeldeinformationen** an, die auf der
    Registerkarte **Resources** Ihrer Lab-VM bereitgestellt werden.

![](./media/image1.png)

3.  Sobald Sie angemeldet sind, auf der Seite **Willkommen bei Microsoft
    Copilot Studio**, verlassen Sie das Land als **United States** und
    klicken Sie auf **Get started**.

![](./media/image7.png)

4.  Wählen Sie auf dem **Begrüßungsbildschirm** die Option Skip aus.

![](./media/image8.png)

## Übung 2: Erstellen und Testen eines autonomen Agents

### Aufgabe 1: Erstellen eines Agenten in Copilot Studio

1.  Klicken Sie auf die Option **Skip to configure** auf der sich
    öffnenden Seite zur Agentenerstellung.

![](./media/image9.png)

2.  Geben Sie im Bereich zur Agentenerstellung die folgenden Details ein
    und klicken Sie auf **Create**.

    - **Name** - +++New file tracker agent+++

    - **Description** - +++This agent will update the File details
      tracker placed in the OneDrive, each time a new file is created in
      the OneDrive+++

![](./media/image10.png)

### Aufgabe 2: Hinzufügen eines Triggers zum Agent

1.  Nachdem der Agent erstellt wurde, scrollen Sie nach unten, um den
    Abschnitt **Trigger** zu finden. Wählen Sie **+ add Trigger**
    aus**.**

![](./media/image11.png)

2.  Wählen Sie im Dialogfeld **Turn on generative orchestration to
    continue,** die Option **Turn it on** aus. Wir müssen diese Option
    auf ON setzen, um einen Auslöser hinzuzufügen.

![](./media/image12.png)

3.  Wählen Sie im Menü Add Trigger den Trigger **When a file is
    created** aus.

![](./media/image13.png)

4.  Wählen Sie im Bildschirm **Add** **Trigger** die Option Continue
    aus.

![](./media/image14.png)

5.  Beachten Sie, dass im nächsten Bildschirm der **Trigger
    name** ausgefüllt ist. Warten Sie, bis die **Verbindungen** zu
    **Microsoft Copilot Studio** und **OneDrive for Business**
    hergestellt sind (für jeden dieser Konnektoren wird ein grünes
    Häkchen angezeigt.).

Klicken Sie dann auf **Next**.

![](./media/image15.png)

6.  Wählen Sie die folgenden Details aus.

    - **Folder** – Root

    - **Include subfolders** – Yes

Lassen Sie die anderen Felder als Standard und wählen Sie **Create
trigger**.

![](./media/image16.png)

![](./media/image17.png)

7.  Nachdem der Trigger erstellt wurde, wird die Meldung **Time to test
    your trigger** angezeigt. **Schließen** Sie es. Wir werden den
    grundlegenden Ablauf des Triggers ein wenig optimieren, um die
    Funktionalität zu implementieren, und sie dann testen.

![](./media/image18.png)

> ![](./media/image19.png)

### Aufgabe 3: Hinzufügen von Logik zum Trigger

1.  Scrollen Sie auf der Seite **New file track agent** nach unten zum
    Abschnitt Auslöser.

2.  Klicken Sie auf die 3 Punkte neben dem Trigger **When a file is
    created**, und wählen Sie **Edit in Power Automate** aus.

![](./media/image20.png)

3.  Wählen Sie das **+**-Symbol zwischen **When the file is
    created** und **Sends a prompt action** und wählen Sie **Add an
    action** aus.

![](./media/image21.png)

4.  Suchen Sie nach +++add a row+++ und wählen Sie **Add a row into the
    table** aus.

![](./media/image22.png)

5.  Wählen Sie für jede Zeile die folgenden Werte aus und klicken Sie
    auf **Save**.

|                  |                                         |
|------------------|-----------------------------------------|
| Property         | Value                                   |
| Location         | OneDrive for Business                   |
| Document Library | OneDrive                                |
| File             | File details.xlsx                       |
| Table            | Table1                                  |
| Date Time Format | Serial Number                           |
| File ID          | Select the variable **File identifier** |
| File Name        | Select the variable **File name**       |
| File Path        | Select the variable **File path**       |

> ![](./media/image23.png)
>
> ![](./media/image24.png)

6.  Der Ablauf sieht nun wie im folgenden Screenshot aus.

![](./media/image25.png)

7.  Klicken Sie auf das Symbol **New designer toggle**.

![](./media/image26.png)

8.  Wählen Sie **Save draft** aus.

![](./media/image27.png)

9.  Wählen Sie **Publish** aus, um den Flow zu veröffentlichen.

![](./media/image28.png)

### Aufgabe 4: Veröffentlichen des Triggers

1.  Wählen Sie im Copilot Studio **Settings** aus.

![](./media/image29.png)

2.  Wählen Sie **Generative AI** -\> **Using generative AI in
    conversations**. Falls noch nicht ausgewählt, wählen Sie
    **Generativ** und klicken Sie dann auf **Save**.

![](./media/image30.png)

3.  Wählen Sie **Security** -\> **Authentication** -\> **No
    authentication** und klicken Sie dann auf **Save**.

![](./media/image31.png)

4.  Wählen Sie im Bestätigungsdialog **Save** aus.

![](./media/image32.png)

5.  Schließen Sie den Bereich Settings.

![](./media/image33.png)

6.  Wählen Sie nun **Publish** aus, um den Agenten zu veröffentlichen.

![](./media/image34.png)

7.  Wählen Sie im Bestätigungsdialog **Publish** aus.

![](./media/image35.png)

### Aufgabe 5: Testen des Triggers

1.  Navigieren Sie im Browser zurück zu **OneDrive**. Klicken Sie auf
    **+** und wählen Sie **Word-Dokument** aus.

![](./media/image36.png)

2.  Geben Sie dem Dokument einen **Namen**, und wählen Sie **Create**
    aus.

![](./media/image37.png)

3.  Klicken Sie auf **Close**, um die Datenschutzoption zu schließen.

![](./media/image38.png)

4.  Fügen Sie auf ähnliche Weise einige weitere Dateien hinzu.

5.  **Öffnen Sie** nun die **Datei details.xlsx** von OneDrive und
    beobachten Sie, dass die Details der erstellten Dateien zum Tracker
    hinzugefügt werden. **Hinweis**: Melden Sie sich mit Ihren
    Anmeldeinformationen auf der Registerkarte "Ressourcen" an, wie
    erforderlich.

![](./media/image39.png)

6.  Wenn die Datei in OneDrive erstellt wird, wird der Trigger
    aufgerufen, der wiederum den Flow ausführt, **When a file is
    added** und den Tracker aktualisiert.

7.  Sie können die Details des autonomen Agenten auch auf der
    Registerkarte "Aktivität" in Copilot Studio überprüfen.

**Zusammenfassung**

In diesem Lab haben wir gelernt, einen autonomen Agenten aus Copilot
Studio zu erstellen, zu veröffentlichen und zu testen.
