import java.util.*;

class atm{
	private double amount;
	Scanner s=new Scanner(System.in);

	public atm(double amount3)
	{
		amount=amount3;
	}

	public void deposit(double amount2)
	{
		if(amount2<=0)
		{
			System.out.println("please enter a valide amount...");
			System.out.println("Enter amount:");
			amount2=s.nextDouble();
		}
		else
		{
			amount+=amount2;
			System.out.println("your account balence is:"+amount);
		}
	}

	public void withdraw(double amount2)
	{
		if(amount2>=amount)
		{
			System.out.println("your account balence is too low you can't withdraw...");
			System.out.println("Enter amount:");
			amount2=s.nextDouble();
		}
		else
		{
			amount-=amount2;
		}
		System.out.println("your account balence is:"+amount);
	}

	public void checkamount(double amount2)
	{
		System.out.println("your account balence is:"+amount);
	}
}

class project3
{
	private String password;	
	double a;
	private atm obj;
	Scanner sc=new Scanner(System.in);
	
	private int pin1=6001;//for sbi
	private int pin2=7001;//for pnb
	private int pin3=8001;//for boi

	public void switchcase1()
	{
		int ch,ch5;
		boolean ch6;
		do{
			System.out.println("Enter 1 for deposit\nEnter 2 for withdraw\nEnter 3 for checkamount\nEnter 4 for exit\nEnter your choice");
			ch=sc.nextInt();
			switch(ch)
			{
			case 1:
				deposit();
				break;
			case 2:
				withdraw();
				break;
			case 3:
				checkamount();
				break;
			case 4:
				System.out.println("Thank you visit again");
				System.exit(0);
			default:
				System.out.println("please enter a valide choice");
		    }
			System.out.println("Enter any number for continue\n 0 for stop");
			ch5=sc.nextInt();
			ch6=(ch5!=0);
		}while(ch6);
	}

	public void switchcase()
	{
		Scanner se=new Scanner(System.in);
		int ch2,ch4;
		boolean ch3;

		do{
			System.out.println("Plese enter 1 for State Bank of India\nPlese enter 2 for Punjab National Bank\nPlese enter 3 for Bank Of India\nPlese enter your choice:");
			ch4=sc.nextInt();
			switch(ch4)
			{
			case 1:
				System.out.println("Enter your password:");
				password=se.nextLine();
				password=pin1+password;
				System.out.println("your password is(please remember for future):"+password);
				switchcase1();
				break;
			case 2:
				System.out.println("Enter your password:");
				password=se.nextLine();
				password=pin2+password;
				System.out.println("your password is(please remember for future):"+password);
				switchcase1();
				break;
			case 3:
				System.out.println("Enter your password:");
				password=se.nextLine();
				password=pin3+password;
				System.out.println("your password is(please remember for future):"+password);
				break;
			}
			System.out.println("Enter any number for continue\n 0 for stop");
			ch2=sc.nextInt();
			ch3=(ch2!=0);
		}while(ch3);
	}

	public project3(double a3)
	{
		obj=new atm(a3);
	}

	Scanner sa=new Scanner(System.in);

	public void deposit()
	{
		int count=4;
		String p;

		while(count!=0){
		System.out.println("Please enter your password:");
		p=sa.nextLine();
		if(p.equals(password))
		{
		System.out.println("Enter the Amount:");
		a=sc.nextDouble();
		obj.deposit(a);
		break;
		}
		else
		{
		count--;
		System.out.println("you have" +count+ "chance");
		}
		}
	}

	public void withdraw()
	{
		int count=4;
		String p;
		while(count!=0){
		System.out.println("Please enter your password:");
		p=sa.nextLine();
		if(p.equals(password))
		{	
		System.out.println("Enter the Amount:");
		a=sc.nextDouble();
		obj.withdraw(a);
		break;
		}
		else
		{
		count--;
		System.out.println("you have"+count+"chance");
		}
		}
	}

	public void checkamount()
	{
		obj.checkamount(a);
	}

	public static void main(String args[])
	{
		double a2=1000.00;
		project3 obj2=new project3(a2);
		obj2.switchcase();
	}
}
