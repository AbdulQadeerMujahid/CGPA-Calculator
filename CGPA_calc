import java.io.*;
import java.util.*;
class Student
{
	BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
	String Name,College;
String na_sub[]=new String[10];
int msub[]=new int[10];
int rollno,sem,no_sub,size;


void getStudent()
{
try{
System.out.println("Enter your name and rollno");
Name=in.readLine();
rollno=Integer.parseInt(in.readLine());
System.out.println("Enter your College Name And semester");
College=in.readLine();
sem=Integer.parseInt(in.readLine());
System.out.println("Enter  no of subjects you have in "+sem+"th sem ");
no_sub=Integer.parseInt(in.readLine());

System.out.println("Enter name of subjects ");

for(int i=0;i<no_sub;i++)
	{
		na_sub[i] = in.readLine();
	}
System.out.println("Enter the marks  you got in each subject out of total(100)");
for(int i=0;i<no_sub;i++)
	{
		System.out.print("Marks of "+na_sub[i]+" : ");
		msub[i] = Integer.parseInt(in.readLine());
	}
}
catch(NumberFormatException e){
	System.out.println("Enter correct value : "+e);
}

catch(Exception e){
	System.out.println(e);
}
}
}

interface CGPA
{
	public void cal_cgpa();
}

class calculate
	extends Student
	implements CGPA
{

	float per,cgpa;
	public void cal_cgpa()
	{
		int totalmarks=no_sub*100;
	int total=0;
	for(int i=0;i<no_sub;i++)
			total=total+msub[i];
	per=total/no_sub;
	cgpa=per/9.5f;
	}

	void display_cgpa()
{
System.out.println();
System.out.println();
System.out.println("/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/");
System.out.println(" ");
System.out.println("   Student Name :		"+Name+"    ");
System.out.println("---------------------------------------------------");
System.out.println("   Roll no :			"+rollno+"    ");
System.out.println("---------------------------------------------------");
System.out.println("   College :			"+College+"    ");
System.out.println("---------------------------------------------------");

System.out.println("   SEMESTER :			"+sem+"    ");
System.out.println("---------------------------------------------------");

for(int i=0;i<no_sub;i++)
System.out.println("   Marks in "+na_sub[i]+"   		"+msub[i]+" /100"+"    ");
System.out.println("---------------------------------------------------");

System.out.println("  	Percentage :		"+per+" ");
System.out.println("---------------------------------------------------");

System.out.println("   CGPA :		  "+cgpa+" ");
System.out.println("---------------------------------------------------");

System.out.println(" ");
System.out.println("/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/");
}

	void FileHandling()throws FileNotFoundException,IOException
	{
	String content,marks,cg;
	FileWriter fw = new FileWriter(Name+".txt");
	content = "/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/"+"\n---------------------------------------------------"+"\n   Student Name :		"+Name+"    "+"\n---------------------------------------------------"+
				"\n   Roll no :			"+rollno+"    "+"\n---------------------------------------------------"+"\n   College :			"+College+"    "+
				"\n---------------------------------------------------"+"\n   SEMESTER :			"+sem+"    "+"\n---------------------------------------------------";
				  

	char buffer[] = new char[content.length()];
	content.getChars(0,content.length(),buffer,0);
	fw.write(buffer);

	for(int i=0 ; i<no_sub ; i++)
	{
	marks = "\n   Marks in "+na_sub[i]+"   		"+msub[i]+" /100";
	char buffer2[] = new char[marks.length()];
	marks.getChars(0,marks.length(),buffer2,0);
	fw.write(buffer2);
	}
	cg = 	"\n---------------------------------------------------"+"\nPercentage :		"+per+" "+
				"\n---------------------------------------------------"+"\n   CGPA :		  "+cgpa+" "+"\n---------------------------------------------------"+"\n/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/*/" ;
	char buffer3[] = new char[cg.length()];
	cg.getChars(0,cg.length(),buffer3,0);
	fw.write(buffer3);
	fw.close();
	}


}

class CGPA_calc
{
	public static void main(String args[])throws FileNotFoundException,IOException
	{
	calculate c1 = new calculate();
	c1.getStudent();
	c1.cal_cgpa();
	c1.display_cgpa();
	c1.FileHandling();
	}
}
