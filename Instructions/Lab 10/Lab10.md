# 실습 10: 퀴즈 생성 에이전트 주제에 대한 즉각적인 조치 구현하기

**목표 :**

프롬프트 액션은 Microsoft Copilot을 확장하는 방법 중 하나입니다.
비즈니스별 자연어 액션을 생성하여 이를 구현합니다. 이러한 액션은 GPT
모델에 의해 해석되어 지시에 따라 필요한 액션을 수행합니다. 이러한 액션은
AI 플러그인 정의에 포함되어 있으며, Copilot은 일치하는 인텐트 또는
발화가 발견될 때 런타임에 이를 호출할 수 있습니다.

이 실습에서는 주어진 주제를 기반으로 퀴즈 문제를 생성하는 퀴즈 생성
주제에 대한 프롬프트 액션을 생성하는 방법을 학습합니다.

## 연습 1: 자연어를 사용하여 에이전트 만들기

1.  브라우저를 열고 +++<https://copilotstudio.microsoft.com/+++>에
    로그인하고, 해당 페이지에 아직 없다면 resources 탭의 자격 증명을
    사용하여 로그인합니다.

![](./media/image1.png)

2.  이미 Copilot Studio 페이지에 있는 경우 **Home**을 클릭하여
    홈페이지로 이동합니다.

![](./media/image2.png)

3.  홈페이지에서 '에이전트를 만들 설명' 아래의 텍스트 영역에 +++I want
    you to be a question and answering assistant that can answer common
    questions from users using the content of a website+++라고 입력하고
    **Send**를 클릭합니다.

![](./media/image3.png)

4.  에이전트의 이름을 제안할 수 있습니다. 제안된 이름을 수락하거나 직접
    이름을 입력합니다.

5.  아래와 같이 상담원의 기능에 대한 기타 세부 정보를 제공합니다.

> +++help answer common product and support questions using the content
> of a website, and help answer HR questions from an uploaded file+++

6.  지식 소스로 사용될 웹사이트 주소
    +++[www.microsoft.com+++](http://www.microsoft.com+++/)을
    제공합니다.

![](./media/image4.png)

7.  지시를 내리는 것이 끝나면 **Create** 를 클릭하여 에이전트를
    만듭니다.

![](./media/image5.png)

8.  에이전트가 생성되고 세부 정보가 표시됩니다. 페이지를 스크롤하여
    제공된 지침에 따라 에이전트가 생성되었는지 확인합니다.

![](./media/image6.png)

![](./media/image7.png)

9.  **Test**아이콘을 클릭하여 에이전트를 테스트합니다. +++ What is
    Copilot Studio?+++를 입력하고 **Enter** 를 누릅니다.

![](./media/image8.png)

10. +++What is the latest xbox model?+++를 입력합니다.

![](./media/image9.png)

> 위의 두 단계 모두에서 상담원은 일반적인 지식을 활용하여 일반적인
> 답변을 제공합니다.

## 연습 2: 생성 답변을 위한 주제에 대한 프롬프트 작업 만들기

작업은 에이전트의 기능을 확장하는 데 사용될 수 있습니다. Microsoft
Copilot Studio에서 에이전트에 여러 유형의 작업을 추가할 수 있습니다.:

- **Power Platform 커넥터를** 사용하여 Salesforce, Zendesk, MailChimp,
  GitHub와 같은 인기 엔터프라이즈 제품과 같은 다른 시스템의 데이터에
  액세스하는 사전 구축된 커넥터 작업.

- **사용자 지정 커넥터 작업:** 공개 또는 비공개 API의 데이터에
  액세스하도록 커넥터를 구축할 수 있습니다.

- **Power Automate 클라우드 플로우:** Power Automate 클라우드 플로우를
  사용하여 작업을 수행하고 데이터를 검색하고 작업합니다.

- **AI Builder 프롬프트:** AI Builder와 자연어 이해를 활용하여 비즈니스
  내 특정 시나리오 및 워크플로를 타겟팅합니다.

- **Bot Framework 스킬:** 스킬이 수행할 수 있는 작업(입력 및 출력
  매개변수, 스킬의 엔드포인트, 스킬의 디스패치 모델 포함)을 설명하는
  스킬 매니페스트를 사용합니다.

이 연습에서는 주제 노드에 작업 프롬프트를 추가하는 방법을 알아봅니다.

1.  에이전트에서 **Topics** 탭을 선택하고 **+ Add a topic** 를 선택한 후
    **From blank**를 선택합니다.

![](./media/image10.png)

2.  주제 이름을 +++ Generate questions for a quiz +++으로 입력합니다.
    트리거의 구문 아래에서 **Edit** 하이퍼링크를 선택합니다. 최소 5개의
    트리거 구문을 입력해야 합니다.

> 아래 구문을 하나씩 추가하세요. 각 구문을 추가하고 + 옵션을 선택하여
> 트리거를 추가하세요.
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
> 주제를 저장하려면 오른쪽 상단의 **Save**을 선택합니다.

![](./media/image11.png)

3.  트리거 노드 아래의 + 기호를 클릭합니다. **Add an action** 옵션을
    선택하고 그 **New prompt (default AI model)** 옵션을 선택합니다.

![](./media/image12.png)

![](./media/image13.png)

4.  프롬프트 대화 상자가 나타나고, 프롬프트 생성 방법을 안내하는
    플라이아웃이 나타날 수 있습니다. **Next**을 선택하여 가이드를
    살펴보세요.

5.  퀴즈 질문을 생성하는 프롬프트를 생성하겠습니다. 프롬프트 이름을 +++
    Quiz Generator +++로 입력합니다.

6.  아래 내용을 프롬프트 필드에 붙여넣습니다.

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++
>
> **Input** 섹션을 확장하고 **+ Add input**를 선택합니다.

![](./media/image14.png)

7.  **Add input** 옵션에서 **Text**를 선택합니다.

![](./media/image15.png)

8.  이름을 +++ number +++로 입력하고 ++++5+++와 같은 샘플 데이터를
    입력합니다. **+ Add input** -\> **Text**를 선택하여 다음 입력을
    추가합니다.

![](./media/image16.png)

9.  이름을 +++ topic +++로 입력하고 +++ Science +++과 같은 샘플 데이터를
    입력한 후 **+ Add input** -\> **Text**를 선택하여 다음 입력을
    추가합니다.

\![\](./media/image16.png)

11. 이름을 +++format+++로 입력하고 +++bullet points+++와 같은 샘플
    데이터를 입력합니다.

![](./media/image17.png)

12. 이제 입력 이름과 예제 데이터를 추가했습니다. 다음으로, 입력을
    프롬프트에 삽입해야 합니다. 프롬프트에서 **\[number\]**를 강조
    표시하고 **+ Add**를 선택한 후, 프롬프트에서 숫자를 선택합니다. 이제
    **number** 입력이 프롬프트에 입력으로 추가되었습니다.

![](./media/image18.png)

![](./media/image19.png)

13. 나머지 입력에 대해서도 같은 단계를 반복합니다.

14. 모든 입력을 프롬프트에 추가한 후, **Test prompt**를 클릭하고
    프롬프트 응답을 관찰합니다.

![](./media/image20.png)

15. **Save**을 선택하여 프롬프트를 저장합니다.

![](./media/image21.png)

16. 이제 주제의 작성 캔버스에 프롬프트 작업 노드가 나타납니다. 다음으로,
    에이전트가 입력할 수 있도록 입력 매개변수 값을 정의해야 합니다. \>
    아이콘을 선택합니다.

![](./media/image22.png)

17. **System** 탭을 선택하고 사용자의 전체 응답을 사용하고 형식 값을
    식별하기 위해 작업의 입력 값으로 **Activity.Text**를 선택합니다.

![](./media/image23.png)

18. 프롬프트 작업의 나머지 입력 매개변수에 대해서도 동일한 작업을
    반복합니다.

![](./media/image24.png)

19. 다음으로, 프롬프트 동작의 출력 변수를 정의해야 합니다. 이는 응답을
    토픽의 하위 항목에서 참조할 수 있도록 하기 위한 것입니다. \>
    아이콘을 선택하고 **Custom** 탭에서 **Create new**를 선택한 후 변수
    이름을 +++**VarQuizQuestionsResponse**+++로 지정합니다.

![](./media/image25.png)

![](./media/image26.png)

20. 프롬프트 작업 아래에서 + 아이콘을 선택하여 새 노드를 추가하고,
    **Send a message**를 선택합니다. **{x}** 변수 아이콘을 선택합니다.

![](./media/image27.png)

21. **VarQuizQuestionsResponse.text** 변수를 선택합니다. 이렇게 하면
    프롬프트 작업 응답의 text 속성이 메시지 보내기 노드에 추가됩니다.
    **Save**을 선택하여 주제를 저장합니다.

![](./media/image28.png)

22. 다음으로 주제 세부 정보를 업데이트해야 합니다. 생성 모드가
    활성화되면 에이전트가 주제를 사용자 의도와 연결하는 데 사용됩니다.
    **Details** 를 선택하고 다음을 입력하세요.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on
      the number of questions, the topic and format provided by the
      user+++

**Save**을 선택하여 주제를 저장합니다.

![](./media/image29.png)

23. 이제 에이전트가 프롬프트 동작으로 주제를 호출할 수 있도록
    **Generative mode**설정을 활성화해야 합니다. 에이전트의
    **Settings**을 선택하세요.

![](./media/image30.png)

> **Generative AI** 설정을 선택하고 **Generate (preview)**을 선택한 다음
> **Save**을 선택합니다.

![](./media/image31.png)

24. 24\. 생성 AI 설정을 선택하고 생성(미리 보기)을 선택한 다음 저장을
    선택합니다..

+++Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

> ![](./media/image32.png)
>
> ![](./media/image33.png)

**요약**

이 실습에서는 사용자 지정 프롬프트를 생성하고 테스트하여 주제에 대한
프롬프트 작업을 생성하는 방법을 학습했습니다.

m365cpltdeplextdepth/Instructions/Lab 10/Lab10.md at
m365cpltdeplextdepth-Dec2K24 · technofocus-pte/m365cpltdeplextdepth

 
