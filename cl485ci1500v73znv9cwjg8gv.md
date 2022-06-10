## My Favorite AWS Tools and Resources that I Use Every Day

Working as a developer and cloud platform engineer working with AWS, I use a ton of tools every day. A lot of these are OS agnostic, but there are some that are not - I'm a Mac user: sorry.


## Terminal: iTerm2 + Fig + Starship = ❤️
My main tool is my terminal. I use it all day, every day and it is probably my most important tool, which is also why it has gone through a ton of modifications over the years and has now gotten to a point where I'm mostly happy with it. 

As for which shell I'm using, I'm still using ZSH with Oh-my-zsh installed, but with mostly default settings and a theme applied.


![Terminal](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779313982/ys2V0fQrS.png align="left")


### iTerm2
iTerm is the base of the terminal. It has a ton more options than the built in terminal, although I rarely use most of them these days. 

**Cost: Free!** from [https://iterm2.com](https://iterm2.com/)

### Starship
Starship is where the customization begins! Starship a customizable prompt that gives me a ton of information at a glance. The prompt is very much context aware, and will change depending on what folder you are in, displaying only relevant information to you. 


![Starship in action](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779333373/_qeiFI-UI.gif align="left")

In my case I display things like current AWS profile in use, git status, and battery information if I'm running low.


![Starship Configuration](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779343899/InnzosGnU.png align="left")

**Cost: Free** from [https://starship.rs/](https://starship.rs/)

### Fig
This is my latest tool in my arsenal and it's fantastic!

Fig is a terminal addition that adds IDE-style autocomplete to your existing terminal. I know you don't **need** this functionality, but boy is it nice to have in a lot of situations when you can't exactly remember a command or what the heck you named your file or folder. 

Fig also allows you to create custom shortcuts and commands the same way aliases let you execute commands more efficiently. It's hard to stay enough good things about Fig and it's well worth a try!


![Fig](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779355114/A6lgmcFbd.gif align="left")

**Cost: Free** from [https://fig.io/](https://fig.io/)

## Jetbrains
I've used pretty much all the code- and text editors as well as IDEs that are on the market. I was a die-hard VScode user since one of the earliest betas, but after a friend showed me the power if the Jetbrains suite, it's hard to go back. Jetbrains offers a myriad of various IDEs for different languages, but they all share the same basic concepts and functionality. It is extremely customizable thanks to a well stocked plugin library from 3rd party developers as well as Jetbrains them selves and as as result, a ton of their software have gotten a permanent place in my dock as I use it on the daily.


![Mac Dock](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779367226/LOFzMybxc.png align="left")

Specifically my most used applications include PyCharm, GoLand, WebStorm and DataGrip. As I'm also still responsible for some PHP apps, PHPStorm is also still used, but not as much.

If you haven't tried out DataGrip yet, it got a significant revamp a while back and is honestly one of the best database management tools I've used. 

**Cost: €649 per year, ex. VAT.** (For Students: **FREE!**) from [https://www.jetbrains.com/](https://www.jetbrains.com/)

## Github Copilot
This is going to cause some controversy I'm sure. Other developers I know claim Copilot is terrible and makes it look like a junior developer wrote the code and is terrible insecure. I disagree. If you think this way, you're not using Copilot right and you're just accepting whatever Copilot suggests without no critical thought. That's not how it's designed, and not how you should be using it. 

Copilot can help you *significantly* speed up your workflow by suggesting the code you are going to type. In the example below, I'm creating a Terraform security group for AWS. I specify the name and ingress, and Copilot suggests the next steps. However, as you can see, it suggests the wrong ports, and I'm not blindly accepting it. You need to be weary of what it suggests and correct what needs to be corrected. However, it even so, it saves me significant time when building these code blocks.


![Copilot Demo](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779469622/QUXfVnlG5.gif align="left")

There are some significant privacy concerns about using copilot, as copilot transmit a good amount of telemetry when it is used, and its suggestions are based on other peoples open-source code submitted to GitHub, so if you are developing top-secret government secrets, I would read the privacy policy before blindly jumping into Copilot. However, if you're already putting your code in Github SaaS and not hosting your own server, and especially if you're using public repos, the telemetry Copilot uses should be no huge privacy concern.

**Cost: Free** (requires invite) from [https://copilot.github.com/](https://copilot.github.com/)

## AWS CLI (and aws-shell)
AWS has a great CLI, but what's even cooler is "aws-shell"! From AWS labs, you can run an interactive shell that connects to your AWS account and from there manipulate it as you wish. It provides auto completion not only for commands, but also for resource names and is incredibly powerful! 


![AWS Shell Demo](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779515214/zHl-0odtV.gif align="left")

I'll be the first to admit that I typically just use the normal CLI, but as soon as I have to deal with instance names and more, the shell is a fantastic tool to be able to use!

In case you don't know - thanks to AWS "API First" philosophy, any resource in AWS should be available as an API and in the CLI, so anything you do in the console should have an API available to you. 

**Cost: Free** from [https://github.com/awslabs/aws-shell](https://github.com/awslabs/aws-shell)

## Infrastructure as Code (IaC) - Terraform and Pulumi
If you're working with cloud and haven't looked at infrastructure as code yet - you need to do so. Today. If you're still configuring your infrastructure by clicking in the console, or running a single CLI command here and there to maintain your infrastructure, it's time to move on - trust me. 

Infrastructure as Code, like the name suggest, allow you to define your infrastructure in code. This means it can be checked into version control, and that it is easily reproducible. It makes it incredibly easy to organize and make sure that knowledge isn't lost when someone leaves the company. The idea is that the infrastructure is *immutable* and should not change after it has been deployed without a redeploy or replacement. 

There are multiple tools available for this task such as CloudFormation, Chef, Puppet and more, but I'd like to recommend two sets of tools: Terraform and Pulumi. 

Terraform is probably the most well-known IaC tool on the market in 2022. It has a very robust set of tools, providers and developer support available making it incredibly powerful and easy to get started with, building your infrastructure. Terraform is made by Hashicorp, a company known for providing robust and well-tested infrastructure tools. You write your code in HCL (Hashicorp Configuration Language) a custom language that is easy to write and easy to read, but there is also a JSON version available if you absolutely prefer JSON for some reason. 

In my opinion, Terraform is *perfect* for infrastructure or someone in operations starting on their IaC journey, or if you have a team of infrastructure people working on this. It is extremely powerful and extendable, and provides the tools a platform team needs.

Terraform is a fantastic companion to AWS and especially if you're testing new things and labbing a project as it is incredibly easy to create a new resource and then destroy everything afterwards.


![Github Copilot Demo](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779544836/GO_2zfkke.gif align="left")

However, if you're a developer with limited or no infrastructure experience, let me suggest an alternative to you: Pulumi.

Unlike Terraform, Pulumi doesn't have use it's own markup language, but instead extends the programming language you're already working in, such as Python, Go, Typescript, C# or Java! Allowing you to define your infrastructure in a language you're already familiar with.

Pulumi has a number of other extremely powerful tooling as well, allowing you to more easily deal with expressions, and logic, not directly possibly in Terraform.

For a lot of developers, it is much easier to get started with Pulumi over Terraform, so it's worth looking into. However, as Pulumi is a newer tool, it is not as well-known as Terraform, but it **uses terraform providers** meaning it has the same support for infrastructure as Terraform.

![Artboard 1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779735768/XVGeKcyUA.png align="left")

**Cost: FREE!** from [https://www.pulumi.com/](https://www.pulumi.com/) and [https://www.terraform.io/](https://www.terraform.io/)
(Terraform has some paid cloud functionality for working with enterprise functionality)

## Alfred
Ok - on to some very Mac specific apps I use, that are incredible. First of all: Alfred.

![](https://www.alfredapp.com/media/pages/home/search.jpg)


I first used Alfred on my very first MacBook, in 2006 - back when Spotlight on the Mac in MacOS X 10.4 was awful and took multiple minutes to launch an application. However, once 10.6 and 10.7 rolled around, Spotlight got to a point where I really didn't feel I needed to install Alfred anymore, since I was just using it as a fancy app launcher anyway. 

That was a mistake.

I started using Alfred again this year, after not having used it for 10 years, and boy has it been great! Yes - Alfred can function as a fancy app launcher, but that's not why you want it. You want Alfred for all the small functionality here and there you can do. Like moving a file from one folder to another with two presses, or searching through Apple Music instantly from your keyboard and without ever leaving your current application. 


![alfred.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779627489/53L7LLhW2.png align="left")

Alfred is incredibly powerful in ways you could probably never imagine. It's FREE except for some functionality, so it's well worth you trying it out!

**Cost: FREE** (some paid features) from 

## Snippetslab
This is a small useful utility that I have yet to utilize to it's full potential, but it's a very lightweight and useful application for storing snippets of code for reusability. 


![snippetslab.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779642109/aV8LG0EGh.png align="left")

It has built in integration with Github Gists, allowing you to instantly publish and share code with others, as well as syntax highlighting for a ton of languages. 

However, what makes Snippetslab most useful to me, is the incredible Alfred integration! With a simple CMD + Space, then type in `snip <search>` followed by ENTER to instantly insert a snippet.


![snippetdemo.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1654779651127/Nz9FUUOPd.gif align="left")

There are tons of other snippet managers around, however what makes this one great, is the fantastic Alfred integration.

**Cost: $9.99** from [https://www.renfei.org/snippets-lab/](https://www.renfei.org/snippets-lab/) or on [SetApp](https://setapp.com/)

### Dropshare
There are again plenty of uploading tools available, but Dropshare has been my favorite for a while. It's a simple menubar application that allows you to easily upload screenshots, documents, videos, or what you want to a myriad of destinations, including AWS S3! 

![](https://dropshare.app/assets/img/product/popup.png)

It's also highly customizable, including giving you the ability to automatically shorten URLs to a custom domain. 

**Cost: $24.99** from [https://dropshare.app](https://dropshare.app) or on [SetApp](https://setapp.com/)

## Conclusion
These are just a few of my every day applications that I use. I have a plan on expanding this series with a few more posts with more of the really useful Mac applications that I've found over the years. 