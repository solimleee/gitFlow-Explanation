1. 포크한 레파지토리를 git clone (포크한 url)을 한다 

2. 클론한 폴더로 넘어가서 <git checkout -t origin/dev> 를 한다 (나의 포크한 레파지토리에 있는 dev 브랜치를 로컬로 가져옴) 

3. dev 브랜치에서 <git checkout -b feature/이슈번호-이름> 형태로 새로운 브랜치를 만들어 제작한다 
체크아웃(checkout)이란, 내가 사용할 브랜치를 지정하는 것을 의미
-t : 추적하다

4. Git remote add codestates (코드스테이츠에서 준 레파지토리 url) 

5. Git pull codedstates dev
(끌어올릴때)

6. 	브랜치를 새로 만들어주세요, (git checkout -b 브랜치이름  / git switch -c 브랜치이름)
	변경된 내용을 먼저, 현재 브랜치에서 git add . 를 한 뒤에
	커밋 메시지를 작성합니다. 
	제작 완료 후, <git checkout dev> 를 통해 dev 브랜치로 넘어와서
 	<git merge feature/이슈번호-이름>으로 방금 전 feature 브랜치에서 작업한 내용을 로컬 dev브랜치에 merge한다. 

(7번, 8번은 뭘 먼저하든 자기 자유임.)

7. <git push origin dev>를 통해 포크한 레파지토리의 dev 브랜치에 수정사항을 반영한다. 
(dev로 가는지 확인!)

8. <git branch -d feature/이슈번호-이름> 으로 필요없어진 방금 전의 개발용 브랜치를 삭제한다. 

9. github에서 pull request를 날린다 (origin 레파지토리의 dev 브랜치로 날리는 것을 유의한다) 

10. 팀장님은 내용을 확인하고 pull request를 confirm한다. 

11. 이제 변경사항이 다 합쳐진 origin 레파지토리의 dev를 pull해온다 (<git remote add 닉네임 origin레파지토리주소> 형태로 등록하여 쓰는 것이 편해보인다) (등록해놓고 현재 로컬이 dev 브랜치인 상태에서 <git pull 닉네임 dev> 로 내 로컬의 dev 브랜치에 origin 레파지토리의 dev의 것으로 최신 업데이트 할 수 있다) 

12. <git push origin dev> 로 내 포크한 레파지토리의 dev브랜치도 최신으로 업데이트한다. 

<fin. 3~10을 반복한다.>

새로기능을 보낼때마다 feature branch다시 만들어서 보내기
