가비지 컬렉션은 자바의 메모리 관리 방법 중 하나로 JVM의 **Heap 영역**에서 동적으로 할당했던 메모리 중 필요 없게 된 메모리 객체를 모아 주기적으로 제거하는 프로세스를 말한다.

단점으로는 메모리가 언제 해제되는지 정확하게 알 수 없어 제어하기 힘들며, 가비지 컬렉션이 동작하는 동안에는 다른 동작을 멈추기 때문에 오버헤드가 발생되는 문제점이 있다.