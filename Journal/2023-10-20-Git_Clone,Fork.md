1. Github Desktop을 사용하다 보면 Clone과 Fork가 있다.
2. 두 기능 전부 특정 Repository를 복사하는 기능이다.
3. 그런데 수정 불가능 Repository를 Clone을 통해서 복사를 하고서 Push를 하면 Fork를 할 것 인지 물어본다. (GithubDesktop)
4. 둘 다 복사를 하는데 두 기능의 차이점은 무엇일까?

5. Clone을 Repository를 복사하여 로컬에 저장을 한다.
6. 로컬에 저장된 것이므로 나의 Github에서는 해당 Repository를 추적하지 않는다.
7. 해당 Clone에서 발생한 Commit을 Push하면 원본 Repository에 영향을 주게 된다.
8. 그런데 해당 Repository가 수정 불가능한 Repository라면 Push가 불가능하다.

9. 그렇기 떄문에 Fork를 사용해서 해당 Repository를 복사를 하고 Fork한 Repository를 Clone을 하여 로컬에 저장을 한다.
10. 해당 Repository는 내 Repository가 되어서 수정이 가능하며, Github에서 추적이 가능하다.

11. 두 방식 모두 최초 Repository에 변경 내용을 반영하려면 Pull Request를 통해서 반영이 가능하다.