# part2practical2



import java.util.Scanner;
public class practical_2 {
        private int id=0;
        private double balance=500;
        private double IR=7;
        private java.util.Date dateCreated;
 
        practical_2()
        {
            int id=0;
            double balance=500;
            double IR=7;
            dateCreated= new java.util.Date();
        }
        practical_2(int i)
        {
            dateCreated= new java.util.Date();
            id=i;
 
        }
 
        void setid(int si)
        {
            id=si;
        }
        int getid()
        {
            return id;
        }
        void setBalance(double sb)
        {
            balance=sb;
        }
        double getBalance()
        {
            return balance;
        }
        void setair(double sair)
        {
            IR=sair;
        }
        double getIR()
        {
            return IR/100;
        }
        java.util.Date getdate()
        {
            return dateCreated;
        }
        double getMonthlyInterestRate()
        {
            return IR/12;
        }
        double getMonthlyInterest(double bal)
        {
            return bal*(IR/1200);
        }
        void withdraw(double w_amount)
        {
            if(w_amount<balance){
                balance=balance-w_amount;
                System.out.println("Your Amount is withdraw successfully !!!");
            }
            else
            {
                System.out.println("Your account dose not have demanded amount !!!");
            }
        }
        void deposit(double d_amount)
        {
            balance=balance+ d_amount;
            System.out.println("Your Amount is deposit successfully !!!");
        }
 
 
    }
    class main{
 
        public static void main(String[] args) {
            Scanner sc= new Scanner(System.in);
 
            int aid;
            System.out.print("Enter a ID : ");
            aid=sc.nextInt();
            practical_2 obj = new practical_2(aid);
            System.out.println("your account created successfully :)");
            System.out.println("Account ID      : "+obj.getid());
            System.out.println("Account balance : "+obj.getBalance());
            System.out.print("Enter annualInterestRate   : ");
            double air= sc.nextDouble();
            obj.setair(air);
            System.out.println("MonthlyInterestRate      : "+obj.getMonthlyInterestRate()+"%");
            System.out.println("MonthlyInterest          : "+obj.getMonthlyInterest(obj.getBalance()));
            System.out.print("Enter deposit amount         : ");
            double pa= sc.nextDouble();
            obj.deposit(pa);
            System.out.println("your account balance   : "+obj.getBalance());
            System.out.print("Enter withdraw amount        : ");
            double tel= sc.nextDouble();
            obj.withdraw(tel);
            System.out.println(" your account balance   : "+obj.getBalance());
            System.out.println(" ");
            System.out.println(" TRANSCATION COMPLETED.");
            System.out.println("21CE063-Manav");
 
        }
    }
