
Content 

1. Snow Family Members
	1. AWS Snowcore
	2. AWS Snowball
	3. AWS Snowmobile
2. AWS Well-Architecture Framework
   
------------------------------------------------------------------------

1. Snow Family Members
   
   AWS Snow Family ဆိုတာက Amazon Web Services (AWS) က data center နဲ့ cloud services များကို သုံးချင်တဲ့ organization များအတွက် အဓိက ဖြစ်စေမယ့် physical devices တွေကို ပြောတာပါ။ ဒီ AWS Snow Family အတွင်းမှာ အောက်ပါ members တွေ ပါဝင်ပါတယ်။
   
   1. AWS Snowcone
      
      Snowcone က Snow Family အထဲမှာ အငယ်ဆုံးနဲ့ အလွယ်တကူ သယ်ဆောင်နိုင်တဲ့ device တစ်ခုပါ။ Edge computing နဲ့ data transfer တွေအတွက် သုံးတတ်ကြပါတယ်။ 8 TB storage capacity နဲ့ရှိပြီး အလွန်နည်းတဲ့ power လိုအပ်ချက်ရှိပါတယ်။
      
   2. AWS Snowball
      
      Snowball က Data transfer နဲ့ edge computing လုပ်ငန်းများအတွက် အသုံးများတဲ့ device ဖြစ်ပါတယ်။ Snowball Edge Storage Optimized နဲ့ Snowball Edge Compute Optimized ဆိုပြီး အမျိုးအစား နှစ်မျိုးရှိပါတယ်။ Storage Optimized က 80 TB storage ပါပြီး Compute Optimized က storage တွေအပြင် CPU နဲ့ GPU ပါဝင်တာကြောင့် ML/AI applications များတွင် အသုံးများပါတယ်။
        
   3. AWS Snowmobile
      
      Snowmobile က data ကို petabyte (PB) အရေအတွက် အထိ physically transfer လုပ်ချင်တဲ့ လုပ်ငန်းများအတွက် သင့်တော်ပါတယ်။ အကြီးဆုံး member ဖြစ်ပြီး 100 PB အထိ storage capacity ရှိပါတယ်။ ဒီတော့ အကြီးမားဆုံး data migration များအတွက် အသုံးပြုပါတယ်။ Snowmobile က 18-wheeler truck အရွယ်ရှိတဲ့ device တစ်ခု ဖြစ်ပါတယ်။

------------------------------------------------------------------------

2. AWS Well-Architecture Framework
   
   **AWS Well-Architected Framework** ဆိုတာက AWS မှာ Application နဲ့ Workloads တွေကို အကောင်းဆုံးဖြစ်အောင် Design လုပ်တဲ့အခါ အသုံးပြုရမယ့် Best Practices တွေကို အခြေခံပေးတဲ့ Framework ဖြစ်ပါတယ်။
   
   6 Pillars of AWS Well-Architected Framework
   
   1. Operational excellence
      
      Operation စနစ်ကောင်းမွန်စွာ ဆောင်ရွက်နိုင်ဖို့အတွက် Monitoring, Automation နဲ့ Continuous Improvement လုပ်ဆောင်ခြင်းက အဓိကပါ။
      
   2. Security
      
      Security Pillar ကတော့ အချက်အလက်များအတွက် ရှေ့ဆုံးအဆင့်ကင်းကောင်းစွာ ပေးနိုင်ဖို့ Encryption, Access Control, Audit, နဲ့ Network Security တွေကို စနစ်တကျ အကောင်းဆုံးလုပ်ဆောင်ခြင်းပါ။
      
   3. Reliability
      
      System တွေအနေဖြင့် အချိန်တိုင်း စနစ်တကျ run ဖြစ်ဖို့အတွက် Fault Tolerance နဲ့ Disaster Recovery ကို အထူးအလေးထားပေးပါတယ်။
      
   4. Performance efficiency
      
      Performance Efficiency ကတော့ AWS ရဲ့ စွမ်းဆောင်ရည်ကို ပျက်ပြယ်မှုမရှိအောင် စွမ်းဆောင်စေဖို့ Architecture Design ကို Optimize လုပ်တာပါ။
      
   5. Cost optimization
      Performance Efficiency ကတော့ AWS ရဲ့ စွမ်းဆောင်ရည်ကို ပျက်ပြယ်မှုမရှိအောင် စွမ်းဆောင်စေဖို့ Architecture Design ကို Optimize လုပ်တာပါ။
      
   6. Sustainability
      
      **Sustainability** ဆိုတာက AWS Well-Architected Framework ရဲ့ နောက်ဆုံးနဲ့ အသစ်ထည့်သွင်းလာတဲ့ Pillar ဖြစ်ပါတယ်။ ဒီ Pillar ရဲ့ အဓိက ရည်ရွယ်ချက်က Cloud Architecture ကို သင့်တော်အောင်လုပ်ဆောင်ဖို့ အထောက်အကူပြုတာပါ
      
      1. Energy Efficiency တိုးတက်စေခြင်း၊ Carbon Footprint လျှော့ချခြင်းနဲ့ Long-term Impact ကို အာရုံစိုက်ခြင်းတို့ဖြင့် ပတ်ဝန်းကျင်အပေါ် အကျိုးသက်ရောက်မှုကို လျှော့ချနိုင်ပါတယ်။
         
	  Notes
	  
	    - AWS Well-Architected Framework မှာ 6 Pillars ရှိပြီး၊ အဲ့အတိုင်းပါဝင်တဲ့ Best Practices တွေကို လိုက်နာခြင်းအားဖြင့် AWS မှာ Applications တွေကို အကောင်းဆုံး စီမံခန့်ခွဲနိုင်ပါတယ်။
    
        - **Pillars**:
            - **Operational Excellence**: Continuous Improvement နဲ့ Automation။
            - **Security**: Data Protection နဲ့ Access Control စနစ်များ။
            - **Reliability**: Fault Tolerance နဲ့ Disaster Recovery။
            - **Performance Efficiency**: Computing Resources တွေကို Optimize လုပ်ခြင်း။
            - **Cost Optimization**: Resource သုံးစွဲမှုကို အကျိုးရှိစွာ စီမံခြင်း။
            - **Sustainability**: Energy Efficiency တိုးတက်စေခြင်း။
        
------------------------------------------------------------------------