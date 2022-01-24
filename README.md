# portfolio

기록 : 

1) v-for를 사용할때 v-for="(item,index) in items" :key="index"를 사용한다면, index는 숫자가 될 수도 있고 키워드가 될 수 있다.
예를 들어서 {이름:'천승현', 나이:'27'}과 같은 객체로 저장했다면 이름과 나이가 index가 되는 것이다. 

2) Object타입의 key들을 추출해서 array타입으로 return해주는 함수 : Object.keys(객체); 필자는 객체에 들어있는 값들이 iterable이라고 판단해서 filter를 정의해 사용하려했는데 iterable이 아니였기에 사용하지 못했다. 이는 Symbol.iterator메소드가 없기 때문이었다.
