tags: #java

see [[2022-09-09 CSCI301#switch statement]] for explanation and examples

ex.
```Java
public static void main(String[] args) {
	switch(args.length) {
	case 0 : printErrorMsg();
		break;
	case 1: case 2:
		print Arguments(args);
		break;
	default: printArguments(args);
		break;
	}
}
```