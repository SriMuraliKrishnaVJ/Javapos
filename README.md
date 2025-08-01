import java.util.Scanner;
import java.time.*;
import java.time.format.DateTimeFormatter;
class GROCERY_BILL{
     Scanner sc=new Scanner(System.in);
     
         int gc[]=new int[100];
    int gup[]=new int[100];
     int gtp[]=new int[100];
     int gq[]=new int[100];
     String gitn[]=new String[100];
     double ggtp=0.0;
     int e=0;String name="";String pno;
     int pass; String str; boolean check;
     
     DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");
      LocalDateTime myObj = LocalDateTime.now();
      String formattedDate = myObj.format(myFormatObj);
    
    private void manualmode(){
          System.out.println("Manual Mode");
            System.out.println("Please enter the item name ");
            String str=sc.next();
            System.out.println("Please enter the cost of the item");
            int cost=sc.nextInt();
            System.out.println("Please enter the code of the item");
            int code=sc.nextInt();
            System.out.println("Please enter the quantity");
            int quantity=sc.nextInt();
            gq[e]=quantity;
                    gc[e]=code;
                    gitn[e]=str;
                    gup[e]=cost;
                    e++;
            System.out.println("noted");
      }
    public   void Login(){
        System.out.println("MK GROUP");
        System.out.println("Please enter customer name ");
        name=sc.next();
        System.out.println("Please enter customer phone number");
         pno=sc.next();
        
        
        if(pno.length()==10){
            invent();
            
        }
        else {
            System.out.println("\f");
            System.out.println("Phone number is not correct please try again");
            Login();
        }
    }
    private  void invent(){
        System.out.println("Please enter :");
        System.out.println("1 for cosmetics \t 2 for vegetables  \t 3 for stationary \t 4 for dairy products \t 5 for fruits \t 0 for bill and exit");
        int opt=sc.nextInt();
        
        switch (opt){
            case 1:cos();break;
            case 2:ve();break;
            case 3:st();break;
            case 4:dp();break;
            case 5:fruits();break;
            case 0:bill();break;
            default: System.out.println("wrong code please try again");invent();break;
        }
    }
    private  void cos(){
        String c[]={"comb","hair dryer","lipstick","powder","makeup set","shampoo","soap"};
        int cc[]={101,102,103,104,105,106,107};
        int cp[]={20,599,45,98,999,50,20};
        System.out.println("code     cost     item ");
        System.out.println("______________________________________");
        for(int i=0;i<=cc.length-1;i++){
            System.out.println(cc[i]+" "+cp[i]+"  "+c[i]);
        }
        
        System.out.println("Please enter the code ");
        System.out.println("if the item you are looking for is not there then please enter 2");
        int d=sc.nextInt();
        if (d==2){
            manualmode();
        }
        else {
            int pos=-1;
            for(int i=0;i<=cc.length-1;i++){
                
                if(cc[i]==d){
                    
                    gc[e]=cc[i];
                    gitn[e]=c[i];
                    gup[e]=cp[i];
                    System.out.println("please enter the quantity");
                    int q=sc.nextInt();
                    gq[e]=q;
                    System.out.println("noted");
                    pos=i;
                    e++;
                }
            }
            if(pos==-1){
                System.out.println("wrong code");
            }
        }
        System.out.println("Please enter");
        System.out.println("1 to continue        2 to billing");
        int f=sc.nextInt();
        if(f==1)
        invent();
        else if(f==2)
        bill();
        
        
    }
    private  void ve(){
        String c[]={"okra","potato","bitter gourd","onion","tomato","capsicum","fruit"};
        int cc[]={111,112,113,114,115,116,117};
        int cp[]={20,45,45,45,87,65,20};
        System.out.println("code     cost     item ");
        System.out.println("______________________________________");
        for(int i=0;i<=cc.length-1;i++){
            System.out.println(cc[i]+" "+cp[i]+"  "+c[i]);
        }
        
        
        System.out.println("Please enter the code ");
        System.out.println("if the item you are looking for is not there then please enter 2");
        int d=sc.nextInt();
        if (d==2){
            manualmode();
        }
        else {
            int pos=-1;
            for(int i=0;i<=cc.length-1;i++){
                
                if(cc[i]==d){
                    
                    gc[e]=cc[i];
                    gitn[e]=c[i];
                    gup[e]=cp[i];
                    System.out.println("please enter the quantity");
                    int q=sc.nextInt();
                    gq[e]=q;
                    System.out.println("noted");
                    pos=i;
                    e++;
                }
            }
            if(pos==-1){
                System.out.println("wrong code");
            }
        }
        System.out.println("Please enter");
        System.out.println("1 to continue        2 to billing");
        int f=sc.nextInt();
        if(f==1)
        invent();
        else if(f==2)
        bill();
        
    }
    private  void st(){
        String c[]={"blackpen","bluepen","eraser","sharpner","pencil","fevicol","stapler"};
        int cc[]={121,122,123,124,125,126,127};
        int cp[]={20,20,5,5,12,30,90};
        System.out.println("code     cost     item ");
        System.out.println("______________________________________");
        for(int i=0;i<=cc.length-1;i++){
            System.out.println(cc[i]+" "+cp[i]+"  "+c[i]);
        }
        
        
        System.out.println("Please enter the code ");
        System.out.println("if the item you are looking for is not there then please enter 2");
        int d=sc.nextInt();
        if (d==2){
            manualmode();
        }
        else {
            int pos=-1;
            for(int i=0;i<=cc.length-1;i++){
                
                if(cc[i]==d){
                    
                    gc[e]=cc[i];
                    gitn[e]=c[i];
                    gup[e]=cp[i];
                    System.out.println("please enter the quantity");
                    int q=sc.nextInt();
                    gq[e]=q;
                    System.out.println("noted");
                    pos=i;
                    e++;
                }
            }
            if(pos==-1){
                System.out.println("wrong code");
            }
        }
        System.out.println("Please enter");
        System.out.println("1 to continue        2 to billing");
        int f=sc.nextInt();
        if(f==1)
        invent();
        else if(f==2)
        bill();
        
    }
    private  void dp(){
        String c[]={"milk","curd","icecream","butter","yogurt","buttermilk","cheese"};
        int cc[]={131,132,133,134,135,136,137};
        int cp[]={20,34,45,290,30,50,20};
        System.out.println("code     cost     item ");
        System.out.println("______________________________________");
        for(int i=0;i<=cc.length-1;i++){
            System.out.println(cc[i]+" "+cp[i]+"  "+c[i]);
        }
        
        
        System.out.println("Please enter the code ");
        System.out.println("if the item you are looking for is not there then please enter 2");
        int d=sc.nextInt();
        if (d==2){
            manualmode();
        }
        else {
            int pos=-1;
            for(int i=0;i<=cc.length-1;i++){
                
                if(cc[i]==d){
                    
                    gc[e]=cc[i];
                    gitn[e]=c[i];
                    gup[e]=cp[i];
                    System.out.println("please enter the quantity");
                    int q=sc.nextInt();
                    gq[e]=q;
                    System.out.println("noted");
                    pos=i;
                    e++;
                }
            }
            if(pos==-1){
                System.out.println("wrong code");
            }
        }
        System.out.println("Please enter");
        System.out.println("1 to continue        2 to billing");
        int f=sc.nextInt();
        if(f==1)
        invent();
        else if(f==2)
        bill();
        
    }
    private   void fruits(){
        String c[]={"banana","orange","mango","pomogranate","guava","apple","grapes"};
        int cc[]={141,142,143,144,145,146,147};
        int cp[]={20,45,45,58,45,50,70};
        System.out.println("code     cost     item ");
        System.out.println("______________________________________");
        for(int i=0;i<=cc.length-1;i++){
            System.out.println(cc[i]+" "+cp[i]+"  "+c[i]);
        }
        
        
        System.out.println("Please enter the code ");
        System.out.println("if the item you are looking for is not there then please enter 2");
        int d=sc.nextInt();
        if (d==2){
            manualmode();
        }
        else {
            int pos=-1;
            for(int i=0;i<=cc.length-1;i++){
                
                if(cc[i]==d){
                    
                    gc[e]=cc[i];
                    gitn[e]=c[i];
                    gup[e]=cp[i];
                    System.out.println("please enter the quantity");
                    int q=sc.nextInt();
                    gq[e]=q;
                    System.out.println("noted");
                    pos=i;
                    e++;
                }
            }
            if(pos==-1){
                System.out.println("wrong code");
            }
        }
        System.out.println("Please enter");
        System.out.println("1 to continue        2 to billing");
        int f=sc.nextInt();
        if(f==1)
        invent();
        else if(f==2)
        bill();
        
    }
    private  void bill(){
        for(int i=0;i<=gc.length-1;i++){
            if(gc[i]>0){
                gtp[i]=gq[i]*gup[i];
            }
            else
            continue;
            ggtp=ggtp+gtp[i];
        }
        System.out.println("\f");
        System.out.println("\t \t \t \tMK GROUP");
        System.out.println("\t \t 60 Paul Revere Road, Groton Estates \n \t \t \t Connecticut,USA");
        System.out.println("____________________________________________________________________");
        System.out.println("\t\t\t\tINVOICE");
        System.out.println("____________________________________________________________________");

        System.out.println("Customer name: "+name);
        System.out.println("Phone number: "+pno);
        System.out.println("time and date  "+formattedDate);
        System.out.println("_____________________________________________________________________");
        System.out.println("Product       Product                  Product  Product      Product");
        System.out.println(" Code          Name                    quantity unit price    price");
        System.out.println("_____________________________________________________________________");
        for(int i=0;i<=e-1;i++){
            System.out.println(gc[i]+"       "+gitn[i]+"\t\t\t\t"+gq[i]+"\t \u20B9"+gup[i]+"    \u20B9"+gtp[i]);
        }
        System.out.println("_____________________________________________________________________");
        System.out.println("Total bill:                                                  \u20B9"+ggtp);
        
        
    }
}
