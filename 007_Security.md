Content
1. AWS Shared Responsibility Model
2. AWS Identity and Access Management ( IAM )
	1. Root User
	2. IAM User
	3. IAM Policies
	4. IAM Groups
	5. IAM Roles
3. AWS Organizations
4. Artifacts
5. Denial-of-Service (DoS) and Distributed Denial of Service (DDoS) Attack

------------------------------------------------------------------------
1. AWS Shared Responsibility Model

	 Cloud service သုံးတဲ့ အခါမှာ AWS (Amazon Web Services) နဲ့ Customer ရဲ့ တာဝန်တွေကို အချိန်ကျကျ ခွဲခြားထားတဲ့ ပုံစံတစ်ခုပဲ ဖြစ်ပါတယ်။ ဒါဆို AWS ကို အသုံးပြုသူအနေနဲ့ သင့်လုပ်ပိုင်ခွင့် (responsibility) က ဘာတွေလဲ၊ AWS က ဘာတွေလဲ ဆိုတာကို နားလည်ထားဖို့ လိုပါတယ်။

	 AWS Shared Responsibility Model မှာ AWS ရဲ့ တာဝန်တွေက Security of the Cloud ပိုင်းကို လုပ်ဆောင်ပေးတာပါ။ ဒီမှာ Server, Storage, Networking, Data Center အစရှိသဖြင့် Physical Security နဲ့ Infrastructure Security တို့ကို AWS က အပြည့်အဝ တာဝန်ယူပါမယ်။ ဒါကြောင့် AWS Cloud Infrastructure ကိုယ်တိုင်မှာ လုံခြုံရေးပြဿနာ မရှိအောင် AWS က တာဝန်ယူပါတယ်။

	 တစ်ဖက်မှာ Customer ရဲ့ တာဝန်က Security in the Cloud ပိုင်းဖြစ်ပြီး Customer ရဲ့ Data, Applications, User Access Control အစရှိသဖြင့် Data Encryption, Identity Management နဲ့ Security Configuration အပိုင်းတွေကို သင့်ကိုယ်တိုင် ကောင်းကောင်း တာဝန်ယူပါမယ်။ အနိမ့်ဆုံး လိုအပ်တဲ့ Security Setting တွေကို လုပ်ထားဖို့ လိုပါတယ်။

	 ဒါဆို AWS Shared Responsibility Model ဟာ Cloud Security ပိုင်းမှာ ကိုယ်တိုင် လုပ်ရမယ့် အပိုင်းတွေကို နားလည်ပြီး အမှန်တကယ် စနစ်တကျ လုပ်ဆောင်နိုင်ဖို့ အရေးကြီးပါတယ်။
	 
------------------------------------------------------------------------
2. AWS Identity and Access Management ( IAM )
   
   AWS Identity and Access Management (IAM) ဆိုတာက AWS Services တွေကို ဘယ်လိုအသုံးပြုမလဲ၊ ဘယ်သူက လုပ်ပိုင်ခွင့်ရှိမလဲ ဆိုတာကို စီမံခန့်ခွဲနိုင်ဖို့အတွက် အသုံးပြုတဲ့ Tool တစ်ခုပဲ ဖြစ်ပါတယ်။ ဒီ IAM နဲ့ပတ်သက်ပြီး အရေးကြီးတဲ့ အချက်တွေကို အောက်မှာ ပြောပြပေးပါမယ်။

	1. Root User
		Root User ဆိုတာ AWS Account တစ်ခုခု တည်ထောင်တဲ့ အချိန်မှာ အထူးသီးသန့် ရရှိတဲ့ User Account ဖြစ်ပါတယ်။ ဒီ Root User က လုပ်ပိုင်ခွင့် အပြည့်အဝ ရှိပြီး Account settings, Billing, IAM setup အပါအဝင် အခြား Functionality တွေကို အကုန်လုံး အုပ်ချုပ်နိုင်ပါတယ်။ ဒါကြောင့် Root User ကို တစ်ခါတစ်ရံမှာပဲ အသုံးပြုဖို့အတွက် အရေးကြီးပါတယ်။

	2. IAM User
		IAM User ဆိုတာ AWS Account အတွင်းမှာ ထည့်သွင်းထားတဲ့ User တစ်ဦးတစ်ယောက်ကို ဆိုလိုပါတယ်။ ဒီ User တွေက Root User ရဲ့ လုပ်ပိုင်ခွင့် အပြည့်အဝ မရဘဲ၊ Assigned Permissions (ခွင့်ပြုချက်) တွေကနေပဲ လုပ်ဆောင်နိုင်ပါတယ်။ ပုံမှန်အားဖြင့် Developer, Administrator, Auditor စသည့် သတ်မှတ်ထားတဲ့ User Account အမျိုးအစားတွေ ဖြစ်ပါတယ်။

	3. IAM Policies
		IAM Policies ဆိုတာက IAM User, Group, Role တွေကို လုပ်ပိုင်ခွင့်တွေ သတ်မှတ်ပေးတဲ့ Document (Policy) ဖြစ်ပါတယ်။ Policies တွေက JSON Format နဲ့ ရေးသားပြီး Resource တွေပေါ်မှာ ဘယ်လို Action တွေ လုပ်လို့ရမလဲ၊ ဘယ်သူက လုပ်လို့ရမလဲ ဆိုတာတွေကို ထည့်သွင်း ဖော်ပြပေးပါတယ်။ AWS Managed Policies (AWS က အသင့်ထားပေးထားတဲ့ Policies) တို့၊ Custom Policies (Customer ကိုယ်တိုင်ရေးတဲ့ Policies) တို့ကို အသုံးပြုနိုင်ပါတယ်။

	4. IAM Groups
		IAM Groups ဆိုတာ က IAM User အများကြီးကို တစ်ခုထဲမှာ အစုအဖွဲ့လုပ်ပြီး ထားသည့် အဖွဲ့တစ်ခုလို့ ဆိုနိုင်ပါတယ်။ Group ထဲက User တွေက အဲဒီ Group ရဲ့ Policies တွေကို အလုံးစုံ ရရှိမယ်။ ဒါကြောင့် User တစ်ယောက်ချင်းစီ ကို Policy တစ်ခုချင်းစီ မပေးပဲ Group အနေနဲ့ Assign လုပ်တာက လုပ်ငန်းစဉ် ကို ပိုမိုလွယ်ကူစေပါတယ်။

	 5. IAM Roles
		IAM Roles ဆိုတာ တစ်ချို့အချိန်တွေမှာ User တွေ မဟုတ်ဘဲ Service တွေကို အသုံးပြုခွင့်ပေးဖို့အတွက် ဖြစ်ပါတယ်။ User တွေ မဟုတ်ဘဲ EC2 Instances, Lambda Functions, Application တို့က Role တွေ သတ်မှတ်ပြီး Access Control ရနိုင်ပါတယ်။ Role တွေကို Temporary Credentials အနေနဲ့ သုံးပြီး Trust Relationship (ယုံကြည်မှုဆက်ဆံရေး) အခြေပြုပြီး အသုံးပြုရတာ ဖြစ်ပါတယ်။

	AWS IAM က AWS ရဲ့ Resource တွေကို ထိန်းချုပ်ပြီး လုံခြုံရေးအတွက် အရေးကြီးတဲ့ လုပ်ငန်းစဉ်ဖြစ်တာကြောင့် အထက်ပါ Components တွေကို ကောင်းကောင်း နားလည်ထားဖို့ လိုပါတယ်။
------------------------------------------------------------------------
3. AWS Organizations
   
	AWS Organizations က AWS Accounts အများကြီးကို စနစ်တကျ စီမံခန့်ခွဲနိုင်တဲ့ အဖွဲ့အစည်းပုံစံ (Organization) တစ်ခု ဖန်တီးပေးပါတယ်။ ဒီ Organizations ထဲမှာ AWS Accounts များစွာ ထည့်သွင်းပြီး Policies တွေ၊ Budget Control တွေ၊ Consolidated Billing (ပြည့်စုံသော ဘီလ်ရှင်းစနစ်) တို့ကို တစ်နေရာတည်းကနေ ထိန်းချုပ်နိုင်ပါတယ်။

	AWS Organizations ကလည်း Service Control Policies (SCPs) ဆိုတဲ့ Policy တွေကို အသုံးပြုကာ အဖွဲ့အစည်းတစ်ခုရဲ့ အပေါ်ဆုံး (Root) ကနေ အောက်စီမံခန့်ခွဲမယ့် Accounts တွေမှာ လုပ်ဆောင်ဖို့ ခွင့်ပြုမည့် သို့မဟုတ် ပိတ်ပင်မည့် Service တွေကို သတ်မှတ်ပေးနိုင်ပါတယ်။ 

	- Organizational Units (OUs)
	  
	  Organizational Units (OUs) ဆိုတာကတော့ AWS Organizations ထဲမှာ Sub-division (အောက်ခံအဖွဲ့အစည်း) လုပ်ထားတဲ့ အဖွဲ့အစည်းလေးတွေပါပဲ။ AWS Accounts များစွာကို အခြေအနေပေါ်မူတည်ပြီး OUs တစ်ခုချင်းစီထဲ ထည့်သွင်းနိုင်ပါတယ်။ ဒါကြောင့် Department, Project, Team အလိုက် အုပ်စုလိုက် စီမံခန့်ခွဲနိုင်ပါတယ်။

     ဥပမာ၊ သင့်ရဲ့ AWS Organization ထဲမှာ Production Unit တစ်ခု၊ Development Unit တစ်ခု ဆိုပြီး OUs နှစ်ခု ခွဲထားတယ် ဆိုပါစို့။ ဒီလို OU တွေမှာ သက်ဆိုင်ရာ AWS Accounts တွေကို ထည့်သွင်းပြီး Policies တွေ၊ Billing တွေကို ခွဲခြားစီမံခန့်ခွဲနိုင်ပါတယ်။
------------------------------------------------------------------------
4. Artifacts
   
   AWS Artifact ဆိုတာ AWS ရဲ့ Security နှင့် Compliance များအတွက် လိုအပ်တဲ့ အချက်အလက်တွေ၊ အတည်ပြုချက်တွေ၊ အစီရင်ခံစာတွေကို On-demand ရယူနိုင်တဲ့ Self-service Portal တစ်ခုပါ။ AWS Artifact က AWS Services တွေ အားလုံးမှာ လုံခြုံရေးနဲ့ သတ်မှတ်ချက်တွေကို တင်းကျပ်စွာ လိုက်နာသွားမယ့် Compliance Requirement များအတွက် အထောက်အကူပြုပါတယ်။
   
   AWS Artifact မှာ အဓိက Feature နှစ်ခု ရှိပါတယ်၊

	1. **AWS Artifact Reports**:  
	   ဒီ Feature က သင့်အနေနဲ့ AWS က လုပ်ဆောင်ထားတဲ့ Compliance Program တွေ၊ အခြေခံ Security Control တွေကို စစ်ဆေးတဲ့ အစီရင်ခံစာများ (Reports) ကို ရယူနိုင်မှာ ဖြစ်ပါတယ်။ SOC (Service Organization Controls) Reports, ISO Certifications, PCI (Payment Card Industry) Reports စတာတွေကို အလွယ်တကူ ရယူနိုင်ပြီး သင့်ရဲ့ Compliance Requirements တွေကို ဖြည့်ဆည်းနိုင်ပါတယ်။

	2. **AWS Artifact Agreements**:  
	   ဒီ Feature က AWS နဲ့ သင့်အဖွဲ့အစည်းကြားမှာ လိုအပ်တဲ့ Compliance Agreement တွေ၊ NDA (Non-disclosure Agreement) စတာတွေကို လက်မှတ်ရေးထိုးနိုင်စေပါတယ်။ AWS Artifact Agreements က အရင်က တာဝန်ထမ်းဆောင်ထားတဲ့ သဘောတူစာချုပ်တွေကို ပြန်လည်ကြည့်ရှုနိုင်တဲ့ အပြင်၊ အသစ်လည်း လက်မှတ်ရေးထိုးနိုင်ပါတယ်။
------------------------------------------------------------------------
5. Denial-of-Service (DoS) and Distributed Denial of Service (DDoS) Attack
   
   Denial-of-Service (DoS) attack နဲ့ Distributed Denial-of-Service (DDoS) attack ဆိုတာ ဝဘ်ဆိုဒ်တွေ၊ ဆာဗာတွေကို အလုပ်လုပ်မရအောင် ပိတ်ပင်တဲ့ နည်းလမ်းတွေပါ။

	1. Denial-of-Service (DoS) Attack
	  DoS attack ဆိုတာ တစ်ယောက်တည်းကနေ Server တစ်ခုကို အမြန်မြန် request တွေ ပို့တာပါ။ ဒီလိုလုပ်တာကြောင့် Server က request တွေကို ဖြေပေးမလို့မရတော့ဘူး၊ Server က အလုပ်လုပ်ဖို့ မလုံလောက်တော့တဲ့ အချိန်မှာ ဝဘ်ဆိုဒ်ကို သာမာန် User တွေ မရောက်နိုင်တော့ပါဘူး။

	  **ဥပမာ** - ကိုယ်မှာ ဝဘ်ဆိုဒ်တစ်ခုရှိတယ်။ Attacker က အလွန်များတဲ့ request တွေကို တစ်ယောက်တည်းကနေ သင့်ဝဘ်ဆိုဒ်ကို ပို့လိုက်တယ်။ Server က overload ဖြစ်သွားပြီး အခြား User တွေ ဝင်လို့မရတော့ပါဘူး။

	2. Distributed Denial-of-Service (DDoS) Attack
	  DDoS attack ဆိုတာ DoS attack နဲ့ ဆင်တူပေမယ့် အများကြီးလက်တွဲပြီး လုပ်တဲ့ attack ပုံစံပါ။ Attacker က Computer အများကြီးကို တစ်ပြိုင်နက်တည်း request တွေ ပို့စေပြီး Target Server ကို ထိခိုက်အောင် လုပ်ပါတယ်။

	**ဥပမာ** - Attacker တစ်ယောက်က အခြား Computer အများကြီးကို ထိန်းချုပ်ထားပြီး၊ ဒီ Computer တွေက တစ်ပြိုင်နက်တည်း သင့်ဝဘ်ဆိုဒ်ကို request တွေ ပို့လိုက်တယ်။ ဒီလိုလုပ်လိုက်တဲ့အခါမှာ Server က overload ဖြစ်ပြီး အခြား User တွေ ဝင်လို့မရတော့ပါဘူး။
------------------------------------------------------------------------