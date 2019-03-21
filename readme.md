
<body lang="en-US" dir="ltr">
<h1 class="western" style="font-variant: normal; letter-spacing: normal; font-style: normal"><a name="m_-3273528688681616859gmail-myassigmenttoaivenoy"></a>
My Assigment to Aiven oy</h1>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
There are two files read.py write.py, I found  basis for the code to
fulfill the assigment  and modified them in my work.</p>
<h2 class="western" style="font-variant: normal; letter-spacing: normal; font-style: normal; orphans: 2; widows: 2"><a name="m_-3273528688681616859gmail-howtoinstall"></a>
how to install</h2>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
you need to have python-pip kafka and postresql.</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
Also with pip you have to install kafka, psycopg2 and peewee. 
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
You need a table with the following</p>
<table width="100%" cellpadding="4" cellspacing="0">
	<col width="128*">
	<col width="128*">
	<tr valign="top">
		<td width="50%" style="border-top: 1px solid #000000; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0.04in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in">
			<p>id</p>
		</td>
		<td width="50%" style="border: 1px solid #000000; padding: 0.04in">
			<p>primary key</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in">
			<p>name</p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in">
			<p>varchar</p>
		</td>
	</tr>
	<tr valign="top">
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: none; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0in">
			<p>data</p>
		</td>
		<td width="50%" style="border-top: none; border-bottom: 1px solid #000000; border-left: 1px solid #000000; border-right: 1px solid #000000; padding-top: 0in; padding-bottom: 0.04in; padding-left: 0.04in; padding-right: 0.04in">
			<p>varchar</p>
		</td>
	</tr>
</table>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
 
</p>
<hr/>

<h2 class="western" style="font-variant: normal; letter-spacing: normal; font-style: normal; orphans: 2; widows: 2"><a name="m_-3273528688681616859gmail-readpy"></a>
read.py</h2>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
Read.py first connects to kafka producer at localhost port 9092 which
is the default port for kafka.</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
It then sends 'my-topic' with a value and key of 'raw_bytes'.</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
Then it prints the results from it</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
then it send to 'my-topic' wit a key of 'foo' and value of 'bar' it
tries max of 5 times</p>
<h2 class="western" style="font-variant: normal; letter-spacing: normal; font-style: normal; orphans: 2; widows: 2"><a name="m_-3273528688681616859gmail-writepy"></a>
write.py</h2>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
it imports peewee its a orm</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2">
<span style="font-style: normal"><span style="font-weight: normal">t</span></span><span style="font-style: normal"><span style="font-weight: normal">hen
i connect to the database create the class to be used for the orm
open a kafka consumer to localhost port 9092</span></span></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
then it loops over the messages it gets and saves them to the
database</p>
<p style="margin-bottom: 0in; line-height: 100%"><br/>

</p>
</body>
</html>
