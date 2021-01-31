What is the tool that you are testing? What is its purpose? Any other aspects that are relevant: size in terms of LOC, languages that it is written in, etc.
	Fastjson is a Java Library that provides methods of converting Java objects to JSON object and vice versa. There are mainly two functions:
JSON.toJSONString:
This method is used to convert Java objects, including maps, lists, self-defined classed into a JSON object. Here is an example of self-defined object class:
```
static class Book{
		
		public String title;
		
		public String price;
		
		public String publish_date;
		
		public String author;
		
		public Book(String title, String price, String date, String author) {
			this.title = title;
			this.price = price;
			this.publish_date = date;
			this.author = author;
		}
		
		
		
	}
```
JSON.parseObject
 
 
 
Use Junit to test. 179182 lines of code. Java.
Document its build. What did you need to do to get it built and running?
The source code on its Github repository includes a pom.xml file. We use Intellij with this pom.xml file to build a Maven project.
Building properties(感覺寫重要的就好？):
Junit version: 4.13.1
Jdk version: 1.5
 
 
換個連結：https://www.javadoc.io/doc/com.alibaba/fastjson/latest/index.html
 
 
 
Document the existing test cases (JUnit or otherwise). This should be a study of the existing testing practices and frameworks that are used already in the system. (This section might evolve as we learn more throughout the quarter.) How do you run them?
他的test檔用了這個測試 diffblue.deeptestutils.Reflector
https://www.diffblue.com/
他test cases 寫的方式蠻固定的
但好像也不一定
有些寫的很簡單 有修就有用到reflector 不知道那個是什麼
可能要看一下在幹嘛
最後再用junit的Assertequal
 
Important
我發現他可以轉map list應該也可以
所以就變nested呀
他要轉換的東西 一定要定義 set 跟 get
	喔
嗯嗯他沒有轉錯吧？（Ｙ）

想說應該可以試試看在array裡面放個hashmap之類的 或放個function
Lambda 
1/31登出 晚安  
Bye  第四題 你也想一下 你覺得這樣partition合理嗎？
還有systematic funcXXXX
已經不記得那啥了
不是random就是systematic吧？
就有邏輯的設計test cases
ㄡ
怎麼看起來像是兩個東西
是啊
但應該是partition 是一種systematic testing 的方式？ 有空再看看講義好了
好拉你快睡覺
我來看看
Partitioning: First, motivate the need for systematic functional testing and partition testing. Describe these concepts. Then, select a feature that allows for partitioning. Specify your partitions (and boundaries when appropriate) in English — describe them. Then, write new test cases in JUnit, and describe and document those test cases and how they run.
分類不同field的ｃｌａｓｓ 
然後也可以試試有繼承的class
Or classes that implement interfaces
 
 
 

