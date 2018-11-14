# SahSparkWordCount
## Links
- [Webpage](https://rohanshah123.github.io/SahSparkWordCount/ "Sah Spark Word Count")
- [Source](https://github.com/rohanshah123/SahSparkWordCount  "Shah Spark Project Source")

## About Me & Objective
My name is Pappu Sah and I am doing the major in Computer Sciece. This project is for my "Big Data" class on Spark and Scala.
The objective of this assignment is to use Spark-shell to find the most frequent words within the text by Shakespeare, Winter's Tale . 

## Data
I used a .txt file of Hamlet by copying and pasting a entire play from the following website:
- [HAMLET](http://shakespeare.mit.edu/winters_tale/winters_tale.1.1.html)

## Scala Commands
> val inputFile = sc.textFile("C:/44564/sparkwordcount/HTML.txt")	

> val topWordCount = inputFile.

     flatMap(str=>str.split(" ")).
	
     filter(!_.isEmpty).
	
     map(word=>(word,1)).
	
     reduceByKey(_+_).
	
     map{case (word, count) => (count, word)}.
	
     sortByKey(false)
	
>topWordCount.take(10).foreach(x=>println(x))


Count      	      word

35              	LEONTES

30               CAMILLO

26             	POLIXENES

15            	HERMIONE

4             	MAMILLIUS

2              	Shakespeare

2               Previous scene

2               Aside

2               my good lord

1           	  To give mine enemy a lasting wink


The result showed that the most frequently used word is 'LEONTES' and it has been used 35 times.
I have represented this data into the visuals using the chart representation.
![sah](https://user-images.githubusercontent.com/42788421/48455265-13ded180-e780-11e8-894a-d7dcb78ad473.png)


