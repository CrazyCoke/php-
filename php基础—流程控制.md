---
title: php基础—流程控制
tags:php study
grammar_cjkRuby: true
---

### if分支
if（）{
}elseif（）{
}else{
}
与java类似，else if  写为 elseif

使用场景：判断条件单一 ，采用elseif 方式。
					判断条件不相同，采用嵌套形式。
					适用于所有的条件判断。

### switch 分支
判断同一条件的不同值。固定值匹配的分支结构。
switch（）{
	case var1：
		代码段
		break；
	case var2：
		代码段
		break；
	case var3：
		代码段
		break；
	default：
		匹配失败执行的代码
		break；
}

### for循环
for ( $i  = 0; $i <= 10 ; $i++){
	echo $i,'<br/>';
}

### while，do-while 循环

while先判断条件，不符合就一次都不执行。
$a = 0;
while($a < 10){
	echo $a;
	$a++;
}

do-while 先执行一次再判断条件。
do{
	echo$a++;
}while($a < 10);



### 循环控制
循环控制：在循环内部对循环本身进行控制。
中断循环：重新开始循环，循环体中还有其他的内容也不再执行。
				continue 关键字；
终止循环：直接结束循环
					break 关键字。
					
					
### 流程控制替代语法
当大括号较多时，可使用替代机制
for( ; ; ){  //  写为  for( ; ; ) :   ；
}             //    写为  endfor;    ；

规律：php镶嵌在html中应该只做数据输出，通常有条件判断和循环操作，因此php提供了对应分支结构和循环结构的替代语法，全部对应一个模式。
左大括号 “ { ”  使用 冒号“ : ” 替代；
右大括号 “ } ” 使用 end+对应的实际标记。如 endfor;  endif; 