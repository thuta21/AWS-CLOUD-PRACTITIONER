Content 

1. What is Cloud Computing?
2. Advantages of Cloud Computing
3. Deployment Model
	1. Cloud-Based Deployment ( Public Cloud )
	2. On-Premises Deployment ( Private Cloud )
	3. Hybrid Deployment
4. Service Model
	1. IaaS ( infrastructure as a service )
	2. PaaS ( platform as a service )
	3. SaaS ( software as a service )

------------------------------------------------------------------------

- Cloud Computing Technologies
  
  "The on-demand delivery of IT resources over the internet with pay-as-you-go pricing"
  
  Cloud Computing ဆိုတာသည် Physically အရ Resources တွေကို သုံးစရာမလိုပဲ အင်တာနက်ပေါ်က တစ်ဆင့် IT Resources ( Apps, Systems, Services, Softwares, Databases. Server, Platform ) တွေကို သုံးသလောက်ပေး ပုံစံ ( Pay-as-you-go pricing ) model နဲ့ ရယူအသုံးပြုချင်း ဖြစ်ပါတယ်။
  
  ဒီလို အင်တာနက်ပေါ်က တစ်ဆင့် အသုံးပြုနိုင်တာကြောင့် On-premise data center တွေလိုမဟုတ်ပဲ Hardware Management ပိုင်းတွေကို maintain လုပ်တဲ့နေရာမှာ အချိန် နဲ့ ငွေကုန်ကြေးကျ သက်သာစေပါတယ်။
  
  Cloud Providers : AWS, AZURE, Google Cloud Platform, IBM Cloud ...

------------------------------------------------------------------------

- Benefits of Cloud Computing
  
  1. Cost Saving : On-premise Data Center တွေ Server တွေ အတွက် Invest လုပ်စရာမလိုတော့ပဲ Cloud မှာ သုံးသလောက်ပဲ ပေးရတဲ့ အတွက် မလိုအပ်တဲ့အချိန်မှာ စရိတ်ကုန်ကျမှုမရှိတော့ပါဘူး။
  2. Flexible Capacity : Demand အလိုက် လွယ်လွယ်ကူကူ scale up or down လုပ်နိုင်တဲ့ အတွက် ဘယ်လောက်ပမာဏသုံးမလဲဆိုတာကို အများကြီး ကြိုတင်ခန့်မှန်းစဥ်းစားစရာမလိုပါဘူး။
  3. Speed and Agility : မြန်မြန်ဆန်ဆန်နဲ့ latency လျော့ချပြီး Customers တွေစီကို Deploy လုပ်ပေးနိုင်တဲ့ အတွက် လုပ်ငန်းတိုးတက်မှုတွေ မြန်ဆန်စေပါတယ်။

------------------------------------------------------------------------

- Deployment Models
	1. Cloud-Based Deployment ( Public Cloud )
	   
	   Public Cloud ကို ကျွန်တော်တို့ အများသုံး Bus ကားလိုမျိုး ။ (AWS, Azure, Sun Cloud) စတဲ့ Third-party Vendor တွေက သူတို့ရဲ့ Services တွေကို လူတိုင်းအသုံးပြုနိုင်အောင် ပေးထားတာကြောင့် ကုန်ကျစရိတ်သက်သာစေပါတယ်။ ဒါပေမယ့် အများနဲ့မျှဝေသုံးနေရတဲ့ အတွက် Security ပိုင်းမှာတော့ အားနည်းနိုင်ပါတယ်။
	   
	   
	2. On-Premises Deployment ( Private Cloud )
	   
	   Private Cloud ကို ကျွန်တော်တို့ရဲ့ ကိုယ်ပိုင်ကားလိုမျိုး မြင်ကြည့်လို့ရပါတယ်။ ဒီ Cloud ဟာ အဖွဲ့အစည်း တစ်ခုတည်းအတွက်သာ ဖန်တီးပေးထားတာ ဖြစ်ပြီး Infrastructure က တစ်ခြားလူတွေမပါဝင်တဲ့ အတွက် လုပ်ငန်းမှာ ပိုပြီးထိရောက်စေပြီး၊ Control နဲ့ Security ကို ပိုမိုပိုင်ဆိုင်နိုင်တာကြောင့် Sensitive Data (အရေးကြီးတဲ့ ဒေတာ) တွေကို ကိုင်တွယ်တဲ့ စီးပွားရေးလုပ်ငန်းတွေ အတွက် အထူးသင့်လျော်ပါတယ်။
	   
	3. Hybrid Cloud ကို ကျွန်တော်တို့ အများသုံးကားနဲ့ ကိုယ်ပိုင်ကား နှစ်မျိုးလုံးပေါင်းထားတဲ့ Taxiလိုမျိုး မြင်ကြည့်နိုင်ပါတယ်။ Hybrid Cloud က Public Cloud နဲ့ Private Cloud နှစ်ခုလုံးကို ပေါင်းစပ်သုံးတဲ့ နည်းပညာဖြစ်ပြီး၊ data တွေ application တွေကို အချင်းချင်း share နိုင်ပါတယ်။ Security အရ Public ထပ် more secure ဖြစ်ပြီး ဆန့်ကျင်ဘက်အနေနဲ့ Private ထပ်တော့ Less secure ဖြစ်နိုင်ပါတယ်။

------------------------------------------------------------------------

- Service Models
  
	1. IaaS ( infrastructure as a service )
	   
	   Infrastructure as a Service (IaaS) ဆိုတာက ကိုယ့် system တစ်ခုကို တည်ဆောက်တဲ့အခါမှာ လိုအပ်တဲ့ Hardware Resources တွေ ဖြစ်တဲ့ Compute devices, Storage devices, နဲ့ network အတွက်လိုအပ်တဲ့ ပစ္စည်းတွေကို ကိုယ်တိုင် ဝယ်ဖို့၊ တပ်ဆင်ဖို့ မလိုအပ်တော့ဘူးဆိုတာပါ။ ဒီပစ္စည်းတွေကို Cloud solution providers (ဥပမာ - Azure, AWS, GCP) ကနေ ထိန်းသိမ်းပေးသွားမယ်ဆိုတော့ ကိုယ့်စက်မှာတပ်ဆင်စရာမလိုတော့ပါဘူး။ အသုံးပြုသူအနေနဲ့ အချိန်မရွေး၊ လိုချင်တဲ့အခါ Virtual Machines (VMs) တွေကို click တချက်နှိပ်ရုံနဲ့ မြန်မြန်ဆန်ဆန်နဲ့ လွယ်ကူစွာ တည်ဆောက်နိုင်ပါတယ်။
	   
	   Examples : AWS EC2, Rackspace, Google compute engine, Digital Ocean
	   
	2. PaaS ( platform as a service )
	   
	   PaaS သည် Developers တွေ အတွက် အဓိက ထား တဲ့ service အမျိုးအစားဖြစ်ပါတယ်။ Underlying infrastructure (hardware နဲ့ middleware တွေကို ကိုယ်တိုင်စီမံဖို့ မလိုတော့ပဲ) ကိုယ့် applications တွေရဲ့ deployment နဲ့ management အပေါ်မှာပဲ အာရုံစိုက်နိုင်ပါသည်။ 
	   
	   Examples: AWS Elastic Beanstalk, Open Shift, Apache, Stratos, Google App Engine
	   
	3. SaaS ( software as a service )
	   
	   SaaS ကတော့ ကျွန်တော်တို့နဲ့ စိမ်းတဲ့ အရာတော့မဟုတ်ပါဘူး။ ကိုယ်လိုအပ်တာ သုံးချင်တာကို ကိုယ့် local machine ထဲမှာ installation လုပ်စရာမလိုပဲ cloud vendor ကနေ monthly paid ဖြစ်စေ Pay as you go ဖြစ်စေ ယူသုံးတာမျိုးဖြစ်တယ်။ resource မလောက်တော့လို့ ထပ်ထည့်ရတာတွေ ထပ်ပြီး maintain လုပ်ရတာတွေရှိမှာ မဟုတ်တော့ဘူး။ analysis လုပ်တဲ့ system တွေ tools တွေကို cloud မှ အလွယ်တကူ ရယူနိုင်ခြင်းကြောင့် အားသာချက်တွေများစွာ ရရှိနိုင်ပါတယ်။‍‍‍‍‍
	   
	   E‍xamples : Dropbox, pCloud, Mediafire, Google apps, microsoft office 365

------------------------------------------------------------------------

KEY CONCEPT ( You only pay what you use )

- What Is Cloud Computing ?
	1. The on-demand delivery of IT resources over the internet with pay-as-you-go pricing.
	2. It allows rapid access to flexible and low-cost IT resources, enabling you to scale resources up or down as needed.
	3. Eliminates the need for large upfront investments in hardware and reduces time spent on hardware management.
	4. Provides easy access to servers, storage, databases, and application services over the Internet.
	5. Platforms like Amazon Web Services (AWS) own and maintain the hardware, while users provision and use resources through a web application.

------------------------------------------------------------------------

- Advantages of Cloud Computing.
	1. Pay only for what you use, eliminating the need for large upfront investments in hardware.
	2. Benefit from cost efficiencies as cloud providers serve many customers, reducing costs compared to managing your own infrastructure.
	3. Easily scale resources up or down based on demand without overcommitting to capacity.
	4. Quickly deploy and manage resources within minutes, enhancing business agility.
	5. Spend less time managing IT infrastructure and focus more on core business activities.
	6. Deploy applications closer to your customers globally, reducing latency and improving performance.

------------------------------------------------------------------------

- Deployment Model
	1. Cloud-Based Deployment ( Public Cloud )
	   
	   The public cloud is a cloud computing model where cloud infrastructure services are provided over the internet to the general public or large industry groups. 
	   
	   1. Anyone can access systems and services, making it open but potentially less secure.
	   2. The cloud infrastructure is owned by the cloud service provider, not the consumer. Applications and their components, like virtual servers and databases, are fully based in the cloud.
	   3. Provides storage, backup, and retrieval services, often offered for free, by subscription, or on a per-user basis.
	   4. Ideal for cloud hosting, where services are provided to multiple customers efficiently.
	   
	   Advantages
	   
	   1. No substantial upfront costs due to the pay-per-use model, making it ideal for businesses needing immediate access to resources.
	   2. Cloud service providers subsidize the entire infrastructure, so no hardware setup is needed.
	   3. Users do not need to manage the infrastructure; the service provider handles it.
	   4. Maintenance is fully managed by the service provider, freeing users from these responsibilities.
	   5. Resources can be scaled up or down on demand to meet business needs.

	   Disadvantages
	   
	   1. Public access to resources makes the public cloud less secure, with no guarantee of high-level security.
	   2. Since it is used by many, the public cloud offers limited customization options to meet individual requirements.
	    
	-----------------------------------------------------------------
  
	2. On-Premises Deployment ( Private Cloud )
	   
	   The private cloud is a cloud computing model where resources are deployed on-premises using virtualization and resource management tools. It is also known as the "private cloud" and provides dedicated resources within a secure environment managed by an organization’s IT department.
	   
	   1. Resources are hosted within the organization's own data center, offering greater control and security but lacking some benefits of cloud computing.
	   2. Unlike the public cloud, the private cloud is a one-on-one environment, where the hardware is not shared with others.
	   3. Provides complete control over service integration, IT operations, and policies, allowing for tailored solutions to specific business needs.
	   
	   Advantages
	   
	   1. Full ownership and control over IT operations, policies, and user behavior.
	   2. Enhanced security and privacy, ideal for sensitive corporate information, with restricted access for authorized personnel only.
	   3. Compatible with legacy systems that may not be suitable for public cloud deployment.
	   4. Offers flexibility to customize solutions according to specific organizational needs.

	   Disadvantages
	   
	   1. Limited scalability compared to public clouds due to fewer clients and resources.
	   2. Higher costs associated with maintaining a personalized and dedicated infrastructure.
	    
	-----------------------------------------------------------------
	    
	3. Hybrid Deployment
	   
	   A hybrid deployment connects infrastructure and applications between cloud-based resources and existing on-premises resources. This model combines public and private cloud environments, allowing organizations to extend their infrastructure into the cloud while maintaining connections with their internal systems.
	   
	   1. Bridges public and private clouds with proprietary software, offering the security of a private cloud and the scalability and cost savings of a public cloud.
	   2. Allows organizations to move data and applications between different clouds based on their needs, offering personalized solutions.
	   
	   Advantages
	   
	   1. Enables businesses to design tailored solutions that meet specific requirements, balancing control and flexibility.
	   2. Leverages public cloud scalability, where extra capacity is paid for only when needed.
	   3. Data is properly segmented, reducing the risk of data theft.

	   Disadvantages
	   
	   1. Managing a combination of public and private clouds can be challenging due to the complexity involved.
	   2. Data transmission through the public cloud may result in slower performance and increased latency.
	        
------------------------------------------------------------------------

- Service Model
	1. IaaS ( infrastructure as a service )
	   
	   It is a computing infrastructure managed over the internet. The main advantage of using IaaS is that it helps users to avoid the cost and complexity of purchasing and managing the physical servers.
	   
	   Examples : DigitalOcean, Linode, Amazon Web Services (AWS), Microsoft Azure, Google Compute Engine (GCE), Rackspace, and Cisco Metacloud
	   
	2. PaaS ( platform as a service )
	   
	   PaaS cloud computing platform is created for the programmer to develop, test, run, and manage the applications.
	   
	   **Example:** AWS Elastic Beanstalk, Windows Azure, Heroku, Force.com, Google App Engine, Apache Stratos, Magento Commerce Cloud, and OpenShift.
	   
	3. SaaS ( software as a service )
	   
	   SaaS is also known as "**on-demand software**". It is a software in which the applications are hosted by a cloud service provider. Users can access these applications with the help of internet connection and web browser.
	   
	   **Example:** BigCommerce, Google Apps, Salesforce, Dropbox, ZenDesk, Cisco WebEx, ZenDesk, Slack, and GoToMeeting.