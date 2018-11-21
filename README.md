# Busca-Recursiva
Códigos em JApublic class Ex02 {

	public static void main(String[] args) {
		int[] v = {0,2,5,6,7,9,12,15};
		
		System.out.println("Fatorial de 8: "+fat(8));
		System.out.println("Fibonacci de 8: "+fib(8));
		hanoi(4,'A','B','C');
		System.out.println("Busca binária recursiva: "+bsRec(v, 0,2));
		
	}
	public static int bsRec(int[] v, int c, int n) {
		if(c<=v.length-1) {
			if(v[c]==n) return 1;
			return bsRec(v,c+1,n);
		}
		return -1;
	}
	public static int fat(int n) {
		if(n==1)return 1;
			return n*fat(n-1);
	}
	
	public static int fib(int n) {
		if(n<3) return 1;
		return fib(n-1) + fib(n-2);
	}
	
	public static void hanoi(int n,char a,char b,char c) {
		if(n>0) {
			hanoi(n-1,a,c,b);
			System.out.println("Disco "+n+" movido da haste "+a+" pata a haste "+c);
			hanoi(n-1,b,a,c);
		}
	}
	
	public static int bbRec(int[] v,int i, int f, int x) {

		if (i <= f) {
			int m = (i + f) / 2;
			if (x < v[m]) return bbRec(v, i, m - 1, x);
			else if (x > v[m]) return bbRec(v, m + 1, f, x);
			else return 1;
			}
			else return 0;
	}
		
	/*public static int bsRec(int[] v,int n, int c) {
		if(c>=0) {
			if(v[c]==n) return 1;
			return bsRec(v,n,c-1);
		}
		return -1;
	}*/

}
VA  
