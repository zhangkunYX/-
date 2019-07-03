### 设计模式

##### Constructor构造函数模式

  1.创建对象
  ```javascript
    var object = new Object();
    var object = {
      key1: 'value1',
      key2: 'value2'
    };
    object.somekey = 'somvalue';
  ```
  
  2.基本构造器Constructor
  ```javascript
  function Car(model, year, miles){
    this.model = model;
    this.year = year;
    this.miles = miles;
    this.toString = function() {
      return this.model + 'has done' + this.miles;
    }
  }
  var civic = new Car('Honda Civic', 2009, 20000);
  ```
  缺点：toString在每个示例之间是没有共享的，单独拥有自己的方法。
  
  3.带原型的构造器
  ```javascript
  function Car(model, year, miles){
    this.model = model;
    this.year = year;
    this.miles = miles;
  }
  Car.prototype.toString = function() {
    return this.model + 'has done' + this.miles;
  }
  var civic = new Car('Honda Civic', 2009, 20000);
  ```
  现在实例之间共享此方法
  
##### Moudle（模块）模式

