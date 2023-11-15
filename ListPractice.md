# 나의 코드

```java
   public class ListPractice {
    
    public static void main(String[] args) {
        runClI();
    }

    private  static void runClI(){
        Scanner scanner =new Scanner(System.in);
        System.out.println("1번 숫자를 입력해주세요 :");
        String add_1_Number =scanner.nextLine();
        System.out.println("2번 숫자를 입력해주세요 :");
        String add_2_Number =scanner.nextLine();
        System.out.println("3번 숫자를 입력해주세요 :");
        String add_3_Number =scanner.nextLine();
        System.out.println("4번 숫자를 입력해주세요");
        String add_4_Number=scanner.nextLine();
        System.out.println("5번 숫자를 입력해주세요");
        String add_5_Number=scanner.nextLine();
        System.out.println(createUserNumberList(add_1_Number,add_2_Number,add_3_Number,add_4_Number,add_5_Number));
    }
  private static List<String> createUserNumberList(String add_1_Number,
                                                   String add_2_Number,
                                                   String add_3_Number,
                                                   String add_4_Number,
                                                   String add_5_Number){
        List <String> result= new ArrayList<>();
        result.add(add_1_Number);
        result.add(add_2_Number);
        result.add(add_3_Number);
        result.add(add_4_Number);
        result.add(add_5_Number);
        return result;
  }
}
```


# 내 코드의 문제점:

1. **중복된 코드**: **runClI** 메서드 내에서 사용자로부터 입력을 받는 부분이 반복되고 있습니다. 이는 루프를 사용하여 간결하게 만들 수 있습니다.
2. **메서드 네이밍**: Java에서는 일반적으로 메서드 이름을 소문자로 시작하는 camelCase 방식을 사용합니다. 예를 들어 **runClI**는 **runCli**로 변경하는 것이 좋습니다.
3. **숫자 입력에 대한 오해**: 문제는 문자열을 입력받는 것이었지만, 메서드와 출력문에서 '숫자'라는 표현을 사용하고 있습니다. 이는 사용자에게 혼란을 줄 수 있습니다.

# 개선된 코드 

```java
public class ListPractice {
    public static void main(String[] args) {
        List<String> strings = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);

        for (int i = 1; i <= 5; i++) {
            System.out.println(i + "번 문자열을 입력해주세요:");
            strings.add(scanner.nextLine());
        }

        System.out.println("입력된 문자열 리스트:");
        for (String str : strings) {
            System.out.println(str);
        }

        scanner.close();
    }
}
```
