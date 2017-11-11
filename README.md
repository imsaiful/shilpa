# shilpa
Menu driven for the TreeSet
```
import java.util.*;
class Shilpa
{
	public static void main(String[] args)
	{
		Scanner in=new Scanner(System.in);
		TreeSet<Integer> ts = new TreeSet<Integer>();
		System.out.println("Enter the initial Capacity of Elements");
		int n=in.nextInt();
		for(int i=1;i<=n;i++)
		{
			System.out.println("Enter the "+i+" element ");
			int x=in.nextInt();			
			ts.add(x);
			
		}
		boolean condition=true;
		while(condition)
		{
			System.out.println("Enter your choise");
		System.out.println("1. View Elements \n2. Insert Element\n3. Delete Elements\n4. Search Element\n5. Exit");
		int c=in.nextInt();
		if(c==1)
		{
			 Iterator<Integer> itr=ts.iterator();  
  			 while(itr.hasNext()){  
   			 System.out.print(itr.next()+" ");
   			 }  
		}
		else if(c==2)
		{
			System.out.println("Enter the element");
			int x=in.nextInt();
			ts.add(x);
			System.out.println("Element is inserted Successfully");
		}
		else if(c==3)
		{
			System.out.println("Enter the element to delete");
			int x=in.nextInt();
			if(ts.remove(x))
			{
				System.out.println("Element deleted");
			}
			else
			{
				System.out.println("Element not exist");
			}

		}
		else if(c==4)
		{
			System.out.println("Enter the element to search");
			int x=in.nextInt();
			boolean flag=true;
			Iterator<Integer> itr=ts.iterator();  
  			while(itr.hasNext()){  
   			     if(itr.next()==x)
   			     {
   			     	System.out.println("Tree Contain the element");
   			     	flag=false;
   			     	break;
   			     	
   			     }
   			 }
   			 if(flag)
   			 {
   			 	System.out.println("There is no such element in TreeSet");
   			 }
		}
		else if(c==5)
		{
			System.exit(0);

		}
		else
		{
			System.out.println("Please enter the correct option");
		}


		}
		
	
}
}


```
