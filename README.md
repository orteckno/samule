1. Exercise using basic server controls:
   ------------------------------------------
         USERNAME   [[[[[[[TEXTBOW]]]]
         PASSWORD    [[[TEXTBOX]]]]]
             LOGIN
  ----------------------------------------
 
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication8
{
 public partial class Form1 : Form
 {
 public Form1()
 {
 InitializeComponent();
 }
 private void button1_Click(object sender, EventArgs e)
 {
 if (textBox1.Text == "")
 {
 MessageBox.Show("Enter Username !!");
 }
 else if (textBox2.Text == "")
 {
 MessageBox.Show("Enter Password !!");
 }
 else if (textBox1.Text == "Gripsy" && textBox2.Text == "123")
 {
 this.Hide();
 Form frm2 = new Form2();
 frm2.ShowDialog();
 }
 else
 {
 MessageBox.Show("Invalid Credential", "Try Again");
 }
 }
 }
}

###############FORM 2#################
-----------------------------------
     ENTER AGE IN NUMBERS    [[[[TEXTBOX]]]]
             [ CHECK  ]
-----------------------------------

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication8
{
public partial class Form2 : Form
{
public Form2()
{
InitializeComponent();
}
private void button1_Click(object sender, EventArgs e)
{
int a;
a = Convert.ToInt32(vote1.Text);
if (a&gt;=18)
{
MessageBox.Show(&quot;Eligibility To Vote !!&quot;);
}
else
{
MessageBox.Show(&quot;Not Eligibility To Vote !!&quot;);
}
}
}
}

###########################################2. Exercise using validation class PROGRAM2################

-------------------------------------------------------------------------------------------------------
[Label]  choose your candidate

Candidate  [ Drop down list]  Required Fiel Validator      [ choose your candidate]
House   [radio button list]  Required Field Validator      [ choose house ]
Class [ textbox ] range validator                           [ choose class ]
email [ textbox] regular expression validator               [ eneter email id ]

[  SUBMIT ]

validation summary
--------------------------------------------------------------------------------------------
Candidate -> click on [ drop down list] -> items (collection)      control to validate - dropdown list
house-> same as  above                                             control to validate - radio button
class-> click on(range validator)-> control to validate( choose -> texbox1) -> maximum (6) ->minimum (1)
email -> control to validate ( choose -> textbox2) -> Validation Expression (choose - internet email)













<configuration>
  <system.web>
    <compilation debug="true" targetFramework="4.6.1"/>
    <httpRuntime targetFramework="4.6.1"/>
    <pages>
      <namespaces>
        <add namespace="System.Web.Optimization"/>
      </namespaces>
      <controls>
        <add assembly="Microsoft.AspNet.Web.Optimization.WebForms" namespace="Microsoft.AspNet.Web.Optimization.WebForms" tagPrefix="webopt"/>
      </controls>
    </pages>
  </system.web>

           
	<appSettings>
		<add key="ValidationSettings:UnobtrusiveValidateionMode" value="None"/>
	</appSettings>

 
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> 
      <dependentAssembly>
        <assemblyIdentity name="Antlr3.Runtime" publicKeyToken="eb42632606e9261f"/>
        <bindingRedirect oldVersion="0.0.0.0-3.5.0.2" newVersion="3.5.0.2"/>
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="Newtonsoft.Json" publicKeyToken="30ad4fe6b2a6aeed"/>
        <bindingRedirect oldVersion="0.0.0.0-11.0.0.0" newVersion="11.0.0.0"/>
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="WebGrease" publicKeyToken="31bf3856ad364e35"/>
        <bindingRedirect oldVersion="0.0.0.0-1.6.5135.21930" newVersion="1.6.5135.21930"/>
      </dependentAssembly>      
    </assemblyBinding>
  </runtime>
  <system.codedom>
    <compilers>
      <compiler language="c#;cs;csharp" extension=".cs"
        type="Microsoft.CodeDom.Providers.DotNetCompilerPlatform.CSharpCodeProvider, Microsoft.CodeDom.Providers.DotNetCompilerPlatform, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
        warningLevel="4" compilerOptions="/langversion:default /nowarn:1659;1699;1701"/>
      <compiler language="vb;vbs;visualbasic;vbscript" extension=".vb"
        type="Microsoft.CodeDom.Providers.DotNetCompilerPlatform.VBCodeProvider, Microsoft.CodeDom.Providers.DotNetCompilerPlatform, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
        warningLevel="4" compilerOptions="/langversion:default /nowarn:41008 /define:_MYTYPE=\&quot;Web\&quot; /optionInfer+"/>
    </compilers>
  </system.codedom>
</configuration>
 

 
protected void Button1_Click(object sender, EventArgs e)
 {
 if (Page.IsValid)
 {
 lblmsg.Text = "Thank You";
 }
 else
 {
 lblmsg.Text = "Fill up all the fields";
 }
 }



Output:

----------------------------------------------------------------------------------------------
             PRESIDENT ELECTION FORM CHOOSE YOUR PRESIDENT

    CANDIDATE  [PLEASE CHHOSE A CANDIDATE]              CHOOSE YOUR CANDIDATE
                    O RED
    HOUSE           O BLUE
                    O YELLOW                              ENTER YOUR HOUSE NAME
                    O GREEN
    CLASS        [ 5]
    EMAIL        [2]
                                        [ SUBMIT ]
    ERRORS:
    O CHOOSE YOUR CANDIDATE
    O ENTER YOUR HOUSE NAME 
    O ENTER YOUR CURRENT AGE IN NUMBERS
    O ENTER YOUR EMAIL
    -----------------------------------------------------------------------------------------

    USERNAM     - REQUIERD FIEL VALIDATOR
    PASSWORD    -REQUIRED FIELD VALIDATION
    CONFROM PASSWORD   -COMPARE VALIDATION
    EMAIL      - REGULAR EXPRESSION
    PHONE NO   -CUSTOM VALIDATION
    AGE   - RANGE VALIDATION

    [SUBMIT]

    ################################################################PROGRAM 33. Exercise using iterative structures###########################################

 

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication2
{
 public partial class Form1 : Form
 {
 public Form1()
 {
 InitializeComponent();
 }
 
 private void Form1_Load(object sender, EventArgs e)
 {
 }
 private void button2_Click(object sender, EventArgs e)
 {
 this.Close();
 }
 
 private void rock_Click(object sender, EventArgs e)
 {
 Random randomGenerator = new Random();
 int computerChoice;
 player.BackgroundImage = rock.BackgroundImage;
 computerChoice = randomGenerator.Next(1, 4);
 switch (computerChoice)
 {
 case 1: computer.BackgroundImage = rock.BackgroundImage;
 winnerLabel.Text = " TIE ";
 break;
 case 2:
 computer.BackgroundImage = paper.BackgroundImage;
 winnerLabel.Text = " Computer wins because paper covers rock ";
 break;
 case 3:
 computer.BackgroundImage = scissor.BackgroundImage;
 winnerLabel.Text = " Player wins because rock breaks scissors ";
 break;
 }
 }
 private void paper_Click(object sender, EventArgs e)
 {
 Random randomGenerator = new Random();
 int computerChoice;
 player.BackgroundImage = paper.BackgroundImage;
 computerChoice = randomGenerator.Next(1, 4);
 switch (computerChoice)
 {
 case 1:
 computer.BackgroundImage = rock.BackgroundImage;
 winnerLabel.Text = " Payer wins because paper covers rock ";
 break;
 case 2:
 computer.BackgroundImage = paper.BackgroundImage;
 winnerLabel.Text = " TIE ";
 break;
 case 3:
 computer.BackgroundImage = scissor.BackgroundImage;
 winnerLabel.Text = " Computer wins because scissors cut paper ";
 break;
 }
 }
 
 private void scissor_Click(object sender, EventArgs e)
 {
 Random randomGenerator = new Random();
 int computerChoice;
 
 player.BackgroundImage = scissor.BackgroundImage;
 computerChoice = randomGenerator.Next(1, 4);
 
 switch (computerChoice)
 {
 case 1:
 computer.BackgroundImage = rock.BackgroundImage;
 winnerLabel.Text = " Computer wins because rock breaks scissors ";
 break;
 case 2:
 computer.BackgroundImage = paper.BackgroundImage;
 winnerLabel.Text = " Player wins because scissors cut paper ";
 break;
 case 3:
 computer.BackgroundImage = scissor.BackgroundImage;
 winnerLabel.Text = " TIE ";
 break;
 }
 }
 
 }
 }



OUTPUT-----

---------------------------------------------------------------------------------------
          [ PICTURE BOX ]    [PICTURE BOX]      [PICTURE BOX ]
           STONE                PAPER              SCISSOR
                              [ LABEL ]
                                                                    [EXIT]                                    FOR ADDING IMAGE CLICK ON IMAGE
           [PICTURE BOX]      [PICTURE BPX]
           PLAYER               COMPUTER
  --------------------------------------------------------------------------------  







##########################################PROGRAM 4  4. Exercise using basic control classes  ##############################################



------------------------------------------------------------------
        [PICTURE BOX]    [PICTURE BOX]     [PICTURE BOX]     
                  [ LABEL ]                                    [TEXTBOX]  OR [ LABEL]
--------------------------------------------------------------------------------


using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication3
{
 
 public partial class Form1 : Form 
 { 
 public int count=10; 
 public int a; 
 
 public Form1() 
 { 
 InitializeComponent(); 
 a = 1; 
 
 pictureBox1.Visible = true; 
 pictureBox2.Visible = false; 
 pictureBox3.Visible = false; 
 txt_msg.Text = "Turn OFF your engine"; 
 timer1.start();
 timer2.start();
 } 
 
 
 private void timer1_Tick(object sender, EventArgs e) 
 { 
 if (a == 1) 
 { 
 count = 10; 
 pictureBox1.Visible = false; 
 pictureBox2.Visible = false; 
 pictureBox3.Visible = true; 
 txt_msg.Text = "Have a safe journey"; 
 timer1.Interval = 1000; 
 a = 2; 
 } 
 else if (a == 2) 
 { 
 count = 10; 
 pictureBox1.Visible = false; 
 pictureBox2.Visible = true; 
 pictureBox3.Visible = false; 
 txt_msg.Text = "slow down your vehicle"; 
 timer1.Interval = 1000; 
 a = 3; 
 } 
 else if (a == 3) 
 { 
 count = 10; 
 pictureBox1.Visible = true; 
 pictureBox2.Visible = false; 
 pictureBox3.Visible = false; 
 txt_msg.Text = "stop your vehicle"; 
 timer1.Interval = 1000; 
 a = 1; 
 } 
 } 
 
 private void timer2_Tick(object sender, EventArgs e) 
 { 
 
 label.Text = count.ToString(); 
 count = count - 1; 
 
 } 
 
 private void Form1_Load(object sender, EventArgs e) 
 { 
 
 }
 private void pictureBox2_Click(object sender, EventArgs e)
 {
 } 
 } 
}

####################################### PROGRAM 5 5. Exercise using exception handling###############################################3

----------------------------------------------------------------------
              EXCEPTION HANDLING 
              [ TEXTBOX]  [ % ]  [ TEXTBOX ] [ = ]  [ TEXT BOX ]
                              [ SUBMIT ]
                                        [ CLICK ]
----------------------------------------------------------------------
FORM 1

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication1
{
 public partial class Form1 : Form
 {
 public Form1()
 {
 InitializeComponent();
 }
 private void button1_Click(object sender, EventArgs e)
 {
 try
 {
 int numerator = Convert.ToInt32(textBox1.Text);
 int denominator = Convert.ToInt32(textBox2.Text);
 int Answer = numerator / denominator;
 textBox3.Text = Answer.ToString();
 }
 catch (FormatException)
 {
 MessageBox.Show("Invalid input enter two numbers please");
 }
 catch (DivideByZeroException divideByZeroException)
 {
 MessageBox.Show(divideByZeroException.Message, "Can't divide by zero");
 }
 finally
 {
 textBox1.Text = "";
 textBox2.Text = "";
 }
 }
 private void textBox1_TextChanged(object sender, EventArgs e)
 {
 }
 private void button2_Click(object sender, EventArgs e)
 {
 var Form2 = new Form2();
 Form2.Show();
 this.Hide();
 }
 }
}


---------------------------------------------------------------------------------
              DAY        MONTH             YEAR
        [ TEXTBOX ]   [ TEXTBOX ]       [ TEXTBOX ]

           [ SUBMIT ]  [ EXIT ]
---------------------------------------------------------------------------------

Form2.cs

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace WindowsFormsApplication1
{
 public partial class Form2 : Form
 {
 public Form2()
 {
 InitializeComponent();
 }
 private void button2_Click(object sender, EventArgs e)
 {
 this.Close();
 }
 private void button1_Click(object sender, EventArgs e)
 {
 try
 {
 int day = Convert.ToInt32(Daybox.Text);
 int year = Convert.ToInt32(Yearbox.Text);
 string month = Monthbox.Text;
 
 }
 catch (FormatException)
 {
 MessageBox.Show("Invalid input, Enter a valid form of date, please!");
 }
 finally
 {
 String date = Convert.ToString(Daybox.Text);
 String yr = Convert.ToString(Yearbox.Text);
 string month = Monthbox.Text;
 MessageBox.Show(date + "/" + month + "/" + yr);
 Daybox.Text = "";
 Monthbox.Text = "";
 Yearbox.Text = "";
 
 }
 
 }
 }
}



####################################### PROGRAM 6 6. String Manipulation  ####################################


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace ConsoleApplication1
{
 class Program
 {
 static void Main(string[] args)
 {
 {
 string s = string.Empty;
 Console.Write("Enter the String:");
 s = Console.ReadLine();
 int number = 0;
 int capitalLetter = 0;
 int smallletter = 0;
 int space = 0;
 int SpecialSymbol = 0;
 char[] a = s.ToCharArray();
 for (int i = 0; i < a.Length; i++)
 {
 if (a[i] >= 48 && a[i] <= 58)
 {
 number += 1;
 }
 else if (a[i] >= 65 && a[i] <= 90)
 {
 capitalLetter += 1;
 }
 else if (a[i] >= 97 && a[i] <= 122)
 {
 smallletter += 1;
 }
 else if (a[i] == 32)
 {
 space += 1;
 }
 else
 {
 SpecialSymbol += 1;
 }
 }
 Console.Write("Capital Letter " + capitalLetter);
 Console.Write("\nsmall letter " + smallletter);
 Console.Write("\nnumber are " + number);
 Console.Write("\nTotal Spaces " + space);
 Console.Write("\nTotal Special Symbol are " + SpecialSymbol);
 Console.WriteLine("\n\n\t\t\t\t Choose a string manipulation function:");
 Console.WriteLine("1. Clone");
 Console.WriteLine("2. Contains");
 Console.WriteLine("3. ToLower");
 Console.WriteLine("4. ToUpper");
 Console.WriteLine("5. Trim");
 Console.WriteLine("6. Substring");
 Console.WriteLine("7. Replace");
 string choice = Console.ReadLine();
 int ch = int.Parse(choice);
 string output = "";
 switch (ch)
 {
 case 1:
 String b = (String)s.Clone();
 output = b;
 Console.WriteLine("Output: " + output);
 break;
 case 2:
 Console.Write("Enter target substring: ");
 string tar = Console.ReadLine();
 Console.WriteLine(s.Contains(tar));
 break;
 case 3:
 output = s.ToLower();
 Console.WriteLine("Output: " + output);
 break;
 case 4:
 output = s.ToUpper();
 Console.WriteLine("Output: " + output);
 break;
 case 5:
 output = s.Trim();
 Console.WriteLine("Output: " + output);
 break;
 case 6:
 Console.Write("Enter start index: ");
 int start = int.Parse(Console.ReadLine());
 Console.Write("Enter length: ");
 int length = int.Parse(Console.ReadLine());
 output = s.Substring(start, length);
 Console.WriteLine("Output: " + output);
 break;
 case 7:
 Console.Write("Enter target substring: ");
 string target = Console.ReadLine();
 Console.Write("Enter replacement substring: ");
 string replacement = Console.ReadLine();
 output = s.Replace(target, replacement);
 Console.WriteLine("Output: " + output);
 break;
 default:
 Console.WriteLine("Invalid choice.");
 break;
 }
 Console.WriteLine("Press any key to exit.");
 Console.ReadKey();
 }
 }
 }
}

###################################### PROGRAM 7  7. Exercise using file operations########################################


using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace ConsoleApp2
{
 class Program
 {
 static void Main(string[] args)
 {
 string filepath = @"D:\Demo.txt";
 File.Create(filepath).Close();
 Console.WriteLine("A text file created successfully.");
 Console.ReadKey();
 if (File.Exists(filepath))
 {
 File.Delete(filepath);
 Console.WriteLine("Existing Text File Deleted.");
 Console.ReadKey();
 }
 File.WriteAllText(filepath, "Writing Hello text to a file.");
 Console.WriteLine("Created a new text file and wrote the text in it.");
 Console.WriteLine(File.ReadAllText(filepath));
 Console.ReadKey();
 try
 {
 using (StreamWriter sw = File.AppendText(filepath))
{
 sw.Write(Environment.NewLine + "Appending this text in a file.");
 sw.Close();
 Console.ReadKey();
 }
 }
 catch (FileNotFoundException fnfe)
 {
 Console.WriteLine("File Not Found Exception: " + fnfe);
 Console.ReadKey();
 }
 finally
 {
 Console.WriteLine(File.ReadAllText(filepath));
 Console.ReadKey();
 }
 string source = @"D:\Demo.txt";
 string destination = @"D:\Siv024.txt";
 try
 {
 File.Move(source, destination);
 File.Copy(destination, source);
 }
 catch (FileNotFoundException fnfe)
 {
 Console.WriteLine(fnfe);
 }
 string dirpath = @"D:\Aish";
 try
 {
 if (!Directory.Exists(dirpath))
 {
 Directory.CreateDirectory(dirpath);
 Console.WriteLine("Directory created successfully.");
 Console.ReadKey();
 }
 else
 {
 Console.WriteLine("Directory already exist.");
 Console.ReadKey();
 }
 }
 catch (IOException ioe)
 {
 Console.WriteLine(ioe);
 Console.ReadKey();
 }
 string filepath1 = @"D:\textfile.txt";
 if (File.Exists(filepath1))
 {
 File.Delete(filepath1);
 Console.WriteLine("Existing Text File Deleted.");
 Console.ReadKey();
 }
 File.Create(filepath1);
 Console.WriteLine("New Text file created successfully.");
 Console.ReadKey();
 }
 }
}



######################## PROGRAM 8 8. Exercise using master pages, menu ##########################################

----------------------------------------------------------------------------------
HEADER 
[ ENTER NAME ]   [ TEXTBOX  ]

 FURTHER
-------------------------------------------------------------------------------


Site1.Master
<%@ Master Language="C#" AutoEventWireup="true" CodeBehind="Site1.master.cs" 
Inherits="WebApplication1.Site1" %>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
 <asp:ContentPlaceHolder ID="head" runat="server">
 </asp:ContentPlaceHolder>
</head>
<body>
 <form id="form1" runat="server">
 <div>
 Header
 </div>
 <div>
 <asp:ContentPlaceHolder ID="ContentPlaceHolder1" runat="server">
 </asp:ContentPlaceHolder>
 <asp:ContentPlaceHolder ID="ContentPlaceHolder2" runat="server">
 </asp:ContentPlaceHolder>
 <asp:ContentPlaceHolder ID="ContentPlaceHolder3" runat="server">
 </asp:ContentPlaceHolder>
 </div>
 <div>
 <p>
 Footer
 </p>
 </div>
 </form>
</body>
</html>


webforms1.apsx
<%@ Page Title="" Language="C#" MasterPageFile="~/Site1.Master" 
AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs" 
Inherits="WebApplication1.WebForm1" %>
<asp:Content ID="Content1" ContentPlaceHolderID="head" runat="server">
</asp:Content>
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" 
runat="server">
</asp:Content>
<asp:Content ID="Content3" ContentPlaceHolderID="ContentPlaceHolder2" 
runat="server">
</asp:Content>
<asp:Content ID="Content4" ContentPlaceHolderID="ContentPlaceHolder3" 
runat="server">
 <asp:Label ID="Label1" runat="server" Text="Enter name"></asp:Label>
<asp:TextBox ID="TextBox1" runat="server" Height="16px" 
 style="margin-left: 9px" Width="208px"></asp:TextBox>
</asp:Content>


 ##################################### PRGRAM 9 9. Exercise using data bound controls ########################################3


 WebForms1.apx
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm2.aspx.cs" 
Inherits="WebApplication2.WebForm2" %>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
</head>
<body>
 <form id="form1" runat="server">
 <asp:Menu ID="Menu1" runat="server">
 <Items>
 <asp:MenuItem Text="College" Value="College">
 <asp:MenuItem Text="About us" Value="About us"></asp:MenuItem>
 <asp:MenuItem Text="Contact Us" Value="Contact Us"></asp:MenuItem>
 <asp:MenuItem Text="Placement report" Value="Placement 
report"></asp:MenuItem>
 </asp:MenuItem>
 <asp:MenuItem Text="Admission" Value="Admission">
 <asp:MenuItem Text="Courses offered" Value="Courses 
offered"></asp:MenuItem>
 <asp:MenuItem Text="Eligibility" Value="Eligibility"></asp:MenuItem>
 </asp:MenuItem>
 </Items>
 </asp:Menu>
 </form>
</body>
</html>

#########################################################   PROGRAM 10 

----------------------------------------------------------------------------------------------
NAME   [ TEXT BOX ]
PHONE  [ TEXTBOX ]
ADDRESS  [ TEXTBOX ]
EMAIL    [ TEXTBOX ]

SQL DATASOURCE 

[REGISTER ]
[VIEW ]

GRID VIEW

[DELETE ALL]

[DELETE ITAM ]
----------------------------------------------------------------------------------------------------

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Data.SqlClient;
namespace WebApplication27
{
public partial class WebForm1 : System.Web.UI.Page
{
SqlConnection con;
SqlCommand cmd;
SqlDataAdapter adp;
DataSet ds;
SqlDataAdapter rd;
string query;
public void dbcon()
{
string conn =
System.Configuration.ConfigurationManager.ConnectionStrings["dbcon"].ToString();
con = new SqlConnection(conn);
con.Open();
}
protected void Page_Load(object sender, EventArgs e)
{
}
protected void Button1_Click(object sender, EventArgs e)
{
dbcon();
query = "insert into Register(Name,Phonenumber,Address,Email)values('" + Name.Text +
"','" + Phoneno.Text + "','" + Address.Text + "','" + Email.Text + "')";
cmd = new SqlCommand(query, con);
cmd.ExecuteNonQuery();
Response.Write("<script>alert ('Data Added Successfully')</script>");
}
protected void Button2_Click(object sender, EventArgs e)
{
dbcon();
query = "Select *from Register";
cmd = new SqlCommand(query, con);
adp = new SqlDataAdapter(cmd);
ds = new DataSet();
adp.Fill(ds);
GridView1.DataSource = ds;
GridView1.DataBind();
}
protected void Button3_Click(object sender, EventArgs e)
{
dbcon();
query = "delete from Register";

cmd = new SqlCommand(query, con);
cmd.ExecuteNonQuery();
}
protected void Button4_Click(object sender, EventArgs e)
{
dbcon();
query = "delete from Register where name='"+Name.Text+"'";
cmd = new SqlCommand(query, con);
cmd.ExecuteNonQuery();
}
}
}

-----------------------------------------------------------------------------

                  STEPS 

-ASP .NET
-EMPTY WEBV FORM
- RIGHT CLICK ON webapplication on right -> add -> new item ->web form
- click on [design ]
- Agian (Right click on web application) -> add -> new item -> LEFT CLICK ON (DATA) -> SQL server database

- GO TO DESIGN
  ----------------------------------------------------------------------------------------------
NAME   [ TEXT BOX ]
PHONE  [ TEXTBOX ]
ADDRESS  [ TEXTBOX ]
EMAIL    [ TEXTBOX ]

SQL DATASOURCE 

[REGISTER ]
[VIEW ]

GRID VIEW

[DELETE ALL]

[DELETE ITAM ]
----------------------------------------------------------------------------------------------------
- Left click on (server explorer) -> data connection(click on arrow) ->database(click on arrow) -> righ click( Table)-> add new Table
- name varchar(50)
- phone varchar(10)
- address varchar(10)
- email varchar(10)
- > down mysql code change the table name as (Register)
  > up leaft corner of table (^| Update)
  > Update database
  
  > Go to webform 1
  > click on arrow [ SQL Database [>]  ] -> click on ( configure data source)
  >  open arrow box [  Database1. mdf  ]
  > next -> next-> finish 

