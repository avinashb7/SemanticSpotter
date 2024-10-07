Semantic Spotter with LlamaIndex:

Prerequisites to run the Semantic Spotter.

Step1. : Run all the cell in install all required library and depended code.

How to Run the Symatic Spotter: 

There are two ways.  you execute the query over list of insuracne documents. 

1. For single Query: you can directly pass the query to query_response method.  
Sample Query and Resposne:

Q: print(query_response("What is beneficiary in HDFC insurance policy?"))

Respone: 

The beneficiary in HDFC insurance policy is the individual or entity designated by the insured member to receive the benefits under the policy in the event of the insured member's death.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.84421738104293

2. Using testing_pipeline method for multiple questions: 
Create a list of test questions and passed to testing_pipeline. it will ask for feedback please reposnd with good or bad. 

Sample Query and Resposne:
Q:
questions = ['What is beneficiary in HDFC insurance policy', 'Which is company name is talking about in provided context?',' Who is eligible member in the context of insurance policy?',
             'When a person can recieve the claims?']
             
>testing_pipeline(questions):   

Response from Semantic Spotter:


The beneficiary in HDFC insurance policy is the individual or entity designated by the insured member to receive the benefits under the policy in the event of the insured member's death. If no designated nominee is filed or if the nominee predeceases the insured member, the benefits will be payable to the legal heir of the insured member. The insured member can change the nominee during their lifetime by providing written notice to the policyholder. In certain cases, such as in affinity groups with a lender-borrower relationship, the beneficiary may be the master policyholder to the extent of the outstanding loan amount of the insured member.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.8300101664354461

 Please provide your feedback on the response provided by the bot
good
Answer  from cache:

Which is company name is talking about in provided context?
Answer from LLM:

HDFC Life
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.7592104517273464

 Please provide your feedback on the response provided by the bot
goos
Answer  from cache:

What is beneficiary in HDFC insurance policy
Answer from LLM:

The beneficiary in HDFC insurance policy is the individual or entity designated by the insured member to receive the benefits under the policy in the event of the insured member's death. If no designated nominee is filed or if the nominee predeceases the insured member, the benefits will be payable to the legal heir of the insured member. The insured member can change the nominee during their lifetime by providing written notice to the policyholder. In cases of affinity groups with a lender-borrower relationship, the beneficiary may be the master policyholder to the extent of the outstanding loan amount of the insured member. Any remaining amount after claim settlement to the master policyholder will be paid to the nominee of the insured member.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.8436984086931596

 Please provide your feedback on the response provided by the bot
Good
Answer  from cache:

Which is company name is talking about in provided context?
Answer  from cache:

HDFC Life
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.7592104517273464

 Please provide your feedback on the response provided by the bot
Bad
Answer  from cache:

 Who is eligible member in the context of insurance policy?
Answer from LLM:

An eligible member in the context of the insurance policy is a person who satisfies the eligibility criteria mentioned in the policy and is aged less than the Benefit Expiry Age.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf for document references.
Similarity score is :0.8238409142018135

 Please provide your feedback on the response provided by the bot
Good
Answer  from cache:

When a person can recieve the claims?
Answer from LLM:

A person can receive the claims under the Policy after submitting all necessary claim documents within 60 days from the date of diagnosis of the condition. However, the company may consider condoning the delay in claim intimation if valid reasons are provided for the delay.
Check further at Copy of HDFC-Life-Easy-Health-101N110V03-Policy-Bond-Single-Pay.pdf for document references.
Similarity score is :0.8119365396045904

 Please provide your feedback on the response provided by the bot
Good
Answer  from cache:

Question	Response	Good or Bad
0	What is beneficiary in HDFC insurance policy	The beneficiary in HDFC insurance policy is th...	Good
1	Which is company name is talking about in prov...	HDFC Life\nCheck further at Copy of HDFC-Life-...	Bad
2	Who is eligible member in the context of insu...	An eligible member in the context of the insur...	Good
3	When a person can recieve the claims?	A person can receive the claims under the Poli...	Good






