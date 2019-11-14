작성자 : gmlwo530


안드로이드 애니메이션에서 쓰이는 Interpolator(보간법)에 대해 다룬다.

보간법은 알려진 데이터 지점의 고립점 내에서 새로운 데이터 지점을 구성하는 방식이다.

예를 들어 선형 보간법은 시작점과 끝점이 주어졌을 때 그 사이에 위치한 값을 추정하기 위해서 직선 거리에 따라 선형적으로 계산하는 방법이다.

### 어떻게 Interpolator가 애니메이션의 변화율을 정의 하는가?

String이 charcter의 순서인 것과 같이 애니메이션은 시간 간격에 따른 이미지(이것을 frame이라고 부른다)의 순서이다.

각 시간 인스턴스마다 frame은 일대일 매핑 되어있다.

Interpolator는 특정 시간의 frame을 다른 frame으로 바꿔준다

즉 interpolator는 기존 시간 인스턴스를 input으로 받고, 대치 프레임의 시간 인스턴스를 output로 하는 수학 연산 도구이다.

Linear Interpolator와 Accelerate Interpolator에 대한 그래프와 예시는 [참고한 블로그](https://medium.com/mindorks/understanding-interpolators-in-android-ce4e8d1d71cd)에서 확인 해보자

### CustomInterporator 만들기

```java
    import android.view.animation.Interpolator;
    
    
    public class CustomInterpolator implements Interpolator {
        public CustomSpringInterpolator() {}
    
        @Override
        public float getInterpolation(float input) {
            return // put your equation
        }
    }
```

---

**Reference** 

- [https://medium.com/mindorks/understanding-interpolators-in-android-ce4e8d1d71cd](https://medium.com/mindorks/understanding-interpolators-in-android-ce4e8d1d71cd)
- [https://ko.wikipedia.org/wiki/보간법](https://ko.wikipedia.org/wiki/%EB%B3%B4%EA%B0%84%EB%B2%95)
- [https://github.com/geetgobindsingh/AndroidAnimationInterpolator](https://github.com/geetgobindsingh/AndroidAnimationInterpolator)
