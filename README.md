# input-helper

## Simple JAVA input util class. 
Add this class in your utility package to call for inputs.

### To get input from users just call

InputHelper.getInput("Your prompt message") to request Strings. 

InputHelper.getIntegerInput("Your prompt message") to request Integers.

InputHelper.getDoubleInput("Your prompt message") to request Doubles.


### Class
Add this class
```
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class InputHelper {

	public static String getInput(String prompt) {
		BufferedReader stdin = new BufferedReader(new InputStreamReader(System.in));
		System.out.print(prompt);
		System.out.flush();

		try {
			return stdin.readLine();
		} catch (Exception e) {
			return "Error: " + e.getMessage();
		}
	}

	public static double getDoubleInput(String prompt) throws NumberFormatException {
		String input = getInput(prompt);
		return Double.parseDouble(input);

	}

	public static int getIntegerInput(String prompt) throws NumberFormatException {
		String input = getInput(prompt);
		return Integer.parseInt(input);	
	}	
}

```


