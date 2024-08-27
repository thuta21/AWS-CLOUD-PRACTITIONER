Content
1. Instance Stores
2. Amazon Elastic Block Stores ( Amazon EBS )
3. Amazon S3
4. Amazon S3 Storage Classes
------------------------------------------------------------------------

1. Instance Stores
   
   Instance Stores ကို **ephemeral storage** လို့လည်းခေါ်ကြတယ်။ EC2 instance နဲ့ တစ်ခါတည်း ထည့်သွင်းထားတဲ့ temporary storage ဖြစ်ပြီး၊ instance ကို ရပ်လိုက်တဲ့အချိန်မှာ storage data ကပါ ပျက်သွားပါတယ်။ ဒါကြောင့် **data durability** မလိုတဲ့ အချက်အလက်တွေ (temporary files, cache, buffer storage) မျိုးတွေအတွက် အသုံးပြုနိုင်တယ်။ Instance store volumes တွေက instance ရဲ့ physical server မှာ direct attached ဖြစ်တဲ့အတွက် very high I/O performance (input/output) ရပါတယ်။

------------------------------------------------------------------------

2. Amazon Elastic Block Stores ( Amazon EBS )
   
   Amazon EBS ကတော့ **persistent storage** ဖြစ်ပါတယ်။ EC2 instance shutdown ဖြစ်သွားလည်း data အပြည့်အဝသိမ်းဆည်းထားနိုင်တဲ့ durable storage ဖြစ်တယ်။ EBS volumes တွေကို EC2 instances အများကြီးနဲ့ attach လုပ်နိုင်ပြီး, snapshots အဖြစ် backup လုပ်ထားလို့ရတယ်။ Data ကို long-term storage အတွက် EBS ကို အသုံးပြုနိုင်ပါတယ်။
   
   Instance Stores နဲ့ EBS အကြား ကွာခြားချက်က data durability နဲ့ usage purpose ပဲ ဖြစ်ပါတယ်။ High performance, temporary storage လိုရင် Instance Store ကို, Persistent storage လိုရင်တော့ Amazon EBS ကို အသုံးပြုရပါမယ်။

------------------------------------------------------------------------

3. Amazon S3 (​ Simple Storage Service )
   
   Amazon S3 (Simple Storage Service) ဆိုတာ AWS ရဲ့ scalable object storage service တစ်ခုဖြစ်ပါတယ်။ Data ကို **objects** အနေနဲ့ သိမ်းဆည်းပြီး၊ အဲ့ဒီ objects တွေကို **buckets** အဖြစ် grouping လုပ်ထားပါတယ်။
   
   1. Durability နဲ့ Availability : Amazon S3 က **99.999999999% (11 9's)** of durability ရှိတယ်။ Data ကို multiple availability zones (AZs) မှာ replicate လုပ်ထားတာကြောင့်, data loss ဖြစ်နိုင်ခြေ မရှိသလောက် ခိုင်မြဲတယ်။ Availability ကလည်း အမြင့်မားဆုံးရှိတယ်။
   2. Security : S3 မှာ data ကို encryption လုပ်ပြီး သိမ်းဆည်းနိုင်တယ်။ Access control policies နဲ့ Bucket Policies တွေ သုံးပြီး Data ကို Secure လုပ်လို့ရတယ်။ 
   3. Use Cases: Amazon S3 ကို data backup, content storage, media hosting, data lakes, သို့မဟုတ် big data analytics နဲ့အမျိုးမျိုးအတွက် အသုံးပြုနိုင်တယ်။ Static website hosting အတွက်ပါ အသုံးပြုလို့ရတယ်။

------------------------------------------------------------------------

4. Amazon S3 Storage Classes
   
   1. S3 Standard ( General Purpose )
      
      S3 Standard ဟာ high availability နဲ့ low-latency access လိုအပ်တဲ့ frequently accessed data တွေအတွက် အသုံးပြုတယ်။ Data ကို multiple Availability Zones (AZs) တွေအတွင်း store ထားတာဖြစ်ပြီး, latency-sensitive applications တွေမှာအထူးသင့်တော်တယ်။
      
      - Stores data in a minimum of three Availability Zones
      - Durability : 99.999999999% (11 9's)
      - Cost : S3 storage classes တွေထဲမှာတန်ဖိုးအမြင့်ဆုံးဖြစ်တယ်။

   2. S3 Intelligent-Tiering ( Unknown or changing access )
      
      **Amazon S3 Intelligent-Tiering** ဆိုတာကတော့ အသုံးပြုသူတွေကြားမှာ popular ဖြစ်တဲ့ cloud storage class တစ်ခုပါ။ ဒီ storage class က data access frequency (အသုံးပြုမှု ပုံစံ) အလိုအလျောက် ခွဲခြားပြီး အသုံးပြုသူများအတွက် သိမ်းဆည်းရေး စရိတ်သက်သာအောင် ပြုလုပ်ပေးပါတယ်။ 

	  **S3 Intelligent-Tiering** ကို အသုံးပြုရင် data များအတွက် latency နည်းပြီး high throughput performance ရရှိပါတယ်။ Unknown (မသိတဲ့) ဒါမှမဟုတ် changing access pattern (အသုံးပြုမှု ပုံစံပြောင်းလဲခြင်း) ရှိတဲ့ data တွေကို သိမ်းဆည်းရာမှာ အထူးသင့်တော်ပါတယ်။ Data lake, data analytics, user-generated content တို့လို workload မျိုးတွေအတွက် ရှယ်အသုံးဝင်ပါတယ်။
	  
	  Intelligent-Tiering ကို အသုံးပြုခြင်းက data usage pattern မသိတဲ့ အခါမျိုးမှာ အထူးသင့်တော်ပြီး cost-saving ဖို့ အကောင်းဆုံး storage class ဖြစ်ပါတယ်။

	  ဒီ storage class မှာအဓိက feature တွေကတော့:

		1. **Automatic Cost Savings**: အချက်အလက်များကို အလွယ်တကူ monitoring လုပ်ပြီး, 30 ရက်လောက် access မလုပ်တဲ့ object တွေကို Infrequent Access tier ကနေ ထားတယ်။ 90 ရက် access မလုပ်ဘဲဖြစ်ရင်တော့ Archive Instant Access tier ကို အလိုအလျောက် ရွှေ့ပါတယ်။

		2. **No Retrieval Charges**: Infrequent Access ဒါမှမဟုတ် Archive Instant Access tier ထဲက object တွေကို ပြန်ခေါ်ချင်ရင် အလိုအလျောက် Frequent Access tier ကို ပြန်ရွှေ့ပေးပါတယ်။ Deep Archive Access tier မှာ ရှိတဲ့ object တွေကို ပြန် retrieve လုပ်ချင်ရင်တော့ restore လုပ်ရပါမယ်။

		3. **Multi-Tiered Storage**: Data များကို အသုံးပြုမှုအပေါ်မူတည်ပြီး အလိုအလျောက် အဆင့်မြင့် တိုက်ရိုက် access tiers သို့ ရွှေ့ပေးပါတယ်။

		4. **Small Monitoring and Automation Charge**: တစ်လအတွင်း object monitoring နဲ့ automation လုပ်တာအတွက် နည်းနည်းလေးပဲ အခကြေးငွေ ထပ်ပေးရတယ်။

		5. **No Operational Overhead**:  S3 Intelligent-Tiering က operational overhead လုံးဝ မရှိဘူးဆိုတာ အရေးကြီးတဲ့ အချက်ပါ။

		6. **High Availability**: S3 Intelligent-Tiering က 99.9% availability ရရှိဖို့ ရည်ရွယ်ထားပြီး SLA က 99% ဖြစ်ပါတယ်။

   3. S3 Standard-IA ( Infrequent access )
      
      **Amazon S3 Standard-Infrequent Access (S3 Standard-IA)** ကို infrequent access လိုအပ်တဲ့ data များအတွက် ထိရောက်တဲ့ storage solution အဖြစ် အသုံးပြုနိုင်ပါတယ်။ Data တွေကိုမကြာခဏ access မလုပ်ပေမယ့်၊ လိုအပ်ချိန်မှာတော့ **rapid access** လိုအပ်တဲ့အခါ အသုံးပြုရမယ့် storage class တစ်ခုဖြစ်တယ်။
      
      S3 Standard-IA ကို access frequency နည်းတဲ့ data များအတွက်၊ Long-term data storage လုပ်ချင်တဲ့အခါ၊ Disaster recovery နဲ့ Backup data တို့အတွက် အသုံးပြုနိုင်ပါတယ်။


		1. **High Durability:** 99.999999999% durability ကို AWS S3 Standard မှာရှိသလို၊ S3 Standard-IA မှာလည်း ပေးထားပါတယ်။
		2. **High Performance:** S3 Standard နဲ့တူတဲ့ **low latency** နဲ့ **high throughput** ရှိတယ်။ Millisecond-level access လိုအပ်တဲ့ data တွေကို ထိရောက်စွာ handle လုပ်နိုင်တယ်။
		3. **Lower Cost:** S3 Standard ထက် storage cost နည်းပေမယ့်၊ **retrieval charge** ရှိတယ်။ ဒါကြောင့် backup data, long-term storage, disaster recovery files တွေအတွက် အထူးသင့်တော်တယ်။
  
	  S3 Standard-IA ရဲ့ နောက်ထပ်တန်ဖိုးကတော့ **S3 Lifecycle policies** ကို အသုံးပြုပြီး, Data အရည်အချင်းကို မတူညီတဲ့ storage classes (S3 Standard, S3 Intelligent-Tiering, S3 Standard-IA, S3 One Zone-IA) ကြားမှာ automatic transition လုပ်ပေးနိုင်တာပဲ ဖြစ်ပါတယ်။ 

   4. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
      
      **Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)** က Infrequent access data အတွက်၊ Rapid access လိုအပ်တဲ့အခါအသုံးပြုဖို့ ဒီဇိုင်းထုတ်ထားတဲ့ Storage Class တစ်ခုဖြစ်ပါတယ်။ ဒါပေမယ့် အခြား S3 Storage Classes တွေလို **three Availability Zones (AZs)** မဟုတ်ဘဲ, **single AZ** မှာပဲ data ကို သိမ်းဆည်းထားတယ်။ ဒီအတွက်ကြောင့် **S3 Standard-IA ထက် 20%** နီးပါး သက်သာတယ်။
      
      S3 One Zone-IA ကို တန်ဖိုးအနည်းဆုံးနဲ့ infrequent access data များအတွက် သုံးနိုင်ပြီး၊ AZ redundancy မလိုတဲ့ data များအတွက် သင့်တော်တယ်။ တစ်ခါတစ်ရံမှာ secondary backup copies တွေ, on-premises data replication, easily re-creatable data တွေကို သိမ်းဆည်းတဲ့အခါမှာ သုံးဖို့ အထူးသင့်တော်တယ်။ အခြား AWS Region ကနေ S3 Cross-Region Replication နဲ့ replication လုပ်ထားတဲ့ data တွေအတွက် cost-effective storage အဖြစ်လည်း သုံးနိုင်တယ်။

		- **Low Cost:** S3 Standard-IA ထက် 20% ထပ်ပြီးသက်သာတဲ့ storage cost ရှိတယ်။ ဒါပေမယ့်, data retrieval လုပ်တဲ့အခါမှာ per GB retrieval charge ကိန်းရဲ့ပါတယ်။
		- **High Performance:** S3 Standard နဲ့တူတဲ့ low latency နဲ့ high throughput ရှိတယ်။
		- **Durability:** 99.999999999% (11 nines) durability ရှိပြီး, AZ တစ်ခုတည်းမှာသာ သိမ်းထားတာဖြစ်တဲ့အတွက် AZ failure ဖြစ်ရင် data loss ဖြစ်နိုင်တယ်။
		  
	  S3 Lifecycle policies ကို သုံးပြီး, S3 Standard, S3 Intelligent-Tiering, S3 Standard-IA, S3 One Zone-IA တို့အကြား Data များကို automatic transition လုပ်နိုင်ပါတယ်။

   5. Amazon S3 Glacier Instant Retrieval

	  **Amazon S3 Glacier Instant Retrieval** သည် archive storage class တစ်ခုဖြစ်ပြီး, long-lived data များအတွက် lowest-cost storage ကို ပေးစွမ်းတယ်။ 
	  
	  S3 Glacier Instant Retrieval ကို အနည်းအကျဉ်း access လုပ်ဖို့ ရည်ရွယ်ထားတဲ့ long-term archive data များအတွက် အသုံးပြုနိုင်ပါတယ်။ Data တွေကို milliseconds အတွင်း retrieve လုပ်ချင်တဲ့ use cases တွေအတွက်လည်း စိတ်ချရတဲ့ storage option တစ်ခုပါ။

		- **Lowest Cost Storage:** Long-lived data ကို S3 Standard-IA နဲ့ နှိုင်းရင်, storage cost ကို 68% ခန့် ပိုမိုသက်သာစေတယ်။ ဒါဟာ quarter တစ်ခုမှာ တစ်ကြိမ်သာ access လုပ်ဖို့ ရည်ရွယ်ထားတဲ့ data များအတွက် အထူးသင့်တော်တယ်။
		- **High Performance:** S3 Standard, S3 Standard-IA storage classes နဲ့တူတဲ့ low latency, high throughput ရှိတယ်။ **Milliseconds-level** access ကိုပေးစွမ်းနိုင်တယ်။
		- **Availability:** 99.9% availability design လုပ်ထားပြီး, 99% SLA availability ရှိတယ်။
		- **Data Types:** Medical images, news media assets, user-generated content archives တို့လို archive data များအတွက် ideal ဖြစ်တယ်။
		- **Direct Uploads & Lifecycle Management:** S3 PUT API ကို အသုံးပြုပြီး, direct uploads လုပ်နိုင်တယ်။ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes (S3 Standard, S3 Standard-IA) ကနေ, S3 Glacier Instant Retrieval သို့ data migration ကို auto လုပ်နိုင်တယ်။
	   
   6. Amazon S3 Glacier Flexible Retrieval (Formerly S3 Glacier)
      
      **Amazon S3 Glacier Flexible Retrieval** သည် low-cost storage ကို archive data များအတွက် ပေးစွမ်းပေးတဲ့ storage class တစ်ခုဖြစ်ပါတယ်။ **S3 Glacier Instant Retrieval** ထက် 10% နီးပါး သက်သာပြီး, data ကို 1-2 ကြိမ်သာ access လုပ်ရတဲ့နှစ်စဉ်သုံးစွဲမှုအတွက် အထူးသင့်တော်တယ်။
      
      S3 Glacier Flexible Retrieval သည် backup, disaster recovery, offsite data storage လိုအပ်ချက်များအတွက် အထူးသင့်တော်ပြီး, occasional data retrievals အတွက် cost-effective option တစ်ခုပါ။ Large sets of data များကို free bulk retrievals နဲ့ retrieve လုပ်နိုင်တဲ့ flexibility သုံးပြီး, cost များအတွက် စိတ်ပျက်မဖြစ်စေရန်အတွက် အထူးသင့်တော်ပါသည်။

	- **Low Cost:** Archive data များအတွက် S3 Glacier Instant Retrieval ထက် 10% အထိ သက်သာတယ်။ အကြမ်းဖျဉ်း data retrieval မလိုချင်တဲ့ cases အတွက် စိတ်ချရတဲ့ option ဖြစ်တယ်။
	- **Flexible Retrieval:** Data ကို minutes မှ hours အထိ retrieve လုပ်နိုင်တဲ့ options ပေးပြီး, bulk retrievals များအတွက် free ဖြစ်တယ်။ ဒါဟာ backup နဲ့ disaster recovery use cases များအတွက် အထူးသင့်တော်တယ်။
	- **High Durability & Availability:** 99.999999999% (11 nines) durability နဲ့ 99.99% availability ရှိပါတယ်။ Data ကို physically separated AWS Availability Zones တွေမှာ redundantly သိမ်းဆည်းထားတယ်။
	- **Encryption & SSL:** Data in transit အတွက် SSL ကို support လုပ်ပြီး၊ data at rest အတွက် encryption ကို အထောက်အပံ့ပေးတယ်။
	- **Configurable Retrieval Times:** Retrieval times ကို minutes မှ hours အထိ configure လုပ်နိုင်ပြီး, free bulk retrievals ကို ပေးစွမ်းပါတယ်။
	- **Direct Uploads & Lifecycle Management:** S3 PUT API ကို သုံးပြီး direct uploads လုပ်နိုင်တယ်။ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes များထဲမှ S3 Glacier Flexible Retrieval သို့ data migration ကို automatic လုပ်နိုင်ပါတယ်။

   7. Amazon S3 Glacier Deep Archive
      
      **Amazon S3 Glacier Deep Archive** သည် Amazon S3 ရဲ့ lowest-cost storage class ဖြစ်ပြီး, long-term retention နှင့် digital preservation အတွက် သင့်လျော်သော option တစ်ခုဖြစ်ပါတယ်။ ဒီ storage class သည် data ကို တစ်နှစ်တစ်ကြိမ် ဒါမှမဟုတ် နှစ်စဉ်တစ်ကြိမ်သာ access လုပ်ရတဲ့အခါတွင် သုံးရန် ရည်ရွယ်ထားပါတယ်။
      
      S3 Glacier Deep Archive သည် long-term data storage များအတွက် အထူးသင့်တော်ပြီး, regulatory compliance requirements တွေကို ပြည့်စုံစေရန် ရည်ရွယ်ထားပါတယ်။ Cost-effective နဲ့ easy-to-manage ဖြစ်ပြီး, magnetic tape systems တွေရဲ့ အစားအသုံးပြုနိုင်ပါတယ်။ Data retrieval ကို 12 hours အတွင်း ပြန်ဖျော်ဖြေရန် လိုအပ်တဲ့ backup နှင့် disaster recovery use cases များတွင်လည်း သုံးနိုင်ပါတယ်။

		- **Lowest Cost:** Data များကို very low cost နဲ့ သိမ်းဆည်းနိုင်ပြီး, S3 Glacier Deep Archive သည် အနိမ့်ဆုံး storage cost ရှိသော option ဖြစ်ပါတယ်။
		- **Long-Term Retention:** 7-10 နှစ် သို့မဟုတ် အထက် data retention လိုအပ်တဲ့ highly-regulated industries (financial services, healthcare, public sectors) အတွက် အထူးသင့်တော်ပါတယ်။
		- **High Durability & Availability:** 99.999999999% (11 nines) durability ရှိပြီး, 99.99% availability နှင့် 99.9% SLA availability ရှိတယ်။ Data ကို အနည်းဆုံး ၃ ခုသော geographically-dispersed Availability Zones တွင် replication လုပ်ထားတယ်။
		- **Retrieval Time:** Data ကို 12 hours အတွင်း ပြန်ဖျော်ဖြေရန် လိုအပ်ပါတယ်။ 
		- **Ideal Alternative:** Magnetic tape libraries အစား cost-effective နဲ့ easy-to-manage alternative အဖြစ် သုံးနိုင်ပါတယ်။
		- **Direct Uploads & Lifecycle Management:** S3 PUT API ကို သုံးပြီး direct uploads လုပ်နိုင်ပြီး၊ S3 Lifecycle policies ကို အသုံးပြုပြီး, S3 storage classes များထဲမှ S3 Glacier Deep Archive သို့ data migration ကို automatic လုပ်နိုင်ပါတယ်။

   8. S3 Outposts
      
      **Amazon S3 on Outposts** သည် on-premises AWS Outposts အတွက် object storage ကို ပေးစွမ်းတဲ့ service တစ်ခုဖြစ်ပြီး, S3 APIs နဲ့ features များကို အသုံးပြုနိုင်ပါတယ်။ AWS Region တွင် ရနိုင်တဲ့ S3 APIs နဲ့ features များကို အသုံးပြု၍, Outpost ပေါ်မှာ data ကို ထိန်းသိမ်းခြင်းနှင့် ပြန်ယူခြင်းကို အလွယ်တကူ စီမံနိုင်ပါတယ်။
      
      S3 on Outposts သည် local data residency requirements တွေအတွက် အထူးသင့်တော်ပြီး, on-premises applications နဲ့ data ကို နီးနီးနားနားသုံးနိုင်ဖို့ အထူးသင့်လျော်ပါသည်။ Local data storage ပေါ်မှာ high performance လိုအပ်တဲ့ workloads အတွက် အထူးသင့်လျော်သည်။

		- **S3 Object Compatibility:** S3 SDK ကို အသုံးပြုပြီး, S3 object storage နဲ့ bucket management လုပ်နိုင်ပါတယ်။
		- **Durability & Redundancy:** Outposts ပေါ်မှာ data ကို multiple devices နဲ့ servers တွေကြား ပြန်လည် သိမ်းဆည်းထားပြီး, data ကို durable နဲ့ redundant အနေနဲ့ သိမ်းဆည်းပါတယ်။
		- **Encryption:** SSE-S3 (Server-Side Encryption with Amazon S3-managed keys) နဲ့ SSE-C (Server-Side Encryption with Customer-provided keys) ကို အသုံးပြုပြီး encryption လုပ်နိုင်ပါတယ်။
		- **Authentication & Authorization:** IAM (Identity and Access Management) နဲ့ S3 Access Points ကို အသုံးပြုပြီး authentication နဲ့ authorization ကို စီမံနိုင်ပါတယ်။
		- **Data Transfer:** AWS DataSync ကို သုံးပြီး AWS Regions သို့ data ကို ပြန်ပို့နိုင်ပါတယ်။
		- **S3 Lifecycle Policies:** Data များကို S3 Lifecycle policies အသုံးပြုပြီး expiration actions လုပ်နိုင်ပါတယ်။

------------------------------------------------------------------------