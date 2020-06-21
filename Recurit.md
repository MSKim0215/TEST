1. 유니티 엔진에서 가장 자신있는 부분과 가장 자신없는 부분은 무엇인가요?

  * 애니메이션 및 PostProcessing을 이용한 연출이 자신있습니다.         
     -> "PacMan" 포트폴리오      
      [ 게임 시작 시 카메라 무빙, 달리는 상태 모션 블러, 적이 점점 다가오는 경우 비네팅, 비네팅 효과 동시에 블룸 등]
  
  * Particle 및 shader를 많이 사용해본 적이 없어서 미흡합니다.                                               
            


            
2. 우리 회사에서 하고 싶은 일을 3가지 정도로 요약해 주세요.

  * 귀사의 "매직 스케치북"과 같이 사용자가 직접 칠한 색을 통해서 렌더링 되는 기술을 구현하고 싶습니다.
        
  * 귀사의 "샌드 크래프트"와 같이 실제 모래의 고저차의 비교를 통해 시작적으로 변하는 컨텐츠를 구현하고 싶습니다.
  
  * 평소에 VR/AR 기술에 대한 관심이 많고, Kincet를 이용한 교육용 게임을 제작할 때 느꼈던 경험과 바탕으로 재미있는 콘텐츠를 제작하고 싶습니다.
  
  
  
  
3. C#에서 static 키워드의 의미를 아는대로 말해 보세요.
  
  * C# static 함수  
    클래스로부터 객체를 생성하지 않고 직접 [클래스명.함수명] 형식으로 호출하는 메서드입니다.
    
    ex)   
      public class A{
      
        // 인스턴스 함수
        public int InsA(){
          // 처리
        }
        // 정적 함수
        public static int StaA(){
          // 처리
        }
      }
         
      public class B{      
      
        public void Test(){      
          // 인스턴스 함수 호출
          A a = new A();
          a.InsA();
          
          // 정적 함수 호출
          A.StaA();
        }         
      }
   
   * C# static 속성, 필드  
    static 함수와 동일하게 [클래스명.속성명]으로 사용합니다.   
    static 필드는 프로그램 실행 후 해당 클래스가 처음으로 사용될 때 한 번 초기화되어 계속 동일한 메모리를 사용합니다.   
    
     ex)
     
      // 정적 필드   
      protected static int a;
      
      // 정적 속성  
      public static string ID {get; set;}
      
   * C# static 클래스  
    static 클래스는 모든 클래스 멤버가 static 멤버로 이루어져있습니다.   
    static 클래스는 public 생성자를 가질 수 없습니다. ( static 클래스는 객체를 생성 할 수 없기 때문 )   
    static 필드를 초기화하는데에 많이 사용합니다.
    
    ex)  
     // 정적 클래스 정의
     public static class A{
      private static int A;
      
      // 정적 생성자
      static A(){
       A = 1;
      }
      
      public static string Convert(int _num){
       return _num.ToString();
      }
    }
    
     // 정적 클래스 사용
     static void main(){
      string str = A.Convert(123);
     }

      
