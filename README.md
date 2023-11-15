# PracticeCollection

# 목적 : 자바를 다루면서 collection 사용이 익숙하지 않아 인공지능을 이용해 문제를 받고, 제가 풀이를 제시하고 , 제 풀이에 대한 문제점을 고찰하는데 있습니다 
# 목표 : 자바의 대표적인 collection 중 List ,Map ,Set 을 익숙하게 사용하는것이 목표입니다 

# 1. List 문제

**문제**: 문자열을 저장하는 ArrayList를 생성하고, 사용자로부터 5개의 문자열을 입력받아 ArrayList에 추가한 후, 저장된 모든 문자열을 출력하세요.
**힌트**: `Scanner` 클래스를 사용하여 사용자 입력을 받고,
 `ArrayList<String>`을 생성한 후, `add` 메서드로 문자열을 추가할 수 있습니다. `for`루프 또는 `for-each` 루프를 사용하여 ArrayList의 내용을 출력합니다

 ---------------------------------------------------------------------------------------------------------------------------------------------

# 2. Set 문제 

**문제**: 사용자로부터 숫자를 입력받아 HashSet에 추가하고, 모든 숫자를 출력하세요. 그 후, 사용자로부터 삭제할 숫자를 입력받아 HashSet에서 제거하고, 다시 HashSet의 내용을 출력하세요.
**힌트**: Scanner 클래스를 사용하여 사용자로부터 숫자를 입력받습니다. HashSet<Integer>를 생성하고, add 메서드로 숫자를 추가한 후 remove 메서드로 숫자를 제거할 수 있습니다. HashSet의 내용은 for-each 루프를 사용하여 출력할 수 있습니다.

-----------------------------------------------------------------------------------------------------------------------------------------------

# 3. Map 문제 

**문제**: 사용자로부터 키(문자열)와 값(정수) 쌍을 입력받아 HashMap에 저장하세요. 몇 개의 키-값 쌍을 추가한 후, 모든 키와 해당하는 값을 출력하세요. 그 다음, 사용자로부터 키를 입력받아 해당 키의 값을 변경하고, 변경된 HashMap을 출력하세요.

**힌트**: Scanner 클래스를 사용하여 사용자로부터 키와 값을 입력받습니다. HashMap<String, Integer>를 생성하고, put 메서드로 키-값 쌍을 추가합니다. keySet 또는 entrySet 메서드를 사용하여 모든 키와 값을 순회하면서 출력할 수 있으며, put 메서드로 기존 키의 값을 변경할 수 있습니다.

1. 문제 나의 코드
   ```
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

내 코드의 문제점:

1. **중복된 코드**: **`runClI`** 메서드 내에서 사용자로부터 입력을 받는 부분이 반복되고 있습니다. 이는 루프를 사용하여 간결하게 만들 수 있습니다.
2. **메서드 네이밍**: Java에서는 일반적으로 메서드 이름을 소문자로 시작하는 camelCase 방식을 사용합니다. 예를 들어 **`runClI`**는 **`runCli`**로 변경하는 것이 좋습니다.
3. **숫자 입력에 대한 오해**: 문제는 문자열을 입력받는 것이었지만, 메서드와 출력문에서 '숫자'라는 표현을 사용하고 있습니다. 이는 사용자에게 혼란을 줄 수 있습니다.

