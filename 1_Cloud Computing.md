
Content 
1. What is Cloud Computing?
2. Service Models
	1. IaaS ( Infrastructure as a Service )
	2. SaaS ( Software as a Service )
	3. PaaS ( Platform as a Service )
3. Deployment Models
	1. Cloud-Based Deployment ( Public Cloud )
	2. On-Premises Deployment ( Private Cloud )
	3. Hybrid Deployment 

------------------------------------------------------------------------

1. What is Cloud Computing?
   
   "The on-demand delivery of IT resources over the internet with pay-as-you-go pricing"
   
   Cloud Computing ဆိုတာက Physically အရ Resources တွေကို သုံးစရာမလိုပဲ အင်တာနက်ပေါ်က တစ်ဆင့် IT Resources ( Apps, Systems, Services, Softwares, Databases. Server, Platform ) တွေကို သုံးသလောက်ပေး ပုံစံ ( Pay-as-you-go pricing ) model နဲ့ ရယူအသုံးပြုချင်း ဖြစ်ပါတယ်။
   
   Cloud Computing နဲ့ပတ်သက်ပြီး နားလည်ရမယ့် အဓိကအချက်ကတော့ Traditional Computing နဲ့မတူပဲ Cloud Computing မှာ Physical Servers ကို ကိုယ့်ဘာသာ ဝယ်ယူပြီး Install လုပ်စရာမလိုဘဲ Cloud Provider (e.g., AWS, Google Cloud) တွေကနေ အငှားပြန်ယူအသုံးပြုရတာပါ။
   
   ဒီလို အင်တာနက်ပေါ်က တစ်ဆင့် အသုံးပြုနိုင်တာကြောင့် On-premise data center တွေလိုမဟုတ်ပဲ Hardware Management ပိုင်းတွေကို maintain လုပ်တဲ့နေရာမှာ အချိန် နဲ့ ငွေကုန်ကြေးကျ သက်သာစေပါတယ်။
   
   ဒါ့အပြင် Cloud Computing က Application တွေရဲ့ Performance, Security နဲ့ Scalability (e.g., Server Load Balancer) တွေကိုလည်း တိုးတက်စေပြီး Maintenance ပိုင်းကိုလည်း လွယ်ကူစေပါတယ်။
  
   Cloud Providers : AWS, AZURE, Google Cloud Platform, IBM Cloud ...

------------------------------------------------------------------------

2. Service Models
   
   Cloud Computing ကို သုံးမယ်ဆိုရင် Services Model တွေ သိထားသင့်ပါတယ်။ 
   
   1. IaaS ( Infrastructure as a Service )

	 Infrastructure ကို Cloud Service အနေနဲ့ပေးတာ။ Cloud Provider က Server, Storage, Network နဲ့ Virtualization စတဲ့ Physical Infrastructure တွေကို အငှားပေးတဲ့ Model ပါ။ User အနေနဲ့ Data Center တွေ၊ Server Hardware တွေ ဝယ်ယူတပ်ဆင်စရာမလိုဘဲ IaaS Provider (e.g., AWS EC2, Google Compute Engine) မှာ Virtual Machines, Storage, Networking Resources တို့ကို လိုအပ်သလို အသုံးပြုနိုင်ပါတယ်။ 
	 
	 ဒီ Model က Application တွေတည်ဆောက်ဖို့ အခြေခံ Infrastructure ကို လျင်မြန်စွာ အပ်ဒိတ်လုပ်နိုင်ပြီး ကိုယ်ပိုင် Control နဲ့ Customization ပိုင်းမှာ တော်တော်လေး Flexible ဖြစ်ပါတယ်။ ဒါပေမယ့် Servers တွေရဲ့ Configuration နဲ့ Management ပိုင်းက User အဆင်ပြေစေဖို့ လေ့လာမှုတွေ လိုအပ်တတ်ပါတယ်။
	 
	 Examples: AWS EC2, Rackspace, Google compute engine, Digital Ocean

   2. SaaS ( Software as a Service )
      
    SaaS ကတော့ ကျွန်တော်တို့နဲ့ စိမ်းတဲ့ အရာတော့မဟုတ်ပါဘူး။ ကိုယ်လိုအပ်တာ သုံးချင်တာကို ကိုယ့် local machine ထဲမှာ installation လုပ်စရာမလိုပဲ cloud vendor ကနေ monthly paid ဖြစ်စေ Pay as you go ဖြစ်စေ ယူသုံးတာမျိုးဖြစ်တယ်။ resource မလောက်တော့လို့ ထပ်ထည့်ရတာတွေ ထပ်ပြီး maintain လုပ်ရတာတွေရှိမှာ မဟုတ်တော့ဘူး။ analysis လုပ်တဲ့ system တွေ tools တွေကို cloud မှ အလွယ်တကူ ရယူနိုင်ခြင်းကြောင့် အားသာချက်တွေများစွာ ရရှိနိုင်ပါတယ်။‍‍‍‍‍
	   
	Examples: Dropbox, pCloud, Mediafire, Google apps, microsoft office 365

   3. PaaS ( Platform as a Service)
   
    PaaS ဆိုတာက Developers အတွက် Application Development, Testing, Deployment စတဲ့ Process တွေကို လွယ်ကူအောင် Cloud Provider က ပေးတဲ့ Platform Services ဖြစ်ပါတယ်။ PaaS က Operating System, Database Management, Middleware, Development Tools စတဲ့ လိုအပ်တဲ့ အရာအားလုံးကို ပံ့ပိုးပေးပါတယ်။ 
   
    အဲဒီတော့ Developers တွေက Infrastructure နဲ့ပတ်သက်ပြီး စိတ်ပူစရာမလိုဘဲ Application Development နဲ့ Maintenance ပိုင်းပဲ အာရုံစိုက်နိုင်ပါတယ်။ ဥပမာ - Google App Engine, Microsoft Azure App Service တို့ဖြစ်ပါတယ်။ PaaS က Development Life Cycle ပိုင်းကို အားပေးတယ်ဆိုပေမယ့် Platform ကိုဘဲ မှီခိုရတဲ့အတွက် တစ်ချို့အခြေအနေတွေမှာ Flexibility ပိုင်းမှာ အားနည်းတတ်ပါတယ်။
   
    Examples: AWS Elastic Beanstalk, Open Shift, Apache, Stratos, Google App Engine
    
------------------------------------------------------------------------

3. Deployment Models
   
   Cloud Services တွေ ဘယ်လိုအသုံးပြုမယ်မလဲဆိုတာ အဓိကအားဖြင့် Cloud-Based Deployment (Public Cloud), On-Premises Deployment (Private Cloud), နဲ့ Hybrid Deployment ဆိုပြီး သုံးမျိုးရှိပါတယ်။
   
   1. Cloud-Based Deployment ( Public Cloud )
      
     Public Cloud ကို ကျွန်တော်တို့ အများသုံး Bus ကားလိုမျိုး ။ (AWS, Azure, Sun Cloud) စတဲ့ Third-party Vendor တွေက သူတို့ရဲ့ Services တွေကို လူတိုင်းအသုံးပြုနိုင်အောင် ပေးထားတာကြောင့် ကုန်ကျစရိတ်သက်သာစေပါတယ်။ ဒါပေမယ့် အများနဲ့မျှဝေသုံးနေရတဲ့ အတွက် Security ပိုင်းမှာတော့ အားနည်းနိုင်ပါတယ်။
      
   2. On-Premises Deployment ( Private Cloud )
      
      Private Cloud ကို ကျွန်တော်တို့ရဲ့ ကိုယ်ပိုင်ကားလိုမျိုး မြင်ကြည့်လို့ရပါတယ်။ ဒီ Cloud ဟာ အဖွဲ့အစည်း တစ်ခုတည်းအတွက်သာ ဖန်တီးပေးထားတာ ဖြစ်ပြီး Infrastructure က တစ်ခြားလူတွေမပါဝင်တဲ့ အတွက် လုပ်ငန်းမှာ ပိုပြီးထိရောက်စေပြီး၊ Control နဲ့ Security ကို ပိုမိုပိုင်ဆိုင်နိုင်တာကြောင့် Sensitive Data (အရေးကြီးတဲ့ ဒေတာ) တွေကို ကိုင်တွယ်တဲ့ စီးပွားရေးလုပ်ငန်းတွေ အတွက် အထူးသင့်လျော်ပါတယ်။
      
   3.  Hybrid Deployment
      
      Hybrid Cloud ကို ကျွန်တော်တို့ အများသုံးကားနဲ့ ကိုယ်ပိုင်ကား နှစ်မျိုးလုံးပေါင်းထားတဲ့ Taxiလိုမျိုး မြင်ကြည့်နိုင်ပါတယ်။ Hybrid Cloud က Public Cloud နဲ့ Private Cloud နှစ်ခုလုံးကို ပေါင်းစပ်သုံးတဲ့ နည်းပညာဖြစ်ပြီး၊ data တွေ application တွေကို အချင်းချင်း share နိုင်ပါတယ်။ Security အရ Public ထပ် more secure ဖြစ်ပြီး ဆန့်ကျင်ဘက်အနေနဲ့ Private ထပ်တော့ Less secure ဖြစ်နိုင်ပါတယ်။

------------------------------------------------------------------------

