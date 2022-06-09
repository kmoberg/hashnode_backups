## A Guide to AWS Certifications

# A Guide to AWS Certifications

# AWS Certifications - What are they?
If you've worked in the IT industry for a while, you'll know that a lot of the industry thrives on certifications. Certifications are exams designed by IT vendors to verify your knowledge about their products and services, resulting in a diploma or badge you can show to employers to prove you have that competency. 


## Who should go for a certification?
So who should consider spending the time, energy and money needed to pass one of these exams in the first place? 

Well, there are many reasons why you'd take a certification exam such as: 
- You want to verify that you have the knowledge in a field and to get the recognition.
- Many employers view certifications as a good way to check that applicants are competent in that field.
- Negotiating pay rises at your current company.
- You just want to learn! 

Especially the last point is important: you don't *have to*  take the exam at the end of a course material (but you should!), however: certification course materials are a great way to learn new topics as they introduce you to a myriad of ideas thoughts and concepts you might not be aware of.


## Introducing the AWS Certifications

Amazon Web Services (AWS), like most other vendors provide at the time of writing, 12 different certifications grouped into four categories:

- Foundational
- Associate
- Professional
- Specialty

If you have no experience with AWS certifications, it can be hard to know where to begin your certification path, which is why I wrote this blog post: Where should you begin?

Well: In theory, you could start **anywhere**. Unlike many other vendors, AWS do not have prerequisites for any certifications and you can at any point, take any certification feel comfortable with. However: that doesn't mean that is a good idea. I've created a flow diagram based on AWS own [certification guides](https://aws.amazon.com/certification/) with suggestions on what path to take. 


![AWS Certification Path.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654769444288/BzOuxasRm.png align="left")

As you can see, there aren't that many certifications, especially if you do not count the specialty certifications, and we'll talk about those later. 

Before I start discussing each certification and it's worth, I'll quickly introduce you to my journey on the AWS certification path.


## My Background
Coming from a background in systems administration and operations, I started working with AWS services in 2017, and since then, I've held two AWS associate level certifications: Solutions Architect Associate and Developer Associate. 

I got started with AWS in 2017 when I joined a small company as a Sysadmin, running their internal IT services, but I was also responsible for managing a number of clients that were hosted in AWS. Having no experience at all with AWS when I started there, I did a lot of research before starting, and ended up finding two certification books to get me started, the SysOps Administrator certification guide, and Solutions Architect Associate certification guide. Being a SysAdmin, I figured the SysOps book would be perfect for me - that was not the case. That certification assumes a lot of preexisting knowledge about AWS services, or at least service names - making it a very difficult read. I gave up. A few weeks later though, I started on the Solutions Architect book that fortunately gives a better introduction to each service covered and made it easier. It didn't make it easy, but *easier*... I studied for a few months, took the exam, and failed. Miserably. 

Turns out: The certification guide itself back when I used it - is not enough to pass, not by a country mile. I went back after the exam, feeling annoyed, but sat down, found services like [A Cloud Guru](https://acloud.guru) (#NotSponsored!) that provided great video training and gave me the additional materials I needed so I passed the exam, two weeks later.

Fast forward a few years, and I used the Solutions Architect Associate certification to score a new job at a new company, with higher pay, and way better working conditions. At that company I took the Certified Developer exam. This time, I was more prepared, has a couple of years experience under my belt, and studied using both the certification guide and video materials.

## AWS Certifications
Now - with that background: learn from my mistakes! If you do not have any experience with AWS - **do not start at the associate level**. I see a lot of people do the same mistake I did - go straight for the Solutions Architect exam, but they either, don't plan on working as SAs or have no experience in the field. Don't do it. It's a hard exam, and without the prerequisite experience, it's not a good experience, and chances are that you have to study significantly more than you need for a more relevant exam.

My suggestion is to start with the foundational exam, the AWS Cloud Practitioner.

### Foundational
#### AWS Cloud Practitioner
- **Who is it for:**  Anyone who is interested in AWS! Both technical and non-technical personell.
- **Requirements:** None. However *recommended* to have: *6 months of exposure to the AWS Cloud. Basic understanding of IT services and how they relate to AWS. Knowledge of core AWS services and use cases, billing and pricing models, security concepts and how cloud impacts the business.*
- **Cost:** $100 USD 
- **Time:** 90 minutes.
- **Number of questions:** 65 either multiple choice or multiple response
 
 

The AWS Cloud Practitioner exam is the entry level certification in AWS. It gives an introduction to the concept of the cloud in general, AWS, and the various AWS services. It is an exam made for both technical and non-technical personell who are interested in learning more about how AWS works. 

It is the recommended entry level certification as it contains a lot of foundational knowledge that can be useful at a later state in your certification journey, but doesn't dive too deep into detailed technical knowledge about each service. 

### Associate
Something to note about the associate level exam is that all three exams cover some of the same materials about how the cloud and AWS is structured, and as a result, it can be relatively easy to go from one associate exam to another. Each exam does however require a significant knowledge of specific domains in addition to the foundational knowledge.


#### AWS Certified Developer Associate

- **Who is it for:** Application or infrastructure developers working on applications deployed on AWS.
- **Requirements:** None. However ==recommended== to have: *1 Year or more of hands-on experience developing and maintaining an AWS based application.*
- **Cost:** $150 USD
- **Time:** 130 minutes
- **Number of questions:** 65 either multiple choice or multiple response

Once passing the Cloud Practitioner, my strongest recommendation for developers is to move straight to the Certified Developer Associate exam. This is the most relevant exam someone coming in as an experienced developer can take. 

The exam covers topics such as introducing AWS features including managed databases, servers and services, how to write code optimized for the cloud, automating building and deployment of code and debugging in the cloud. All topics that are extremely relevant to a developer making the exam a more fun experience than other more infrastructure focused exams.

When working in the modern cloud, it is, unfortunately, no longer possible for a developer to say: "I don't care about infrastructure". A developer *needs* to understand the basics about a database, how utilizing a read-only DB URI when possible is preferable to pushing all traffic to a single URI, or know how basic networking functions when configuring access between a front and backend application. This certification covers these things in a way that makes it understandable for someone with limited or no infrastructure experience.

#### AWS Certified SysOps Associate

- **Who is it for:** IT personell with infrastructure experience, typically sysadmins, architects, etc.
- **Requirements:** None. However ==recommended== to have:  *1 Year or more of hands-on experience developing and maintaining an AWS based application.*
- **Cost:** $150 USD
- **Time:** 180 minutes
- **Number of questions:** 65 scoring opportunities, may be multiple choice, multiple response, or exam lab
- **URL:** [AWS Training and Certification](https://aws.amazon.com/certification/certified-sysops-admin-associate/?ch=tile&tile=getstarted)

If you've previously been working as a SysAdmin, IT admin, Linux Guru, Windows Server God, etc. this is the exam for you. The SysOps administrator exam gives you more in-depth knowledge about AWS services, how to maintain them, how to scale out and up as needed, and how to optimize your cloud for security and cost. 

The exam is designed to test the candidates experience in both daily tasks on how to build and maintain auto-scaling groups, and how you can ensure your data is securely stored with access logged. It is ideal for personell tasked with maintaining and optimizing AWS infrastructure and will introduce you to incident response, disaster recovery procedures, and how you can figure out what has gone wrong and how to remediate an incident. 

#### AWS Certified Solutions Architect Associate

- **Who is it for:** IT Architects.
- **Requirements:** None. However ==recommended== to have: *1 or MORE years of hands-on experience architecting AWS infrastructure*
- **Cost:** $150 USD
- **Time:** 130 minutes
- **Number of questions:** 65 multiple choice or multiple response
- **URL:** [AWS Training and Certification](https://aws.amazon.com/certification/certified-solutions-architect-associate/?ch=tile&tile=getstarted)

The AWS Certified Solutions Architect Associate (a mouthful to say and type...) is most likely the most misunderstood exam in IT. I see a ton of people, including myself, take this exam, yet have no need for the exam in practice, as they don't work as an architect, but rather either work as an engineer or developer which this exam is not geared towards. 

The Architect Associate exam is difficult. Really difficult. It requires you to know a significant number of services, not very in depth, but you must understand what they can do and how they work together. You must know how you can design an infrastructure to be resilient against failure, yet be high-preforming, secure and finally cheap. 

The exam is a very interesting exam, but for most people it is very much not relevant. And it is most **certainly** not the exam you should be going for after the foundational level. If you have previous experience with the developer and/or sysops, and want more, the SA might be for you, but personally I'd go straight for the DevOps Pro exam instead.

This is a wide-spanning exam and you'll be expected to know the difference between most of AWS various services and how these services work together. 

### Professional Exams
#### AWS Certified DevOps Engineer - Professional

- **Who is it for:** Developers or SysAdmins
- **Requirements:** None. However, ==recommended== to have: *2 or MORE years of hans-on experience*
- **Cost:** $300 USD
- **Time:** 180 minutes
- **Number of questions:** 75 questions, either multiple choice or multiple response
- **URL:** [AWS Training and Certification](https://aws.amazon.com/certification/certified-devops-engineer-professional/?ch=tile&tile=getstarted)

The professional level exams are where the fun begins! These are the two hardest exams AWS has to offer, and are considered some of the most difficult exams in IT, period.

The DevOps Pro is a very fun exam! It covers foundational DevOps concepts and how to implement these in AWS. It requires you to have an understanding of how AWS services interact and how you can automate building and deploying code on AWS using tools such as Infrastructure as Code (IaC) and Pipelines. 

Just like all other AWS exams, it has no prerequisites, so anyone can take the exam at any time, however - I strongly recommend having a ton of experience before taking this exam. It does require a deep experience working with a breath of various AWS and DevOps tools, with experience that is hard to come by without having tried it.


#### AWS Certified Solutions Architect - Professional

- **Who is it for:** Architects.
- **Requirements:** None. However, ==recommended== to have: *2 or MORE years of hans-on experience*
- **Cost:** $300 USD
- **Time:** 180 minutes
- **Number of questions:** 75 questions, either multiple choice or multiple response
- **URL:** [AWS Training and Certification](https://aws.amazon.com/certification/certified-solutions-architect-professional/?ch=tile&tile=getstarted)

Considered by many to be one of the hardest exams in IT, the SA Pro is complicated... It requires you to have experience with most of the AWS tools including the AWS CLI, API, CloudFormation templates, billing, scripting languages **and** Linux and Windows administration. Yeah, I said it was complicated.

There are a metric-ton of features you need to understand (see my mind-map from my notes from the SA pro below - this image is at 10% scaling and my 1440p monitor cannot display more than half at a time...) and have a fair bit of comprehension about. You don't need deep specialty competency in all of them, but you still need a fair bit.


![Screen Shot 2022-06-09 at 11.40.03.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654769427533/fRMnsPU0m.png align="left")

Another thing to keep in mind about this exam is that you will most likely have limited time. Even though you have 180 minutes and only 75 questions, giving you 2 1/2 minutes per question - each question is **long**. The questions are for the most part scenario questions with one or more paragraphs of information that you need to decipher and figure out what is the correct answer. To make things even worse, in most questions there are **multiple plausible answers**. You must pick the **most correct** answer which can be really, really hard at times.


### Specialty Exams
There are six specialty exams at the time of writing, and I'm not going to cover them as if you're interested in them, you're going to need to know how to study for them on your own anyway. Unfortunately the specialty exams often have very limited official support and you need to rely on white papers and notes. 

However, when you take one: good luck! I see more and more people take them every week and I'm equally as happy every time I see people do so! <3 

## Learning Materials
For all of these exams, you'll need learning materials. No matter what exam you are going to take, make sure you do a few things:
* Go to the [AWS Training and Certification website](https://aws.amazon.com/certification/)
* Download the exam guide and read it!
* Download the sample questions. They'll help you out in understanding the exam!
* AWS Has FREE practice exams for all exams! You need to go to a separate website, linked from the Training and Certification site.
* Read the white papers linked for each exam. I know they are boring as all hell, but they contain a ton of useful information, I promise!

With those things taken care of, I personally learn a lot more from a combination of reading and watching video materials. I've used the official certification guides (available on Amazon) in the past, combined with video materials from multiple sources. I recommend:
* [A Cloud Guru](https://acloud.guru)
* [Stephane Maarek on Udemy!](https://www.udemy.com/user/stephane-maarek/)

They have very different teaching styles, and I'd say I prefer Stephanes approach in a lot of situations, but both work very well. 

## The Exam
### Booking The Exam
Booking the exam is easy and is handled through the [AWS Training and Certification](https://aws.amazon.com/certification/) site. Find the correct exam and click "Schedule an Exam". You'll be redirected to either Person VUE or PSI - the official proctors of AWS.

You can book either an in-person exam at an official testing center, or an at-home exam. If you do an at-home exam, in mind that there are some very strict requirements for at-home exams and you are required to have a webcam and microphone on at all times during the exam.

### Exam Day
On exam day, make sure to read up on the exam requirements for either the in-person on at-home exams. You are not allowed to have a phone or watch on you or nearby when taking the exam, nor any other electronics. 

Most of the exams are multiple choice, situational questions where you will be presented with a situation and you will pick one or more correct answers. 

### Post Exam
Once you are done with the exam, you will immediately be told if you passed or failed, however, you will **not** be told your exact score immediately, this will be sent to you within a few business days. 

If you fail, you can reschedule a new exam after a set period, depending on which exam you took.


## Finally
The AWS Certification path is pretty simple and straight forward. However, if you have any questions, feel free to reach out!