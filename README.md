<h1>SOC Automation (Home Lab)</h1>


<h2>Description</h2>
Are you looking for a project that you can do for free to impress hiring managers? Or maybe you want to build something challenging and rewarding. I want you to imagine something having your own SOC automation lab that will include Wasa, which will be your SIEM and XDR. The Hive, for case management, and Shuffle, for SOAR capabilities.
<br />
<br />
If you are someone that is wanting to get some solid hands-on experience. I am positive that this project will do just that. The good news is that this can be done in the cloud, so that means, anybody can do this project from scratch. I'll take you from not having a home Lab at all to a fully functional home lab with responsive capabilities and a case management system to mimic a real SOC environment. It will be up to you at the end to scale it to how you want it to be and automate to your liking. You can seriously make this go from a basic home lab to a very Advanced Home lab quickly.
<br />
<br />
This will be a five-part series... 
<br />
<br />
Part 1
I will walk you through how you can draw a logical diagram, as this will help you visualize your lab and make it easier; for not only yourself but also for others to digest. 
<br />
<br />
Part 2
<br />
<br />
I will walk you through on how to install the components and get you set up in the cloud. If you don't want to use the cloud and have the resources to spin up a virtual machine on your host, you can do that as well.
<br />
<br />
Day 3 
<br />
<br />
I will walk you through how to configure the servers and endpoints to talk to one another.
<br />
<br />
Day 4
<br />
<br />
The fourth day will be exciting because we will begin generating telemetry that is related to Mimikatz on our endpoint, which will then trigger an alert on Wasa that you created on purpose.
<br />
<br />
Day 5 
<br />
<br />
The final day will be a long one as we will go through how to set up SOAR step by step and integrate everything. This means our Wasah, The Hive, and Shuffle. We will see how alerts get sent over to the SOAR platform and created in the Hive, while automatically emailing analysts such as yourself about the details of the alert along with automated responsive availabilities. 
<br />
<br />
Now that might sound extremely intimidating but don't worry, I'll walk you through it step by step. Now the reason we want to send these alerts over to the Hive is so we can keep track of who is working on the alerts, similar to what a real SOC environment would do. Along with sending emails directly to an inbox to review the details of the set alert. 
<br />
<br />
For example, if an IDS alert was generated for a Cobalt Strike, the analyst would then begin by looking at surrounding events and if they identified the user had accessed, let's say a domain called malware.com, prior to the alert. They could then perform additional analysis on that domain. Analysts can utilize domain reputation tools for passive analysis, and if they have the go-ahead, they can perform dynamic analysis by looking at the domain's behavior by accessing it. Using a platform, for example, SquareX.
<br />
<br />
Squarex provides consumers with what is called Disposable Web Browsers, Disposable File Viewers, Disposable Emails, and offers smart integration. I've personally switched over to using squarex to help me perform additional investigation especially when I want to perform some dynamic browser analysis, because there are times when I am curious what this particular website will do if access. Perhaps a file was downloaded, or maybe the site redirected you to another site that hosts suspicious or malicious activity. 
<br />
<br /> 
Now of course, with every investigation, you want to make sure you do your due diligence and perform what is called passive analysis on your IOC's. Also known as your indicators of compromise; before you think think about dynamic analysis. But after you've done your due diligence and perhaps been given the green light from senior analysts using Square X's disposable products is extremely easy to use and convenient and it also has one amazing feature that I'll show at the end because of that I've switched over from using other browser tools to using Square X to begin we'll head over to their site you will be presented with two options the first one is using their web extension and and that is available on Chrome Edge and brave or number two you can use their web app there are benefits on using either one of them and regardless of the option you will still have the capability of utilizing these amazing disposable products for example if you were to use the extension squarex will integrate its capability onto your web browser this means that you can quickly spin up a disposable browser a follow viewer or even email with just a couple couple clicks and it will all integrate with each other in other words if I were to receive a link in my disposable email I can go ahead and click on the link and it will open up a disposable web browser automatically you can only do this with  the extension it also comes with what are called smart Integrations this will provide you with the capability to block all email trackers so senders will never know that you've viewed their email and as a bonus it's a seamless inter ation with Gmail but if you're like me and don't like to install web extensions because they tend to be well extremely permissive that's okay because squarex thought of that as well and built out a web application for people like myself who is extremely paranoid and I can still use the tool without the extension we do not get the smart integration or any integration but that is okay we can still utilize the Disposable browser file viewer and the emails separately let me show you how easy it is to use Square X if you have the web extension installed to spin up a web browser all you need to do is click
8:11
on the icon select from the dropdown and
8:14
select the country where you want the
8:16
browser to Source from so for me I'll go
8:19
ahead and select Canada and hit start
8:22
and just like that a disposable browser
8:24
is spun up a couple of quick pointers
8:26
here though on the bottom right I want
8:29
you to take a look at those download
8:30
speeds if you have terrible internet you
8:33
could potentially use this to your
8:35
advantage now secondly this browser has
8:38
a capability to share the session
8:41
amongst others this is extremely helpful
8:45
for us analysts who work from home and
8:47
I'll tell you why if I wanted another
8:49
analyst to take a look at a certain site
8:52
maybe I needed some help with an
8:53
investigation instead of sharing my
8:55
screen I could easily just share my
8:57
session next are the options to block or
9:01
see an ad now I know what you might be
9:03
thinking why would I want to see an ad
9:07
maybe you're investigating something
9:08
that relates to ads perhaps a malicious
9:11
embedded URL in an ad the next option is
9:15
the sound option you can turn that on or
9:17
off and finally the ability to full
9:20
screen the browser you might have
9:22
noticed that there's a timer as well
9:24
when it's around 3 minutes you can
9:27
actually extend the timer by 10 minutes
9:30
which is a nice feature to have so let's
9:32
go ahead and type in speed test and
9:34
check it out and just look at those
9:36
speeds crazy we can also check our IP
9:40
just to make sure it isn't running on
9:42
our public IP moving on to the
9:45
Disposable file viewer we can open this
9:48
by clicking on the icon and hit start
9:50
this is a lifesaver for me personally
9:53
because there have been so many times
9:55
when my family members ask me if I could
9:57
open up a certain doc document because
10:00
they just don't have the application
10:02
installed and me being extremely
10:05
paranoid I second guess everything
10:08
before executing so file viewers are a
10:12
lifesaver with the file viewer I could
10:14
simply just drag and drop the document
10:17
or instruct my family to sign up for
10:19
square X and use it and open it there
10:22
honestly I say this way too many times
10:25
but it's a lifesaver for example let's
10:28
say that Bobby wants to open up an Excel
10:31
document and ask if you can help him see
10:33
the contents within that document well
10:36
you yourself don't have Excel as well so
10:38
you instruct Bobby to head over to
10:40
square X sign up and log in and open up
10:43
a disposable file viewer so let's just
10:46
say that this is Bobby's computer as you
10:48
can see he wants to open up an Excel
10:50
file called cyber security terminology
10:53
and he can't because he does not have
10:55
Excel installed so let's go ahead and
10:58
drag this file into the file viewer and
11:02
now Bobby can learn all the terminology
11:05
he wants there are a couple of options
11:07
on the bottom right you have the option
11:10
to share the session similar to the web
11:13
browser along with the sound however
11:17
there are two additional options and one
11:20
of it is uploading a file and the second
11:22
is to download the file now just for fun
11:25
let's go ahead and copy the file session
11:27
and then dispose our our session just to
11:30
see if we could re access our session to
11:32
dispose our web browser or even a file
11:35
viewer you can simply close out the tab
11:38
click on the extension icon if you're
11:40
using the extension and then click on
11:43
dispose this should tear down the
11:45
session and we'll paste in the session
11:48
that we copied earlier and look at that
11:52
it's gone next is the Disposable emails
11:55
by default squarex generates a random
11:58
email for for you and you have the
12:00
option to regenerate these if you like
12:03
or edit them to your liking we can
12:05
simply access our inbox by clicking on
12:08
inbox and all of the emails will be here
12:12
this is a great way to prevent using
12:15
your actual email when a company asks
12:17
you for well your email do keep in mind
12:20
though because these are disposable
12:23
emails you will not have the option to
12:25
actually send from them because that's
12:27
not the purpose as for smart
12:30
Integrations this is automatically
12:32
turned on and integrated with Gmail so
12:35
if we go ahead and right click our email
12:38
and select preview in enhanced privacy
12:41
mode the email will open up in a
12:44
disposable file viewer and will block
12:47
all email trackers including images and
12:50
will not alert the senders that you had
12:52
read the email you have the ability to
12:55
modify the settings by simply toggling
12:58
on or off and you're good to go lastly
13:02
in addition to the ease of use the one
13:05
feature that made me switch over from
13:08
other web
13:11
products now I know what you are
13:13
thinking what happens to my data or is
13:16
my data being sent to square X isn't
13:20
this a privacy issue well I'm always
13:23
skeptical trust me however Square X
13:25
claims that they do not track or store
13:28
any of the user's data therefore
13:31
anything that happens within the
13:33
container itself is out of their
13:35
visibility there are no logs retained
13:38
and everything is destroyed so this
13:41
includes artifacts or history or
13:44
anything once you dispose the browser or
13:46
file viewer it is all gone I'll leave a
13:49
link down below for you to sign up with
13:52
squarex seriously try them out for
13:54
yourself and if you've used other
13:57
browser tools before you will love
14:00
squarex really the sky is the limit once
14:03
you have completed the sock automation
14:06
project and have it up and running you
14:08
will likely come across a lot of Errors
14:10
during this project but please don't get
14:13
discouraged I want you to try and
14:16
research for the answers and see if you
14:18
can solve it if you cannot find the
14:21
answer leave it in the comment section
14:23
below and I'm sure someone may have the
14:25
answer to that you might be asking can
14:28
you just do well everything from Wasa I
14:32
mean kind of yeah but that's just too
14:35
simple I want you to flex your skills
14:38
work on your troubleshooting and get
14:40
some exposure to SAR and a case
14:43
management system such as the hive that
14:46
is it for the video and I hope you are
14:48
excited as I am to get started if you
14:51
plan on following along do set up a
14:54
GitHub account or a free site if you
14:56
haven't done so already because you do
14:59
want to showcase your work and prove to
15:02
others that you have built a sock
15:05
automation lab



<br />


<h2>Utilities used...</h2>

- <b>Remote Desktop Tool</b> 
- <b>Virtual Box</b>
- <b>Windows Virtual Machine</b>

<h2>Environments Used </h2>

- <b>Windows 11</b>
- <b>Windows 10 (Version 22H2)</b>

<h2>Platform walk-through:</h2>

<p align="center">
Go to https://www.microsoft.com/en-us/software-download/windows10%20 and download the installation build: <br/>
<br />
<img src="https://snipboard.io/NrGytV.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/w8zxDQ.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Go to https://www.virtualbox.org/wiki/Download_Old_Builds_7_1 and download the 7.1.2 version build : <br/>
<br />
<img src="https://snipboard.io/VZeY7x.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/5OPW09.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Go to https://accounts.spiceworks.com/join?referrer_source=login&referrer_reference=joinlink and create an account: <br/>
<br />
<img src="https://snipboard.io/HTGY4E.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Launch Virtual Box and create the new Windows virtual machine : <br/>
<br />
<img src="https://snipboard.io/mpUL8O.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/0U963K.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Launch the Windows virtual machine:  <br/>
<br />
<img src="https://snipboard.io/iQmljB.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/gaoPSF.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Click on I don't have a product key:  <br/>
<br />
<img src="https://snipboard.io/ST6bXt.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Click on Windows 10 Pro:  <br/>
<br />
<img src="https://snipboard.io/mRz7q1.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Click on the drive that you would like to install Windows:  <br/>
<br />
<img src="https://snipboard.io/S8JHyC.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/maQdUc.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Create your Windows account:  <br/>
<br />
<img src="https://snipboard.io/q73I8k.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/8WH9Zg.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Go to https://www.spiceworks.com/tools/remote-support/ back on your original operating system and click on Start remote Session:  <br/>
<br />
<img src="https://snipboard.io/0x7yW6.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/4HP5Oa.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Go back to your Windows virtual machine and copy and paste the link from the original operating system to enter the digits: <br />
<br />
<img src="https://snipboard.io/QgGstn.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Click on Agree and Download. When you do this you'll receive a downloadable installation on your Windows virtual machine which you need to install: <br />
<br />
<img src="https://snipboard.io/ZEcg8K.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/cz65IS.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Click on Agree and Download. When you do this you'll receive a downloadable installation on your Windows virtual machine which you need to install: <br />
<br />
<img src="https://snipboard.io/ZEcg8K.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
When you see this pop-up on your virtual machine press Join from there will be a direct connection from your original system to your virtual system:  <br/>
<br />
<img src="https://snipboard.io/4Er6m3.jpg" height="10%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
As you can see, the virtual system can be controlled from the original system. There are a load of impressive features that you can use for remote troubleshooting. :  <br/>
<img src="https://snipboard.io/fSjo89.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/TgwtAq.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Task manager to check for performance issues, Firewall for malware, and security concerns, Computer Management to check software errors and crashes, etc.:  <br/>
<br />
<img src="https://snipboard.io/x3woUs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
