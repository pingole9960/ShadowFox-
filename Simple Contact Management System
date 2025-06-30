import java.util.* ;

class contact
{
	String name;
	String phone;
	String email;
	
	contact(String name,
	String phone,
	String email)
	{
		this.name=name;
		this.phone=phone;
		this.email=email;
	}
	public String toString()
	{
		return "Name: " + name + ", Phone: " + phone + ", Email: " + email;
	}
}
public class Manager{
	private static ArrayList<contact>contacts=new ArrayList<>();
	private static Scanner scn=new Scanner(System.in);
	public static void main(String arg[])
   {
   	int choice;
   	do{
   		System.out.println("**Contact Management**");
   		System.out.print("\n\n");
   		System.out.println("1.Add contact.   \n2.View Contact\n3.Update Contact\n4.Delete Contact\n5.Exit  ");
   		System.out.print("Enter Your Choice:");
   		
   		//validation is here...
   		while(!scn.hasNextInt()){
   			System.out.println("Invalid choice! please enter the digit");
   			scn.nextInt();
   			System.out.println("Enter choice:");
   		}
   			choice=scn.nextInt();
   			scn.nextLine();
   		    switch(choice){
   			           case 1:
   			                    addContact();
   			                    break;
   			             case 2:
   			                    viewContact();
   			                    break;
   			              case 3:
   			                    updateContact();
   			                    break;
   			               case 4:
   			                    deleteContact();
   			                    break;
   			               case 5:
   			                    break;
   		    }
   		}while(choice!=5);
   }
    private static void addContact() {
        System.out.print("Enter name: ");
        String name = scn.nextLine();
        System.out.print("Enter phone: ");
        String phone = scn.nextLine();
        System.out.print("Enter email Id: ");
        String email = scn.nextLine();
	    
	    contacts.add(new contact(name,phone,email));
	    System.out.println("Contact Added...");
    }
    
    private static void viewContact() {
    	if(contacts.isEmpty()){
    		System.out.println("No contact is Displayed...!");
    	}
    	else{
    		for(int i=0;i<contacts.size();i++){
    			System.out.println((i+1)+"."+contacts.get(i));
    		}
    	}
    }
    
    private static void updateContact() {
    	if(!contacts.isEmpty()){
    		System.out.println("Enter the contact no to for update=");
    		int ind=scn.nextInt()-1;
    		scn.nextLine();
    		if(ind>=0 && ind<contacts.size()){
    			System.out.print("Enter new name: ");
                String name = scn.nextLine();
                System.out.print("Enter new phone: ");
                String phone = scn.nextLine();
                System.out.print("Enter new email: ");
                String email = scn.nextLine();
                
                contacts.set(ind,new contact(name,phone,email));
                 System.out.println("Contact updated.");
    		}
    		else{
    			 System.out.println("Invalid Contact Number.");
    		}
    	}
    }
    
    private static void deleteContact() {
    	if(!contacts.isEmpty()){
    		 System.out.println("Enter Contact no for  deleting:");
    		 int index=scn.nextInt()-1;
    		 scn.nextLine();
    		 if(index>=0 && index<contacts.size()){
    		      contacts.remove(index);
    		       System.out.println("\nContact deleted!.");
    		 }
    		 else{
    		      		 System.out.println("Invalid Contact Number.");
    		}
    	}
    }
}
    		      
 
