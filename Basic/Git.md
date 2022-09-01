# Git
**파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템**

<br>

## 명령어

<table>
  <tr>
    <th>분류</th>
    <th>명령어</th>
    <th>설명</th>
  </tr>
  <tr>
    <td>새로운 저장소 생성</td>
    <td>$ git init</td>
    <td>.git 하위 디렉토리 생성</td>
  </tr>
  <tr>
    <td rowspan="3">저장소 복제/다운로드(clone)</td>
    <td>$ git clone <https:.. URL></td>
    <td>기존 소스 코드 다운로드/복제</td>
  </tr>
  <tr>
    <td>$ git clone /로컬/저장소/경로</td>
    <td>로컬 저장소 복제</td>
  </tr>
  <tr>
    <td>$ git clone 사용자명@호스트:/원격/저장소/경로</td>
    <td>원격 서버 저장소 복제</td>
  </tr>
  <tr>
    <td rowspan="3">추가 및 확정(commit)</td>
    <td>$ git add <파일명><br>$ git add *</td>
    <td>커밋에 단일 파일의 변경 사항을 포함(인덱스에 추가된 상태)</td>
  </tr>
  <tr>
    <td>$ git commit -m "커밋 메시지"</td>
    <td>커밋 생성(실제 변경사항 확정)</td>
  </tr>
  <tr>
    <td>$ git status</td>
    <td>파일 상태 확인</td>
  </tr>
  <tr>
    <td rowspan="8">가지(branch)치기 작업</td>
    <td>$ git branch</td>
    <td>브랜치 목록</td>
  </tr>
  <tr>
    <td>$ git branch <브랜치이름></td>
    <td>새 브랜치 생성 (local로 만듦)</td>
  </tr>
  <tr>
    <td>$ git checkout -b <브랜치이름></td>
    <td>브랜치 생성 & 이동</td>
  </tr>
  <tr>
    <td>$ git checkout master</td>
    <td>master branch로 되돌아 옴</td>
  </tr>
  <tr>
    <td>$ git branch -d <브랜치이름></td>
    <td>브랜치 삭제</td>
  </tr>
  <tr>
    <td>$ git push origin <브랜치이름></td>
    <td>만든 브랜치를 원격 서버에 전송</td>
  </tr>
  <tr>
    <td>$ git push -u < remote > <브랜치이름></td>
    <td>새 브랜치를 원격 저장소로 push</td>
  </tr>
  <tr>
    <td>$ git pull < remote > <브랜치이름></td>
    <td>원격에 저장된 git 프로젝트의 현재 상태를 다운받고 + 현재 위치한 브랜치로 병합</td>
  </tr>
  <tr>
    <td rowspan="5">변경 사항 발행(push)</td>
    <td>$ git push origin master</td>
    <td>변경사항 원격 서버에 업로드</td>
  </tr>
  <tr>
    <td>$ git push < remote > <브랜치이름></td>
    <td>커밋을 원격 서버에 업로드</td>
  </tr>
  <tr>
    <td>$ git push -u < remote > <브랜치이름></td>
    <td>커밋을 원격 서버에 업로드</td>
  </tr>
  <tr>
    <td>$ git remote add origin <등록된 원격 서버 주소></td>
    <td>클라우드 주소 등록 및 발행(git에게 새로운 원격 서버 주소 알림)</td>
  </tr>
  <tr>
    <td>$ git remote remove <등록된 클라우드 주소></td>
    <td>클라우드 주소 삭제</td>
  </tr>
  <tr>
    <td rowspan="4">갱신 및 병합(merge)</td>
    <td>$ git pull</td>
    <td>원격 저장소의 변경 내용이 현재 디렉토리에 가져와지고(fetch) 병합(merge)됨</td>
  </tr>
  <tr>
    <td>$ git merge <다른 브랜치이름></td>
    <td>현재 브랜치에 다른 브랜치의 수정사항 병합</td>
  </tr>
  <tr>
    <td>$ git add <파일명></td>
    <td>각 파일을 병합할 수 있음</td>
  </tr>
  <tr>
    <td>$ git diff <브랜치이름><다른 브랜치이름></td>
    <td>변경 내용 merge 전에 바뀐 내용을 비교할 수 있음</td>
  </tr>
  <tr>
    <td>태그tag 작업</td>
    <td>$ git log</td>
    <td>현재 위치한 브랜치 커밋 내용 확인 및 식별자 부여됨</td>
  </tr>
  <tr>
    <td rowspan="2">로컬 변경사항 return 작업</td>
    <td>$ git checkout -- <파일명></td>
    <td>로컬의 변경 사항을 변경 전으로 되돌림</td>
  </tr>
  <tr>
    <td>$ git fetch origin</td>
    <td>원격에 저장된 git프로젝트의 현 상태를 다운로드</td>
  </tr>
</table>

<br>

## 용어

### 📌 태그
커밋을 참조하기 쉽도록 알기 쉬운 이름을 붙이는 것이다. 한 번 붙인 태그는 브랜치처럼 위치가 이동하지 않고 고정되며, 태그 이름을 지정하여 checkout/reset 함으로써, 간단하게 과거의 특정 상태로 되돌릴 수 있다.

### 📌 브랜치
독립적으로 어떤 작업을 진행하기 위한 개념이다. 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있다.

### 📌 fetch
`pull`을 실행하면, 원격 저장소의 내용을 가져와 자동으로 병합 작업을 실행한다. 그러나 단순히 원격 저장소의 내용을 확인만 하고 로컬 데이터와 병합은 하고 싶지 않은 경우에는 fetch 명령어를 사용할 수 있다.

<br>

## GitHub와 GitLab의 차이

<table>
  <tr>
    <th>GitHub</th>
    <th>GitLab</th>
  </tr>
  <tr>
    <td>여러 저장소에서 문제를 추적할 수 있다.</td>
    <td>여러 저장소에서 문제를 추적할 수 없다.</td>
  </tr>
  <tr>
    <td>Travis CI, CircleCI와 같은 타사 도구로만 지속적인 통합이 가능하다.</td>
    <td>지속적인 통합 기능을 포함한다.</td>
  </tr>
  <tr>
    <td>내장 배포 플랫폼이 없다.</td>
    <td>쿠버네티스를 통한 소프트웨어 배포를 할 수 있다.</td>
  </tr>
  <tr>
    <td>문제 및 풀링 요청을 추적하는 개인 대시보드</td>
    <td>프로젝트 계획 및 모니터링을 위한 분석 대시보드</td>
  </tr>
</table>

<br>

# 참고
> https://velog.io/@delilah/GitHub-Git-%EB%AA%85%EB%A0%B9%EC%96%B4-%EB%AA%A8%EC%9D%8C  
> https://backlog.com/git-tutorial/kr/  
> https://volvootofinans.com/ko/gitlab-vs-github-ndash-a-comparison-of-the-two-version-control-systems.html
