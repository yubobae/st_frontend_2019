# ECMA script

## 템플릿 문자열

백틱 문자를 사용

템플릿 문자열을 사용

예제 1)

* 기존 ECMA 5

```javascript
var number = "one = "+"1"+"\n tow =" +"2";
console.log(number);
```

* ECMA 6

  ```javascript
  let name = "jake";
  let weight = 60;
  
  conosle.log(`
  name = ${name}
  weight = ${weight}
  weight + bagweight = ${weight + 3};
  `);
  ```

표현식과 템플릿 문자열

백틱(backtick)문자`를 사용

템플릿 문자열 표현식 처리

### 정리하기

백틱 내에 multi-line string 을 입력

템플릿 문자열의 표현식을 통해 변수를 입력한다.

해석이 가능한 모든 계산식을 사용할수있다.

# 비구조화 할당(Destructuring)

## 비 구조화 할당 (destructuring assignment)

구조화된 object나 array를 비구조화 하영 변수에 할당.

- 객체 또는 배열에서 데이터를 분석하여 각각의 변수에 할당하는것을 의미.

- json과같은 데이터를 변수에 쉽게 할당 할 수있다.

  ```javascript
  let data = [{
  count:1,
  list:[{
  	name : ['jack','paul'],
  	group:'sprots'
  	}]
  }];
  
  let [{count,list:[{name, group}]}] = data;
  console.log(`
  count: ${count}
  group: ${group}
  `);
  ```

- 객체 표현식을 인자로 넘길때

  ```javascript
  function productObject ({name, price, color}) {
  	return{
  		productName: "This product name: " + name,
  		addToCart(){
  			console.log(name+"is added");
  		},
  		detailView(){
  			console.log(`
  			${productName}
  			price:${price}
  			color:${color}
  			`);
  		}
  	}
  }
  var {productName,addToCart,detailView} = productObject({name:'apple,price:199,color:silver'});
  addToCart();
  detailView();
  ```

  



