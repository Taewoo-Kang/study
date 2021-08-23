---


---

<h1 id="장-변수">4장 변수</h1>
<h2 id="변수란-무엇이고-왜-필요한가">4.1 변수란 무엇이고 왜 필요한가?</h2>
<p>메모리 상의 임의의 위치에 저장되고 cpu는 이 값을 읽어들여 연산 수행<br>
자바스크립트는 개발자의 직접적인 메모리 제어를 허용하지 않음<br>
<strong>변수(variable)</strong>: 하나의 값을 저장하기 위해 확보한 메모리 공간 혹은 그 이름</p>
<p>할당(assignment): 변수에 값을 저장하는 것<br>
참조(reference): 변수에 저장된 값을 읽어들이는 것</p>
<h2 id="식별자">4.2 식별자</h2>
<p>식별자(Identifier): 어떤 값을 구별해서 식별할 수 있는 고유한 이름 — 값이 아닌 메모리 주소를 기억<br>
변수, 함수, 클래스 등 메모리 상에 존재하는 어떤 값을 식별할 수 있는 이름을 모두 식별자라고 부름</p>
<h2 id="변수-선언">4.3 변수 선언</h2>
<p><strong>변수 선언(variable declaration)</strong>: 값을 저장하기 위한 메모리 공간을 확보(allocate)하고, 변수 읾과 확보된 메모리 공간의 주소를 연결(name binding)해서 값을 저장할 수 있게 준비하는 것</p>
<p>var, let const 키워드를 사용해서 변수를 선언해야지만 변수 사용 가능<br>
변수 선언을 통해 확보된 메모리 공간에는 자바스크립트 엔진에 의해 undefined라는 값이 암묵적으로 할당되어 초기화된다.</p>
<p>변수 이름을 비롯한 모든 식별자와 그 값은 실행 컨텍스트내에 key/value 형식인 객체로 등록되어 관리된다.</p>
<h2 id="변수-선언의-실행-시점과-변수-호이스팅">4.4 변수 선언의 실행 시점과 변수 호이스팅</h2>
<p>소스코드를 한 줄씩 순차적으로 실행하기에 앞서 소스콛의 평가 과정에서 자바스크립트 엔진은 변수 선언을 포함한 모든 선언문을 소스코드에서 찾아내 먼저 실행한다.</p>
<p><strong>변수 호이스팅</strong>: 변수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징(모든 선언된 식별자는 동일)</p>
<h2 id="값의-할당">4.5 값의 할당</h2>
<p>자바스크립트 엔진은 변수 선언과 값의 할당을 하나의 문(statement)으로 단축 표현해도 변수 선언과 값의 할당을 2개의 문으로 나누어 각각 실행</p>
<p>변수에 값을 할당할 때는 이전 값 undefined가 저장되어 있던 공간을 지우고 새로 저장하는 것이 아닌 <mark>새로운 메모리 공간을 확보</mark>하고 그곳에 할당값을 저장한다는 점에 주의</p>
<h2 id="값의-재할당">4.6 값의 재할당</h2>
<p>재할당은 현재 변수에 저장된 값ㅇ르 버리고 새로운 값을 저장하는 것<br>
const 키워드를 사용한 상수는 재할당 불가<br>
어떤 식별자와도 연결되어 있지 않은 불필요한 값들은 가비지 콜렉터에 의해 메모리에서 자동 해제된다. — managed language</p>
<blockquote>
<p>가비지 콜렉터: 애플리케이션이 할당한 메모리 공간을 주기적으로 검사하여 더 이상 사용되지 않는 메모리(어떤 식별자도 참조하지 않는 메모리 공간)를 해제하는 기능 -&gt; 메모리 누수 방지</p>
</blockquote>
<h2 id="식별자-네이밍-규칙">4.7 식별자 네이밍 규칙</h2>
<ul>
<li>식별자는 문자, 숫자, 언더스코어, 달러 기호 포함 가능</li>
<li>숫자로 시작 불가</li>
<li>예약어는 식별자로 사용 불가</li>
</ul>
<h1 id="표현식과-문">5. 표현식과 문</h1>
<h2 id="값">5.1 값</h2>
<p>값: 표현식(expression)이 평가(evaluate)되어 생성된 결과</p>
<h2 id="리터럴">5.2 리터럴</h2>
<p>리터럴(literal)은 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해 값을 생성하는 표기법</p>
<h2 id="표현식">5.3 표현식</h2>
<p>표현식은 값으로 평가될 수 있는 문. 표현식이 평가되면 새로운 값을 생성하거나 기존 값을 참조한다.<br>
값으로 평가될 수 있는 문은 모든 표현식이다.</p>
<h2 id="문">5.4 문</h2>
<p>문(statement)은 프로그램을 구성하는 기본 단위이자 최소 실행 단위<br>
문은 여러 토큰으로 구성<br>
토큰은 문법적인 의미를 가지며, 문법적으로 더 이상 나눌 수 없는 코드의 기본 요소를 의미(ex. 키워드, 식별자, 연산자, 리터럴, 세미콜론 등)</p>
<h2 id="세미콜론">5.5 세미콜론</h2>
<p>세미콜론은 문의 종료를 나타낸다.<br>
코드 블록({…}) 뒤에는 세미콜론을 붙이지 않는다<br>
자바스크립트 엔진의 세미콜론 자동 삽입 기능이 암묵적으로 수행되지만, 붙이는 것을 권장</p>
<h2 id="표현식인-문과-표현식이-아닌-문">5.6 표현식인 문과 표현식이 아닌 문</h2>
<p>표현식인 문은 값으로 평가될 수 있는 문<br>
구분하는 가장 간단한 방법은 변수에 할당해 보는 것</p>
<h1 id="장-데이터-타입">6장 데이터 타입</h1>
<h2 id="숫자-타입">6.1 숫자 타입</h2>
<p>int, double 등 구분이 없이 배정밀도 64비트 부동소수점 형식을 따름<br>
2진수, 8진수 등을 표현하기 위한 데이터 타입을 제공하지 않기 때문에 이들 값을 참조하면 모두 10진수로 해석<br>
추가적으로 Infinity, NaN 표현</p>
<h2 id="문자열-타입">6.2 문자열 타입</h2>
<p>자바스크립트의 문자열은 원시 타입이며 변경 불가능한 값이다.</p>
<h2 id="템플릿-리터럴">6.3 템플릿 리터럴</h2>
<p>백틱(`)을 사용해 표현</p>
<h3 id="멀티라인-문자열">6.3.1 멀티라인 문자열</h3>
<p>일반 문자열 내에서는 줄바꿈이 허용되지 않으므로 이스케이프 시퀀스를 사용해야 함<br>
템플릿 리터럴 내에서는 이스케이프 시퀀스를 사용하지 않고도 줄바꿈이 허용되며, 모든 공백도 있는 그대로 적용</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> template <span class="token operator">=</span> <span class="token template-string"><span class="token string">`&lt;ul&gt;
  &lt;li&gt;&lt;a href=“”#&gt;Home&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;`</span></span><span class="token punctuation">;</span>
</code></pre>
<h3 id="표현식-삽입">6.3.2 표현식 삽입</h3>
<p>문자열은 문자열 연산자+를 사용해 연결할 수 있다.<br>
템플릿 리터럴 내에서는 표현식 삽입(expression interpolation)을 통해 간단히 문자열 삽입 가능</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> first <span class="token operator">=</span> ‘Ung<span class="token operator">-</span>mo’<span class="token punctuation">;</span>
<span class="token keyword">var</span> last <span class="token operator">=</span> ‘Lee’<span class="token punctuation">;</span>

console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token template-string"><span class="token string">`My name is </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>first<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>last<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.`</span></span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>문자열이 아니더라도 문자열로 타입이 강제로 변환되어 삽입된다.</p>
<h2 id="불리언-타입">6.4 불리언 타입</h2>
<p>true, false</p>
<h2 id="undefined-타입">6.5 undefined 타입</h2>
<p>var 키워드로 선언한 변수는 암묵적으로 undefined로 초기화 된다.<br>
변수를 참조했을 때 undefined가 반환된다면 참조한 변수가 선언 이후 값이 할당된 적 없는, 초기화 되지 않은 변수라는 것을 알 수 있음<br>
변수에 값이 없다는 것을 명시하고 싶을 때는 null을 할당</p>
<h2 id="null-타입">6.6 null 타입</h2>
<p>이전에 할당되어 있던 값에 대한 참조를 명시적으로 제거하는 것을 의미미함수가 유효한 값을 반환할 수 없는 경우 명시적으로 null을 반환하기도 함</p>
<h2 id="심벌-타입">6.7 심벌 타입</h2>
<p>심벌 값은 다른 값과 중복되지 않는 유일무이한 값<br>
주로 이름이 충돌할 위험이 없는 객체의 유일한 프로퍼티 키를 만들기 위해 사용</p>
<h2 id="객체-타입">6.8 객체 타입</h2>
<p>6가지 데이터 타입 이외의 값은 모두 객체 타입</p>
<h2 id="데이터-타입의-필요성">6.9 데이터 타입의 필요성</h2>
<h3 id="데이터-타입에-의한-메모리-공간의-확보와-참조">6.9.1 데이터 타입에 의한 메모리 공간의 확보와 참조</h3>
<p>값은 메모리에 저장하고 참조할 수 있어야 하므로, 먼저 확보해야 할 메모리 공간의 크기를 결정해야 한다.<br>
값의 타입을 기준으로 한번에 읽어들여야 할 메모리 공간의 크기를 알아야 값이 훼손되지 않음</p>
<blockquote>
<p>심벌 테이블: 컴파일러 또는 인터프리터가 식별자를 키로 바인딩된 값의 메모리 주소, 데이터 타입, 스코프 등을 관리하는 자료구조</p>
</blockquote>
<h3 id="데이터-타입에-의한-값의-해석">6.9.2 데이터 타입에 의한 값의 해석</h3>
<p>2진수로 저장된 메모리 값을 타입에 따라서 해석하게 됨</p>
<h2 id="동적-타이핑">6.10 동적 타이핑</h2>
<h3 id="동적-타입-언어와-정적-타입-언어">6.10.1 동적 타입 언어와 정적 타입 언어</h3>
<p>정적 타입 언어는 변수를 선언할 때 데이터 타입을 사전에 선언 — 명시적 타입 선언<br>
정적 타입 업어는 컴파일 시점에 타입 체크를 수행하여 런타임 에러를 줄인다.</p>
<p>자바스크립트에서는 값을 할당하는 시점에 변수의 타입이 결정되고 변수의 타입을 언제든지 자유롭게 변경할 수 있다.<br>
변수는 선언이 아니라 할당에 의해 타입이 결정(타입 추론)<br>
재할당에 의해 변수의 타입은 언제든지 동적으로 변할 수 있다 — 동적 타이핑</p>
<h3 id="동적-타입-언어와-변수">6.10.2 동적 타입 언어와 변수</h3>
<p>변수 값은 언제든지 변경도리 수 있기 때문에 변화하는 값을 추적하기 어려울 수 있다. — 동적 타입 언어의 변수는 값을 확인하기 전에는 타입을 확신할 수 없다<br>
개발자의 의도와는 상관없이 자바스크립트 엔진에 의해 암묵적으로 타입이 자동으로 변환되기도 한다.</p>
<h1 id="장-연산자">7장 연산자</h1>
<h2 id="산술-연산자">7.1 산술 연산자</h2>
<p>피연산자를 대상으로 수학적 계산ㅇ르 수행해 새로운 숫자 값을 만든다. 산술 연산이 불가능한 경우 NaN을 반환</p>
<h3 id="이항-산술-연산자">7.1.1 이항 산술 연산자</h3>
<p>모든 이항 산술 연산자는 피연산자의 값을 변경하는 부수 효과(side effect)가 없다.</p>
<h3 id="단항-산술-연산자">7.1.2 단항 산술 연산자</h3>
<p>증가/감소(++/–) 연산자는 피연산자의 값을 변경하는 부수 효과<br>
전위 증가/감소 연산자: 피연산자의 값을 증가/감소 후 다른 연산을 수행<br>
후위 증가/감소 연산자: 먼저 다른 연산을 수행한 후 피연산자의 값을 증가/감소</p>
<p>숫자 타입이 아닌 피연산자에 + 단항 연산자를 사용하면 피연산자를 숫자 타입으로 변환하여 반환한다.(부수 효과는 없고 변환한 값을 생성해서 반환)</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token operator">+</span><span class="token punctuation">(</span><span class="token operator">-</span><span class="token number">10</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// -&gt; -10 (음수를 양수로 변환하지 않음)</span>

<span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token boolean">false</span>
<span class="token operator">+</span>x<span class="token punctuation">;</span> <span class="token comment">// -&gt; 0</span>
x<span class="token punctuation">;</span> <span class="token comment">// -&gt; false (부수 효과 없음)</span>

x <span class="token operator">=</span> ‘Hello’
<span class="token operator">+</span>x<span class="token punctuation">;</span> <span class="token comment">// -&gt; NaN</span>
</code></pre>
<h3 id="문자열-연결-연산자">7.1.3 문자열 연결 연산자</h3>
<p>+연산자는 피연산자 중 하나 이상이 문자열인 경우 문자열 연결 연산자로 동작</p>
<h2 id="할당-연산자">7.2 할당 연산자</h2>
<p>할당문은 값으로 평가되는 표현식인 문으로서 할당된 값으로 평가<br>
이런 특징을 활용해 동일한 값으로 연쇄 할당 가능</p>
<h2 id="비교-연산자">7.3 비교 연산자</h2>
<h3 id="동등일치-비교-연산자">7.3.1 동등/일치 비교 연산자</h3>
<p>동등 비교(loose equality): 값이 같음 — 먼저 암묵적 타입 변환을 통해 타입을 일치시킨 후 같은 값인지 비교<br>
일치 비교(strict equality): 값과 타입이 같음</p>
<p>NaN은 자신과 일치하지 않는 유일한 값이다.<br>
양의 0과 음의 0이 있는데 이들을 비교하면 true임</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token operator">-</span><span class="token number">0</span> <span class="token operator">===</span> <span class="token operator">+</span><span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// true</span>
Object<span class="token punctuation">.</span><span class="token function">is</span><span class="token punctuation">(</span><span class="token operator">-</span><span class="token number">0</span><span class="token punctuation">,</span> <span class="token operator">+</span><span class="token number">0</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// false</span>
<span class="token number">NaN</span> <span class="token operator">===</span> <span class="token number">NaN</span><span class="token punctuation">;</span> <span class="token comment">// false</span>
Object<span class="token punctuation">.</span><span class="token function">is</span><span class="token punctuation">(</span><span class="token number">NaN</span><span class="token punctuation">,</span><span class="token number">NaN</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true</span>
</code></pre>
<h3 id="대소-관계-비교-연산자">7.3.2 대소 관계 비교 연산자</h3>
<h2 id="삼항-조건-연산자">7.4 삼항 조건 연산자</h2>
<p>조건식 ? 조건식이 true일 때 반환할 값 : 조건식이 false일 때 반환할 값</p>
<p>삼항 조건 연산자 표현식은 값으로 평가할 수 있는 표현식인 문</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> result <span class="token operator">=</span> x <span class="token operator">%</span> <span class="token number">2</span> <span class="token operator">?</span> ‘홀수’ <span class="token punctuation">:</span> ‘짝수’<span class="token punctuation">;</span>
</code></pre>
<h2 id="논리-연산자">7.5 논리 연산자</h2>
<p>표현식의 평가 시 피연산자가 불리언 값이 아니면 불리언 타입으로 암묵적 타입 변환</p>
<h2 id="쉼표-연산자">7.6 쉼표 연산자</h2>
<p>왼쪽 연산자부터 차례대로 피연산자를 평가하고 마지막 피연산자의 평가가 끝나면 마지막 피연산자의 평가 결과를 반환</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> x<span class="token punctuation">,</span> y<span class="token punctuation">,</span> z<span class="token punctuation">;</span>
x <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">,</span> y <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">,</span> z <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span> <span class="token comment">// 3</span>
</code></pre>
<h2 id="그룹-연산자">7.7 그룹 연산자</h2>
<p>소괄호로 피연산자를 감싸며 연산자 우선순위가 가장 높다</p>
<h2 id="typeof-연산자">7.8 typeof 연산자</h2>
<p>피연산자의 데이터 타입을 문자열로 반환</p>
<p>typeof 연산자로 null 값을 연산하면 null이 아닌 object를 반환하므로 값이 null 타입인지 확인할 때는 일치 연산자(===)를 사용</p>
<h2 id="지수-연산자">7.9 지수 연산자</h2>
<p>지수 연산자는 이항 연산자 중에서 우선순위가 가장 높다</p>
<h2 id="그-외의-연산자">7.10 그 외의 연산자</h2>

<table>
<thead>
<tr>
<th>연산자</th>
<th>개요</th>
</tr>
</thead>
<tbody>
<tr>
<td>?.</td>
<td>옵셔널 체이닝 연산자</td>
</tr>
<tr>
<td>??</td>
<td>null 병합 연산자</td>
</tr>
<tr>
<td>delete</td>
<td>프로퍼티 삭제</td>
</tr>
<tr>
<td>new</td>
<td>생성자 함수를 호출할 때 사용하여 인스턴스를 생성</td>
</tr>
<tr>
<td>instanceof</td>
<td>좌변의 객체가 우변의 생성자 함수와 연결된 인스턴스인지 판별</td>
</tr>
<tr>
<td>in</td>
<td>프로퍼티 존재 확인</td>
</tr>
</tbody>
</table><h2 id="연산자의-부수-효과">7.11 연산자의 부수 효과</h2>
<p>부수 효과(side effect)가 있는 연산자는 할당 연산자(=), 증가/감소 연산자(++/–), delete 연산자다.</p>
<h2 id="연산자-우선순위">7.12 연산자 우선순위</h2>
<h2 id="연산자-결합-순서">7.13 연산자 결합 순서</h2>
<p>좌항-&gt;우항인지 우항-&gt;좌항인지</p>
<h1 id="장-제어문">8장 제어문</h1>
<p>일반적인 코드는 위에서 아래 방향으로 순차적으로 실행되지만, 제어문을 사용하면 코드의 실행 흐름을 인위적으로 제어할 수 있다.</p>
<h2 id="블록문">8.1 블록문</h2>
<p>문을 중괄호로 묶은 것<br>
블록문은 언제나 문의 종료를 의미하는 자체 종결성을 갖기 때문에 블록문의 끝에는 세미콜론을 붙이지 않는다</p>
<h2 id="조건문">8.2 조건문</h2>
<h3 id="if-…-else-문">8.2.1 if … else 문</h3>
<h3 id="switch-문">8.2.2 switch 문</h3>
<p>if … else 문이 조건식은 불리언 값으로 평가되어야 하지만, switch 문의 표현식이 불리언 값보다는 문자열이나 숫자값인 경우가 많다<br>
break 키워드를 통해 switch문을 빠져나가지 않으면 fall through가 됨</p>
<h2 id="반복문">8.3 반복문</h2>
<h3 id="for-문">8.3.1 for 문</h3>
<h3 id="while-문">8.3.2 while 문</h3>
<h3 id="do-…-while-문">8.3.3 do … while 문</h3>
<h2 id="break-문">8.4 break 문</h2>
<p>코드 블록을 탈출<br>
다중 for문에서 lable이 붙은 문으로 탈출도 가능</p>
<h2 id="continue-문">8.5 continue 문</h2>
<p>반복문의 코드 블록 실행을 현 지점에서 중단하고 반복문의 증감식으로 실행 흐름을 이동</p>
<p>if문 내에서 실행해야 할 코드가 길다면 들여쓰기가 한 단계 더 깊어지므로 continue를 사용하는 편이 가독성이 좋다</p>
<h1 id="장-타입-변환과-단축-평가">9장 타입 변환과 단축 평가</h1>
<h2 id="타입-변환이란">9.1 타입 변환이란?</h2>
<p><strong>명시적 타입 변환(타입 캐스팅)</strong>: 개발자가 의도적으로 값의 타입을 변환<br>
<strong>암묵적 타입 변환(타입 강제 변환)</strong>: 개발자의 의도와는 상관없이 표현식을 평가하는 도중에 자바스크립트 엔진에 의해 암묵적으로 타입이 변환</p>
<p><mark>원시값은 변경 불가능한 값</mark>이므로 기존 원시값을 변경하는 것이 아닌 새로운 원시 값을 생성하는 것</p>
<h2 id="암묵적-타입-변환">9.2 암묵적 타입 변환</h2>
<h3 id="문자열-타입으로-변환">9.2.1 문자열 타입으로 변환</h3>
<p>문자열 연결 연산자 표현식을 평가하기 위해 피연산자를 문자열 타입으로 암묵적 타입 변환</p>
<h3 id="숫자-타입으로-변환">9.2.2 숫자 타입으로 변환</h3>
<p>산술 연산자의 표현식을 평가하기 위해 피연사를 숫자 타입으로 암묵적 타입 변환<br>
비교 연산자(&gt;)와 같이 크기를 비교할 경우 숫자 타입으로 변환<br>
단항 연상자+도 숫자 타입으로 변환</p>
<p>객체와 빈 배열이 아닌 배열, undefined는 NaN으로 변환</p>
<h3 id="불리언-타입으로-변환">9.2.3 불리언 타입으로 변환</h3>
<p>Falsy: false, undefined, null, 0, -0, NaN, 빈 문자열<br>
Truthy: Falsy가 아닌 모든 값</p>
<h2 id="명시적-타입-변환">9.3 명시적 타입 변환</h2>
<h3 id="문자열-타입으로-변환-1">9.3.1 문자열 타입으로 변환</h3>
<ol>
<li>String 생성자 함수를 new 연산자 없이 호출하는 방법</li>
<li>Object.prototype.toString 메서드를 사용하는 방법</li>
<li>문자여려 연결 연산자를 이용하는 방법</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">String</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// -&gt; “1”</span>
<span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">toString</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// -&gt; “1”</span>
<span class="token number">1</span> <span class="token operator">+</span> ‘’<span class="token punctuation">;</span> <span class="token comment">// -&gt; “1”</span>
</code></pre>
<h3 id="숫자-타입으로-변환-1">9.3.2 숫자 타입으로 변환</h3>
<ol>
<li>Number 생성자 함수를 new 연산자 없이 호출하는 방법</li>
<li>parseInt.parseFloat 함수를 사용하는 방법(문자열만 가능)</li>
<li>+단항 산술 연산자를 이용하는 방법</li>
<li>*산술 연산자를 이용하는 방법</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">Number</span><span class="token punctuation">(</span>‘<span class="token number">0</span>’<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token function">parseInt</span><span class="token punctuation">(</span>‘<span class="token number">0</span>’<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token operator">+</span>’<span class="token number">0</span>’<span class="token punctuation">;</span>
’<span class="token number">0</span>’ <span class="token operator">*</span> <span class="token number">1</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="불리언-타입으로-변환-1">9.3.3 불리언 타입으로 변환</h3>
<ol>
<li>Boolean 생성자 함수를 new 연산자 없이 호출하는 방법</li>
<li>! 부정 논리 연산자를 두 번 사용하는 방법</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">Boolean</span><span class="token punctuation">(</span>‘x’<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// -&gt; true</span>
<span class="token operator">!</span><span class="token operator">!</span>’x’<span class="token punctuation">;</span> <span class="token comment">// -&gt; true</span>
</code></pre>
<h2 id="단축-평가">9.4 단축 평가</h2>
<h3 id="논리-연산자를-사용한-단축-평가">9.4.1 논리 연산자를 사용한 단축 평가</h3>
<p><strong>단축 평가(short-circuit evaluation)</strong>: 표현식을 평가하는 도중에 평가 결과가 확정된 경우 나머지 평가 과정을 생략하는 것<br>
논리곱(&amp;&amp;) 연산자와 논리합(||) 연산자는 논리 연산의 결과를 결정하는 피연산자를 타입 변환하지 않고 그대로 반환</p>
<p>단축 평가의 유용한 패턴</p>
<ol>
<li><strong>객체를 가리키기를 기대하는 변수가 null 또는 undefined가 아닌지 확인하고 프로퍼티를 참조할 때</strong><br>
객체를 가리키기를 기대하는 변수의 값이 객체가 아니라 null 또는 undefined일 경우 객체의 프로퍼티를 참조하면 타입 에러가 발생</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> elem <span class="token operator">=</span> <span class="token keyword">null</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> value <span class="token operator">=</span> elem <span class="token operator">&amp;&amp;</span> elem<span class="token punctuation">.</span>value<span class="token punctuation">;</span> <span class="token comment">// -&gt; null</span>
</code></pre>
<ol start="2">
<li><strong>함수 매개변수에 기본값을 설정할 때</strong><br>
함수를 호출할 때 인술르 전달하지 않으면 매개변수에는 undefined가 할당되므로 단축 평가를 이용하여 기본값을 전달하면 에러 방지 가능</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// 단축 평가를 사용한 매개변수의 기본값 설정</span>
<span class="token keyword">function</span> <span class="token function">getStringLength</span><span class="token punctuation">(</span>str<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  str <span class="token operator">=</span> str <span class="token operator">||</span> ‘’<span class="token punctuation">;</span>
  <span class="token keyword">return</span> str<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">// ES6의 매개변수의 기본값 설정</span>
<span class="token keyword">function</span> <span class="token function">getStringLength</span><span class="token punctuation">(</span>str <span class="token operator">=</span> ‘’<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> str<span class="token punctuation">.</span><span class="token function">length</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="옵셔널-체이닝-연산자">9.4.2 옵셔널 체이닝 연산자</h3>
<p>옵셔널 체이닝 연산자 <code>?.</code>는 좌항의 피연산자가 null 또는 undefined인 경우 undefined를 반환하고, 그렇지 않으면 우항의 프로퍼티 참조를 이어감</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> str <span class="token operator">=</span> ‘’<span class="token punctuation">;</span>

<span class="token comment">// 단축 평가는 Falsy 값의 경우 평가되지 않는 경우가 있음</span>
<span class="token keyword">var</span> length <span class="token operator">=</span> str <span class="token operator">&amp;&amp;</span> str<span class="token punctuation">.</span>length<span class="token punctuation">;</span> <span class="token comment">// -&gt; ‘’</span>

<span class="token comment">// 옵셔널 체이닝으로는 null 또는 undefined가 아니므로 프로퍼티 참조 가능</span>
length <span class="token operator">=</span> str<span class="token operator">?</span><span class="token punctuation">.</span>length<span class="token punctuation">;</span> <span class="token comment">//  -&gt; 0</span>
</code></pre>
<h3 id="null-병합-연산자">9.4.3 null 병합 연산자</h3>
<p>null 병합 연산자 <code>??</code>는 좌항의 피연산자가 null 또는 undefined인 경우 우항의 피연산자를 반환, 아니면 좌항의 피연산자를 반환 — 변수에 기본값 설정할 때 유용</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// 단축평가의 경우 Falsy값이 기본값으로 유용할 경우에 예기치 않은 동작 발생 가능</span>
<span class="token keyword">var</span> foo <span class="token operator">=</span> ‘’ <span class="token operator">||</span> ‘<span class="token keyword">default</span> string’<span class="token punctuation">;</span> <span class="token comment">// “default string”</span>

<span class="token comment">// null 병합 연산자는 null 또는 undefined가 아니므로 좌항의 피연산자 그대로 반환</span>
foo <span class="token operator">=</span> ‘’ <span class="token operator">?</span><span class="token operator">?</span> ‘<span class="token keyword">default</span> string’<span class="token punctuation">;</span> <span class="token comment">// “”</span>
</code></pre>
<h1 id="장-객체-리터럴">10장 객체 리터럴</h1>
<h2 id="객체란">10.1 객체란?</h2>
<p>원시 값을 제외한 나머지 값(함수, 배열, 정규 표현식 등)은 모두 객체다<br>
객체 타입은 다양한 타입의 값을 하나의 단위로 구성한 복합적인 자료구조이며, <strong>변경 가능한 값</strong>이다.<br>
객체는 0개 이상의 프로퍼티로 구성된 집합이며, 프로퍼티는 key와 value로 구성된다.</p>
<p>자바스크립트 함수는 일급 객체이므로 값으로 취급할 수 있으며, 따라서 프로퍼티 값으로 사용할 수 있음 — 이 경우 메서드라고 부름</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> counter <span class="token operator">=</span> <span class="token punctuation">{</span>
  num<span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span> <span class="token comment">// 프로퍼티 (num이 key, 0이 value)</span>
  increase<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// 메서드</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span>num<span class="token operator">++</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>프로퍼티: 객체의 상태를 나타내는 값(data)</li>
<li>메서드: 프로퍼티를 참조하고 조작할 수 있는 동작</li>
</ul>
<h2 id="객체-리터럴에-의한-객체-생성">10.2 객체 리터럴에 의한 객체 생성</h2>
<p>자바스크립트는 프로토타입 기반 객체지향 언어로서 클래스 기반 객체지향 언어와는 다리 다양한 객체 생성 방법을 지원</p>
<ul>
<li>객체 리터럴</li>
<li>Object 생성자 함수</li>
<li>생성자 함수</li>
<li>Object.create 메서드</li>
<li>클래스</li>
</ul>
<p>가장 일반적이고 간단한 방법은 객체 리터럴을 사용하는 방법<br>
중괄호 내에 0개 이상의 프로퍼티를 정의</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> person <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’<span class="token punctuation">,</span>
  sayHello<span class="token punctuation">:</span> <span class="token function">fuction</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token template-string"><span class="token string">`Hello! myname is </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span><span class="token keyword">this</span><span class="token punctuation">.</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.`</span></span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> empty <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">;</span> <span class="token comment">// 빈 객체</span>
</code></pre>
<p>객체 리터럴의 중괄호는 코드 블록을 의미하지 않음. 값으로 평가되는 표현식이므로 세미콜론을 붙인다.</p>
<h2 id="프로퍼티">10.3 프로퍼티</h2>
<p>객체는 프로퍼티의 집합이며, 프로퍼티는 키와 값으로 구성된다.<br>
프로퍼티 키는 문자열 또는 심벌 값을 사용할 수 있고, 식별자 네이밍 규칙을 준수하는 이름의 경우 따옴표를 생략할 수 있다.<br>
프로퍼티 키로 사용할 표현식을 대괄호로 묶어 프로퍼티 키를 동적으로 생성할 수도 있다.<br>
객체를 만들 때 객체 리터럴 안의 프로퍼티 키가 대괄호로 둘러싸여 있는 경우 <em>계산된 프로퍼티</em> 라고 부름</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> person <span class="token operator">=</span> <span class="token punctuation">{</span>
  firstName<span class="token punctuation">:</span> ‘Taewoo’<span class="token punctuation">,</span> <span class="token comment">// 식별자 네이밍 규칙을 준수 -&gt; 따옴표 생략</span>
  ’last<span class="token operator">-</span>name’<span class="token punctuation">:</span> ‘Kang’ <span class="token comment">// 식별자 네이밍 규칙을 준수하지 않음</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token comment">// ES5: 프로퍼티 키 동적 생성</span>
person<span class="token punctuation">[</span>age<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token number">29</span><span class="token punctuation">;</span>
<span class="token comment">// ES6: 계산된 프로퍼티 이름</span>
<span class="token comment">// var person = { [age]: ‘29 };</span>
</code></pre>
<p>이미 존재하는 프로퍼티 키를 중복 선언하면 나중에 선언한 프로퍼티가 먼저 선언한 프로퍼티를 덮어쓴다.</p>
<h2 id="메서드">10.4 메서드</h2>
<p>자바스크립트의 함수는 일급 객체이므로 값으로 취급할 수 있어 프로퍼티 값으로 사용 가능 — 메서드</p>
<h2 id="프로퍼티-접근">10.5 프로퍼티 접근</h2>
<ul>
<li>마침표 표기법: <code>person.name</code></li>
<li>대괄호 표기법: <code>person[‘name’]</code> 처럼 대괄호 프로퍼티 접근 연산자 내부에 지정하는 <strong>프로퍼티 키는 반드시 따옴표로 감싼 문자열</strong>이어야 한다.<br>
프로퍼티 키가 숫자로 이뤄진 문자열인 경우 따옴표를 생략할 수 있다.</li>
</ul>
<p>프로퍼티 키가 식별자 네이밍 규칙을 준수하는 이름일 경우 마침표 표기법과 대괄호 표기법 모두 사용할 수 있다.</p>
<p>객체에 존재하지 않는 프로퍼티에 접근함녀 undefined를 반환한다.</p>
<h2 id="프로퍼티-값-갱신">10.6 프로퍼티 값 갱신</h2>
<p>이미 존재하는 프로퍼티에 값을 할당하면 프로퍼티 값이 갱신</p>
<h2 id="프로퍼티-동적-생성">10.7 프로퍼티 동적 생성</h2>
<p>존재하지 않는 프로퍼티에 값을 할당하면 프로퍼티가 동적으로 생성되어 추가되고 프로퍼티 값이 할당</p>
<h2 id="프로퍼티-삭제">10.8 프로퍼티 삭제</h2>
<p>delete 연산자는 객체의 프로퍼티를 삭제<br>
만약 존재하지 않는 프로퍼티를 삭제하면 아무런 에러 없이 무시된다.</p>
<h2 id="es6에서-추가된-객체-리터럴의-확장-기능">10.9 ES6에서 추가된 객체 리터럴의 확장 기능</h2>
<h3 id="프로퍼티-축약-표현">10.9.1 프로퍼티 축약 표현</h3>
<p>프로퍼티 값으로 변수를 사용하는 경우 변수 이름과 프로퍼티 키가 동일한 이름일 때 프로퍼티 키를 생략할 수 있다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> x <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">,</span> y <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> obj <span class="token operator">=</span> <span class="token punctuation">{</span> x<span class="token punctuation">,</span> y <span class="token punctuation">}</span><span class="token punctuation">;</span> <span class="token comment">// 프로퍼티 축약 표현</span>
</code></pre>
<h3 id="계산된-프로퍼티-이름">10.9.2 계산된 프로퍼티 이름</h3>
<p>프로퍼티 키로 사용할 표현식을 대괄호로 묶어 값으로 평가되는 표현식을 사용해 프로퍼티 키를 동적으로 생성할 수 있음</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> frefix <span class="token operator">=</span> ‘prop’<span class="token punctuation">;</span>
<span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>

<span class="token comment">// ES5</span>
<span class="token keyword">var</span> <span class="token operator">=</span> obj <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">;</span>
obj<span class="token punctuation">[</span>prefix <span class="token operator">+</span> ‘<span class="token operator">-</span>‘ <span class="token operator">+</span> <span class="token operator">++</span>i<span class="token punctuation">]</span> <span class="token operator">=</span> i<span class="token punctuation">;</span>
obj<span class="token punctuation">[</span>prefix <span class="token operator">+</span> ‘<span class="token operator">-</span>‘ <span class="token operator">+</span> <span class="token operator">++</span>i<span class="token punctuation">]</span> <span class="token operator">=</span> i<span class="token punctuation">;</span>

<span class="token comment">// ES6</span>
<span class="token keyword">const</span> obj <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token punctuation">[</span><span class="token template-string"><span class="token string">`</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>prefix<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">-</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span><span class="token operator">++</span>i<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">`</span></span><span class="token punctuation">]</span><span class="token punctuation">:</span> i<span class="token punctuation">,</span>
  <span class="token punctuation">[</span><span class="token template-string"><span class="token string">`</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>prefix<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">-</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span><span class="token operator">++</span>i<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">`</span></span><span class="token punctuation">]</span><span class="token punctuation">:</span> i
<span class="token punctuation">}</span><span class="token punctuation">;</span>

console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>obj<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// {prop-1: 1, prop-2: 2}</span>
</code></pre>
<h3 id="메서드-축약-표현">10.9.3 메서드 축약 표현</h3>
<p>메서드를 정의할 때 function 키워드를 생략한 축약 표현을 사용 가능</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> obj <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’<span class="token punctuation">,</span>
  <span class="token function">sayHi</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// 메서드 축약 표현</span>
    <span class="token function">consolelog</span><span class="token punctuation">(</span>‘Hi<span class="token operator">!</span> ` <span class="token operator">+</span> <span class="token keyword">this</span><span class="token punctuation">.</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
</code></pre>
<h1 id="원시-값과-객체의-비교">11. 원시 값과 객체의 비교</h1>

<table>
<thead>
<tr>
<th>원시 값</th>
<th>객체</th>
</tr>
</thead>
<tbody>
<tr>
<td>변경 불가능한 값</td>
<td>변경 가능한 값</td>
</tr>
<tr>
<td>실제 값이 저장</td>
<td>참조 값이 저장</td>
</tr>
<tr>
<td>값에 의한 전달</td>
<td>참조에 의한 전달</td>
</tr>
</tbody>
</table><h2 id="원시-값">11.1 원시 값</h2>
<h3 id="변경-불가능한-값">11.1.1 변경 불가능한 값</h3>
<p>변경 불가능하다는 것은 변수가 아니라 값에 대한 진술이다.</p>
<p>재할당 시 변수가 참조하던 메모리 공간의 주소가 변경되는 이유는 변수에 할당된 원시 값이 변경 불가능한 값이기 때문</p>
<p>불변성(immutability)을 갖는 원시 값을 할당한 변수는 재할당 이외에 변수 값을 변경할 수 있는 방법이 없다.</p>
<h3 id="문자열과-불변성">11.1.2 문자열과 불변성</h3>
<p>자바스크립트의 문자열은 원시 타입이며, 변경 불가능하다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> str <span class="token operator">=</span> ‘string’<span class="token punctuation">;</span>
str<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span> <span class="token operator">=</span> ‘S’<span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>str<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// string (변하지 않음!)</span>
</code></pre>
<h3 id="값에-의한-전달">11.1.3 값에 의한 전달</h3>
<p>원시 값을 갖는 변수를 할당하면 값이 복사되어 전달 — 값에 의한 전달<br>
할당받는 변수는 서로 다른 메모리 공간에 저장된 별개의 값임</p>
<h2 id="객체">11.2 객체</h2>
<p>객체는 원시 값과 같이 확보해야 할 메모리 공간의 크기를 사전에 정해둘 수 없다.<br>
경우에 따라 객체를 생성하고 프로퍼티에 접근하는 것도 많은 비용이 들 수 있으므로 원시 값과는 다른 방식으로 동작하도록 설계</p>
<h3 id="변경-가능한-값">11.2.1 변경 가능한 값</h3>
<p>객체는 할당한 변수가 기억하는 메모리 주소를 통해 메모리 공간 참조값에 접근<br>
메모리를 효율적으로 사용하기 위해, 그리고 객체를 복사해 생성하는 비용을 절약하여 성능을 향상시키기 위해 객체는 변경 가능한 값으로 설계됨<br>
단, 구조적 단점으로 여러 개의 식별자가 하나의 객체를 공유할 수 있음</p>
<h3 id="참조에-의한-전달">11.2.2 참조에 의한 전달</h3>
<p>객체를 가리키는 변수를 다른 변수에 할당하면 원본의 참조값이 복사되어 전달된다 — 참조에 의한 전달<br>
두 변수가 저장된 메모리 주소는 다르지만 동일한 객체의 참조값을 갖는다<br>
두 식별자가 하나의 객체를 공유함으로써 서로 영향을 주고받는다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> person1 <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’
<span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> person2 <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’
<span class="token punctuation">}</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>person1 <span class="token operator">===</span> person2<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 참조값 비교: false</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>person1<span class="token punctuation">.</span>name <span class="token operator">===</span> person2<span class="token punctuation">.</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 원시값 비교: true</span>
</code></pre>
<h1 id="함수">12. 함수</h1>
<h2 id="함수란">12.1 함수란?</h2>
<p>매개변수(parameter): 함수 정의 시 내부로 입력을 전달받는 변수<br>
인수(argument): 함수 호출 시 입력</p>
<h2 id="함수를-사용하는-이유">12.2 함수를 사용하는 이유</h2>
<p>코드의 재사용 측면에서 유용 -&gt; 유지보수 편의성을 높이고 실수를 줄요 코드의 신뢰성을 높인다.<br>
적절한 함수 이름을 사용함으로써 코드의 가독성을 향상시킨다.</p>
<h2 id="함수-리터럴">12.3 함수 리터럴</h2>
<p>함수는 객체 타입의 값이다.<br>
일반 객체는 호출할 수 없지만 함수는 호출할 수 있다.</p>
<h2 id="함수-정의">12.4 함수 정의</h2>
<h3 id="함수-선언문">12.4.1 함수 선언문</h3>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">add</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span> y<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p>함수 리터럴은 함수 이름을 생략할 수 있으나, 함수 선언문은 함수 이름을 생략할 수 없다.<br>
이름이 있는 기명 함수 리터럴은 코드 문맥에 따라 함수 선언문 또는 함수 리터럴 표현식으로 해석된다.<br>
함수 리터럴의 함수 이름은 함수 몸체 내에서만 참조할 수 있는 식별자이므로 호출상의 차이가 있다.<br>
자바스크립트 엔진은 함수 선언문으로 생성된 함수를 호출하기 위해 함수 이름과 동일한 이름의 식별자를 암묵적으로 생성하고 거기에 함수 객체를 할당한다.</p>
<blockquote>
<p>함수는 함수 이름으로 호출하는 것이 아니라 함수 객체를 가리키는 식별자로 호출한다.</p>
</blockquote>
<h3 id="함수-표현식">12.4.2 함수 표현식</h3>
<p>일급 객체: 값의 성질을 갖는 객체<br>
함수는 일급 객체이므로 함수 리터럴로 생성한 함수 객체를 변수에 할당할 수 있다 — 함수 표현식<br>
함수 표현식의 함수 리터럴은 함수 이름을 생략하는 것이 일반적</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> <span class="token function-variable function">add</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token function">foo</span> <span class="token punctuation">(</span>x<span class="token punctuation">,</span> y<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token comment">// 함수 객체를 가리키는 식별자로 호출</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">add</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="함수-생성-시점과-함수-호이스팅">12.4.3 함수 생성 시점과 함수 호이스팅</h3>
<p>함수 선언문으로 함수를 정의하면 런타임 이전에 함수 객체가 먼저 생성 — 함수 호이스팅</p>
<p>변수 호이스팅은 undefined로 초기화 되지만, 함수 선언문을 통해 암묵적으로 생성된 식별자는 함수 객체로 초기화 되어 함수 호이스팅에 의해 호출이 가능</p>
<p>함수 표현식으로 함수를 정의하면 함수 호이스팅이 아닌 변수 호이스팅이 발생되어 undefined로 초기화되어 미리 호출 불가</p>
<p>함수 호이스팅은 함수를 호출하기 전에 반드시 함수를 선언해야 한다는 당연한 규칙을 무시하므로 함수 표현식 사용을 권장</p>
<h3 id="function-생성자-함수">12.4.4 Function 생성자 함수</h3>
<p>Function 생성자 함수로 생성한 함수는 클로저를 생성하지 않는 등 함수 선언문이나 함수 표현식으로 생성한 함수와 다르게 동작한다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> add1 <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">var</span> a <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
  <span class="token keyword">return</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>x<span class="token punctuation">,</span> y<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> x <span class="token operator">+</span> y <span class="token operator">+</span> a<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> add2 <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">var</span> a <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
  <span class="token keyword">return</span> <span class="token keyword">new</span> <span class="token class-name">Function</span><span class="token punctuation">(</span>‘x’<span class="token punctuation">,</span> ‘y’<span class="token punctuation">,</span> ‘<span class="token keyword">return</span> x <span class="token operator">+</span> y <span class="token operator">+</span> a<span class="token punctuation">;</span>’<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">add1</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 13</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">add2</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// ReferenceError</span>
</code></pre>
<h3 id="화살표-함수">12.4.5 화살표 함수</h3>
<p>화살표 함수는 기존의 함수보다 표현만 간략한 것이 아니라 내부 동작 또한 간략화 되어있다.<br>
26.3절 화살표 함수에서 자세히 나옴</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> <span class="token function-variable function">add</span> <span class="token operator">=</span> <span class="token punctuation">(</span>x<span class="token punctuation">,</span> y<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">add</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 7</span>
</code></pre>
<h2 id="함수-호출">12.5 함수 호출</h2>
<h3 id="매개변수와-인수">12.5.1 매개변수와 인수</h3>
<p>함수를 실행하기 위해 필요한 값을 함수 외부에서 함수 내부로 전달할 필요가 있는 경우, 매개변수를 통해 인수를 전달한다.</p>
<p>매개변수의 스코프는 함수 내부이다.</p>
<p>인수가 부족해서 인수가 할당되지 않은 매개변수의 값은 undefined다.<br>
매개변수보다 인수가 더 많은 경우 초과된 인수는 무시된다.<br>
모든 인수는 암묵적으로 arguments 객체의 프로퍼티로 보관된다. — arguments 객체는 함수를 정의할 때 매개변수 개수를 확정할 수 없는 가변 인자 함수를 구현할 때 유용하게 사용된다.</p>
<h3 id="인수-확인">12.5.2 인수 확인</h3>
<ul>
<li>자바스크립트 함수는 매개변수와 인수의 개수가 일치하는지 확인하지 않음</li>
<li>자바스크립트 함수는 매개변수의 타입을 사전에 지정할 수 없음(동적 타입 언어)</li>
</ul>
<p>따라서 자바스크립트의 경우 함수를 정의할 때 적절한 인수가 전달되었는지 확인할 필요가 있다.<br>
부적절한 호출을 사전에 방지할 수는 없고 에러는 런타임에 발생하게 된다.</p>
<h3 id="매개변수의-최대-개수">12.5.3 매개변수의 최대 개수</h3>
<p>매개변수는 순서에 의미가 있으므로 매개변수가 많아지면 함수를 호출할 때 실수가 발생할 가능성을 높이므로 유지보수성이 나빠짐</p>
<p>함수의 매개변수는 코드를 이해하는 데 방해되는 요소이므로 이상적인 매개변수 개수는 0개이며 적을수록 좋다. — 매개변수의 개수가 많다는 것은 함수가 여러가지 일을 한다는 증거!</p>
<p>매개변수는 최대 3개 이상을 넘지 않는 것을 권장<br>
그 이상의 매개변수가 필요하다면 하나의 매개변수를 선언하고 객체를 인수로 전달하는 것이 유리하다.<br>
객체를 인수로 사용하는 경우 프로퍼티 키만 정확히 지정하면 매개변수의 순서를 신경쓰지 않아도 된다.</p>
<h3 id="반환문">12.5.4 반환문</h3>
<p>함수 호출 표현식은 return 키워드가 반환한 표현식의 평가 결과인 반환값으로 평가된다.<br>
return 키워드 뒤에 반환값으로 사용할 표현식을 명시적으로 지정하지 않으면 undefined가 반환된다.</p>
<h2 id="참조에-의한-전달과-외부-상태의-변경">12.6 참조에 의한 전달과 외부 상태의 변경</h2>
<p>객체 타입 인수는 참조값이 복사되어 매개변수에 전달되기 때문에 함수 몸체에서 참조값을 통해 객체를 변경할 경우 원본이 훼손될 수 있다.</p>
<p>해결방법 중 하나는 객체를 불변 객체로 만들어 사용하는 것</p>
<p><strong>순수 함수</strong>: 외부 상태를 변경하지 않고 외부 상태에 의존하지도 않는 함수<br>
순수 함수를 통해 side effect를 최대한 억제하여 오류를 피하고 프로그램의 안정성을 높이려는 프로그래밍 패러다임을 <em>함수형 프로그래밍</em> 이라고 한다.</p>
<h2 id="다양한-함수의-형태">12.7 다양한 함수의 형태</h2>
<h3 id="즉시-실행-함수">12.7.1 즉시 실행 함수</h3>
<p>즉시 실행 함수(IIFE, Immediately Invoked Function Expression): 함수 정의와 동시에 즉시 호출되는 함수. 단 한번만 호출되며 다시 호출할 수 없다.</p>
<p>즉시 실행 함수는 반드시 그룹 연산자 (…)로 감싸야 한다.<br>
그룹 연산자로 함수를 묶은 이유는 먼저 함수 리터럴을 평가해서 함수 객체를 생성하기 위함</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// 즉시 실행 함수에도 일반 함수처럼 값 반환, 인수 전달 가능</span>
<span class="token keyword">var</span> res <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> a <span class="token operator">*</span> b<span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="재귀-함수">12.7.2 재귀 함수</h3>
<p>재귀 함수: 자기 자신의 호출을 수행하는 함수<br>
재귀 함수 내에는 자귀 호출을 멈출 수 있는 탈출 조건을 반드시 만들어야 한다.<br>
재귀 함수는 반복문을 사용하는 것보다 재귀 함수를 사용한느 편이 더 직관적으로 이해하기 쉬울 때만 한정적으로 사용하는 것이 바람직</p>
<h3 id="중첩-함수">12.7.3 중첩 함수</h3>
<p>중첩 함수: 함수 내부에 정의된 함수<br>
일반적으로 중첩 함수는 자신을 포함하는 외부 함수를 돕는 헬퍼 함수의 역할을 한다.</p>
<h3 id="콜백-함수">12.7.4 콜백 함수</h3>
<p>콜백 함수: 함수의 매개변수를 통해 다른 함수의 내부로 전달되는 함수<br>
고차 함수: 변수를 통해 함수의 외부에서 콜백 함수를 전달받은 함수</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">repeat</span><span class="token punctuation">(</span>n<span class="token punctuation">,</span> f<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> n<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">f</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span> <span class="token function-variable function">logAll</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>i<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> <span class="token function-variable function">logOdds</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>i<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span>i <span class="token operator">%</span> <span class="token number">2</span><span class="token punctuation">)</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token function">repeat</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span> logAll<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 0 1 2 3 4</span>
<span class="token function">repeat</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span> logOdds<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1 3</span>

<span class="token comment">// 콜백 함수가 고차 함수 내부에만 호출된다면 익명 함수 리터럴로 정의하는 것이 일반적</span>
<span class="token comment">// 하지만 호출마다 함수 객체를 생성하므로 자주 호출된다면 외부에서 정의한 후 함수 참조를 전달하는 편이 효율적임</span>
<span class="token function">repeat</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>i<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span>i <span class="token operator">%</span> <span class="token number">2</span><span class="token punctuation">)</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>i<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<p>함수의 변하지 않는 공통 로직은 미리 정의해두고, 경우에 따라 변경되는 로직은 추상화해서 함수 외부에서 함수 내부로 전달하도록 하여 구현</p>
<p>콜백 함수는 함수형 프로그래밍 패러다임 뿐만 아니라 비동기 처리에 활용되는 중요한 패턴이다.</p>
<h3 id="순수-함수와-비순수-함수">12.7.5 순수 함수와 비순수 함수</h3>
<p>순수 함수: 어떤 외부 상태에 의존하지도 않고 변경하지도 않는 함수<br>
-&gt; 외부 상태에 의존하지 않고 오직 매개변수를 통해 함수 내부로 전달된 인수에게만 의존해 반환값을 만든다.</p>
<p>함수가 외부 상태를 변경하면 상태 변화를 추적하기 어려워지므로 순수 함수를 사용하는 것이 좋다.</p>
<p>함수형 프로그래밍: 순수 함수와 보조 함수의 조합을 통해 외부 상태를 변경하는 부수 효과를 최소화해서 불변성을 지향하는 프로그래밍 패러다임</p>
<h1 id="스코프">13 스코프</h1>
<h2 id="스코프란">13.1 스코프란?</h2>
<p>모든 식별자는 자신이 선언된 위치에 의해 다른 코드가 식별자 자신을 참조할 수 있는 유효 범위를 결정<br>
<strong>스코프</strong>: 식별자가 유효한 범위</p>
<p>식별자 결정: 이름이 같ㅇ느 두 개의 변수 중에서 어떤 변수를 참조해야 할 것인지를 결정하는 것 — 실행 컨텍스트와 관련</p>
<p>식별자는 어떤 값을 구별할 수 있어야 하므로 유일해야 함<br>
스코프 내에서 식별자는 유일해야 하지만 다른 스코프에는 같은 이름의 식별자를 사용할 수 있다. — 스코프는 네임스페이스다.</p>
<p><em>참고: var 키워드로 선언된 변수는 같은 스코프 내에서 중복 선언이 허용됨</em><br>
<strong>-&gt; let, const 키워드 사용</strong></p>
<h2 id="스코프의-종류">13.2 스코프의 종류</h2>
<h3 id="전역과-전역-스코프">13.2.1 전역과 전역 스코프</h3>
<p>전역: 코드의 가장 바깥 영역<br>
전역 변수는 어디서든지 참조 가능</p>
<h3 id="지역과-지역-스코프">13.2.2 지역과 지역 스코프</h3>
<p>지역: 함수 몸체 내부<br>
지역 변수는 자신의 지역 스코프와 하위 지역 스코프에서 유효</p>
<h2 id="스코프-체인">13.3. 스코프 체인</h2>
<p>함수는 중첩될 수 있으므로 함수의 지역 스코프도 중첩될 수 있다.<br>
스코프 체인: 스코프가 계층적으로 연결된 것</p>
<h3 id="스코프-체인에-의한-변수-검색">13.3.1 스코프 체인에 의한 변수 검색</h3>
<p>변수를 참조할 때 자바스크립트 엔진은 스코프 체인을 통해 변수를 참조하는 코드의 스코프에서 시작하여 상위 스코프 방향으로 이동하며 선언된 변수를 검색(identifier resolution)한다.</p>
<p>상위 스코프에서 유효한 변수는 하위 스코프에서 자유롭게 참조할 수 있지만 하위 스코프에서 유효한 변수를 상위 스코프에서 참조할 수 없다.</p>
<h3 id="스코프-체인에-의한-함수-검색">13.3.2 스코프 체인에 의한 함수 검색</h3>
<p>스코프는 변수를 검색할 때 사용하는 규칙이라기보다는 식별자를 검색하는 규칙</p>
<h2 id="함수-레벨-스코프">13.4 함수 레벨 스코프</h2>
<p>코드 블록이 아닌 함수에 의해서 지역 스코프가 생성된다.<br>
<strong>블록 레벨 스코프</strong>(C, Java 등): 함수 몸체 뿐만 아니라 모든 코드 블록(if, for 등)이 지역 스코프를 만든다.<br>
<strong>함수 레벨 스코프</strong>: <mark>var 키워드</mark>로 선언된 변수는 <em>오직 함수의 코드 블록만을</em> 지역 스코프로 인정한다.</p>
<p><em>참고: let, const 키워드는 블록 레벨 스코프를 지원한다.</em></p>
<h2 id="렉시컬-스코프">13.5 렉시컬 스코프</h2>
<p>동적 스코프: 함수가 호출되는 시점에 동적으로 상위 스코프를 결정<br>
렉시컬 스코프: 함수 정의가 평가되는 시점에 상위 스코프가 정적으로 결정</p>
<p>함수 정의가 실행되어 생성된 함수 객체는 이렇게 결정된 상위 스코프를 기억한다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> <span class="token function">foo</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
  <span class="token function">bar</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">function</span> <span class="token function">bar</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token function">foo</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1</span>
<span class="token function">bar</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1</span>
</code></pre>
<h1 id="전역-변수의-문제점">14 전역 변수의 문제점</h1>
<h2 id="변수의-생명-주기">14.1 변수의 생명 주기</h2>
<h3 id="지역-변수의-생명-주기">14.1.1 지역 변수의 생명 주기</h3>
<p>변수는 자신이 선언된 위치에서 생성되고 소멸한다.<br>
지역변수의 생명 주기는 함수의 생명 주기와 일치한다.(변수 호이스팅x)</p>
<p>지역변수가 함수보다 오래 생존하는 경우도 있다.<br>
변수의 생명 주기는 메모리 공간이 확보된 시점부터 메모리 공간이 해제되어 가용 메모리 풀에 반환되는 시점까지이다.<br>
할당된 메모리 공간은 더이상 누구도 참조하지 않을 때 가비지 콜렉터에 의해 해제되어 메모리 풀에 반환된다.<br>
따라서 누군가 스코프를 참조하고 있으면 스코프는 소멸하지 않고 생존</p>
<h3 id="전역-변수의-생명-주기">14.1.2 전역 변수의 생명 주기</h3>
<p>전역 코드는 코드가 로드되자마자 곧바로 해석되고 실행된다.<br>
var 키워드로 선언한 전역 변수는 전역 객체의 프로퍼티가 되며, 전역 객체의 생명 주기와 일치한다.</p>
<h2 id="전역-변수의-문제점-1">14.2 전역 변수의 문제점</h2>
<ol>
<li>암묵적 결합<br>
모든 코드가 전역 변수를 참조하고 변경할 수 있는 암묵적 결합을 허용하게 됨</li>
<li>긴 생명 주기<br>
메모리 리소스도 오랜 기간 소비하며, 변수 이름이 중복되면 의도치 않은 재할당이 이루어진다.</li>
<li>스코프 제인 상에서 종점에 존재<br>
변수 검색 시 가장 마지막에 검색되어 전역 변수의 검색 속도가 가장 느리다</li>
<li>네임 스페이스 오염<br>
파일이 분리되어 있다해도 하나의 전역 스코프를 공유하므로 예상치 못한 결과를 가져올 수 있다.</li>
</ol>
<h2 id="전역-변수의-사용을-억제하는-방법">14.3 전역 변수의 사용을 억제하는 방법</h2>
<p>전역 변수를 반드시 사용해야 할 이유를 찾지 못한다면 지역 변수를 사용해야 한다.</p>
<h3 id="즉시-실행-함수-1">14.3.1 즉시 실행 함수</h3>
<p>즉시 실행 함수는 단 한번만 호출되므로 전역 변수 사용 제한</p>
<h3 id="네임스페이스-객체">14.3.2 네임스페이스 객체</h3>
<p>전역에 네임스페이스 역할을 담당할 객체를 생성하고 전역 변수처럼 사용하고 싶은 변수를 프로퍼티로 추가하는 방법</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> MYAPP <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">;</span>
MYAPP<span class="token punctuation">.</span>person <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’<span class="token punctuation">,</span>
  address<span class="token punctuation">:</span> ‘Seoul’
<span class="token punctuation">}</span><span class="token punctuation">;</span>

console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>MYAPP<span class="token punctuation">.</span>person<span class="token punctuation">.</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="모듈-패턴">14.3.3 모듈 패턴</h3>
<p>클래스를 모방해서 관련이 있는 변수와 함수를 모아 즉시 실행 함수로 감싸 하나의 모듈을 만든다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> Counter <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token comment">//private</span>
  <span class="token keyword">var</span> num <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>

  <span class="token keyword">return</span> <span class="token punctuation">{</span>
    <span class="token comment">// public</span>
    <span class="token function">increase</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token operator">++</span>num<span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
    <span class="token function">decrease</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token operator">--</span>num<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>Counter<span class="token punctuation">.</span>num<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// undefined</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>Counter<span class="token punctuation">.</span><span class="token function">increase</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>Counter<span class="token punctuation">.</span><span class="token function">decrease</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 0</span>
</code></pre>
<h3 id="es6-모듈">14.3.4 ES6 모듈</h3>
<p>ES6 모듈은 파일 자체의 독자적인 모듈 스코프를 제공</p>
<h1 id="let-const-키워드와-블록-레벨-스코프">15 let, const 키워드와 블록 레벨 스코프</h1>
<h2 id="var-키워드로-선언한-변수의-문제점">15.1 var 키워드로 선언한 변수의 문제점</h2>
<h3 id="변수-중복-선언-허용">15.1.1 변수 중복 선언 허용</h3>
<h3 id="함수-레벨-스코프-1">15.1.2 함수 레벨 스코프</h3>
<h3 id="변수-호이스팅">15.1.3 변수 호이스팅</h3>
<p>변수 선언문 이전에 변수를 참조하는 것은 변수 호이스팅에 의해 에러를 발생시키지는 않짐나 프로그램 흐름상 맞지 않을뿐더러 가독성을 떨어뜨리고 오류를 발생시킬 여지를 남긴다.</p>
<h2 id="let-키워드">15.2 let 키워드</h2>
<p>let 키워드로 선언된 변수는 변수 중복 선언이 허용되지 않으며 블록 레벨 스코프를 따른다.</p>
<p>let 키워드로 선언된 변수는 “선언 단계”와 “초기화 단계”가 분리되어 진행<br>
스코프의 선언 시점부터 초기화 시점까지 변수를 참조할 수 없는 구간을 일시적 사각지대(Temporal Dead Zone)라고 부른다.</p>
<p>let 전역 변수는 전역 객체의 프로퍼티가 아닌 보이지 않는 개념적인 블록 내에 존재하게 된다.</p>
<h2 id="const-키워드">15.3 const 키워드</h2>
<h3 id="선언과-초기화">15.3.1 선언과 초기화</h3>
<p>const 키워드로 선언한 변수는 반드시 선언과 동시에 초기화해야 한다.</p>
<h3 id="재할당-금지">15.3.2 재할당 금지</h3>
<h3 id="상수">15.3.3 상수</h3>
<p>원시값은 변경 불가능한 값이므로 재할당 없이 값을 변경할 수 있는 방법이 없기 때문</p>
<h3 id="const-키워드와-객체">15.3.4 const 키워드와 객체</h3>
<p>const 키워드로 선언된 변수에 객체를 할당한 경우 값을 변경할 수 있다.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> person <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Lee’
<span class="token punctuation">}</span><span class="token punctuation">;</span>

person<span class="token punctuation">.</span>name <span class="token operator">=</span> ‘Kang’<span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>person<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// {name: “Kang”}</span>
</code></pre>
<h2 id="var-vs.-let-vs.-const">15.4 var vs. let vs. const</h2>
<ul>
<li>ES6를 사용한다면 var 키워드는 사용하지 않는다.</li>
<li>재할당이 필요한 경우에 한정해 let 키워드를 사용한다. 이 때 변수의 스코프는 최대한 좁게 만든다.</li>
<li>변경이 발생하지 않고 읽기 전용으로 사용하는 원시 값과 객체에는 const 키워드를 사용한다.</li>
</ul>
<h1 id="프로퍼티-어트리뷰트">16 프로퍼티 어트리뷰트</h1>
<h2 id="내부-슬롯과-내부-메서드">16.1 내부 슬롯과 내부 메서드</h2>
<p>내부 슬롯과 내부 메서드는 자바스크립트 엔진의 구현 알고리즘을 설명하기 위해 사용하는 의사 프로퍼티와 의사 메서드다.</p>
<p>개발자가 직접 접근할 수 있도록 외부로 공개된 객체의 프로퍼티는 아니지만, 일부는 간접적으로 접근할 수 있는 수 있는 수단을 제공하기도 한다.</p>
<h2 id="프로퍼티-어트리뷰트와-프로퍼티-디스크립터-객체">16.2 프로퍼티 어트리뷰트와 프로퍼티 디스크립터 객체</h2>
<p>자바스크립트 엔진은 프로퍼티를 생성할 때 프로퍼티의 상태를 나타내는 프로퍼티 어트리뷰트를 기본값으로 자동 정의한다.</p>
<p>프로퍼티 상태 - 프로퍼티의 값, 값의 갱신 가능 여부, 열거 가능 여부, 재정의 가능 여부</p>
<p>프로퍼티 어트리뷰트는 자바스크립트 엔진이 관리하는 내부 상태 값인 내부 슬롯이다.<br>
프로퍼티 디스크립터 객체: 프로퍼티 어트리뷰트 정보를 제공</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> person <span class="token operator">=</span> <span class="token punctuation">{</span>
  name<span class="token punctuation">:</span> ‘Kang’
<span class="token punctuation">}</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>Object<span class="token punctuation">.</span><span class="token function">getOwnPropertyDescriptor</span><span class="token punctuation">(</span>person<span class="token punctuation">,</span> ‘name’<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// {value: “Kang”, writable: true, enumerable: true, configurable: true}</span>
</code></pre>
<h2 id="데이터-프로퍼티와-접근자-프로퍼티">16.3 데이터 프로퍼티와 접근자 프로퍼티</h2>
<ul>
<li>데이터 프로퍼티: 키와 값으로 구성된 일반적인 프로퍼티</li>
<li>접근자 프로퍼티: 자체적으로 값을 갖지 않고 다른 데이터 프로퍼티의 값을 읽거나 저장할 때 호출되는 접근자 함수로 구성된 프로퍼티</li>
</ul>
<h3 id="데이터-프로퍼티">16.3.1 데이터 프로퍼티</h3>
<p>데이터 프로퍼티의 프로퍼티 어트리뷰트</p>
<ul>
<li>value: 프로퍼티 값</li>
<li>writable: 값의 변경 가능 여부</li>
<li>enumerable: 열거 가능 여부</li>
<li>configurable: 재정의 가능 여부</li>
</ul>
<h3 id="접근자-프로퍼티">16.3.2 접근자 프로퍼티</h3>
<p>접근자 플퍼티는 자체적으로 값을 가지지 않으며 다만 데이터 프로퍼티의 값을 읽거나 저장할 때 관여할 뿐이다.</p>
<p>접근자 프로퍼티의 프로퍼티 어트리뷰트</p>
<ul>
<li>get: 접근자 프로퍼티를 통해 데이터 프로퍼티의 값을 읽을 때 호출되는 접근자 함수</li>
<li>set: 접근자 프로퍼티를 통해 데이터 프로퍼티의 값을 저장할 때 호출되는 접근자 함수</li>
<li>enumerable</li>
<li>configurable</li>
</ul>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> person <span class="token operator">=</span> <span class="token punctuation">{</span>
  firstName<span class="token punctuation">:</span> ‘Taewoo’<span class="token punctuation">,</span>
  lastName<span class="token punctuation">:</span> ‘Kang’<span class="token punctuation">,</span>

  <span class="token keyword">get</span> <span class="token function">fullName</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> ‘$<span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>firstName<span class="token punctuation">}</span> $<span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>lastName<span class="token punctuation">}</span>’<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token keyword">set</span> <span class="token function">fullName</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token punctuation">[</span><span class="token keyword">this</span><span class="token punctuation">.</span>firstName<span class="token punctuation">,</span> <span class="token keyword">this</span><span class="token punctuation">.</span>lastName<span class="token punctuation">]</span> <span class="token operator">=</span> name<span class="token punctuation">.</span><span class="token function">split</span><span class="token punctuation">(</span>‘ ‘<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token comment">// 데이터 프로퍼티를 통한 프로퍼티 값 참조</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>person<span class="token punctuation">.</span>firstName <span class="token operator">+</span> ‘ ‘ <span class="token operator">+</span> person<span class="token punctuation">.</span>lastName<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Taewoo Kang</span>

<span class="token comment">// setter</span>
person<span class="token punctuation">.</span>fullName <span class="token operator">=</span> ‘Minsoo Kang’<span class="token punctuation">;</span>

<span class="token comment">// getter</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>person<span class="token punctuation">.</span>fullName<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Minsoo Kang</span>

<span class="token keyword">let</span> descripter <span class="token operator">=</span> Object<span class="token punctuation">.</span><span class="token function">getOwnPropertyDescripter</span><span class="token punctuation">(</span>person<span class="token punctuation">,</span> ‘firstName’<span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>descripter<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// {value: ‘Minsoo Kang’, writable: true, enumerable: true, configurable: true}</span>

descripter <span class="token operator">=</span> Object<span class="token punctuation">.</span><span class="token function">getOwnPropertyDescripter</span><span class="token punctuation">(</span>person<span class="token punctuation">,</span> ‘fullName’<span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>descripter<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// {get: f, set:f, enumerable: true, configurable: true}</span>
</code></pre>
<h2 id="프로퍼티-정의">16.4 프로퍼티 정의</h2>
<p>프로퍼티 정의: 새로운 프로퍼티를 추가하면서 프로퍼티 어트리뷰트를 명시적으로 정의하거나 기존 프로퍼티의 프로퍼티 어트리뷰트를 재정의하는 것</p>
<p><code>Object.defineProperty</code> 메서드를 사용<br>
디스크립터 객체의 프로퍼티를 누락시키면 undefined, false가 기본값이다</p>
<h2 id="객체-변경-방지">16.5 객체 변경 방지</h2>

<table>
<thead>
<tr>
<th>구분</th>
<th>메서드</th>
<th>추가</th>
<th>삭제</th>
<th>읽기</th>
<th>쓰기</th>
<th>재정의</th>
</tr>
</thead>
<tbody>
<tr>
<td>객체 확장 금지</td>
<td>Object.preventExtensions</td>
<td>X</td>
<td>O</td>
<td>O</td>
<td>O</td>
<td>O</td>
</tr>
<tr>
<td>객체 밀봉</td>
<td>Object.seal</td>
<td>X</td>
<td>X</td>
<td>O</td>
<td>O</td>
<td>X</td>
</tr>
<tr>
<td>객체 동결</td>
<td>Object.freeze</td>
<td>X</td>
<td>X</td>
<td>O</td>
<td>X</td>
<td>X</td>
</tr>
</tbody>
</table><h3 id="객체-확장-금지">16.5.1 객체 확장 금지</h3>
<p>확장이 금지된 객체는 프로퍼티 추가가 금지된다.</p>
<h3 id="객체-밀봉">16.5.2 객체 밀봉</h3>
<p>밀봉된 객체는 읽기와 쓰기만 가능하다.</p>
<h3 id="객체-동결">16.5.3 객체 동결</h3>
<p>동결된 객체는 읽기만 가능하다.</p>
<h3 id="불변-객체">16.5.4 불변 객체</h3>
<p>변경 방지 메서드들은 얕은 변경 방지<br>
-&gt; 객체의 중첩 객체까지 동결하여 변경이 불가능한 읽기 전용의 불변 객체를 구현하려면 객체를 값으로 갖는 모든 프로퍼티에 대해 재귀적으로 <code>Object.freeze</code> 메서드를 호출해야 함</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">deepFreeze</span><span class="token punctuation">(</span>target<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span>target <span class="token operator">&amp;&amp;</span> <span class="token keyword">typeof</span> target <span class="token operator">===</span> ‘object’ <span class="token operator">&amp;&amp;</span> <span class="token operator">!</span>Object<span class="token punctuation">.</span><span class="token function">isFrozen</span><span class="token punctuation">(</span>target<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    Object<span class="token punctuation">.</span><span class="token function">freeze</span><span class="token punctuation">(</span>target<span class="token punctuation">)</span><span class="token punctuation">;</span>
    Object<span class="token punctuation">.</span><span class="token function">keys</span><span class="token punctuation">(</span>target<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">forEach</span><span class="token punctuation">(</span>key <span class="token operator">=&gt;</span> <span class="token function">deepFreeze</span><span class="token punctuation">(</span>target<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  <span class="token keyword">return</span> target<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h1 id="생성자-함수에-의한-객체-생성">17 생성자 함수에 의한 객체 생성</h1>
<h2 id="object-생성자-함수">17.1 Object 생성자 함수</h2>
<p><code>new</code> 연산자와 함께 Object 생성자 함수를 호출하면 빈 객체를 생성하여 반환<br>
프로퍼티 또는 메서드를 추가하여 객체를 완성</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> person <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Object</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

person<span class="token punctuation">.</span>name <span class="token operator">=</span> ‘Kang’<span class="token punctuation">;</span>
person<span class="token punctuation">.</span><span class="token function-variable function">sayHello</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>‘Hi<span class="token operator">!</span> My name is ‘ <span class="token operator">+</span> <span class="token keyword">this</span><span class="token punctuation">.</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="생성자-함수">17.2 생성자 함수</h2>
<h3 id="객체-리터럴에-의한-객체-생성-방식의-문제점">17.2.1 객체 리터럴에 의한 객체 생성 방식의 문제점</h3>
<p>객체 리터럴에 의한 객체 생성 방식은 직관적이고 간편하지만 단 하나의 객체만 생성하므로 동일한 프로퍼티를 갖는 객체를 여러 개 생성해야 하는 경우 비효율적</p>
<h3 id="생성자-함수에-의한-객체-생성-방식의-장점">17.2.2 생성자 함수에 의한 객체 생성 방식의 장점</h3>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">Circle</span><span class="token punctuation">(</span>radius<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>radius <span class="token operator">=</span> radius<span class="token punctuation">;</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function-variable function">getDiameter</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token keyword">this</span><span class="token punctuation">.</span>radius<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">const</span> circle1 <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Circle</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> circle2 <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Circle</span><span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="생성자-함수의-인스턴스-생성-과정">17.2.3 생성자 함수의 인스턴스 생성 과정</h3>
<p>생성자 함수의 역할은 템플릿으로서 동작하여 <strong>인스턴스를 생성</strong>하는 것과 <strong>생성된 인스턴스를 초기화</strong>(인스턴스 프로퍼티 추가 및 초기값 할당)하는 것</p>
<p>자바스크립트 엔진은 암묵적인 처리를 통해 인스턴스를 생성하고 반환</p>
<ol>
<li>인스턴스 생성과 this 바인딩: 런타임 이전에 실행되어 암묵적으로 빈 객체 생성</li>
<li>인스턴스 초기화 — 개발자가 기술 필요</li>
<li>인스턴스 반환: this 반환</li>
</ol>
<h3 id="내부-메서드-call과-construct">17.2.4 내부 메서드 [[Call]]과 [[Construct]]</h3>
<p>함수는 객체!</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">foo</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span><span class="token punctuation">}</span>

<span class="token comment">// [[Call]] 호출</span>
<span class="token function">foo</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// [[Construct]] 호출</span>
<span class="token keyword">new</span> <span class="token class-name">foo</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h3 id="constructor와-non-constructor의-구분">17.2.5 constructor와 non-constructor의 구분</h3>
<ul>
<li>constructor: 함수 선언문, 함수 표현식, 클래스</li>
<li>non-constructor: 메서드(ES6 메서드 축약 표현), 화살표 함수</li>
</ul>
<p>함수가 어디에 할당되어 있는지가 아닌 함수 정의 방식에 따라 구분</p>
<h3 id="new-연산자">17.2.6 new 연산자</h3>
<p>new 연산자 없이 생성자 함수를 호출하면 일반 함수로 호출된다.<br>
일반 함수로서 호출하면 함수 내부의 this는 전역 객체 window를 가리킨다.</p>
<h3 id="new.target">17.2.7 new.target</h3>
<p>new 연산자와 함께 생성자 함수로서 호출되면 함수 내부의 new.target은 함수 자신을 가리킨다.<br>
일반 함수로서 호출된 함수 내부의 new.target은 undefined다.</p>
<pre class=" language-js"><code class="prism  language-js">fuction <span class="token function">Circle</span><span class="token punctuation">(</span>radius<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span><span class="token keyword">new</span><span class="token punctuation">.</span>target<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token keyword">new</span> <span class="token class-name">Circle</span><span class="token punctuation">(</span>radius<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  
  <span class="token keyword">this</span><span class="token punctuation">.</span>radius <span class="token operator">=</span> radius<span class="token punctuation">;</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>getDiameter <span class="token operator">=</span> <span class="token function">fuction</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token number">2</span> <span class="token operator">*</span> <span class="token keyword">this</span><span class="token punctuation">.</span>radius<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">// new 연산자 없이 생성자 함수를 호출하여도 생성자 함수로 호출</span>
<span class="token keyword">const</span> circle <span class="token operator">=</span> <span class="token function">Circle</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>circle<span class="token punctuation">.</span><span class="token function">getDiameter</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<h1 id="함수와-일급-객체">18 함수와 일급 객체</h1>
<h2 id="일급-객체">18.1 일급 객체</h2>
<p>다음과 같은 조건을 만족하는 객체를 일급 객체라 한다.</p>
<ol>
<li>무명의 리터럴로 생성할 수 있다. 즉, 런타임에 생성이 가능하다.</li>
<li>변수나 자료구조에 저장할 수 있다.</li>
<li>함수의 매개변수에 전달할 수 있다.</li>
<li>함수의 반환값으로 사용할 수 있다.</li>
</ol>
<p>함수가 일급 객체라는 것은 함수를 객체와 동일하게 사용할 수 있다는 의미</p>
<h2 id="함수-객체의-프로퍼티">18.2 함수 객체의 프로퍼티</h2>
<h3 id="arguments-프로퍼티">18.2.1 arguments 프로퍼티</h3>
<p>함수 객체의 arguments 프로퍼티 값은 arguments 객체<br>
arguments 객체는 함수 호출 시 전달된 인수들의 정보를 담고 있는 순회 가능한 유사 배열 객체이며, 함수 내부에서 지역변수처럼 사용된다.<br>
<strong>유사 배열 객체</strong>: length 프로퍼티를 가진 객체로 for문으로 순회할 수 있는 객체</p>
<p>arguments 객체는 인수를 프로퍼티 값으로 소유하며, 프로퍼티 키는 인수의 순서를 나타낸다</p>
<p>arguments 객체는 매개변수 개수를 확정할 수 없는 가변 인자 함수를 구현할 때 유용</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">sum</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">let</span> res <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
  <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> arguments<span class="token punctuation">.</span>length<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    res <span class="token operator">+=</span> argements<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  <span class="token keyword">return</span> res<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="caller-프로퍼티">18.2.2 caller 프로퍼티</h3>
<p>자신을 호출한 함수를 가리킨다</p>
<h3 id="length-프로퍼티">18.2.3 length 프로퍼티</h3>
<p>arguments 객체의 length 프로퍼티는 인자(argument)의 개수<br>
함수 객체의 length 프로퍼티는 매개변수(parameter)의 개수</p>
<h3 id="name-프로퍼티">18.2.4 name 프로퍼티</h3>
<p>함수 이름을 나타내는 프로퍼티<br>
익명 함수의 경우 함수 객체를 가리키는 변수 이름을 가짐</p>
<h3 id="proto-접근자-프로퍼티">18.2.5 <strong>proto</strong> 접근자 프로퍼티</h3>
<p>[[Prototype]] 내부 슬롯이 가리키는 프로토타입 객체에 접근하기 위해 사용하는 접근자 프로퍼티</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> obj <span class="token operator">=</span> <span class="token punctuation">{</span> a<span class="token punctuation">:</span> <span class="token number">1</span> <span class="token punctuation">}</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>obj<span class="token punctuation">.</span>__proto__ <span class="token operator">===</span> Object<span class="token punctuation">.</span>prototype<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true</span>
<span class="token comment">// __proto__는 상속받은 프로퍼티</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>obj<span class="token punctuation">.</span><span class="token function">hasOwnProperty</span><span class="token punctuation">(</span>‘__proto__’<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">//false</span>
</code></pre>
<h3 id="prototype-프로퍼티">18.2.6 prototype 프로퍼티</h3>
<p>생성자 함수로 호출할 수 있는 constructor만이 소유하는 프로퍼티<br>
생성자 함수가 생성할 인스턴스의 프로토타입 객체를 가리킨다.</p>
<h1 id="프로토타입">19 프로토타입</h1>
<p>자바스크립트는 클래스 기반 객체지향 프로그래밍 언어보다 효율적이며 더 강력한 객체지향 프록래밍 능력을 지니고 있는 <strong>프로토타입 기반의 객체지향 프로그래밍 언어</strong>다.</p>
<h2 id="객체지향-프로그래밍">19.1 객체지향 프로그래밍</h2>
<p><strong>객체</strong>: 상태 데이터와 동작을 하나의 논리적인 단위로 묶은 복합적인 자료구조</p>
<h2 id="상속과-프로토타입">19.2 상속과 프로토타입</h2>
<p>자바스크립트는 <strong>프로토타입을 기반으로 상속을 구현</strong>하여 불필요한 중복을 제거</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">Circle</span><span class="token punctuation">(</span>radius<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>radius <span class="token operator">=</span> radius<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">// prototype 프로퍼티에 바인딩하여 공유할 수 있도록</span>
Circle<span class="token punctuation">.</span>prototype<span class="token punctuation">.</span><span class="token function-variable function">getArea</span> <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> Math<span class="token punctuation">.</span>PI <span class="token operator">*</span> <span class="token keyword">this</span><span class="token punctuation">.</span>radius <span class="token operator">**</span> <span class="token number">2</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token keyword">const</span> circle1 <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Circle</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> circle2 <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Circle</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>circle1<span class="token punctuation">.</span>getArea <span class="token operator">===</span> circle<span class="token punctuation">.</span>getArea<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// true</span>
</code></pre>
<h2 id="프로토타입-객체">19.3 프로토타입 객체</h2>
<p>객체 간 상속을 구현하기 위해 사용<br>
모든 객체는 하나의 프로토타입을 가지며, 모든 프로토타입은 생성자 함수와 연결되어 있다.</p>
<h3 id="proto-접근자-프로퍼티-1">19.3.1 <strong>proto</strong> 접근자 프로퍼티</h3>
<p>객체가 자신의 [[Prototype]] 내부 슬롯에 간접적으로 접근할 수 있는 접근자 프로퍼티<br>
접근자 프로퍼티를 사용한느 이유는 상호 참조에 의해 프로토타입 체인이 생성되는 것을 방지하기 위해</p>
<p>__proto__접근자 프로퍼티를 코드 내에서 직접적으로 사용하는 대신 getPrototypeOf(), Object.setPrototypeOf() 메서드 사용</p>
<h3 id="함수-객체의-prototype-프로퍼티">19.3.2 함수 객체의 prototype 프로퍼티</h3>
<p>함수 객체만이 소유하는 prototype 프로퍼티는 생성자 함수가 생성할 인스턴스의 프로토타입을 가리킨다.</p>
<h3 id="프로토타입의-constructor-프로퍼티와-생성자-함수">19.3.3 프로토타입의 constructor 프로퍼티와 생성자 함수</h3>
<p>모든 프로토타입은 constructor 프로퍼티를 갖는다</p>
<h2 id="리터럴-표기법에-의해-생성된-객체의-생성자-함수와-프로토타입">19.4 리터럴 표기법에 의해 생성된 객체의 생성자 함수와 프로토타입</h2>
<p>리터럴 표기법에 의해 생성된 객체도 상속을 위해 프로토타입이 필요하므로 가상적인 생성자 함수를 가진다.</p>
<h2 id="프로토타입의-생성-시점">19.5 프로토타입의 생성 시점</h2>
<p>프로토타입은 생성자 함수가 생성되는 시점에 함께 생성</p>
<h3 id="사용자-정의-생성자-함수와-프로토타입-생성-시점">19.5.1 사용자 정의 생성자 함수와 프로토타입 생성 시점</h3>
<p>constructor는 함수 정의가 평가되어 함수 객체를 생성하는 시점에 생성<br>
함수 선언문은 함수 호이스팅에 의해 먼저 실행</p>
<pre class=" language-js"><code class="prism  language-js">console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>Person<span class="token punctuation">.</span>prototype<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// {constructor: f}</span>

<span class="token keyword">function</span> <span class="token function">Person</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">this</span><span class="token punctuation">.</span>name <span class="token operator">=</span> name<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="빌트인-생성자-함수와-프로토타입-생성-시점">19.5.2 빌트인 생성자 함수와 프로토타입 생성 시점</h3>
<p>빌트인 생성자 함수는 전역 객체가 생성되는 시점에 생성</p>
<h2 id="객체-생성-방식과-프로토타입의-결정">19.6 객체 생성 방식과 프로토타입의 결정</h2>
<h3 id="객체-리터럴에-의해-생성된-객체의-프로토타입">19.6.1 객체 리터럴에 의해 생성된 객체의 프로토타입</h3>

