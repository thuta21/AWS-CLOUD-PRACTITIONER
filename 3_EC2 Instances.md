
Content 
1. EC2 Instance Type
2. Amazon EC2 Instance Families 
   
------------------------------------------------------------------------

1. EC2 Instance Type
   
   EC2 Instance Type ဆိုတာက Amazon Web Services (AWS) ရဲ့ Elastic Compute Cloud (EC2) မှာ Virtual Servers တွေကို တည်ဆောက်ရာမှာ Resource (CPU, Memory, Storage) ပမာဏအရ ရွေးချယ်အသုံးပြုရတဲ့ စိတ်ကြိုက် Server Configuration မျိုးစုံကို ပြောတာပါ။
   
   Notes : 
   
    1. Each Amazon EC2 instance type is grouped under EC2 instance family.
    2. Amazon EC2 provides us with the wide selection of instance types that are optimized for different use cases.
    3. Instance types comprises of varying combinations of CPU, memory, storage and networking capacity and this gives us the flexibility to choose the most appropriate mix of resources for the applications.
    4. Each instance type includes one or more instance sizes, that allows us to scale the resources to the requirements of the target workloads.
    5. The instance types can be divided into following.
       
------------------------------------------------------------------------

2. Amazon EC2 Instance Families 
   
   Instance Type ရွေးတဲ့ နေရာမှာ ကိုယ့် Application ရဲ့ Requirements ပေါ်မူတည်ပြီး ဘာသုံးမလဲဆိုတာ ရွေးချယ်ရပါတယ်။ 
   ![INSTANCEFAMILIES](images/InstanceFamilies.png) 
1. General Purpose
   
	  General Purpose မှာက Balance Resources (Compute + Memory + Networking) ဆိုပြီး ထုတ်ပေးထားတဲ့ အမျိုးအစားပါ။ Web Server လိုမျိုး Code Repositories လိုမျိုးတွေအတွက် အသုံးပြုလို့ကောင်းပါတယ်။ 
   
	  Instance Series အနေနဲ့က M series နဲ့ T series ဆိုပြီးရှိပါတယ်။ AWS မှာ Free tier အနေနဲ့ T2 micro ဆိုပြီး ပေးထားတာ ရှိပါတယ်။
   
2. Compute Optimized
   
	  Compute ဆိုထဲက Intensive Tasks တွေ တွက်ချက်ဖို့ Processing Power ခပ်မြင့်မြင့် သုံးနိုင်မယ့် High Performance Processors အမျိုးအစားဖြစ်ပါတယ်။ ဖော်ပြထားတာအရ Media transcoding တွေ Gaming Servers တွေ Machine Learning Inference တွေ Scientific Modeling တွေ စွမ်းဆောင်ရည်မြင့်မားပြီး တွက်ချက်မှုတွေလုပ်ရတဲ့ High performance computing (HPC) တွေအတွက် သုံးရန်သင့်တော်ပါတယ်။ 
   
	  Instance Series အနေနဲ့က C series ဆိုပြီးရှိပါတယ်။ 

3. Memory Optimized
   
	  Memory ဦးစားပေး အမျိုးအစားဖြစ်ပြီး Data ( Read / Write ) အတွက်သင့်တော်ပါတယ်။ 
	  Abilities 
		- Fast Performance
	    - Large Dataset of Memories
		- Open Sources Databases
		- In-memory caches
		- Real-time big data analytics
	     
	  Instance Series အနေနဲ့က Z series, High Memory, X series, R series ဆိုပြီးရှိပါတယ်။ 
	  
4. Accelerated Computing
   
	  Application performance ကို smoothly run နိုင်ဖို့ CPU load လျော့ချပေးတဲ့ စွမ်းဆောင်ရည်မြင့်ပြီး one specific job နဲ့ အလုပ်လုပ်တဲ့ Hardware Acceleration (co-processors) တွေ အသုံးပြုထားတဲ့အတွက် floating-point number calculations, graphics processing, game streaming တွေအတွက် သင့်တော်ပါတယ်။ 
   
	  Instance Series အနေနဲ့က V series, F series, D series, Inf series, Trn1, G series, P series ။ 
   
5. Storage Optimized
   
	  large datasets တွေအတွက် Read / Write တို့ tens နဲ့ ချီတဲ့ I/O process တွေလုပ်တဲ့ အချိန်မှာ Latency လျော့ချချင်တဲ့ အချိန်၊ ရှုပ်ထွေးတဲ့ Transaction တွေ ရှိလာတဲ့ အချိန် Data ကိုမြန်မြန်ရယူသုံးစွဲချင်တဲ့အခါမျိုးတွေ အတွက်သင့်တော်ပါတယ်။
	  
	  Abilities
		- distributed file systems
		- data warehousing applications
	    - high-frequency online transaction processing (OLTP) systems
	    - input/output operations per second (IOPS)
     
	  Instance Series အနေနဲ့က H series, D series, I seriers
    
6. HPC Optimized 
   
	ဈေးကြီးသလောက် အရည်အသွေးမြင့်မြင့် သုံးနိုင်ဖို့လိုတဲ့ လုပ်ငန်းတွေအတွက် ရည်ရွယ်တယ်။ ကြီးကြီးမားမား ရှုပ်ရှုပ်ထွေးထွေး တွက်ချက် အဖြေထုတ်ရမယ့် လုပ်ငန်းတွေ သုံးသင့်တယ်။
   
	Instance Series : Hpc series

------------------------------------------------------------------------