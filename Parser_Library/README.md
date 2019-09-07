# Parser_Library: An easy-to-use library to quickly debug your work.

A basic usage of the library is as easy as follows:

```java
LR1Parser obj=new LR1Parser();//Create an instance of the desired parser-In this case LR1 type parser
obj.read_grammar("D://Documents/Lab4/LR0.txt");//Read the grammar file
obj.buildDFA();//Build a dfa from the file
System.out.println(states)//Prints the transitions in all states
obj.print_transitions();//Print all the transitions
obj.getParsingTable(true);//Use false to avoid printing the table after creation
obj.parse("a c e",true);//Parse the string; use false to prevent the stack actions from displaying on screen
```
- The map of the states

![map](https://user-images.githubusercontent.com/25523604/64479680-d9936480-d1d7-11e9-9461-66f5ae88e970.PNG)

- The parse table

![table](https://user-images.githubusercontent.com/25523604/64479682-d9936480-d1d7-11e9-95a1-c502f42eb3e1.PNG)

- The actions taken by stack to parse the table

![Stack_actions](https://user-images.githubusercontent.com/25523604/64479679-d8face00-d1d7-11e9-826b-1674716a80aa.PNG)

<h2>Functions</h2>

*Parser.java* is the base class which all the other classes inherit from. It exposes the following methods:

|Function|Return Type|Action|
|------|---------|---------|
read_grammar|void|Reads the grammar, augments it and fills in the list of terminals and non-terminals
join|String|Utility method to join convert ArrayList to String
getClosure|void|Accepts a HashSet of type <Parser.Pair> and computes it's closure
getGoto|HashSet<Parser.Pair>Computes Goto
augment, unaugment| void,void| Augments and unaugments the grammar
parse|void|Parses the string using the generated table
getIndex|int|Returns the index of the state, or -1 if a new state
pretty_it|void|Formatting
print_transitions|void|Prints all transitions

More documentation coming soon!