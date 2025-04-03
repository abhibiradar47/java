# java
import java.util.Scanner;

public class bookmain {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int n=0,ch;
		int id;
		float max;
		
		bookservice bb= new bookservice ();
		Book b[]=new Book[100];
		
		while (true) {
			Scanner sc = new Scanner(System.in);
			System.out.println("ENTER THE CHOICE : ");
			System.out.println("1.INSERT "
					+"2. Display"
					+ "3. SEARCH BY ID "
					+ "4. SEARCH BY NAME "
					+ "5.MAX PRICE " 
					+ "6 MIN PRICE "
					+ "7. EXIT ");
			
			 ch=sc.nextInt();
			switch (ch) {
			case 1: {
				
				b[n] =bb.insert();
				break;
			}
			case 2:
				bb.display(b, n);
				break;
			case 3:
				System.out.println("Enter the id to search");
				id=sc.nextInt();
				if(bb.Search(b, n, id)==-1)
					System.out.println(" NOT FOUND ");
				else
					System.out.println(b[bb.Search(b, n, id)]);
				break;
				
				
			case 4:
				System.out.println("Enter the name to search");
				String name=sc.next();
				if(bb.search(b, n, name));
				else
					System.out.println("NOT FOUND ");
				break;
				
			case 5:
				bb.max(b, n);
				
				break;
			case 6:
				System.exit(0);
			//default:
				//System.out.println("PLEASE ENTER A VALID CHOICE :");
			}
		}
		

	}

}
