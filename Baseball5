import java.util.Scanner;

public class Baseball5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] computer = new int[3]; // int 배열을 computer라는 변수를 생성한다, 그리고 computer 변수에 숫자 3개 생성한다. [0, 0 ,0]
        int[] user = new int[3]; // int 배열을 user라는 변수를 생성한다, 그리고 user 변수에 숫자 3개 생성한다.
        int count = 1; // 변수 count는 사용자의 시도 횟수다. 만일 "count=0;"이면 사용자의 0번째 시도 횟수부터 시작되버린다.

        for (int i = 0; i < computer.length; i++) {
            computer[i] = (int) (Math.random() * 10); // 컴퓨터가 위의 3자리 숫자를 무작위로 생성한다.

            // (0 <= 랜덤 < 1) x 9 => 0 <= 랜덤 < 10
            for (int j = 0; j < i; j++) {
                if (computer[i] == computer[j]) {
                    i--;
                    //
                    break;
                }
            }
        }
        System.out.println("컴퓨터가 숫자를 생성하였습니다. 답을 맞춰보세요!");

        while (true) {
            int strike = 0;
            int ball = 0;
            int[] numbers = new int[3];

            System.out.print(count + "번째 시도 : ");
            String input = sc.nextLine();

            if (input.length() == 3) {
                numbers[0] = input.charAt(0) - '0';
                numbers[1] = input.charAt(1) - '0';
                numbers[2] = input.charAt(2) - '0';
            } else {
                continue;
            }

            for (int i = 0; i < computer.length; i++) {
                for (int j = 0; j < numbers.length; j++) {
                    if (computer[i] == numbers[j] && i == j) {
                        strike++;
                    } else if (computer[i] == numbers[j]) {
                        ball++;
                    }
                }
            }
            System.out.println(ball + "B" + strike + "S");

            if (strike == 3) {
                System.out.println(count + "번만에 맞히셨습니다.");
                System.out.println("게임을 종료합니다.");
                break;
            }
            count++;
        }
    }
}
