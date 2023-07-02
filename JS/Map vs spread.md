스프레드 연산자(**...**)는 주로 배열이나 객체를 펼치는 데 사용됩니다.

배열에서의 스프레드 연산자는 배열을 개별 요소로 분리하여 새로운 배열이나 

함수 호출 시 인수로 사용할 수 있습니다.

객체에서의 스프레드 연산자는 객체를 개별 속성으로 분리하여 

새로운 객체를 생성하거나 기존 객체를 병합할 때 사용됩니다.

예를 들어, 배열에서 스프레드 연산자를 사용하여 배열을 펼치면 각 요소가 개별적인 값으로 분리됩니다.

이를 통해 새로운 배열을 생성하거나 기존 배열을 확장할 수 있습니다.

```jsx

const numbers = [1, 2, 3];
const newNumbers = [...numbers, 4, 5]; // [1, 2, 3, 4, 5]

반면에 map()은 배열의 각 요소를 변환하여 새로운 배열을 생성하는 함수입니다. 기존 배열을 변경하지 않고, 각 요소에
대해 지정된 함수를 실행하고 반환된 결과를 새로운 배열에 저장합니다.

const numbers = [1, 2, 3];
const doubledNumbers = numbers.map((num) => num * 2); // [2, 4, 6]

// map만을 이용했을 때,

const handleUpdate = () => {
  const prev = prompt('누구의 이름을 변경하고 싶은가요?');
  const current = prompt('어떤 이름으로 변경하고 싶은가요?');
  setPerson((prevPerson) => ({
    name: prevPerson.name,
    title: prevPerson.title,
    mentors: prevPerson.mentors.map((mentor) => {
      if (mentor.name === prev) {
        return {
          name: current,
          title: mentor.title,
        };
      }
      return mentor;
    })
  }));
}

// 스프레드를 이용했을 때,

const handleUpdate = () => {
    const prev = prompt('누구의 이름을 변경하고 싶은가요?');
    const current = prompt('어떤 이름으로 변경하고 싶은가요?');
    setPerson((prevPerson) => ({
      ...prevPerson,
      mentors: prevPerson.mentors.map((mentor) => {
        if(mentor.name === prev) {
          return {...mentor, name: current};
        }
        return mentor;
      })
    }))
    }
```