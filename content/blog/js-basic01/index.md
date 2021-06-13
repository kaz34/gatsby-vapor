---
title: JavScript.infoでJSのベーシックを学ぶ01
date: "2021-06-13"
tags: [JavaScript]
---

SPAでアプリケーションを作りたいと思い、Vueでいきなり実装しようとしたが、わからない事だらけだったので、まずはJS(TS)のベーシックから学ぼうと思ったのがきっかけです。

```
        //object
        let person ={
            name: 'Mosh',
            age: 30
        };
        //Railsでよく使ったドット(メソッドチェーンだっけ？)と、[]の書き方二通りがある。
        person.name = 'John';
        person['name'] = 'Mary';
        //こういう書き方もできる。nameをstringとして囲ってるのに、何で変数として
        //コンピューターが理解できるか不思議
        let selection = 'name';
        person[selection] = 'Mary02'
        //なるほど。結果的にperson.nameってなってる。.nameを変数で入れたってだけだね。



        console.log(person.name)


        //array
        let selectColors = ['red', 'blue'];
        selectColors[2] = 1;
        console.log(selectColors[2])

        //functions
        function greet(personsName, lastName){
            console.log('Hello ' + personsName + lastName)
        }
        greet('John', 'smith')// greet(personsName)をrunしたことになる。って事は内部のconsole.logをみる。

        function square(number){
            return number * number;
        }
        console.log(square(20));

        //function02 globalとlocal

        //functionの外と中で定義されているとそれぞれglobalとlocalになるよ。
        //globalで定義されたletは、ファイル内で全部適応されるから、命名規則気をつける。
        function showMessage(){
            let message = "Hello mf"
            alert(message);
        }
        // showMessage();

        //function03: multiple data = parameters
        function showMessage(from, text){
            alert(from + ':' + text);
        }

        // showMessage('Ann', 'Hello');
        // showMessage('Ann', 'youre good');

        //function04 variable of variable
        function showMessagee(fromm, textt){
            fromm = '*' + fromm + '*';
            alert (fromm + ':' + textt);
        }
        let fromm = "Ann";
        showMessagee(fromm, "Hello");

        //function05
        //このundifinedは、methodって事でいいのかな？
        function undifinedMethod(text){
            // if (text === undefined){
            //     text = 'empty message';
            // }
            //or こういう書き方もできる。↓　rubyの時と書き方同じ。
            text = text || 'empty';
            alert(text);
        }
        //you can try either way and see whats happen
        // undifinedMethod('h');
        undifinedMethod();

        //function06 prompt which allow to insert data in the box
        //and make sure write a result after it
        function checkAge(age) {
  if (age >= 18) {
    return true;
  } else {
    return confirm('Do you have permission from your parents?');
  }
}

let age = prompt('How old are you?', 18);

if ( checkAge(age) ) {
  alert( 'Access granted' );
} else {
  alert( 'Access denied' );
}

//functions name should be shrot and inside of function make sure do the one simple thing.


//function 07
//same result different way to express
function sayHello() {
  alert( "Hello" );
}

let sayHello = function() {
  alert( "Hello" );
};



```
