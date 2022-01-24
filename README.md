# portfolio

기록 : 

1) v-for를 사용할때 v-for="(item,index) in items" :key="index"를 사용한다면, index는 숫자가 될 수도 있고 키워드가 될 수 있다.
예를 들어서 {이름:'천승현', 나이:'27'}과 같은 객체로 저장했다면 이름과 나이가 index가 되는 것이다. 

2) Object타입의 key들을 추출해서 array타입으로 return해주는 함수 : Object.keys(객체); 필자는 객체에 들어있는 값들이 iterable이라고 판단해서 자바스크립트의 for or문에 넣어, filter를 정의해 사용하려했는데 iterable이 아니였기에 사용하지 못했다. 이는 Symbol.iterator메소드가 없기 때문이었다. 
이를 해결하기 위해서는 Symbol.iterator함수와, next()함수를 이용해 리턴해주는 것이 객체 내부 메소드에 정의 해주어야한다.

3)데이터 필터링 시 객체에서 한 요소만을 제거하고 싶을 때 delete를 사용하면 된다. 
예시로 delete obj[no]을 하게 된다면 obj객체의 no값이 사라지게 된다.

4)fx.js에서 정의하는 이터러블 호환함수 map과 filter는 객체를 리턴한다. 때문에 사용시 반환타입에 따라 잘 가공해서 쓰는 게 좋다.

5)flex에서 요소배치할 때 width는 자식요소에서, flex-wrap과 같은 설정은 부모요소에서 해준다.
