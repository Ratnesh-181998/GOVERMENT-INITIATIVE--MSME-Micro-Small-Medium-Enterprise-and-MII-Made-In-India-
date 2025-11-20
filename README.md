Government Initiative: 

Business Requirement:  

GeM wants to build a product recommendation based on government initiative such as Micro & Small 
Enterprise (MSE) and Make in India (MII). 
Today on GeM portal, buyer can shortlist products based on a specific set of parameters and get the 
best price for the given set of parameters. However, no options / directional recommendations based 
on the government initiatives are provided to the buyers on possible parameter combination, that is not 
only an equivalent of the selected set of parameters but also is associated in government driven 
initiative. 

With this solution, buyers will gain access to: 

• Similar MSE Products at Lower Prices: Identifying products with equivalent features at more 
competitive prices. 
<img width="2012" height="1057" alt="image" src="https://github.com/user-attachments/assets/af9f9a7c-9985-4382-9bb6-8cc4d650c346" />


• Similar MII Products at Lower Price: Highlighting options that offer superior features or quality 
without exceeding the buyer's budget. 
<img width="2021" height="1084" alt="image" src="https://github.com/user-attachments/assets/4bbc05f9-8b2a-4b94-8f13-24509663f406" />

<img width="1914" height="1059" alt="image" src="https://github.com/user-attachments/assets/8a68112c-b889-40b9-ac79-bc597f35f6b2" />


By implementing the government initiative module using product similarity module, GeM aims to help 
buyers procure products having required govt initiative feature and can fulfill their quota of 
procurement mandated by Government of India. 

Proposed solution: 

Government initiative-based product recommendation module leverage the Product Similarity module 
to identify similar products with similar or better feature of a product.  
In addition to this, the module also filters out the products which qualify to the government driven 
initiatives and provide that to the current selection by the buyer. 
The objective of the Government initiative-based product recommendation module is to identify similar 
products associated with government driven initiatives for a given product of interest based on three 
primary criteria: 
• The shortlisted products are fulfilling the govt initiative criteria. 
• Features of the shortlisted products are similar to the product of interest 
• Price of the shortlisted product should be lower than the product of interest / relatively better 
priced with upgraded components 

Solution Consumption: 

Currently, this solution is integrated into the Product Display Page (PDP) of the GeM portal, providing 
buyers with actionable recommendations directly where they view product detail. 

<img width="1146" height="1357" alt="image" src="https://github.com/user-attachments/assets/a271a562-11ce-4fa7-9542-796df5fa6a13" />

<img width="1127" height="618" alt="image" src="https://github.com/user-attachments/assets/1d60d260-2925-4672-9479-7a567dbe0b10" />

Data: 

To build this solution, we will be using data from product similarity module as well as some other tables 
which has the information regarding the govt initiatives. In future there may some table will be added or 
removed as per the information given by GeM task force. Apart from all the tables required for product 
similarity, we will be needing below mentioned tables:  
• Table: inb_seller  
• Table: arx_tb_arm_branch  
• Table: arx_tb_arm_user_entity  
• Table: arx_tb_arm_master  
• Table: arx_tb_arm_branch_env

Model Methodology: 

The module works on the outcome of the product similarity module to determine which products are 
similar to the selected product based on the specifications. Over the selected products an additional 
filter is added to determine similar products associated with government initiative. 

Steps In Model:  

1. Find list of products fulfilling govt initiative.  
2. Run Product Similarity module to identify most similar product from the above mentioned list.

<img width="1043" height="531" alt="image" src="https://github.com/user-attachments/assets/70df870d-3bf9-4ed5-8ce5-2c1ccd880baf" />

Business Value: 
 
Qualitative – Buyers will get recommendation to fulfill their quota and sellers will be encouraged to 
register under government driven initiatives.

Integration & API: Developed and integrated RESTful APIs using FlaskAPI :

Input: Solution requires product Id as input.  

<img width="1256" height="390" alt="image" src="https://github.com/user-attachments/assets/6724208f-4bc3-49ad-9275-0b762ccd52f0" />

<img width="1292" height="946" alt="image" src="https://github.com/user-attachments/assets/189a23f6-fa9e-4366-96e1-da4cc17860c3" />

<img width="1330" height="459" alt="image" src="https://github.com/user-attachments/assets/ca37bc79-f34a-4633-b6d0-3b87bd29726f" />





