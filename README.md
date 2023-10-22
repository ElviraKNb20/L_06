# L_06
public interface Фільм {
    void відтворити();
    String отриматиНазву();
}
public class ВітчизнянийФільм implements Фільм {
    private String назва;

    public ВітчизнянийФільм(String назва) {
        this.назва = назва;
    }

    @Override
    public void відтворити() {
        System.out.println("Відтворюємо вітчизняний фільм: " + назва);
    }

    @Override
    public String отриматиНазву() {
        return назва;
    }
}
public class Комедія implements Фільм {
    private String назва;

    public Комедія(String назва) {
        this.назва = назва;
    }

    @Override
    public void відтворити() {
        System.out.println("Відтворюємо комедію: " + назва);
    }

    @Override
    public String отриматиНазву() {
        return назва;
    }
}
public class Main {
    public static void main(String[] args) {
        Фільм фільм1 = new ВітчизнянийФільм("Незламна");
        Фільм фільм2 = new Комедія("Сусідка");

        фільм1.відтворити();
        фільм2.відтворити();

        System.out.println("Назва фільму 1: " + фільм1.отриматиНазву());
        System.out.println("Назва фільму 2: " + фільм2.отриматиНазву());
    }
}
