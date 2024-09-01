Content
1. Instance Stores
2. Amazon Elastic Block Stores ( Amazon EBS )
3. Amazon S3
4. Amazon S3 Storage Classes
	1. S3 Standard ( General Purpose )
	2. S3 Intelligent-Tiering ( Unknown or changing access )
	3. S3 Standard-IA ( Infrequent access )
	4. Amazon S3 One Zone-Infrequent Access ( S3 One Zone-IA )
	5. Amazon S3 Glacier Instant Retrieval
	6. Amazon S3 Glacier Flexible Retrieval ( Formerly S3 Glacier )
	7. Amazon S3 Glacier Deep Archive
	8. S3 Outposts
5. Amazon EFS ( Elastic File System )
------------------------------------------------------------------------

1. Instance Stores
   
   Instance Stores ကို **ephemeral storage** လို့လည်းခေါ်ကြတယ်။ EC2 instance နဲ့ တစ်ခါတည်း ထည့်သွင်းထားတဲ့ temporary storage ဖြစ်ပြီး၊ instance ကို ရပ်လိုက်တဲ့အချိန်မှာ storage data ကပါ ပျက်သွားပါတယ်။ ဒါကြောင့် **data durability** မလိုတဲ့ အချက်အလက်တွေ (temporary files, cache, buffer storage) မျိုးတွေအတွက် အသုံးပြုနိုင်တယ်။ Instance store volumes တွေက instance ရဲ့ physical server မှာ direct attached ဖြစ်တဲ့အတွက် very high I/O performance (input/output) ရပါတယ်။

------------------------------------------------------------------------

2. Amazon Elastic Block Stores ( Amazon EBS )
   
   Amazon EBS ကတော့ **persistent storage** ဖြစ်ပါတယ်။ EC2 instance shutdown ဖြစ်သွားလည်း data အပြည့်အဝသိမ်းဆည်းထားနိုင်တဲ့ durable storage ဖြစ်တယ်။ EBS volumes တွေကို EC2 instances အများကြီးနဲ့ attach လုပ်နိုင်ပြီး, snapshots အဖြစ် backup လုပ်ထားလို့ရတယ်။ Data ကို long-term storage အတွက် EBS ကို အသုံးပြုနိုင်ပါတယ်။
   
   Instance Stores နဲ့ EBS အကြား ကွာခြားချက်က data durability နဲ့ usage purpose ပဲ ဖြစ်ပါတယ်။ High performance, temporary storage လိုရင် Instance Store ကို, Persistent storage လိုရင်တော့ Amazon EBS ကို အသုံးပြုရပါမယ်။

------------------------------------------------------------------------

3. Amazon S3 (​ Simple Storage Service )
   
   Amazon S3 (Simple Storage Service) ဆိုတာ AWS ရဲ့ scalable object storage service တစ်ခုဖြစ်ပါတယ်။ S3 မှာ Data တွေကို **objects** အနေနဲ့ သိမ်းဆည်းပြီး၊ အဲ့ဒီ objects တွေကို **buckets** အဖြစ် grouping လုပ်ထားပါတယ်။
   
   Notes: 

    1. Amazon S3 က **99.999999999% (11 9's)** of durability ရှိပါတယ်။ ဒါက Data durability အလွန်အမင်း မြင့်မားတဲ့အတွက် Data loss ဖြစ်နိုင်ခြေ မရှိသလောက်နဲ့ Availability ကလည်း အမြင့်ဆုံးရှိတယ်ဆိုတာကို ဆိုလိုပါတယ်။ Data durability ရရှိဖို့အတွက် Data ကို multiple availability zones (AZs) မှာ replicate လုပ်ထားတဲ့ စနစ်ကို သုံးထားပါတယ်။

    2. S3 မှာ Data ကို encryption လုပ်ပြီး သိမ်းဆည်းနိုင်ပါတယ်။ ဒါ့အပြင် Access control policies နဲ့ Bucket Policies တွေကို သုံးပြီး Data security ကို အထောက်အပံ့ ပေးနိုင်ပါတယ်။

    3. Amazon S3 ကို data backup, content storage, media hosting, data lakes, သို့မဟုတ် big data analytics စတဲ့ အမျိုးမျိုးသော usage scenarios တွေအတွက် အသုံးပြုနိုင်တယ်။ Static website hosting အတွက်ပါ အသုံးပြုလို့ရပါတယ်။

------------------------------------------------------------------------

4. Amazon S3 Storage Classes
   
   1. S3 Standard ( General Purpose )
      
      S3 Standard ကို General Purpose Storage လို့လည်း ခေါ်ပါတယ်။ ဒီ storage class က data ကို အမြဲတမ်း store ထားဖို့အတွက် အသင့်တော်ဆုံးဖြစ်ပြီး, high availability (စွမ်းဆောင်ရည်မြင့်မားမှု) နဲ့ low latency (အချိန်နှောင့်နှေးမှုနည်း) တို့ကို ပေးစွမ်းနိုင်ပါတယ်။ ဒါကြောင့် အကြိမ်ကြိမ်ထပ်ခါထပ်ခါ read/write လုပ်ရမယ့် frequently accessed data တွေအတွက် အထူးသင့်တော်ပါတယ်။
      
	  Notes: 
      
	    1. S3 Standard သည် 99.999999999% (11 9s) တာရှည်ခံမှု (durability) ပါဝင်ပြီး data loss ဖြစ်မယ့်အနည်းဆုံးဖြစ်စေပါတယ်။
	       
	    2. Data ကို low latency နဲ့ access လုပ်နိုင်တာကြောင့်, real-time applications များမှာ အသုံးပြုရန်သင့်တော်ပါတယ်။
	       
	    3. S3 Standard ရဲ့ cost က data တွေကို အမြဲသိမ်းထားတဲ့ other classes တွေထက် စျေးနှုန်းပိုများတတ်ပေမဲ့, frequently accessed data တွေကို အမြဲမပြောင်းလဲရင်တော့ သက်သာပါတယ်။

   2. S3 Intelligent-Tiering ( Unknown or changing access )
      
      **Amazon S3 Intelligent-Tiering** ဆိုတာကတော့ အသုံးပြုသူတွေကြားမှာ popular ဖြစ်တဲ့ cloud storage class တစ်ခုပါ။ ဒီ storage class က data access frequency (အသုံးပြုမှု ပုံစံ) အလိုအလျောက် ခွဲခြားပြီး အသုံးပြုသူများအတွက် သိမ်းဆည်းရေး စရိတ်သက်သာအောင် ပြုလုပ်ပေးပါတယ်။ 

	  **S3 Intelligent-Tiering** ကို အသုံးပြုရင် data များအတွက် latency နည်းပြီး high throughput performance ရရှိပါတယ်။ Unknown (မသိတဲ့) ဒါမှမဟုတ် changing access pattern (အသုံးပြုမှု ပုံစံပြောင်းလဲခြင်း) ရှိတဲ့ data တွေကို သိမ်းဆည်းရာမှာ အထူးသင့်တော်ပါတယ်။ Data lake, data analytics, user-generated content တို့လို workload မျိုးတွေအတွက် ရှယ်အသုံးဝင်ပါတယ်။
	  
	  Intelligent-Tiering ကို အသုံးပြုခြင်းက data usage pattern မသိတဲ့ အခါမျိုးမှာ အထူးသင့်တော်ပြီး cost-saving ဖို့ အကောင်းဆုံး storage class ဖြစ်ပါတယ်။

	  Notes: 

		1. S3 Intelligent-Tiering က 99.9% availability ရရှိဖို့ ရည်ရွယ်ထားပြီး SLA က 99% ဖြစ်ပါတယ်။

		2. **အချက်အလက်များကို အလွယ်တကူ monitoring လုပ်ပြီး, 30 ရက်လောက် access မလုပ်တဲ့ object တွေကို Infrequent Access tier ကနေ ထားတယ်။ 90 ရက် access မလုပ်ဘဲဖြစ်ရင်တော့ Archive Instant Access tier ကို အလိုအလျောက် ရွှေ့ပါတယ်။

		3. Infrequent Access ဒါမှမဟုတ် Archive Instant Access tier ထဲက object တွေကို ပြန်ခေါ်ချင်ရင် အလိုအလျောက် Frequent Access tier ကို ပြန်ရွှေ့ပေးပါတယ်။ Deep Archive Access tier မှာ ရှိတဲ့ object တွေကို ပြန် retrieve လုပ်ချင်ရင်တော့ restore လုပ်ရပါမယ်။

		4. Data များကို အသုံးပြုမှုအပေါ်မူတည်ပြီး အလိုအလျောက် အဆင့်မြင့် တိုက်ရိုက် access tiers သို့ ရွှေ့ပေးပါတယ်။

   3. S3 Standard-IA ( Infrequent access )
      
      **Amazon S3 Standard-Infrequent Access (S3 Standard-IA)** ကို infrequent access လိုအပ်တဲ့ data များအတွက် ထိရောက်တဲ့ storage solution အဖြစ် အသုံးပြုနိုင်ပါတယ်။ Data တွေကိုမကြာခဏ access မလုပ်ပေမယ့်၊ လိုအပ်ချိန်မှာတော့ **rapid access** လိုအပ်တဲ့အခါ အသုံးပြုရမယ့် storage class တစ်ခုဖြစ်တယ်။
      
      S3 Standard-IA ကို access frequency နည်းတဲ့ data များအတွက်၊ Long-term data storage လုပ်ချင်တဲ့အခါ၊ Disaster recovery နဲ့ Backup data တို့အတွက် အသုံးပြုနိုင်ပါတယ်။
      
      S3 Standard-IA ရဲ့ နောက်ထပ်တန်ဖိုးကတော့ **S3 Lifecycle policies** ကို အသုံးပြုပြီး, Data အရည်အချင်းကို မတူညီတဲ့ storage classes (S3 Standard, S3 Intelligent-Tiering, S3 Standard-IA, S3 One Zone-IA) ကြားမှာ automatic transition လုပ်ပေးနိုင်တာပဲ ဖြစ်ပါတယ်။ 

	  Notes: 

		1. 99.999999999% durability ကို AWS S3 Standard မှာရှိသလို၊ S3 Standard-IA မှာလည်း ပေးထားပါတယ်။
		   
		2. S3 Standard နဲ့တူတဲ့ **low latency** နဲ့ **high throughput** ရှိတယ်။ Millisecond-level access လိုအပ်တဲ့ data တွေကို ထိရောက်စွာ handle လုပ်နိုင်တယ်။
		   
		3. S3 Standard ထက် storage cost နည်းပေမယ့်၊ **retrieval charge** ရှိတယ်။ ဒါကြောင့် backup data, long-term storage, disaster recovery files တွေအတွက် အထူးသင့်တော်တယ်။
	  
   4. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
      
      **Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)** က Infrequent access data အတွက်၊ Rapid access လိုအပ်တဲ့အခါအသုံးပြုဖို့ ဒီဇိုင်းထုတ်ထားတဲ့ Storage Class တစ်ခုဖြစ်ပါတယ်။ ဒါပေမယ့် အခြား S3 Storage Classes တွေလို **three Availability Zones (AZs)** မဟုတ်ဘဲ, **single AZ** မှာပဲ data ကို သိမ်းဆည်းထားတယ်။ ဒီအတွက်ကြောင့် **S3 Standard-IA ထက် 20%** နီးပါး သက်သာတယ်။
      
      S3 One Zone-IA ကို တန်ဖိုးအနည်းဆုံးနဲ့ infrequent access data များအတွက် သုံးနိုင်ပြီး၊ AZ redundancy မလိုတဲ့ data များအတွက် သင့်တော်တယ်။ တစ်ခါတစ်ရံမှာ secondary backup copies တွေ, on-premises data replication, easily re-creatable data တွေကို သိမ်းဆည်းတဲ့အခါမှာ သုံးဖို့ အထူးသင့်တော်တယ်။ အခြား AWS Region ကနေ S3 Cross-Region Replication နဲ့ replication လုပ်ထားတဲ့ data တွေအတွက် cost-effective storage အဖြစ်လည်း သုံးနိုင်တယ်။
      
      S3 Lifecycle policies ကို သုံးပြီး, S3 Standard, S3 Intelligent-Tiering, S3 Standard-IA, S3 One Zone-IA တို့အကြား Data များကို automatic transition လုပ်နိုင်ပါတယ်။

	  Notes: 

		1. S3 Standard-IA ထက် 20% ထပ်ပြီးသက်သာတဲ့ storage cost ရှိတယ်။ ဒါပေမယ့်, data retrieval လုပ်တဲ့အခါမှာ per GB retrieval charge ကိန်းရဲ့ပါတယ်။
		   
		2. S3 Standard နဲ့တူတဲ့ low latency နဲ့ high throughput ရှိတယ်။
		   
		3. ** 99.999999999% (11 nines) durability ရှိပြီး, AZ တစ်ခုတည်းမှာသာ သိမ်းထားတာဖြစ်တဲ့အတွက် AZ failure ဖြစ်ရင် data loss ဖြစ်နိုင်တယ်။  

   5. Amazon S3 Glacier Instant Retrieval

	  **Amazon S3 Glacier Instant Retrieval** သည် archive storage class တစ်ခုဖြစ်ပြီး, long-lived data များအတွက် lowest-cost storage ကို ပေးစွမ်းတယ်။ 
	  
	  S3 Glacier Instant Retrieval ကို အနည်းအကျဉ်း access လုပ်ဖို့ ရည်ရွယ်ထားတဲ့ long-term archive data များအတွက် အသုံးပြုနိုင်ပါတယ်။ Data တွေကို milliseconds အတွင်း retrieve လုပ်ချင်တဲ့ use cases တွေအတွက်လည်း စိတ်ချရတဲ့ storage option တစ်ခုပါ။

	  Notes: 

		1. Long-lived data ကို S3 Standard-IA နဲ့ နှိုင်းရင်, storage cost ကို 68% ခန့် ပိုမိုသက်သာစေတယ်။ ဒါဟာ quarter တစ်ခုမှာ တစ်ကြိမ်သာ access လုပ်ဖို့ ရည်ရွယ်ထားတဲ့ data များအတွက် အထူးသင့်တော်တယ်။
		  
		2. S3 Standard, S3 Standard-IA storage classes နဲ့တူတဲ့ low latency, high throughput ရှိတယ်။ **Milliseconds-level** access ကိုပေးစွမ်းနိုင်တယ်။
		  
		3. 99.9% availability design လုပ်ထားပြီး, 99% SLA availability ရှိတယ်။
		  
		4. Medical images, news media assets, user-generated content archives တို့လို archive data များအတွက် ideal ဖြစ်တယ်။
		  
		5. S3 PUT API ကို အသုံးပြုပြီး, direct uploads လုပ်နိုင်တယ်။ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes (S3 Standard, S3 Standard-IA) ကနေ, S3 Glacier Instant Retrieval သို့ data migration ကို auto လုပ်နိုင်တယ်။
	   
   6. Amazon S3 Glacier Flexible Retrieval (Formerly S3 Glacier)
      
      **Amazon S3 Glacier Flexible Retrieval** သည် low-cost storage ကို archive data များအတွက် ပေးစွမ်းပေးတဲ့ storage class တစ်ခုဖြစ်ပါတယ်။ **S3 Glacier Instant Retrieval** ထက် 10% နီးပါး သက်သာပြီး, data ကို 1-2 ကြိမ်သာ access လုပ်ရတဲ့နှစ်စဉ်သုံးစွဲမှုအတွက် အထူးသင့်တော်တယ်။
      
      S3 Glacier Flexible Retrieval သည် backup, disaster recovery, offsite data storage လိုအပ်ချက်များအတွက် အထူးသင့်တော်ပြီး, occasional data retrievals အတွက် cost-effective option တစ်ခုပါ။ Large sets of data များကို free bulk retrievals နဲ့ retrieve လုပ်နိုင်တဲ့ flexibility သုံးပြီး, cost များအတွက် သက်သာစေနိုင်ပါတယ်။

	  Notes: 

		1. Archive data များအတွက် S3 Glacier Instant Retrieval ထက် 10% အထိ သက်သာတယ်။ အကြမ်းဖျဉ်း data retrieval မလိုချင်တဲ့ cases အတွက် စိတ်ချရတဲ့ option ဖြစ်တယ်။
		  
		2. Data ကို minutes မှ hours အထိ retrieve လုပ်နိုင်တဲ့ options ပေးပြီး, bulk retrievals များအတွက် free ဖြစ်တယ်။ ဒါဟာ backup နဲ့ disaster recovery use cases များအတွက် အထူးသင့်တော်တယ်။
		  
		3. 99.999999999% (11 nines) durability နဲ့ 99.99% availability ရှိပါတယ်။ Data ကို physically separated AWS Availability Zones တွေမှာ redundantly သိမ်းဆည်းထားတယ်။
		  
		4. Data in transit အတွက် SSL ကို support လုပ်ပြီး၊ data at rest အတွက် encryption ကို အထောက်အပံ့ပေးတယ်။
		  
		5. Retrieval times ကို minutes မှ hours အထိ configure လုပ်နိုင်ပြီး, free bulk retrievals ကို ပေးစွမ်းပါတယ်။
		  
		6. S3 PUT API ကို သုံးပြီး direct uploads လုပ်နိုင်တယ်။ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes များထဲမှ S3 Glacier Flexible Retrieval သို့ data migration ကို automatic လုပ်နိုင်ပါတယ်။

   7. Amazon S3 Glacier Deep Archive
      
      **Amazon S3 Glacier Deep Archive** သည် Amazon S3 ရဲ့ lowest-cost storage class ဖြစ်ပြီး, long-term retention နှင့် digital preservation အတွက် သင့်လျော်သော option တစ်ခုဖြစ်ပါတယ်။ ဒီ storage class သည် data ကို တစ်နှစ်တစ်ကြိမ် ဒါမှမဟုတ် နှစ်စဉ်တစ်ကြိမ်သာ access လုပ်ရတဲ့အခါတွင် သုံးရန် ရည်ရွယ်ထားပါတယ်။
      
      S3 Glacier Deep Archive သည် long-term data storage များအတွက် အထူးသင့်တော်ပြီး, regulatory compliance requirements တွေကို ပြည့်စုံစေရန် ရည်ရွယ်ထားပါတယ်။ Cost-effective နဲ့ easy-to-manage ဖြစ်ပြီး, magnetic tape systems တွေရဲ့ အစားအသုံးပြုနိုင်ပါတယ်။ Data ပြန်ယူတဲ့အခါမှာ, hours အနည်းငယ်နဲ့ up to 12 hours အထိ ကြာနိုင်ပါတယ်။ ဥပမာ - 12 hours တိတိ မိမိ data ကို ပြန်ရနိုင်ပါတယ်။

	  S3 Glacier Deep Archive က ultra-low cost ရှိတဲ့ storage class ဖြစ်တဲ့အတွက်, သိမ်းဆည်းမှုအတွက် စျေးသက်သာပါတယ်။ ဒါပေမယ့်, data ကို retrieve လုပ်တဲ့အခါ, time နည်းနည်းကြာပြီးတော့ cost တွေလည်း တချို့ရှိနိုင်ပါတယ်။
	  
	  Notes: 

		1. Data များကို very low cost နဲ့ သိမ်းဆည်းနိုင်ပြီး, S3 Glacier Deep Archive သည် အနိမ့်ဆုံး storage cost ရှိသော option ဖြစ်ပါတယ်။
		  
		2. 7-10 နှစ် သို့မဟုတ် အထက် data retention လိုအပ်တဲ့ highly-regulated industries (financial services, healthcare, public sectors) အတွက် အထူးသင့်တော်ပါတယ်။
		  
		3. S3 PUT API ကို သုံးပြီး direct uploads လုပ်နိုင်ပြီး၊ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes များထဲမှ S3 Glacier Deep Archive သို့ data migration ကို automatic လုပ်နိုင်ပါတယ်။

   8. S3 Outposts
      
      S3 Outposts ကို S3 Storage ကို AWS Outposts နဲ့အတူသုံးဖို့ design လုပ်ထားတဲ့ storage class တစ်ခုဖြစ်ပါတယ်။ S3 Outposts က data ကို မိမိရဲ့ on-premises ထဲမှာပဲ သိမ်းဆည်းနိုင်ဖို့ အထူးသင့်တော်ပါတယ်။ ဒါက မြန်ဆန်တဲ့ response time နဲ့ အတူ အချက်အလက်တွေကို local data center မှာပဲ သိမ်းဆည်းဖို့လိုတဲ့ use cases တွေအတွက် သင့်တော်တဲ့ solution ဖြစ်ပါတယ်။
      
      S3 on Outposts သည် local data residency requirements တွေအတွက် အထူးသင့်တော်ပြီး, on-premises applications နဲ့ data ကို နီးနီးနားနားသုံးနိုင်ဖို့ အထူးသင့်လျော်ပါသည်။ Local data storage ပေါ်မှာ high performance လိုအပ်တဲ့ workloads အတွက် အထူးသင့်လျော်သည်။

	  Notes: 
	  
		1. S3 SDK ကို အသုံးပြုပြီး, S3 object storage နဲ့ bucket management လုပ်နိုင်ပါတယ်။
		  
		2. Outposts ပေါ်မှာ data ကို multiple devices နဲ့ servers တွေကြား ပြန်လည် သိမ်းဆည်းထားပြီး, data ကို durable နဲ့ redundant အနေနဲ့ သိမ်းဆည်းပါတယ်။
		  
		3. SSE-S3 (Server-Side Encryption with Amazon S3-managed keys) နဲ့ SSE-C (Server-Side Encryption with Customer-provided keys) ကို အသုံးပြုပြီး encryption လုပ်နိုင်ပါတယ်။
		  
		4. IAM (Identity and Access Management) နဲ့ S3 Access Points ကို အသုံးပြုပြီး authentication နဲ့ authorization ကို စီမံနိုင်ပါတယ်။
		  
		5. AWS DataSync ကို သုံးပြီး AWS Regions သို့ data ကို ပြန်ပို့နိုင်ပါတယ်။
		  
		6. Data များကို S3 Lifecycle policies အသုံးပြုပြီး expiration actions လုပ်နိုင်ပါတယ်။

------------------------------------------------------------------------

5. Amazon EFS ( Elastic File System )
   
   Amazon EFS (Elastic File System) က Amazon Web Services (AWS) ရဲ့ managed service တစ်ခု ဖြစ်ပြီး fully managed, scalable, အလွန် flexibly သုံးနိုင်တဲ့ cloud-based file storage system တစ်ခုဖြစ်ပါတယ်။ Amazon EFS ကို AWS Cloud ရဲ့ EC2 instances တွေနဲ့အတူ အသုံးပြုဖို့ အသင့်လျော်ပြီး, shared file system ပုံစံဖြင့် အခြား instances များစွာကနေ access လုပ်နိုင်ပါတယ်။ Data တွေကို အလိုအလျောက် scale up နဲ့ scale down လုပ်ပေးနိုင်တဲ့အတွက်, လိုအပ်သလို အသုံးပြုနိုင်ပါတယ်။
   
   EFS ကိုအသုံးပြုပုံက Linux-based workloads များအတွက် optimized လုပ်ထားတာကြောင့် ရိုးရှင်းပါတယ်။ မိမိရဲ့ instances တွေကနေ အချိန်နှင့်တပြေးညီ access လုပ်ပြီး data ကို share လုပ်ဖို့အတွက် အသင့်တော်ဆုံးပါ။ Multi-AZ deployments ရဲ့ အားသာချက်နဲ့ failover support ပေးတဲ့ အပြင်, တစ်ပြိုင်နက်တည်းမှာ data က backup လုပ်ထားတာကြောင့် data loss ဖြစ်စေမယ့် ပြဿနာတွေကနေနဲ့ လုံခြုံစိတ်ချရပါတယ်။
   
   Notes: 
   
    1. EFS က data storage ကို အလိုအလျောက် scale up/down လုပ်ပေးနိုင်ပါတယ်။ ပုံမှန် အခြေအနေအရ storage volume ကနေ petabytes အထိ အဆင့်မြှင့်တင်နိုင်ပါတယ်။
        
    2. Amazon EFS က data ကို multiple Availability Zones (AZs) တွင် replicate လုပ်ထားပါတယ်။ ဒါကြောင့် အရမ်းတည်ငြိမ်တဲ့ storage အဖြစ် အသုံးပြုနိုင်ပါတယ်။
       
    3. EFS က pay-as-you-go pricing နဲ့ လုပ်ဆောင်ပါတယ်။ ဒါကသိမ်းဆည်းထားတဲ့ data size အပေါ် မူတည်ပြီး storage fee ကိုပေးဆောင်ရမှာ ဖြစ်ပါတယ်။

   EFS သည် နေရာတစ်ခုတည်းမှာ data များအရမ်းလိုအပ်တဲ့ application များအတွက် အသင့်တော်ဆုံးဖြစ်ပြီး, cloud environment များမှာ ဖိုင်များကို shared access နဲ့ တည်ဆောက်လိုတဲ့ အခါမှာ အသုံးပြုသင့်ပါတယ်။
   
------------------------------------------------------------------------

6. Amazon RDS 
   
   **Amazon Relational Database Service (Amazon RDS)** ဆိုတာ AWS ရဲ့ managed service တစ်ခုဖြစ်ပြီး, relational databases များကို အလွယ်တကူ setup လုပ်နိုင်အောင်, operate နဲ့ scale လုပ်နိုင်အောင် ပံ့ပိုးပေးတယ်။ ဒီ service က database administration ရဲ့ tasks များဖြစ်တဲ့ provisioning, patching, backup, recovery, နဲ့ scaling အလုပ်တွေကို စက်မှန်အလိုလုပ်ဆောင်ပေးတာကြောင့်, developers တွေအနေနဲ့ database management အပေါ်မှာ အချိန်ကုန်မှုနည်းပြီး, အခြားအရေးကြီးတဲ့ application development task တွေကို အာရုံစိုက်နိုင်တယ်။

	1. Amazon RDS သည် fully managed service ဖြစ်တဲ့အတွက်, database administration နဲ့ပတ်သက်တဲ့ operations များကို စက်မှန်အလိုလုပ်ဆောင်ပေးတယ်။ ဒီလိုမျိုးဖြစ်လို့, developers တွေအနေနဲ့ application development နဲ့ operation အပေါ်မှာသာ အာရုံစိုက်နိုင်တယ်။
    
	2. High availability နဲ့ failover support အတွက် Multi-AZ (Multiple Availability Zones) deployment ကို ပံ့ပိုးပေးတယ်။ ဒီ feature လို့ database instance တစ်ခု fail ဖြစ်ရင်, အခြား AZ မှာရှိတဲ့ standby instance ကို seconds အတွင်း ပြောင်းလုပ်ပေးနိုင်တယ်။
    
	3. Data encryption အတွက် support လုပ်ပေးပြီး, data-at-rest နဲ့ data-in-transit အတွက် SSL/TLS encryption ကို အသုံးပြုနိုင်တယ်။ Authentication နဲ့ authorization အတွက် AWS Identity and Access Management (IAM) ကိုပံ့ပိုးပေးတယ်။
    
	4. Vertical scaling နဲ့ horizontal scaling နည်းလမ်းနှစ်မျိုးလုံးကို ပံ့ပိုးပေးတယ်။ ဒါကြောင့်, application workload တိုးလာတဲ့အခါမှာ, မိမိ database ကို အလွယ်တကူ scale လုပ်နိုင်တယ်။
    
	5. Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, နှင့် Microsoft SQL Server ကဲ့သို့သော popular relational database engines များကို ပံ့ပိုးပေးတယ်။
