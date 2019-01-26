# JS-DataFilter
JavaScript/ 循环的分析for/forEach/map/fuilter

    
			/* 
				for
				for of/each  
				map
				reduce
				fuilter
			 */
			/* 
			//循环对象能拿到对象的id，但不能拿到值
			for(var i in obj){
				
			}
			//循环数组，能拿到值
			for(var i of list){
				
			} */
			let array1 = [];
			let array2 = [];
			array.forEach(e => {
				if (e.salary >= 3000 && e.salary <= 3500) array1.push(e);
			});
			console.log(array1);
			/* 定义*/
			function agetMethods(birthday) {
				return new Date().getFullYear() - birthday.substring(0, birthday.indexOf('.'));
				//console.log(new Date().getFullYear() -  birthday.substring(0, birthday.indexOf('.')));
			}
			function sumMethods(firstNumber, twoNumber) {
				return firstNumber + twoNumber;
			}
			array1.map(v => {
				if (agetMethods(v.birth) <= 19 && v.city != "湖南") {
					v.age = agetMethods(v.birth);
					array2.push(v);
				}
			});
			console.log(array2);
			let num = [];
			
			let count = 0;
			
			array2.filter(v => num.push(v.salary));
			
			num.filter(v => count = num.reduce(sumMethods));
			
			console.log(count);
