## clone 재정의는 주의해서 진행하라

**Cloneable**은 복제해도 되는 클래스임을 명시하는 용도의 믹스인 인터페이스([[아이템 20]] )지만, 의도한 목적을 제대로 이루지 못함.

**clone 메서드**가 선언된 곳이 Cloneable이 아닌 Object이고, 그 마저도 protected다. 그래서 Cloneable을 구현하는 것만으로는 외부 객체에서 clone 메서드를 호출할 수 없다.

**리플렉션**([[아이템 65]])을 사용하면 가능하지만, 해당 객체가 접근이 허용된 clone 메서드를 제공한다는 보장이 없다.

1. clone 메서드는 객체 복제에 사용된다.
   - clone 메서드는 Object 클래스에서 상속된 메서드로, 객체의 얕은 복제(Shallow Copy)를 수행한다. 즉, 객체를 복제하면 새로운 객체가 생성되지만 그 안에 있는 내부 객체들은 참조를 공유한다.
2. clone 메서드를 재정의할 때 주의해야 한다.
   - clone 메서드를 잘못 재정의하면 프로그램의 동작이 예측하기 어려워질 수 있다.
   - clone 메서드를 재정의하면 얕은 복제에서 깊은 복제(Deep Copy)를 수행하도록 구현할 수 있다.
3. Cloneable 인터페이스를 구현해라.
   - clone 메서드를 호출하기 전에 해당 객체가 Cloneable 인터페이스를 구현했는지 확인해야 한다. 그렇지 않으면 'CloneNotSupportedException'이 발생할 수 있다.
4. 복제의 유형을 고려해라.
   - 얕은 복제가 충분하다면 super.clone() 을 호출하여 기본 복제 기능을 활용할 수 있다.
   - 깊은 복제가 필요한 경우에는 내부 객체들끼리 복제하고, 이를 위해 재귀적으로 clone을 호출하고 복제된 객체를 적절히 조립한다.