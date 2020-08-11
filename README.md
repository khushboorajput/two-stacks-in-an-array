package stacks;

public class Two_stacks_in_an_array {

	int arr[];
	int t1,t2;
	int cap;
	
	Two_stacks_in_an_array(int d)
	{
		arr=new int[d];
		t1=-1;
		t2=d-1;
		cap=d;
	}
	public void push1(int dd)
	{
		if(t1<t2-1)
		{
			arr[++t1]=dd;
		}
	}
	public void push2(int ddd)
	{
		if(t2>t1)
		{
			arr[t2--]=ddd;
		}
	}
	void arrayOne()
	{
	int i=0;
	System.out.println("First list is :-");
		while(i<=t1)
		{
			System.out.println(arr[i]);
			i++;
	}
	}
	public void arrayTwo()
	{
		int j=cap-1;
		System.out.println("Second list is :-");
		while(j>t2)
		{
			System.out.println(arr[j]);
			j--;
		}
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Two_stacks_in_an_array sick =new Two_stacks_in_an_array(100);
		
		sick.push1(1);
		sick.push1(2);
		sick.push1(3);
		sick.push1(4);
		sick.push1(5);
		
		sick.push2(25);
		sick.push2(24);
		sick.push2(23);
		sick.push2(22);
		sick.push2(21);
		
		sick.arrayOne();
		sick.arrayTwo();
	}

}
