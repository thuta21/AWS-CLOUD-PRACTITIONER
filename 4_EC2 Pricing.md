
Content
1. EC2 Pricing
	1. On Demand
	2. Reserved Instances
	3. Sport Instance Type
	4. Dedicated Instance ( or ) Hosting
	5. Saving Plans

------------------------------------------------------------------------

1. EC2 Pricing

	1. On Demand
	   
	   ကိုယ်သုံးမယ့် Operation System ၊ Instance type ပေါ်မူတည်ပြီး Run အခါ Duration (hr, min, s) အလိုက် cost တွက်ပါတယ်။ EC2 စဖွင့်ရင်တော့ On Demand နဲ့ပဲ သုံးရမှာပါ။ ဒီအတွက်ကြောင့် Long-term payment တွေ upfront payment ( ငွေကြိုပေး ) တာတွေ မလိုပါဘူး။ ဒီ Instance ကိုတေ Short-term application တွေ ၊ developing ၊ testing app တွေ unpredictable usage ( ခန့်မှန်းရမလွယ်ကူနိုင်တဲ့ App ) တွေအတွက် သုံးသင့်ပြီး Yearly အလိုက် Plan ထားတဲ့ Long-term project တွေအတွက်တော့ မသုံးသင့်ပါဘူး။
	   
	2. Reserved Instances
	   
	   ဒီ Instance ကတော့ Long-term application run ချင်တဲ့အချိန်မျိုး ၊ steady-state workload ရှိထားပြီးတဲ့ App မျိုး ၊ usage ကို ကြိုတင်သတ်မှတ်ထားပြီး သေချာတဲ့ အခါမျိုးမှာ သုံးသင့်တယ်။ Long-term အတွက်ဖြစ်တဲ့အတွက် Payment အနေနဲ့က one or three year အထိ စာချုပ်ချုပ်ဖို့ လိုအပ်ပါတယ်။ 
	   
	   Payment Options တွေ အနေနဲ့က 
	
	   1. All Upfront : One or three year အတွက် ကြိုပြီး အလုံးလိုက်ငွေချေလိုက်တာပါ။ ဒီလိုပေးလိုက်ချင်းအားဖြင့် Monthly အလိုက်ပေးချေရာမှာ သက်သာသွားပါတယ်
	   2. Partial Upfront : Instances အတွက် စုစုပေါင်းကုန်ကျစရိတ်ထဲကနေ 50% ကြိုပေးရပါတယ်။ ကျန်တဲ့ 50% ကိုတော့ hourly / monthly ခွဲပေးလို့ရပါတယ်။ 
	   3. No Upfront : Software Development Company တစ်ခုရှိတယ်ဆိုကြပါစို့။ Project duration ကလည်း 1 year ရှိမယ်။ Company budget ကလည်း မတတ်နိုင်တဲ့ အခါမျိုးမှာဆိုရင် No Upfront Payment Option ကို သုံးကြပါတယ်။ ကြိိုတင်ပြီး ပေးစရာမလို။ ခွဲပေးစရာလည်း မလိုပဲ သူ Discount ပေးထားတဲဲ့ အတိုင်း Hourly အလိုက်ပေးချေရုံပါပဲ။ အနည်းဆုံးတော့ 1 year contract တော့ ချုပ်ရပါတယ်။
	      
	   RI / Reserved Instances Type (3) မျိုးရှိတယ်။ 
	   
	   1. Standard : Steady-state usage တွေအတွက် အထူးသင့်တော်ပြီး On-demand pricing ထပ် ( up to 72% off ) သက်သာပါတယ်။ AWS ရဲ့ Reserved Instance Marketplace မှာ တင်ပြီးလည်း ပြန်ရောင်းတာ / ပြန်ဝယ်တာ တို့လည်း ရပါသေးတယ်။
	   2. Convertible : RI attributes တွေကို တိုးလိုက်တာတို့ ညီလိုက်တာတို့ (​equal) စသည်ဖြင့်ပြောင်းလိုက်လို့ရပါတယ်။ သူလည်းပဲ Steady-stage usage တွေအတွက် သင့်တော်ပြီး On-demand ထပ် ( up to 54% off ) သက်သာပါတယ်။
	   3. Schedule : ဒီ RIs ကတော့ Schedule ဆိုတဲ့ အတိုင်း ကိုယ်လိုချင်တဲ့ အချိန် ( Specific time )မှာ Compute capacity အသုံးပြုမယ်ဆိုပြီး သတ်မှတ်လို့ရပါတယ်( တစ်ပတ်မှာ ဘယ်နှစ်နာရီပဲ သုံးမယ် )။ 

	3. Spot Instance Type
	   
	   ဒီ Instance type မှာတော့ On-demand ထပ် ( Up to 90% off ) သက်သာပါတယ်။ ဘယ်လိုအလုပ်လုပ်လည်းဆိုတော့ Flexible start and end times ဆိုပြီးလုပ်ပါတယ်။ ဥပမာ Background Processing တစ်ခုရှိတယ်။ အဲ့ဟာက Customer survey တို့ Video transcoding တို့ ဒီလိုမျိုး လုပ်တဲ့အချိန်မှာ Instance ကိုဖွင့်မယ် ( start )။ Processing ပြီးတာနဲ့ ပိတ်မယ် ( end )။ 
	   
	   တစ်ခုရှိတာကတော့ ကျွန်တော်တို့က spot request လုပ်မယ်။ Computing Capacity ကလည်း Available ဖြစ်တယ်ဆို Instance Launchသွားမယ်။ Available မဖြစ်ဘူးဆိုရင်တော့ Background Processing Delay ဖြစ်တာမျိုး ဖြစ်နိုင်ပါတယ်။ ဒါမှမဟုတ် Provider ဖြစ်တဲ့ AWS က လုံးဝပိတ်လိုက်တဲ့အခါမျိုးမှာဆိုရင်တော့ Processing time က ကြာခဲ့တဲ့ အချိန်အလိုက်ပိုက်ဆံပေးစရာမလိုပါဘူး။ ဒီလိုမျိုးကို ရှောင်ရှားချင်ရင်တော့ တခြား EC2 Instance types တွေကို ရွေးချယ်ရတော့မှာပါ။ 
	   
	4. Dedicated Instance ( or ) Hosting
	   
	   ဒီတစ်ခုကတော့ Physical Server တစ်မျိုးဖြစ်ပြီး စျေးအကြီးဆုံးအမျိုးအစားလည်း ဖြစ်ပြီးတော့ ကိုယ်ပိုင် သီးသန့် Dedicated Server Host ထားပေးထားပါတယ်။ သီးသန့် host ထားပေးထားတဲ့အတွက်ကြောင့် System Security Concern အရလည်း စိတ်ချရတယ်။ On-demand ထပ် ( Up to 70% off ) ပေးပါတယ်။ 

	5. Saving Plans
	   
	   AWS Savings Plans ကတော့ AWS Usage (Compute Usage) ကို တချိန်တည်းမှာ စရိတ်သက်သာစေတဲ့ Flexible Pricing Model တစ်ခုဖြစ်ပါတယ်။ သုံးစွဲမယ့် Resources တွေ အတွက် Usage Cost (USD per hour) ကို 1 နှစ် ဒါမှမဟုတ် 3 နှစ်အထိ ကျရင်အနေအထားကို Commitment လုပ်ပေးရပြီး On-Demand Pricing ထက် 72% အထိသက်သာစေပါတယ်။ Savings Plans က Reserved Instances ထက်ပိုပြီး Flexible ဖြစ်ပြီး Regions, Instance Types, Services များအကြား Discount ကို သက်ရောက်စေမှာဖြစ်ပါတယ်။
	   
	   Saving Plans အမျိုးအစားများ
	   
	   1. Compute Savings Plans : EC2 Instances များအပြင် AWS Fargate နဲ့ AWS Lambda Usage တွေအားလုံးအတွက် အကျုံးဝင်ပါတယ်။ Region, Instance Type, Operating System, Tenancy တို့မရွေး အကုန်သက်ရောက်ပါတယ်။ On-Demand Pricing ထက် 66% အထိသက်သာစေပါတယ်။
	      
	   2. EC2 Instance Savings Plans: အသုံးပြုမှုကို Region တစ်ခုအတွင်းမှာ အထူးပြုထားတဲ့ Instance Family တစ်ခုတည်း အတွက် Commitment လုပ်ပေးရပါတယ် (ဥပမာ M5 usage in N. Virginia တို့)။ အဲ့ဒီ Savings Plans က AZ, Instance Size, Operating System (OS), သို့မဟုတ် Tenancy အရ အလိုအလျှောက် စျေးနှုန်းလျော့ပါတယ်။  

