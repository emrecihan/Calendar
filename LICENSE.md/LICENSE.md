package calendarprogram;

import java.util.Scanner;

public class calendarprog {

	public static void main(String[] args) {
		Scanner input=new Scanner(System.in);
		
		System.out.println("Lütfen yılı giriniz :");
		int yil=input.nextInt();
		System.out.println("Lütfen ayı giriniz :");
		int ay=input.nextInt();
		
		printMonth(yil, ay);
		
		public static void printMonth(int yil,int ay)
		{
			printMonthmTitle(yil, ay);
			
			printMonthBody(yil, ay);
		}
		public static void printMonthTitle(int yil, int ay)
		{
			System.out.println("        "+getMonthName(ay)
			+ " "+yil);
			System.out.println("-----------------------------");
			System.out.println(" Sun Mon Tue Wed Thu Fri Sat");
		}
		public static String getMonthName(int month)
		{
			String monthName= " ";
			switch (ay)
			{
			case 1: monthName = "January"; break;
		      case 2: monthName = "February"; break;
		      case 3: monthName = "March"; break;
		      case 4: monthName = "April"; break;
		      case 5: monthName = "May"; break;
		      case 6: monthName = "June"; break;
		      case 7: monthName = "July"; break;
		      case 8: monthName = "August"; break;
		      case 9: monthName = "September"; break;
		      case 10: monthName = "October"; break;
		      case 11: monthName = "November"; break;
		      case 12: monthName = "December";
			}
			return Monthname;
		}
		public static void printMonthBody(int yil, int ay)
		{
			int startDay= getStartDay(yil, ay);
			
			int numberOfDaysInMonth = getNumberOfDaysInMonth(yil, ay);
			
			int i=0;
			for(i=0; i<startDay;i++)
				System.out.print("   ");
			
			for(i=1; <= numberOfDaysInMonth; i++)
			{
				System.out.println("%4",i);
				
				if ((i + startDay) % 7 == 0)
			        System.out.println();
			}
		     
			System.out.println();

		}
		

	}

}
