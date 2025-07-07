# 실습 02 - Microsoft 365 Copilot 채팅에서 에이전트 만들기 및 구성하기

**목표**

이 실습에서는 설명 및 구성 탭을 사용하여 Copilot 에이전트를 만들고
구성합니다.

Copilot Studio Agent Builder를 사용하게 됩니다:

- • Copilot Studio Agent Builder의 설명 및 구성 탭을 사용하여 에이전트를
  만듭니다.

참고: **Describe** 탭의 사용 가능 여부는 [**geographic availability and
language
support**](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build)여부에
따라 달라집니다. **Describe** 탭이 해당 지역 또는 기본 언어에서 지원되지
않는 경우, **Configure** 탭을 통해 에이전트를 수동으로 빌드할 수
있습니다.

- 에이전트 지침, 지식 소스 및 시작 프롬프트를 맞춤 설정합니다.

- 에이전트를 테스트하고 편집합니다.

- 조직 내에서 에이전트를 관리하고 공유합니다.

**연습 1: 설명 탭을 사용하여 Copilot 에이전트 만들기**

이 연습에서는 Copilot Studio의 설명 탭을 사용하여 기본 에이전트를
만듭니다.

1.  Microsoft Edge 브라우저를 열고 다음 URL을 입력하세요:
    +++https://m365.cloud.microsoft+++ **Microsoft 365 Copilot 앱**(이전
    Office) 홈페이지로 이동합니다.

**참고**: 오른쪽 **Resources** 탭에 제공된 **Credentials**을 사용하여
로그인해야 합니다(메시지가 표시되면).

2.  **Copilot 채팅** 페이지가 열립니다.

3.  어떤 이유로든 " **Something went wrong** "라는 메시지가 나타나면 "
    **Try again** "를 두 번 클릭하여 Copilot 앱을
    엽니다.![](./media/image1.png)

참고: 이 실습을 실행할 때 Copilot Chat 사용자 인터페이스가 다르게 보일
수 있습니다(Microsoft에서 Microsoft Build-2025 이벤트의 일환으로 UI
변경과 함께 새로운 기능 및 업데이트된 기능을 출시했기
때문입니다). ![](./media/image2.png)

![](./media/image3.png)

4.  **Create an agent**를 클릭합니다.

![](./media/image4.png)

5.  Copilot Studio Agent Builder가 열립니다.

![](./media/image5.png)

6.  **Describe tab**에 에이전트의 목적에 대한 설명을 자연어 설명으로
    입력합니다.

이 연습에서는 ++ **An agent that assists users in finding popular
learning paths and modules from Microsoft**++를 입력합니다.

![](./media/image6.png)

7.  Submit을 클릭하여 초안 에이전트를 미리 봅니다.

8.  초기 구성이 설정된 초안 에이전트는 자동으로 저장됩니다. 자동 생성된
    필드를 검토하고 필요한 사항을 조정합니다. 이 연습에서는 자동 생성된
    필드를 그대로 사용합니다.
    ![](./media/image7.png)

9.  에이전트 이름을 확인하거나 제안하라는 메시지가 표시됩니다. 이
    연습에서는 이름을 **LearnAssist Buddy**로 지정합니다.

![](./media/image8.png)

![](./media/image9.png)

10. 이제 기본 정보를 사용하여 에이전트를 생성했습니다. 에이전트에 대한
    지침을 수정하고 필요한 조정을 수행하라는 메시지가 표시됩니다. 이
    연습에서는 기본 설정을 사용하여 생성 과정을 빠르게 진행합니다.

![](./media/image10.png)

**연습 2: 구성 탭을 사용하여 에이전트 세부 정보 구성하기**

이 연습에서는 에이전트 설정을 구성하여 에이전트의 동작을 세부적으로
조정합니다.

**참고:** 구성 탭에서 직접 에이전트를 생성하는 경우, 에이전트의 이름,
설명 및 용도를 정의해야 합니다.

1.  Agent Builder에서 Configure탭으로 전환합니다.

![](./media/image11.png)

응답 톤 및 상호작용 스타일을 포함한 상담원의 행동 설정을 구성할 수
있습니다. 이 연습에서는 기본 지침을
따르겠습니다.![](./media/image12.png)

2.  이제 에이전트가 사용할 지식 소스(예: 특정 SharePoint 사이트, 문서
    라이브러리, 웹사이트)를 설정합니다. 이 연습에서는 웹사이트를 지식
    소스로 사용하여 에이전트의 응답을 기반으로 삼습니다.

+++https://learn.microsoft.com/en-us/training+++을 입력하고 Enter를
누르세요.![](./media/image13.png)

![](./media/image14.png)

**참고**: 웹사이트 URL은 두 단계를 초과할 수 없습니다. 또한, URL을
추가하지 않고 웹 검색을 활성화하면 에이전트가 공개 웹사이트를
검색합니다.![](./media/image15.png)

3.  구성 변경 사항은 자동으로 저장됩니다.

![](./media/image16.png)

4.  이제 조직의 필요에 맞춰 사용자 지정 설정을 사용하여 에이전트 구성을
    완료했습니다. 이제 에이전트가 의도한 대로 작동하는지 확인하고 필요한
    조정을 수행해 보겠습니다.

**연습 3: 에이전트 테스트 및 편집하기**

이제 에이전트가 구성 설정에 따라 응답하는지 테스트합니다.

1.  이제 에이전트의 응답을 평가하기 위해 다음 프롬프트를 입력합니다.

++**List the popular learning paths and modules offered by
Microsoft**++.

![](./media/image17.png)

2\. 지식 소스로 사용된 URL에 있는 정보와 비교하여 응답을 확인할 수
있습니다.![](./media/image18.png)

2.  관련 없는 프롬프트를 입력하여 응답을 테스트할 수도 있습니다.

++**Help me with instructions for baking cakes**++

![](./media/image19.png)

에이전트는 “Avoid discussing topics unrelated to Microsoft learning
paths and modules”라는 지침에 따라 답변을 제공하지 않았습니다.

**참고**: 사례에 따라 기본 지침 세트가 다를 수 있습니다. 에이전트가
답변을 제공하지 않도록 지침이 올바르게 구성되었는지 확인하세요.

3.  필요에 따라 에이전트의 설정, 지침 또는 지식 출처를 편집하려면 '
    **Configure tab** 으로 돌아갑니다.

4.  만족스러우면 오른쪽 상단의 **Create**를 클릭하여 에이전트를
    게시합니다.

![](./media/image20.png)

![](./media/image21.png)

5.  LearnAssist Buddy 에이전트가 성공적으로 생성되었습니다.

![](./media/image22.png)

**연습 4: 에이전트 관리 및 공유합니다**

이제 조직 내에서 에이전트를 배포하고 접근성을 관리하게 됩니다.

1.  적절한 권한을 설정하여 특정 사용자나 그룹과 에이전트를 공유합니다.

![](./media/image23.png)

![](./media/image24.png)

2.  사용자 피드백과 성과 지표를 기반으로 반복적인 개선을 실시합니다.

**시도해보기:**

- 제품 세부 정보를 얻기 위해 에이전트 " Product Buddy"를 만듭니다\` \\

- 실습 0 - 실습 실행 준비"에서 만든 문서 라이브러리에 지식 소스를
  매핑합니다.

![](./media/image25.png)

![](./media/image26.png)

![](./media/image27.png)

![](./media/image28.png)

- 관련 제품 관련 프롬프트를 묻고 에이전트가 제대로 작동하는지
  테스트합니다.

**요약:**

이제 다양한 지식 소스와 명령어 집합에 매핑된 에이전트를 만들어서
에이전트로부터 예상한 응답을 얻는 작업이 완료되었습니다.
