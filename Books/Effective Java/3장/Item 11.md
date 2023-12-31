## equals를 재정의 하려거든 hashCode도 재정의하라

'hashCode' 메서드는 객체의 해시 코드를 반환하는데, 이 해시 코드는 객체를 저장하고 검색하는 해시 테이블 같은 자료구조에서 중요한 역할을 한다.

'equals' 메서드를 재정의할 때는 다음과 같은 규약을 따라야 한다.

1. 'equals'가 두 객체를 논리적으로 동등하다고 판단하면, 두 객체의 'hashCode' 값은 반드시 같아야 한다.
2. 'equals'가 두 객체를 논리적으로 다르다고 판단하면, 두 객체의 'hashCode' 값은 서로 다를 수 있지만, 다른 경우에도 다르도록 구현하는 것이 좋다.
   
만약 'equals' 메서드를 재정의하고 'hashCode' 메서드를 재정의하지 않으면, 해시 테이블과 같은 자료구조에서 제대로 동작하지 않을 수 있다. 즉, 동일한 객체로 판단되어도 해시 코드가 다르게 나와서 검색 성능이 저하될 수 있다.

### 좋은 hashCode 작성 방법

- 이미 정의된 hashCode(Integer.hashCode, ArraysCode 등)를 최대한 사용해라
- equals 비교에 사용되지 않은 필드는 hashCode 에서도 반드시 제외해야 한다.
- 해시 충돌이 더욱 적은 방법을 써야 한다면 Guava Hashing을 참고하자
- (주의) hashCode 반환 값의 생성 규칙을 사용자에게 알리지 말아라
- 사용하자는 개발자가 이 값에 의지하고 코드에 반영해버리면 문제가 생길 수 있다.

