# git-playground
git 다양한 기능 연습하기

##git amend 마지막에 사용한 커밋에 추가하기

-소스트리 기준 : 커밋할때 '마지막 커밋 정정'을 클릭하고 
-커밋하게 되면, 기존 커밋이 정정되고 새로운 커밋이 추가되지 않는다.

-원격 저장소의 마지막 커밋을 수정할때
-로컬 저장소에서 amend를 사용해 '마지막 커밋 정정'후 push를 하게 되면 오류메세지 발생
->푸시 사용시 강제 푸쉬에 체크하고 푸쉬하면 깔끔하게 원격저장소의 커밋도 정정된다.
-'git commit --amend'
-커밋 수정 후 덮어쓰기

# 원격저장소(깃허브에서 pull request되돌리기-revert)
-되돌려야하는 PR (merge가 완료된)이 있을 경우
-깃헙 저장소 > pull request > closed
-되돌려야하는 RP선택후
-revert 선택
-revert를 위한 새로운 PR이 생성됨
-새로운 PR을 merge하고 나면 기존 PR이 되돌려진 상태로 복귀

## 브랜치 보호하기
-branch protect rule
-깃허브 > 저장소 > setting > branch
->add브랜치 프로텍트룰
   -branch name patten-(패턴가능 feature*=> 모든 feature브랜치)
                      -일반적으로 main브랜치를 보호
-request a pull request before merging
    -반드시 병합하기 위해서는 PR이 필요
    -일반적인 커밋 n 푸쉬를 통한 병합은 원격저장소에서 block                  