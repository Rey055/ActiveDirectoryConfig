# ActiveDirectoryConfig

<p align="center">
<img src="https://www.secsign.com/wp-content/uploads/2018/02/active-directory-logo.png" alt="Active Directory logo"/>
</p>

<h2> Enviroments and Technologies used   </h2>
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows 10 Server

<h2> Operating Systems</h2>
- Windows 10
  
  
  
  <h2>Active Directory setup</h2>
  
  <p>
  <img/ src = "https://i.imgur.com/j4L9yBj.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   Using microsoft Azure. I have created two Virtual machines. ONe our data Server named "DC-1" this is where our main windows server will be on. The other being "Client-1 " this client being our test cimputer to connect to our server that will contain Active directory. Now will need to test traffic for both the Client to DC.
  </p>
  
   <p>
  <img/ src = "https://i.imgur.com/FeHYRvE.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   First, Logging on to Client-1 we will need to ping Dc-1. We notice that no specfic traffic is reaching from client to DC.
    we staart noticing by defualt ICMP4 traffic cannot be eastibalished from our DC-1(10.0.0.4). Now we need to enable this traffic in our DC-1
  </p>
  
   <p>
  <img/ src = "https://i.imgur.com/qOhdg78.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p> In DC-1, once wew log on we have to access windows firewall security. Once we lauch this program, we go to far left and slect inbound rules from a clent.
  Once here we fileter protcol trasffic and slelect the first two ICMp4 rules. Once they are highlighted we go to right and enable rule.
  </p>
  
   <p>
  <img/ src = "https://i.imgur.com/erCiiTU.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  Then once enabled, we go back to our client. and we notice the results. ICMP4 traffic is able to be established from DC-1 To Client-1.
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/y69ffIu.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>  Now with everything established we can start setting up active directory. CLick on the 2nd step "add roles" amd features. You can just ciick the defaults. Just be sure on server slection to check Active dDirectory and Domain services pictured here. Once this is done just click through it all after and press install.
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/pNdk8Bu.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   Now that we installed it we need to set up a domain name. In order for all our users to easily connect to our server.
  We click on the flag icon on the upper right. We then press promote this this pc to domain controller.  Be sure on config to Slect add a new forest. Ijn this example our domain is called "Domain.com". Also, secondly be sure to set a password for our domain admin.  Now you canleave the defaults and just install everything.
  once done the server will have to restart to set all the settings for the domain Controller. Be sure the user is formatted, in this case, Domain.com\user.
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/NQqLY9t.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   its time to set up are directories. One will be For employees and one for admins in the "Active Directory  users and comoputers" You can just search this up on the bottom left of windows search bar.  As pictured here u create a new organizational unit. I will create on for admin here. 
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  
  
  <p>
  <img/ src = "https://i.imgur.com/VxiwwFq.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>  since joe is made and categorized as an admin. We need to set him as an admin. So we right click on them and press properties. Then we click the sub menu of "Memebr of " and press add . then in this we type Domain Admins. then apply and press ok.
  </p>
  
  
  
  <p>
  <img/ src = "https://i.imgur.com/xMR1o3z.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   Now we need to test out our Admin account on DC-1
  </p>
  
  
  
  <p>
  <img/ src = "https://i.imgur.com/2o9QKDs.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   
  Now its time to connect our Client-1 to DC-1. Here we need to set our DNS settings for Client-1. We set it to DC-1 IP settings.
  </p>
  
  
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
  
  
  <p>
  <img/ src = "https://i.imgur.com/VCbfLH2.png" height ="80%" width = "80%" alt= "Active Directory img"/>
  </p>
    
 <p>   now we need to create our admin. Here its gonna be Joe Doe. Their Log in is going to be joe_admin. 
  </p>
    
