ES6 새로운 기능



 Arrow Function 

    const func1 = arg => 'hello world'



var, let, const

- var
      console.log(var1);
  에러 발생 하나요?
      console.log(var1);
      var var1 = "hello world";
  이건 에러가 발생하나요?
  
- let
      console.log(var1);
      let var1 = "hello world";
  이건..?
  
- const
      const val1 = 1;
      val1 = 2; //?
      
      const val2; //?



... 연산자

- 전개 연산자?
- 사용예
      function myFunction(x, y, z) { }
      var args = [0, 1, 2];
      myFunction(...args); // myFunction(args[0], args[1], args[2])
  인덱스 순서에 따라 알아서 할당된다.
  
      function myFunction(v, w, x, y, z) {
          console.table(arguments);
      }
      var args = [0, 1];
      myFunction(-1, ...args, 2, ...[3]);
  - z를 배열로 받고 싶다면?
  
  - 복사
      const array1 = [1,2,3,4]
      const array2 = [...array1] // array 복사
      
      const obj1 = {
          "a": 1,
          "b": 2,
          "c": 3
      }
      
      const obj2 = Object.assign({}, obj1)
      
      console.dir(array1)
      console.dir(array2)
      console.dir(obj1)
      console.dir(obj2)
  
  

비구조화 할당(destructuring assignment)

비구조화 할당(destructuring assignment) 구문은 배열의 값이나 객체의 속성을 별개의 변수로 추출할 수 있게 하는 자바스크립트 식(expression)입니다.



    var a, b, rest;
    [a, b] = [10, 20];
    console.log(a); // 10
    console.log(b); // 20
    
    [a, b, ...rest] = [10, 20, 30, 40, 50];
    console.log(a); // 10
    console.log(b); // 20
    console.log(rest); // [30, 40, 50]
    
    ({ a, b } = { a: 10, b: 20 });
    console.log(a); // 10
    console.log(b); // 20
    
    
    // Stage 3 proposal
    ({a, b, ...rest} = {a: 10, b: 20, c: 30, d: 40});
    console.log(a); // 10
    console.log(b); // 20
    console.log(rest); //{c: 30, d: 40}
    
    const errorFunc = ( { errMsg } ) => console.log(errMsg);
    errorFunc({
        a: 10,
        b: 20,
        errMsg: "이런이런"
    })
    
    errorFunc({
        errMsg: "저런저런"
    })
