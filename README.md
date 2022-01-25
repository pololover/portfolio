# portfolio

기록 : 

*v-for를 사용할때 v-for="(item,index) in items" :key="index"를 사용한다면, index는 숫자가 될 수도 있고 키워드가 될 수 있다.
예를 들어서 {이름:'천승현', 나이:'27'}과 같은 객체로 저장했다면 이름과 나이가 index가 되는 것이다. 

*Object타입의 key들을 추출해서 array타입으로 return해주는 함수 : Object.keys(객체); 필자는 객체에 들어있는 값들이 iterable이라고 판단해서 자바스크립트의 for or문에 넣어, filter를 정의해 사용하려했는데 iterable이 아니였기에 사용하지 못했다. 이는 Symbol.iterator메소드가 없기 때문이었다. 이를 해결하기 위해서는 Symbol.iterator함수와, next()함수를 이용해 리턴해주는 것이 객체 내부 메소드에 정의 해주어야한다.

*데이터 필터링 시 객체에서 한 요소만을 제거하고 싶을 때 delete를 사용하면 된다. 
예시로 delete obj[no]을 하게 된다면 obj객체의 no값이 사라지게 된다. 

*fx.js에서 정의하는 이터러블 호환함수 map과 filter는 객체를 리턴한다. 때문에 사용시 반환타입에 따라 잘 가공해서 쓰는 게 좋다.

*flex에서 요소배치할 때 width는 자식요소에서, flex-wrap과 같은 설정은 부모요소에서 해준다.

*animation > @keyfreme > transition순서대로 애니메이션을 정의하는 게 좋다.
animation은 전체 효과들을 어떻게 사용할지, @keyframes는 animatino이 실행되는 동안 어떤 타이밍에 어떤 효과를 줄지 더 디테일하게 설정이 가능하게 하고 좀 더 자연스러운 애니메이션을 하게 해 주며, transition은 일부 효과를 지닌다.

*프로젝트 진행하면서 ref에 대한 부분을 어떻게 처리할 지 고민을 했다. v-for문에서는 해당 객체를 ref바인딩함으로써 ref배열에 담기게 할 수 있었는데 만약 v-for가 아닌경우에는 바인딩해도 되지 않았다. 이에 대한 해결책을 모색하며 vue3에서는 이를 어떻게 처리했는지도 날 잡아서 깊게 공부해봐야겠다.
