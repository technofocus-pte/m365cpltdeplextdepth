**실습 07: 직원 역량 강화 – Copilot – HR**

**목표:**

Microsoft 365용 Copilot HR 전문가를 통해 HR 전문가는 채용, 온보딩, 성과
관리, 직원 참여 및 규정 준수 관리와 같은 핵심 비즈니스 프로세스에서
워크플로를 간소화하고 생산성을 향상시킬 수 있습니다.

이 실습에서는 다음을 사용합니다.:

- Word의 Copilot을 사용하여 새 역할에 대한 작업 설명을 생성하기.

- Word의 Copilot을 사용하여 여러 이력서를 분석하고 각 후보자의 강점과
  약점을 비교하는 보고서를 제공하고, 가장 자격이 있는 후보자부터 가장
  적은 후보자까지 순위를 매기고, 추천하기.

- Loop의Copilot 를 사용하여 이 역할에 대한 후보자를 인터뷰하기 위한
  일련의 면접 질문을 생성하기.

**연습 #1: Word에서 Copilot을 사용하여 작업 설명 생성하기**

그래픽 디자인 인스티튜트(Graphic Design Institute)의 인사 관리자로서
새로운 선임 애니메이션 디자이너를 채용하기 시작했습니다. 직원이 이
역할에 대한 모든 직무를 간략하게 설명하는 문서를 생성했습니다. 이
연습에서는 Word에서 Copilot을 사용하여 이 문서의 역할 책임에 따라 작업
설명을 생성합니다.

1.  Microsoft Edge 브라우저에서 **Microsoft 365** 탭이 열려 있는 경우
    지금 선택하고, 그렇지 않으면 새 탭을 열고
    +++[https://www.office.com+++ URL을
    입력하여](https://www.office.com+++/) **Microsoft 365** 홈페이지로
    이동하세요.

**참고**: 오른쪽의 **Resources **탭 아래에 제공된 **Microsoft 365
Credentials **을 사용하여 로그인(메시지가 표시되는 경우) 해야 합니다.

2.  **Microsoft 365** 탐색 창에서 열기 위해 **OneDrive**를 선택하세요.

3.  **C:\LabFiles** 폴더로 이동하여 **Graphic Design Institute - Design
    Team** 문서를 선택하고 **OneDrive**에 업로드하세요.

**팁**: 파일을 열고 닫아 Most Recently Used (MRU) 파일 목록에
추가하세요.

![](./media/image1.png)

**참고**: **Preparing for the lab execution** 섹션에 제안된 대로 모든
실습 자산을 OneDrive에 이미 업로드한 경우 이 단계를 건너뛸 수 있습니다.

4.  Microsoft Edge 브라우저에서 Microsoft 365 탭이 열려 있는 경우 지금
    선택하세요. 그렇지 않으면 새 탭을 열고 다음 URL을
    입력하세요: +++[https://www.office.com+++](https://www.office.com+++/)

5.  **Microsoft 365** 홈페이지에서 **Microsoft Word**를 선택한 다음 빈
    문서를 여세요.

6.  **Draft with Copilot** 창에서 다음 프롬프트를 입력하지만 다음
    단계에서 책임 파일을 프롬프트에 연결할 때까지 **Generate** 버튼을
    선택하지 마세요:

+++I'm the HR Manager at the Graphic Design Institute. We've currently
started the hiring process for a new Senior Animation Designer. Please
review the attached document that outlines the job responsibilities for
this role and create a job description based on those
responsibilities.+++ 
![](./media/image2.png)

7.  이제 다운로드한 **Graphic Design Institute - Design Team
    Responsibilities.docx** 파일을 프롬프트에 첨부해야 합니다. **Draft
    with Copilot** 창에서 **Reference your content** 버튼을 선택하세요.
    나타나는 드롭다운 메뉴에서 **Graphic Design Institute - Design Team
    Responsibilities.docx** 파일이 파일 목록에 나타나면 해당 파일을
    선택하세요.

8.  **Browse files from cloud**를 선택하고 **Recent**  파일 목록에서
    파일을 선택한 후 **Attach** 버튼을 선택하세요. 파일이
    **Recent** 파일 목록에 표시되지 않으면 **Pick a file** 창의 탐색 창
    맨 위에 있는 **My files** 을 선택하고 파일을 저장한 폴더로 이동하고
    파일을 선택한 후 첨부를 선택하세요

![](./media/image3.png)

9.  프롬프트에 파일이 표시되는 방식을 확인하고 **Generate**를
    선택하세요.

![](./media/image4.png)

10. 직무 설명 문서의 첫 번째 초안을 검토하세요.

![](./media/image5.png)

11. 직무 책임 문서에 있는 많은 세부 정보가 포함되어 있지 않습니다. 대신
    각 책임에 대해 요약된 한두 문장을 제공하세요. 이 단점을 해결하려면
    다음 프롬프트를 입력하고 앞으로 화살표를 선택하세요:

+++While this job description draft is a good start, you failed to
include most of the details found in the job responsibilities document.
Please try again, and this time outline each responsibility area and
select the responsibilities required of a Senior Animation Designer.+++

![](./media/image6.png)

12. 두 번째 초안을 검토하세요.

![](./media/image7.png)

13. 다시 말하지만, Copilot이 더 많은 세부 정보를 제공해야 한다고
    생각합니다. 다음 프롬프트를 입력하여 더 구체적으로 지정할 수 있는지
    확인하세요:

+++This job description draft is better, but it still lacks the details
that I'm looking for. The job responsibilities document outlined
detailed responsibilities for each area. Include those details in this
job description. Be as specific as you can.+++

14. 결과를 검토한 후, "당신이 바라는 것을 조심하십시오"라는 속담이
    떠오를 것입니다.이 세 번째 초안의 책임 목록은 길다. 사실, 실행
    가능한 직무 설명 문서에는 너무 길었을 수 있습니다. 이 시점에서 이전
    초안을 검토하여 이전 초안이 이 긴 초안보다 더 나은지 확인하려고
    합니다. Copilot 창에서 프롬프트 필드 바로 위에 현재 버전의 문서
    초안을 확인합니다. 이 경우 초안 3/3에 있습니다. 이전 초안을
    검토하려면 뒤로 화살표(\<)를 선택하여 두 번째 초안과 첫 번째
    초안으로 돌아갑니다. 앞으로 화살표(\>)를 사용하여 최신 초안으로
    돌아가세요.

![](./media/image8.png)

이 경우 두 번째 초안으로 돌아갑니다. 책임 목록을 다시 검토합니다. 세
번째 초안의 목록만큼 광범위하지는 않지만 더 깔끔해 보이며 구직자가 이
선임 애니메이션 디자이너 역할에서 기대하는 바를 이해할 수 있는 충분한
정보를 제공하세요. 두 번째 초안이 최종 초안보다 더 낫다고 결정하여 이
초안을 사용하도록 선택하세요. Copilot 창에서 **Keep it** 버튼을
선택하세요.

15. 이 작업 설명 문서를 계속 진행할 준비가 되었으므로 **Graphic Design
    Institute - Job descriptions.docx** 파일 이름으로 OneDrive 계정에
    저장하세요.

![](./media/image9.png)

**참고:** 이 문서는 다음 연습에서 사용하게 되므로 이 문서를 저장하는
것이 중요합니다.

**연습 \#2: Word에서 Copilot을 사용하여 이력서를 분석하고 추천하기**

이전 연습에서는 Word의 Copilot이 HR 전문가가 직무 설명을 작성하는 데
어떻게 도움이 되는지 알아보았습니다. 이 연습에서는 이력서 심사
프로세스의 초기 단계를 자동화하여 대규모 지원자 풀에서 가장 적합한
후보자를 신속하게 식별하는 방법을 배웁니다.

**참고**: Copilot에 문서를 생성하거나 특정 유형의 변경 사항을 적용하도록
요청하면 초안이 표시되기 시작했다가 중지되는 경우가 있습니다. 이러한
상황이 발생하면 **Regenerate** 버튼을 선택하여 새 초안을 생성하도록
하거나 프롬프트를 바꿔 말하고 다시 시도하세요.

![](./media/image10.png)

그래픽Graphic Design Institute의 인사 관리자로서, 웹의 채용 공고와
회사의 내부 직원 웹사이트를 기반으로 새로운 시니어 애니메이션 디자이너
직책에 대한 예상 후보자로부터 이력서를 받기 시작했습니다. 이제 Word에서
Copilot을 사용하여 해당 역할에 대해 받은 이력서 묶음을 선별하고 면접에
적합한 후보자에 대한 추천을 제공합니다.

이전 연습의 끝에서 생성한 작업 설명 파일을 저장했습니다. 파일을
**Graphic Design Institute - Job descriptions.docx**로 저장하라는 지시를
받았습니다. 다른 파일 이름으로 저장된 경우 이 연습에서 파일을 찾을 수
있도록 사용한 이름을 기억하세요.

1.  Microsoft Edge 브라우저에서 **Microsoft 365** 탭이 열려 있는 경우
    지금 선택하고, 그렇지 않으면 새 탭을 열고 다음 URL을 입력하세요:
    +++[https://www.office.com+++](https://www.office.com+++/)

**참고**: 오른쪽의 **Resources **탭 아래에 제공된 **Microsoft 365
Credentials **을 사용하여 로그인 (메시지가 표시되는 경우)해야 합니다.

2.  **Microsoft 365** 탐색 창에서 열기 위해 **OneDrive**를 선택하세요.

3.  **C:\LabFiles** 폴더로 이동하여 다음 문서의 복사본을 선택하고
    OneDrive에 업로드하세요,

    - **Resume - Patti Fernandez**

    - **Resume - Nestor Wilke**

    - **Resume - Holly Dickson**

    - **Resume - Alex Wilber** .

**참고**: **Preparing for the lab execution**에 제안된 대로 모든 랩
자산을 OneDrive에 이미 업로드한 경우 이 단계를 건너뛸 수 있습니다.

4.  이 연습에서는Most Recently Used (MRU) 파일 목록에서 문서에
    액세스합니다. 파일을 MRU 목록에 표시하려면 각 문서를 연 후 닫으세요.
    OneDrive에서 4개의 이력서 파일을 각각 열고 닫으세요.

5.  **Microsoft 365** 탐색 창에서 **Microsoft Word**를 선택한 후 새 빈
    문서를 여세요.

6.  빈 문서의 맨 위에 표시되는 **Draft with Copilot**창에서 다음
    프롬프트를 입력하지만 아직 프롬프트를 제출하지 마세요. 다음 단계에서
    프롬프트에 파일을 첨부해야 합니다:

+++I'm the Hiring Manager for Graphic Design Institute. We're hiring for
the position of Senior Animation Designer. Please create a report that
compares the attached resumes to the requirements for a Senior Animation
Designer in the attached job description file and rank the candidates
from most qualified to least qualified. Thank you!+++

![](./media/image11.png)

7.  이제 이전 연습을 마칠 때 OneDrive 계정에 저장한 **Graphic Design
    Institute - Job descriptions.docx** 파일을 프롬프트에 첨부해야
    합니다. **Draft with Copilot** 창에서 **Reference your content**
    버튼을 선택하세요. 표시되는 드롭다운 메뉴에서 작업 설명 파일이 파일
    목록에 나타나면 선택하세요. 그렇지 않으면 **Browse files from
    cloud**를 선택하세요

8.  다운로드한 4개의 이력서 각각에 대해 이전 단계를 반복하세요. 세 번째
    이력서를 첨부하려고 할 때 어떤 일이 발생하는지 확인하세요. Copilot은
    프롬프트에 최대 3개의 파일만 포함할 수 있음을 나타내는 메시지를
    표시합니다. Copilot에 작업 요구 사항을 제공하는 작업 설명 파일을
    포함해야 했기 때문에 이 초기 프롬프트로 이력서 중 두 개만 제출할 수
    있습니다.

![](./media/image12.png)

9.  작업 설명 파일과 처음 두 개의 이력서를 프롬프트에 첨부했으므로
    **Generate**을 선택하세요. 이 시점에서 Copilot은 작업 설명 파일에서
    관련 정보를 추출하고 처음 두 개는 이력서를 작성하고 이력서 비교
    보고서를 생성하세요. 이 시점에서 Copilot 드래프트 모드에 있습니다.

10. 이 첫 번째 초안의 결과를 검토하세요.

![](./media/image13.png)

**참고**: **Draft with Copilot** 창을 살펴보고 **Attach** 버튼이
포함되어 있지 않습니다. 현재와 같이 초안 모드에 있으면 Copilot은 후속
프롬프트에 더 이상 파일을 첨부할 수 없습니다. 프롬프트 필드를 사용하여
문서를 수정할 수 있지만 더 이상 다른 파일을 첨부할 수 없습니다. 다음
단계를 진행할 때 이 요구 사항을 염두에 두세요. 이 현재 초안은 처음 두
이력서만 비교합니다. 나머지 두 개의 이력서를 현재 초안에 있는 두 개의
이력서와 비교하려면 이 보고서의 초안을 유지한 후 나머지 두 개의 이력서를
방금 생성한 문서와 비교하는 두 번째 보고서를 생성해야 합니다.

11. 이제 처음 두 이력서를 직무 설명 파일과 비교하는 보고서의 첫 번째
    초안을 보고 있습니다. Copilot은 원하는 초안을 찾을 때까지 원하는
    만큼 초안을 재생성할 수 있는 기능을 제공합니다. 이 첫 번째 초안이
    괜찮아 보인다고 생각되더라도 Copilot이 두 번째 초안을 생성하도록
    하려면 **Draft with Copilot** 창에서 **Regenerate** 버튼을
    선택하세요.

![](./media/image14.png)

12. 다시 생성할 때 "문제가 발생했습니다" 오류 메시지가 나타날 수
    있습니다. 다시 생성된 보고서를 얻을 때까지 비교 보고서를 무시하고
    다시 생성해 보세요.

13. Copilot이 생성한 두 번째 초안을 검토하세요. 현실 세계에서는 특정
    초안에 만족할 때까지 이 프로세스를 반복할 수 있습니다. 이전 초안으로
    돌아가서 최신 초안과 비교하려면 앞으로(\>) 및 뒤로(\<) 화살표를
    선택하여 초안을 앞뒤로 이동하세요. 생성한 두 초안을 비교하고 원하는
    초안이 표시되는지 확인하세요 (**1 of 2** 또는 **2 of 2**). 사용할
    초안을 찾으면 **Keep it** 버튼을 선택하세요.

![](./media/image15.png)

**참고**: **Keep it**를 선택하면 Copilot이 초안 모드에서 일반 Microsoft
Word 모드로 이동하세요. 또한 **Report Comparison**문서를 OneDrive 계정에
자동으로 저장하세요.

14. 이제 Copilot이 마지막 두 개의 이력서를 검토할 준비가 되었습니다.
    그러나 이전 단계에서 설명한 것처럼 나머지 두 이력서를 처음 두
    이력서를 비교하기 위해 방금 생성한 **Report Comparison** 문서와
    비교해야 합니다. 이렇게 하려면 새 **Word** 문서를 열어야 합니다.
    현재 **Report Comparison** 문서가 표시되는 브라우저의 Word 탭에
    여전히 있으므로 **Word** 리본 위의 메뉴에서 **File** 을 선택한 후
    **Home**  페이지의 **New** 생성 섹션에서 **Blank document**를
    선택하세요. 이렇게 하면 브라우저에 새 Word 문서와 함께 새 탭이
    열리세요

15. **Draft with Copilot** 창에서 다음 프롬프트를 입력하되 제출하지는
    마세요. 다음 단계에서 나머지 두 개의 이력서 파일과 첫 번째 **Report
    Comparison**보고서를 프롬프트에 첨부해야 합니다:

+++That was a good start. Please create a report that compares the
attached resumes to the prior resume comparison report (attached) and
rank the candidates from most qualified to least qualified. Thank
you!+++

16. 이제 처음 두 이력서를 비교한 방금 생성한 보고서를 나머지 두 이력서와
    함께 첨부해야 합니다. 이전 단계에서 프롬프트를 입력한 후 **Draft
    with Copilot**  창에서 **Reference your content** 버튼을 선택하세요.
    표시되는 드롭다운 메뉴에서 생성한 **Report Comparison of
    Resumes** 문서가 파일 목록의 맨 위에 나타나야 합니다. 이 문서를
    선택하세요.

17. **Draft with Copilot** 창에서 **Reference your content** 버튼을
    선택하세요. 나타나는 드롭다운 메뉴에서 나머지 두 이력서 중 하나를
    첨부해야 합니다. 파일 목록에 파일 중 하나가 보이면 해당 파일을
    선택하세요. 그렇지 않으면 **Browse files from cloud**를 선택하고
    나머지 두 이력서 중 하나를 찾고(**Recent** 파일 목록을 스크롤하면
    표시되어야 함) 선택한 후 **Attach** 버튼을 선택하세요. 이 과정을
    반복하여 마지막으로 남은 이력서를 선택하세요

![](./media/image16.png)

18. 첫 번째 보고서 비교 보고서와 나머지 두 개의 이력서가 프롬프트에
    첨부되면 **Draft with Copilot**창에서 **Generate** 버튼을
    선택하세요.

**참고**: 연속적인 이력서가 포함된 비교 보고서를 생성할 때 "문제가
발생했습니다" 오류 메시지가 표시될 수 있습니다. 보고서를 받을 때까지
비교 보고서를 무시하고 생성해 보세요.

19. Copilot은 처음 두 개의 이력서와 마지막 두 개의 이력서를 비교하고
    후보자의 순위 목록을 제공해야 합니다. 이 시점에서 새 초안을 다시
    생성하거나 Copilot에 변경을 요청할 수 있습니다. 이 교육 연습에서는
    보고서에 만족한다고 결정하므로 **Keep it** 버튼을 선택하세요.

![](./media/image17.png)

20. 이 시점에서 Copilot은 두 개의 보고서 비교 문서를 생성했으며, 그 중
    두 번째는 네 가지 후보를 모두 비교하는 최종 보고서입니다. Word에서
    Copilot을 사용하여 실제 환경에서 유사한 작업을 수행해야 하는 경우 이
    시나리오를 염두에 두어야 합니다. Microsoft Edge 브라우저에서 이 탭을
    닫을 수 있습니다.

**연습 #3: Loop의 Copilot를 사용하여 면접 질문 생성하기**

Loop의 Copilot를 사용하면 작업 공간과 페이지를 만들고, 지능형 검색 및
템플릿을 사용하여 관련 콘텐츠를 추가하고, 다른 사람과 작업을 공유할 수
있습니다. Loop의 Copilot는 아이디어를 제안하고 프로젝트를 시작하는 데
도움을 줄 수 있으므로 막혔을 때 더 쉽게 진행할 수 있습니다. 텍스트
초안을 작성하고, 표를 만들고, 질문에 빠르게 답변할 수도 있습니다.

Loop의 Copilot는 채용 프로세스부터 직원 관리, 중요한 문서 처리, 내부
커뮤니케이션 관리에 이르기까지 HR 경험의 여러 측면을 통해 HR 전문가를
지원할 수 있습니다.

이 연습에서는 Loop의 Copilot를 사용하여 새 역할에 대한 채용 프로세스를
지원합니다. 이전 연습에서는 이력서를 선별하기 위해 Word의 Copilot을
사용했지만, 루프의 Copilot을 사용하여 상위 후보자에 대한 면접 질문
목록을 생성합니다. 이 연습을 하는 동안 Loop의 Copilot가 사용자의 지시에
따라 질문 목록을 수정할 수 있는지 여부를 확인할 수 있습니다.

1.  탭에서 **Microsoft 365**를 열어 놓은 경우 다음 단계로 진행합니다.
    그렇지 않으면 **Microsoft Edge** 브라우저에서 새 탭을 열고 다음
    URL을
    입력하세요: +++[https://www.office.com+++](https://www.office.com+++/)

2.  **Microsoft 365**에서 왼쪽 탐색 창에 표시되는 경우 **Loop** 를
    선택하세요. 탐색 창에 나타나지 않으면 **App Launcher**를 선택하고
    **Apps**  페이지에서 아래로 스크롤하여 **Loop** 를 찾은 후
    선택하세요

![](./media/image18.png)

3.  **Sign-in** 버튼이 표시되면 사용자 자격 증명을 사용하여
    로그인하세요.

![](./media/image19.png)

**참고**: 로그인한 후 Loop 브라우저 창을 닫고 앱 페이지에서 Loop를 다시
여세요.

4.  **Microsoft Loop**에서는 **Workspaces** 탭이 기본적으로 표시됩니다.
    이 프로젝트에 대한 새 작업 영역을 생성하려면 **Getting started**
    옆에 있는 **+**를 선택한 후 **+New workspace**버튼을 선택하세요

![](./media/image20.png)

5.  **Create a new workspace** 창에서 작업 영역 이름에 대한 **Interview
    questions**을 입력한 후 표시되는 **Continue**또는 **Create** 버튼
    (Loop 버전에 따라 다름)을 선택하세요.

6.  **Add files to your workspace**작업 영역에 파일 추가 창 (Loop 버전에
    따라 이 창 은 **Workspace Switcher**로 표시될 수 있음)에서 **Create
    workspace**를 선택하세요.

7.  이제 새 작업 영역의 첫 번째 페이지에 있습니다. 페이지 이름은 현재
    **Untitled**입니다. 페이지(제목 없음)는 왼쪽 탐색 창에도 나타납니다.
    페이지 본문에서 **Untitled** 필드를 선택하고 페이지 이름을 다음으로
    변경하세요: **15 interview questions for the Senior Animation
    Designer role**. 탐색 창에서 페이지 이름이 자동으로 업데이트되는
    방식을 확인하세요.

![](./media/image21.png)

8.  **Just** **start typing...** 필드에 슬래시**(/)**를 입력하세요.

![](./media/image22.png)

9.  표시되는 드롭다운 메뉴의 메뉴 맨 위에 있는 **Copilot** 섹션에서
    **Draft page content**를 선택하세요.

10. 표시되는 **Copilot** 창에서 다음 프롬프트를 입력하고
    **Submit **아이콘을 선택하세요:

++**Create a list of the 15 best interview questions that should be
asked to candidates applying for a new Senior Animation Designer role at
the Graphic Design Institute**.++

![](./media/image23.png)

**참고**: 경우에 따라 Create, Brainstorm, Blueprint 및 Describe 옵션이
있는 **Copilot** 창이 표시되지 않을 수 있습니다. 이러한 예외가 발생하면
작업 영역을 닫고 다시 한 번 시도하세요.

11. 질문 목록을 검토하세요.

![](./media/image24.png)

12. 이 초기 목록이 좋은 시작이라고 생각하지만 몇 가지 유형의 질문이
    누락되었음을 알게 됩니다. 표시되는 Copilot 창에서 다음 프롬프트를
    입력하세요:

++**Add a question about having failed at a project and what they
learned from it**.++

![](./media/image25.png)

13. Loop에서 생성한 새 질문을 검토하세요.

![](./media/image26.png)

14. 마지막으로 목록을 한 번 훑어보고 나면 리더십에 대한 질문이 거의
    없다는 것을 알게 됩니다. 이 상황을 해결하려면 다음 프롬프트를
    입력하세요:

++**As a Senior Animation Designer, the candidate is expected to lead
their design team on projects. Ask them to talk about a couple of their
most significant experiences in leading other design team members, and
what their leadership style is**.++

![](./media/image27.png)

15. Loop에서 무슨 일이 일어났는지 주목하세요. 현재 페이지를
    업데이트하도록 구체적으로 요청하지 않고 변경을 요청하면 Copilot은
    이전 프롬프트에서와 같이 현재 페이지가 아닌 새 페이지를 열고 변경할
    수 있습니다. 이렇게 하면 Copilot 창에서 프롬프트를 추적하는 방법과
    가장 최근의 프롬프트가 창 맨 위에 표시되는 방식에 유의하세요.

이전 프롬프트를 선택합니다. 페이지의 콘텐츠가 밝은 글꼴로 어떻게
나타나는지 확인합니다. 또한 **Rewrite with Copilot** 프롬프트 필드를
선택해 보세요. Copilot은 현재 페이지가 아니므로 이 필드를
비활성화하세요. 현재 페이지를 활성 페이지라고도 합니다. 이제 최신
프롬프트를 선택하고 콘텐츠가 얼마나 명확한지 확인하여 이 페이지가 현재
페이지 또는 활성 페이지임을 나타냅니다. 활성 페이지만 수정할 수 있으므로
이 페이지에서 **Rewrite with Copilot**프롬프트 필드를 선택할 수
있습니다.

![](./media/image28.png)

16. 한 가지 더 변경해 보겠습니다. 현재 질문 목록이 충분한지 확신이 서지
    않습니다. 안전하게 플레이하기 위해Loop의 Copilot에게 몇 가지 질문을
    더 추천해 달라고 요청하기로 결정합니다. 다음 프롬프트를 입력하세요:

++**Are there any other questions that you think should be added to the
list**?++

17. Note the final list of questions that Copilot in Loop generated.

![](./media/image29.png)

18. 이제 입사 후보자를 면접할 때 선택할 수 있는 다양한 질문이 있습니다.
    또한 Loop를 사용하면 HR 팀의 다른 구성원이 다른 앱과 기기를
    사용하더라도 동일한 Loop 구성 요소에서 이러한 질문을 실시간으로 볼
    수 있습니다.

**요약:**

이 실습에서는 다음을 수행합니다.:

- Word에서 Copilot을 사용하여 조직의 새 역할에 대한 작업 설명을
  생성했습니다.

- 여러 이력서를 분석하고 각 후보자의 강점과 약점을 비교하는 보고서를
  생성하고, 가장 자격이 있는 후보자부터 가장 자격이 없는 후보자까지
  순위를 매기고, Word에서 Copilot을 사용하여 추천했습니다.

- Loop의 Copilot를 사용하여 직무 역할에 대한 후보자를 인터뷰하기 위한
  일련의 면접 질문 초안을 작성했습니다.
