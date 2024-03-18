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
if (textBox1.Text == &quot;&quot;)
{
MessageBox.Show(&quot;Enter Username !!&quot;);
}
else if (textBox2.Text == &quot;&quot;)
{
MessageBox.Show(&quot;Enter Password !!&quot;);
}
else if (textBox1.Text == &quot;Gripsy&quot; &amp;&amp; textBox2.Text == &quot;123&quot;)
{
this.Hide();
Form frm2 = new Form2();
frm2.ShowDialog();
}
else
{
MessageBox.Show(&quot;Invalid Credential&quot;, &quot;Try Again&quot;);
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

&lt;form id=&quot;form1&quot; runat=&quot;server&quot;&gt;
&lt;div&gt;
&lt;table style=&quot;width: 66%;&quot;&gt;
&lt;tr&gt;
&lt;td class=&quot;style1&quot; colspan=&quot;3&quot; align=&quot;center&quot;&gt;
&lt;asp:Label ID=&quot;lblmsg&quot;
Text=&quot;President Election Form : Choose your president&quot;
runat=&quot;server&quot; /&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;tr&gt;
&lt;td class=&quot;style3&quot;&gt;
Candidate:
&lt;/td&gt;
&lt;td class=&quot;style2&quot;&gt;
&lt;asp:DropDownList ID=&quot;candidate&quot; runat=&quot;server&quot; style=&quot;width:239px&quot;&gt;
&lt;asp:ListItem&gt;Please Choose a Candidate&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Deekshana&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Elakiya&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Abirami&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Buddy&lt;/asp:ListItem&gt;
&lt;/asp:DropDownList&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;asp:RequiredFieldValidator ID=&quot;rfvcandidate&quot; runat=&quot;server&quot;
ControlToValidate=&quot;candidate&quot; InitialValue=&quot;Please Choose a Candidate&quot;
ErrorMessage=&quot;Choose Your Candidate&quot;&gt;
&lt;/asp:RequiredFieldValidator&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;tr&gt;
&lt;td class=&quot;style3&quot;&gt;
House:
&lt;/td&gt;
&lt;td class=&quot;style2&quot;&gt;
&lt;asp:RadioButtonList ID=&quot;rblhouse&quot; runat=&quot;server&quot; RepeatLayout=&quot;Flow&quot;&gt;
&lt;asp:ListItem&gt;Red&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Blue&lt;/asp:ListItem&gt;

&lt;asp:ListItem&gt;Yellow&lt;/asp:ListItem&gt;
&lt;asp:ListItem&gt;Green&lt;/asp:ListItem&gt;
&lt;/asp:RadioButtonList&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;asp:RequiredFieldValidator ID=&quot;rfvhouse&quot; runat=&quot;server&quot;
ControlToValidate=&quot;rblhouse&quot; ErrorMessage=&quot;Enter your house name&quot; &gt;
&lt;/asp:RequiredFieldValidator&gt;
&lt;br /&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;tr&gt;
&lt;td class=&quot;style3&quot;&gt;
Class:
&lt;/td&gt;
&lt;td class=&quot;style2&quot;&gt;
&lt;asp:TextBox ID=&quot;txtclass&quot; runat=&quot;server&quot;&gt;&lt;/asp:TextBox&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;asp:RangeValidator ID=&quot;rvclass&quot;
runat=&quot;server&quot; ControlToValidate=&quot;txtclass&quot;
ErrorMessage=&quot;Enter your current year in numbers&quot; MaximumValue=&quot;3&quot;
MinimumValue=&quot;1&quot; Type=&quot;Integer&quot;&gt;
&lt;/asp:RangeValidator&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;tr&gt;
&lt;td class=&quot;style3&quot;&gt;
Email:
&lt;/td&gt;
&lt;td class=&quot;style2&quot;&gt;
&lt;asp:TextBox ID=&quot;txtemail&quot; runat=&quot;server&quot; style=&quot;width:250px&quot;&gt;
&lt;/asp:TextBox&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;asp:RegularExpressionValidator ID=&quot;remail&quot; runat=&quot;server&quot;
ControlToValidate=&quot;txtemail&quot; ErrorMessage=&quot;Enter your email&quot;
ValidationExpression=&quot;\w+([-+.&#39;]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*&quot;&gt;
&lt;/asp:RegularExpressionValidator&gt;
&lt;/td&gt;

&lt;/tr&gt;
&lt;tr&gt;
&lt;td class=&quot;style3&quot; align=&quot;center&quot; colspan=&quot;3&quot;&gt;
&lt;asp:Button ID=&quot;Button1&quot; runat=&quot;server&quot; onclick=&quot;Button1_Click&quot; Text=&quot;Submit&quot; /&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;/table&gt;
&lt;asp:ValidationSummary ID=&quot;ValidationSummary1&quot; runat=&quot;server&quot;
DisplayMode =&quot;BulletList&quot; ShowSummary =&quot;true&quot; HeaderText=&quot;Errors:&quot; /&gt;
&lt;/div&gt;
&lt;/form&gt;
protected void Button1_Click(object sender, EventArgs e)
{
if (Page.IsValid)
{
lblmsg.Text = &quot;Thank You&quot;;
}
else
{
lblmsg.Text = &quot;Fill up all the fields&quot;;
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
winnerLabel.Text = &quot; TIE &quot;;
break;

case 2:
computer.BackgroundImage = paper.BackgroundImage;
winnerLabel.Text = &quot; Computer wins because paper covers rock &quot;;
break;
case 3:
computer.BackgroundImage = scissor.BackgroundImage;
winnerLabel.Text = &quot; Player wins because rock breaks scissors &quot;;
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
winnerLabel.Text = &quot; Payer wins because paper covers rock &quot;;
break;
case 2:
computer.BackgroundImage = paper.BackgroundImage;
winnerLabel.Text = &quot; TIE &quot;;
break;
case 3:
computer.BackgroundImage = scissor.BackgroundImage;
winnerLabel.Text = &quot; Computer wins because scissors cut paper &quot;;
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
winnerLabel.Text = &quot; Computer wins because rock breaks scissors &quot;;
break;
case 2:
computer.BackgroundImage = paper.BackgroundImage;
winnerLabel.Text = &quot; Player wins because scissors cut paper &quot;;
break;
case 3:
computer.BackgroundImage = scissor.BackgroundImage;
winnerLabel.Text = &quot; TIE &quot;;
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
txt_msg.Text = &quot;Turn OFF your engine&quot;;
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
txt_msg.Text = &quot;Have a safe journey&quot;;
timer1.Interval = 1000;
a = 2;
}
else if (a == 2)
{
count = 10;
pictureBox1.Visible = false;

pictureBox2.Visible = true;
pictureBox3.Visible = false;
txt_msg.Text = &quot;slow down your vehicle&quot;;
timer1.Interval = 1000;
a = 3;
}
else if (a == 3)
{
count = 10;
pictureBox1.Visible = true;
pictureBox2.Visible = false;
pictureBox3.Visible = false;
txt_msg.Text = &quot;stop your vehicle&quot;;
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
Form1.CS

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
MessageBox.Show(&quot;Invalid input enter two numbers please&quot;);
}
catch (DivideByZeroException divideByZeroException)
{
MessageBox.Show(divideByZeroException.Message, &quot;Can&#39;t divide by zero&quot;);
}
finally
{
textBox1.Text = &quot;&quot;;
textBox2.Text = &quot;&quot;;
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

MessageBox.Show(&quot;Invalid input, Enter a valid form of date, please!&quot;);
}
finally
{
String date = Convert.ToString(Daybox.Text);
String yr = Convert.ToString(Yearbox.Text);
string month = Monthbox.Text;
MessageBox.Show(date + &quot;/&quot; + month + &quot;/&quot; + yr);
Daybox.Text = &quot;&quot;;
Monthbox.Text = &quot;&quot;;
Yearbox.Text = &quot;&quot;;
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
Console.Write(&quot;Enter the String:&quot;);
s = Console.ReadLine();
int number = 0;
int capitalLetter = 0;
int smallletter = 0;
int space = 0;
int SpecialSymbol = 0;
char[] a = s.ToCharArray();
for (int i = 0; i &lt; a.Length; i++)

{
if (a[i] &gt;= 48 &amp;&amp; a[i] &lt;= 58)
{
number += 1;
}
else if (a[i] &gt;= 65 &amp;&amp; a[i] &lt;= 90)
{
capitalLetter += 1;
}
else if (a[i] &gt;= 97 &amp;&amp; a[i] &lt;= 122)
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
Console.Write(&quot;Capital Letter &quot; + capitalLetter);
Console.Write(&quot;\nsmall letter &quot; + smallletter);
Console.Write(&quot;\nnumber are &quot; + number);

Console.Write(&quot;\nTotal Spaces &quot; + space);
Console.Write(&quot;\nTotal Special Symbol are &quot; + SpecialSymbol);
Console.WriteLine(&quot;\n\n\t\t\t\t Choose a string manipulation function:&quot;);
Console.WriteLine(&quot;1. Clone&quot;);
Console.WriteLine(&quot;2. Contains&quot;);
Console.WriteLine(&quot;3. ToLower&quot;);
Console.WriteLine(&quot;4. ToUpper&quot;);
Console.WriteLine(&quot;5. Trim&quot;);
Console.WriteLine(&quot;6. Substring&quot;);
Console.WriteLine(&quot;7. Replace&quot;);
string choice = Console.ReadLine();
int ch = int.Parse(choice);
string output = &quot;&quot;;

switch (ch)
{
case 1:
String b = (String)s.Clone();
output = b;
Console.WriteLine(&quot;Output: &quot; + output);
break;
case 2:
Console.Write(&quot;Enter target substring: &quot;);
string tar = Console.ReadLine();
Console.WriteLine(s.Contains(tar));

break;
case 3:
output = s.ToLower();
Console.WriteLine(&quot;Output: &quot; + output);
break;
case 4:
output = s.ToUpper();
Console.WriteLine(&quot;Output: &quot; + output);
break;
case 5:
output = s.Trim();
Console.WriteLine(&quot;Output: &quot; + output);
break;
case 6:
Console.Write(&quot;Enter start index: &quot;);
int start = int.Parse(Console.ReadLine());
Console.Write(&quot;Enter length: &quot;);
int length = int.Parse(Console.ReadLine());
output = s.Substring(start, length);
Console.WriteLine(&quot;Output: &quot; + output);
break;
case 7:
Console.Write(&quot;Enter target substring: &quot;);
string target = Console.ReadLine();
Console.Write(&quot;Enter replacement substring: &quot;);

string replacement = Console.ReadLine();
output = s.Replace(target, replacement);
Console.WriteLine(&quot;Output: &quot; + output);
break;
default:
Console.WriteLine(&quot;Invalid choice.&quot;);
break;
}
Console.WriteLine(&quot;Press any key to exit.&quot;);
Console.ReadKey();
}
}
}
}

###################################### PROGRAM 7  7. Exercise using file operations########################################

using System;
using System.IO;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication1
{
class Program
{
static void Main(string[] args)
{
string filepath = @&quot;D:\Demo.txt&quot;;
File.Create(filepath);                                            OR File. Create(filepath). Close() ;
Console.WriteLine(&quot;A text file created successfully.&quot;);

Console.ReadKey();

/* if(File.Exists(filepath))
{
File.Delete(filepath);
Console.WriteLine(&quot;Existing Text File Deleted.&quot;);
Console.ReadKey();

}
File.WriteAllText(filepath, &quot;Writing Hello text to a file.&quot;);
Console.WriteLine(&quot;Created a new text file and wrote the text in it.&quot;);
Console.WriteLine(File.ReadAllText(filepath));
Console.ReadKey();*/
/* try
{
using (StreamWriter sw = File.AppendText(filepath))
{
sw.Write(Environment.NewLine + &quot;Appending this text in a file.&quot;);
sw.Close();
Console.ReadKey();
}
}
catch (FileNotFoundException fnfe)
{
Console.WriteLine(&quot;File Not Found Exception: &quot; + fnfe);
Console.ReadKey();
}
finally
{
Console.WriteLine(File.ReadAllText(filepath));
Console.ReadKey();
}
/* string source = @&quot;D:\Demo.txt&quot;;

string destination = @&quot;F:\Demo.txt&quot;;
try
{
File.Move(source, destination);
File.Copy(destination, source);
}
catch (FileNotFoundException fnfe)
{
Console.WriteLine(fnfe);
}*/
/* string dirpath = @&quot;F:\Aish&quot;;
try
{
if (!Directory.Exists(dirpath))
{
Directory.CreateDirectory(dirpath);
Console.WriteLine(&quot;Directory created successfully.&quot;);
Console.ReadKey();
}
else
{
Console.WriteLine(&quot;Directory already exist.&quot;);
Console.ReadKey();
}
}

catch (IOException ioe)
{
Console.WriteLine(ioe);
Console.ReadKey();
}
/* string filepath1 = @&quot;D:\textfile.txt&quot;;
if (File.Exists(filepath1))
{
File.Delete(filepath1);
Console.WriteLine(&quot;Existing Text File Deleted.&quot;);
Console.ReadKey();
}
File.Create(filepath1);
Console.WriteLine(&quot;New Text file created successfully.&quot;);
Console.ReadKey();

*/
//}

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
&lt;%@ Master Language=&quot;C#&quot; AutoEventWireup=&quot;true&quot; CodeBehind=&quot;Site1.master.cs&quot;
Inherits=&quot;WebApplication1.Site1&quot; %&gt;
&lt;!DOCTYPE html PUBLIC &quot;-//W3C//DTD XHTML 1.0 Transitional//EN&quot;
&quot;http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd&quot;&gt;
&lt;html xmlns=&quot;http://www.w3.org/1999/xhtml&quot;&gt;
&lt;head runat=&quot;server&quot;&gt;
&lt;title&gt;&lt;/title&gt;
&lt;asp:ContentPlaceHolder ID=&quot;head&quot; runat=&quot;server&quot;&gt;
&lt;/asp:ContentPlaceHolder&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;form id=&quot;form1&quot; runat=&quot;server&quot;&gt;
&lt;div&gt;
Header
&lt;/div&gt;
&lt;div&gt;
&lt;asp:ContentPlaceHolder ID=&quot;ContentPlaceHolder1&quot; runat=&quot;server&quot;&gt;
&lt;/asp:ContentPlaceHolder&gt;
&lt;asp:ContentPlaceHolder ID=&quot;ContentPlaceHolder2&quot; runat=&quot;server&quot;&gt;
&lt;/asp:ContentPlaceHolder&gt;
&lt;asp:ContentPlaceHolder ID=&quot;ContentPlaceHolder3&quot; runat=&quot;server&quot;&gt;
&lt;/asp:ContentPlaceHolder&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;p&gt;
Footer
&lt;/p&gt;
&lt;/div&gt;
&lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;

webforms1.apsx

&lt;%@ Page Title=&quot;&quot; Language=&quot;C#&quot; MasterPageFile=&quot;~/Site1.Master&quot;
AutoEventWireup=&quot;true&quot; CodeBehind=&quot;WebForm1.aspx.cs&quot;
Inherits=&quot;WebApplication1.WebForm1&quot; %&gt;
&lt;asp:Content ID=&quot;Content1&quot; ContentPlaceHolderID=&quot;head&quot; runat=&quot;server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:Content ID=&quot;Content2&quot; ContentPlaceHolderID=&quot;ContentPlaceHolder1&quot; runat=&quot;server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:Content ID=&quot;Content3&quot; ContentPlaceHolderID=&quot;ContentPlaceHolder2&quot; runat=&quot;server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:Content ID=&quot;Content4&quot; ContentPlaceHolderID=&quot;ContentPlaceHolder3&quot; runat=&quot;server&quot;&gt;
&lt;asp:Label ID=&quot;Label1&quot; runat=&quot;server&quot; Text=&quot;Enter name&quot;&gt;&lt;/asp:Label&gt;
&lt;asp:TextBox ID=&quot;TextBox1&quot; runat=&quot;server&quot; Height=&quot;16px&quot;
style=&quot;margin-left: 9px&quot; Width=&quot;208px&quot;&gt;&lt;/asp:TextBox&gt;
&lt;/asp:Content&gt;


 ##################################### PRGRAM 9 9. Exercise using data bound controls ########################################3


 WebForms1.apx
&lt;%@ Page Language=&quot;C#&quot; AutoEventWireup=&quot;true&quot; CodeBehind=&quot;WebForm2.aspx.cs&quot;
Inherits=&quot;WebApplication2.WebForm2&quot; %&gt;
&lt;!DOCTYPE html PUBLIC &quot;-//W3C//DTD XHTML 1.0 Transitional//EN&quot;
&quot;http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd&quot;&gt;
&lt;html xmlns=&quot;http://www.w3.org/1999/xhtml&quot;&gt;
&lt;head runat=&quot;server&quot;&gt;
&lt;title&gt;&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;form id=&quot;form1&quot; runat=&quot;server&quot;&gt;
&lt;asp:Menu ID=&quot;Menu1&quot; runat=&quot;server&quot;&gt;
&lt;Items&gt;
&lt;asp:MenuItem Text=&quot;College&quot; Value=&quot;College&quot;&gt;
&lt;asp:MenuItem Text=&quot;About us&quot; Value=&quot;About us&quot;&gt;&lt;/asp:MenuItem&gt;
&lt;asp:MenuItem Text=&quot;Contact Us&quot; Value=&quot;Contact Us&quot;&gt;&lt;/asp:MenuItem&gt;
&lt;asp:MenuItem Text=&quot;Placement report&quot; Value=&quot;Placement
report&quot;&gt;&lt;/asp:MenuItem&gt;
&lt;/asp:MenuItem&gt;
&lt;asp:MenuItem Text=&quot;Admission&quot; Value=&quot;Admission&quot;&gt;
&lt;asp:MenuItem Text=&quot;Courses offered&quot; Value=&quot;Courses offered&quot;&gt;&lt;/asp:MenuItem&gt;
&lt;asp:MenuItem Text=&quot;Eligibility&quot; Value=&quot;Eligibility&quot;&gt;&lt;/asp:MenuItem&gt;
&lt;/asp:MenuItem&gt;
&lt;/Items&gt;
&lt;/asp:Menu&gt;
&lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;


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



