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
Now that might sound extremely intimidating but don't worry, I'll walk you through it step by step. Now the reason we want to send these alerts over to the Hive is so we can keep track of who is working on the alerts, similar to what a real SOC environment would do, along with sending emails directly to an inbox to review the details of the set alert. 
<br />
<br />
For example, if an IDS alert was generated for a Cobalt Strike, the analyst would then begin by looking at surrounding events and if they identified the user had accessed, let's say a domain called malware.com, prior to the alert. They could then perform additional analysis on that domain. Analysts can utilize domain reputation tools for passive analysis, and if they have the go-ahead, they can perform dynamic analysis by looking at the domain's behavior by accessing it. Using a platform.
<br />
<br />
You might be asking, Can't you just do everything from Wasa? I mean, kind of, but that's just too simple. I want you to flex your skills, work on your troubleshooting, and get some exposure to SAR and a case management system such as the Hive.

That is it for this intro. I hope you are as excited as I am to get started. If you plan on following along, do set up a GitHub account or a free site if you haven't done so already, because you do want to showcase your work and prove to others that you have built a SOC automation lab.
