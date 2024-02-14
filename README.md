This is a translation of Parker, Adam E., "Solving First-Order Linear Differential Equations: Gottfried Leibniz' "Intuition and Check" Method" (2020). Differential Equations. 1. https://digitalcommons.ursinus.edu/triumphs_differ/1

<p align=right> Ursinus College 우르시누스 대학교 </p>
<p align=right> <b> Digital Commons @ Ursinus College </b> 디지털 커먼스 @ 우르시누스 대학교 </p>
<p align=right> Transforming Instruction in Undergraduate Mathematics via Primary Historical Sources (TRIUMPHS) </p>
<p align=right> 학부 수학 수업을 역사적 자료를 통해 변화시키기 </p>
2020년 여름
<h3>일차 선형 미분 방정식 풀이: 고트프리트 라이프니츠의 "직관과 확인" 방법</h3>
<p align=center>Adam E. Parker<sup>*</sup></p>

<p align=center> 2021년 1월 10일 </p>

### 서론
1926년 영국의 수학자 에드워드 린제이 인스(1891-1941)는 미적분학에서 (그리고 미분방정식과 일반적인 과학에서) 해를 구하는 테크닉이 어떻게 진화해왔는지를 설명한다. <sup>1</sup>

-----------------------

<p>
미적분학의 초기 역사에는 사실상 미분방정식과 같은 방법으로 문제를 푸는 예가 많았다; 16세기 중반에는 심지어 미분방정식의 가장 간단한 형태의 해로 취급할 수 있는 적분 문제가 실질적인 문제였다고 해도 과언이 아니다. 탄젠트의 역 문제의 특별한 경우 -기울기가 특정 방정식으로 정해진 곡선을 찾는 문제- 는 미적분학이 발명되기 전에도 성공적으로 해결됐다. 
</p>

<p>
하지만 과학의 역사적 가치는 얼마나 많은 특정 현상을 보여주는가에 있지 않고 다양한 사실들을 정리해서 하나의 간단한 코드로 설명할 수 있는 힘에 있다. [인스, 1926]
</p>

-----------------------
<p><sup>*</sup> 비텐베르크 대학교 수학 컴퓨터과학과, 미국 오하이오주 스프링필드 45504; aparker@wittenberg.edu</p>

<p><sup>1</sup> 인스도 미분방정식에 관한 이야기의 일부이다. 그는 <i>Ince 방정식</i> 을 개발했다 (1923년 경), </p>

```math
(a+acos(2t))y''(t)+(bsin(2t))y'(t)+(\lambda+dcos(2t))y(t) = 0,
```

이는 각각 1868년, 1914년부터 잘 알려진 두개 이상의 다른 방정식들을 일반화한 것이다. $a=b=0$으로 두고 $d=-2q$로 두면, <i>Mathieu 방정식</i> 을 얻을 수 있다 (드럼 모양을 타원형으로 모델링한다), 

```math
y''(t)+(\lambda-2qcos(2t))y(t) = 0,
```

$a=0,b=-4q,d=4q(\nu-1)$로 두면, <i>Whittaker-Hill 방정식 </i>을 얻는다 (달의 안정성과 양자 역학에서 쓰인다)

```math
y''(t)-4q(sin(2t))y'(t)+(\lambda+4q(\nu-1)cos(2t))y(t)=0.
```

Ince 방정식은 또한 <i>일반화된 Ince 방정식 </i>의 특별한 경우이다 ([Moussa, 2014]에서 연구되었다)

```math
(1+\epsilon A(t))y''(t) + \epsilon B(t)y'(t) + (\lambda + \epsilon D(t))y(t)=0.
```

------------------------

이것은 정확히 일차 선형 상미분 방정식 해를 구하는 방법이 진화하는 과정과 같다. 먼저, 특별한 문제가 그 문제를 너머 일반화된 문제에는 적용할 수 없는 "일회성" 방법으로 풀린다. 하지만 이 결과들은 통합된 이론이 개발될 때까지 결합되고 일반화된다. 

과제 1
> [!IMPORTANT]
> 상기된 글에서 인스는 <b>"모든 종류의 미분방정식 중 가장 간단한 미분 방정식의 해"</b>와 <b>"기울기가 특정 방정식에 의해 정해진 곡선을 찾는 문제"</b>를 연결지었다. 두 문장을 연결하라. 미분방정식이
> ```math
> \frac{dy}{dx} = f(x,y),
> ```
> 일 때, <b>곡선,</b>과 <b>기울기,</b>와 <b>특정 방정식</b>은 무엇인가?

과제 2
> [!IMPORTANT]
> 비동차 일차 선형 상미분 방정식이 다음과 같음을 기억하라
> ```math
> p(x)\frac{dy}{dx}+q(x)y = f(x),
> ```
> 최고차항을 1로 만들면,
> ```math
> \frac{dy}{dx}+P(x)y = Q(x),
> ```
> 첫번째 방정식에서 어떻게 두번째 방정식처럼 최고차항을 1로 만들 수 있는지 설명하라. 특히, 왜 우리는 p(x)가 0이 아니라고 가정할 수 있는가? P(x)와 Q(x)를 p(x), q(x), f(x)에 대해서 써보라.

본 프로젝트의 테마는 
