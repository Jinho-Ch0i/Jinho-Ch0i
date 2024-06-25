/*
ID: ch0ijin1
LANG: JAVA
PROG: shell
*/
import java.io.*;
import java.util.*;
public class shell {
	public static void main(String[] args) throws IOException{
		BufferedReader br = new BufferedReader(new FileReader("shell.in"));
        // input file name goes above
		PrintWriter out = new PrintWriter(new BufferedWriter(new FileWriter("shell.out")));
		StringTokenizer s = new StringTokenizer(br.readLine());
		int n = Integer.parseInt(s.nextToken());
		int[] shellPos = new int[]{0, 1, 2};
		int[] cupGuessTotal = new int[] {0,0,0};
		
		
		
		for(int i = 0; i < n; i++) {
			s = new StringTokenizer(br.readLine());
			int aSwapPos = Integer.parseInt(s.nextToken())-1;
			int bSwapPos = Integer.parseInt(s.nextToken())-1;
			int guess = Integer.parseInt(s.nextToken())-1;
			int temp = shellPos[aSwapPos];
			
			shellPos[aSwapPos] = shellPos[bSwapPos];
			shellPos[bSwapPos] = temp;
			
			cupGuessTotal[shellPos[guess]]++;
		}
		out.print(Math.max(Math.max(cupGuessTotal[0], cupGuessTotal[1]), cupGuessTotal[2]));
		out.close();
	}
}
