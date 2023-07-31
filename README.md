# Github Repository 병합하는 방법

새로운 repository = 레포1
병합할 repository = 레포2

1.github 사용자 등록
git config --global user.name "github 사용자 이름"
git config --global user.email "github 이메일 주소"

2.레포1을 만든다.
3.branch를 맞춘다.(로컬과 github - main으로 설정)
git branch -m master main

4.로컬에 레포1을 clone 한다. 경고문구가 나오지만 신경쓰지 않아도 된다.
git clone https://github.com/heydgmon/SpringJavappt.git aa 
(aa는 디렉토리)

cd aa

5. 병합할 레포를 remote한다.
git remote add 0619 https://github.com/heydgmon/0619.git

6.fetch한다.
git fetch 0619

7.모든 commit log를 남겨 merge 한다.
git merge --allow-unrelated-histories 0619/main
:wq 로 나오기

8. remote 연결을 끊어준다
git remote remove 0619

9.push하기
git push origin main

결과 : 레포의 readme파일이 들어감.

참고사이트
https://yuricoding.tistory.com/84
