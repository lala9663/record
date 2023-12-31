## 상속을 고려해 설계하고 문서화하라. 그러지 않았다면 상속을 금지하라

이 원칙은 코드의 유지보수성과 확장성을 향상시키기 위해 사용된다.

### 상속을 고려해 설계하고 문서화하라

1. 설계 과정: 객체지향 소프트웨어를 설계할 때, 상속을 활용할 가능성을 고려한다. 부모 클래스와 자식 클래스 간의 관계를 신중하게 고려하고, 부모 클래스에 공통적인 특성과 메서드를 식별한다.
2. 문서화: 상속을 사용하는 경우, 클래스와 메서드 사이의 상속 계층을 문서화한다. 이를 통해 다른 개발자들이 코드를 이해하고 확장할 때 도움을 받을 수 있다.
3. Liskov 치환 원칙 준수: 상속을 사용할 때, Liskov 치환 원칙을 준수해야 한다. 자식 클래스는 부모 클래스를 대체할 수 있어야 하며, 부모 클래스의 기능을 포함하고 확장하는 역할을 해야 한다.

### 그렇지 않았다면 상속을 금지하라

1. 무분별한 상속 사용 금지: 상속을 고려하지 않고 부모 클래스를 정의하고, 문서화하지 않은 경우, 상속을 금지하는 것이 좋다. 이렇게 하면 부모 클래스와 자식 클래스 간의 관계와 의도가 불문명하게 될 수 있다.
2. 인터페이스 활용: 인터페이스를 통해 필요한 기능을 구현하고, 클래스가 인터페이스를 구현하도록 하는 방법을 고려한다. 이는 더 유연하고 결합도가 낮은 설계를 가능하게 한다.