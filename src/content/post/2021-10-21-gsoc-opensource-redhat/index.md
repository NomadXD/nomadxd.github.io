---
title: "Our journey to open source during Google Summer of Code"
description: "Explore a personal journey through Google Summer of Code with Red Hat. Learn about open source contributions, project experiences, and insights gained during this unique opportunity."
publishDate: "23 October 2021"
updatedDate: "23 October 2021"
tags: ["envoy"]
---

:::note
This article was originally published on [Opensource.com](https://opensource.com/) and co-authored by Rahul Anand and Lahiru De Silva (myself).

Read the original article here: [Original Article on Opensource.com](https://opensource.com/article/21/10/google-summer-code)
:::

## How we made it to GSoC and what we learned about open source code.

Every year, Google organizes a program called Summer of Code (GSoC). Students worldwide can write open source code under an open source mentoring organization and get paid to do so! You get to work on cool open source projects, network with talented engineers, and get paid during the summer break. How cool is that!?

In this blog post, we'll guide you through our GSoC experience and give you tips and tricks so that you can have a fantastic experience like we did. We'll also share our differing perspectives based on our different interests and challenges.

## About us

**Rahul**: My name is Rahul Anand, and, at the time of writing this, I am in my senior year of college, majoring in computer engineering at Thapar University, Patiala, India. My interest is in distributed computing because it's one of the significant areas allowing scalability of applications worldwide. Computer vision is sprinkled on top just because AI will take over the world.

**Lahiru**: I am Lahiru Udayanga, currently a final-year undergraduate at the Department of Computer Science and Engineering, University of Moratuwa, Sri Lanka. My main focus areas in computer science are distributed systems, API gateways, proxies, and cloud-native technologies.

## Choosing the proper organization and project

The first and the most crucial decision you'll make during this journey is choosing the most suitable organization and the project you want to contribute to. This decision will heavily influence your experience, so be very diligent here. Don't worry—at the end of this section, we have listed factors you should consider for this stage.

We both decided to apply for the same project: 3scale-envoy proxy authorization cache. However, we each had a slightly different thought process behind choosing this project.

**Rahul**: I discussed the options with a senior who participated in GSoC'20 under the JBoss umbrella and described his experience as very enriching. That's how I decided which organization I wanted to participate with. I advise juniors to focus on one good organization and start exploring different projects in it. Regarding project choice, a mix of various factors influenced me. Most important was my first interaction with my mentor, Alejandro Martinez Ruiz. I asked him numerous questions, and he was always ready with detailed replies to all of them. (Tip: Be concise in your questions and respect your mentor's time.) I also wanted to work with distributed systems, learn Rust, and build a project from the ground up.

**Lahiru**: The main reason I applied to this project is my deep interest in middleware, API gateways, and proxies. Also, I had some previous experience with envoy proxy from my internship project. I believe that envoy proxy will revolutionize the domain of proxies and that there will be a lot of opportunities for envoy-proxy-related technologies. Like Rahul, my first interaction with Alex and the conversations we had before the proposal-submitting phase also had a significant impact on my decision to apply.

## Tips for this period:

- If you find any technology cool or want to learn more about it, look for those projects.
- Ask seniors about their experiences with different organizations.
- Consider the future of this project: do you see a future for this area of research?
- If you have a good initial connection with a potential mentor, continue to build rapport.

## Developing the proposal

After deciding on which project we wanted to work on, we put our research caps on and started digging for any information related to the problem and possible solutions. During this phase, we were constantly interacting with our mentor about any questions, resources, and solution designs that we were thinking of going forward with independently. It's best to come as close as possible to the actual outcome and document everything in a separate document for your reference, because it will help immensely during your proposal-creation phase.

After researching for about one to two months, as we neared the opening of proposal submissions, our mentor asked us to start putting everything into a separate Google Doc to be presented as a proposal in front of a committee. It was time to make friends with Shakespeare and type hard work into a document that would change our lives forever!

Jokes aside, it's imperative to have this document look presentable, with excellent diagrams. We used and recommend draw.io (now diagrams.net), an open source diagramming software. Remember that no one can write a perfect document the first time through, and have a few review cycles with your mentor to get their feedback. You can look at our proposals for an example.

[Rahul's Proposal](https://drive.google.com/file/d/1R7uwJd6kohBC9xHzUFjmzsCWA6CoSesN/view)

[Lahiru's Proposal](https://docs.google.com/document/d/1WpW-UUSwgVVvSFZvJaIpXNZB0DRUSQGDFOJCoM88h9k/edit?usp=sharing)

We remember the day we clicked the submit button on the GSoC dashboard—it was raining fire from the sky in the Indian subcontinent. With our fates now in the hands of the JBoss organization and the 3scale team at Red Hat, we waited until that fateful day when our parents awoke at 2AM to newly minted adults screaming at top of their lungs, "GSOC BABY!!"

## Learning by doing

The next day, we received our first email with onboarding information, each other's proposal to refer to, and an invitation to a call between Alex and us. During the first call, we learned about each other, our respective cultures, and the 3scale team, and we were tasked with creating a shared document with a realistic timeline. Since this project was massive compared to other GSoC projects and we found clashing obligations in the future, we decided to start working before the coding period began. We were able to finalize a design with proofs-of-concept (POCs) showcasing certain guarantees required by our use cases and an initialized GitHub repository before the official start.

To progress faster, we separated our concerns. Rahul took the responsibility of the Cache-Filter and Lahiru of the Singleton-Service, and with a standard interface finalized during an online meeting. To make sure that we were on the same page and to find blockers early on, Alex scheduled two meetings: weekly syncs for progress, blockers, possible design changes, and POCs, and biweekly syncs for just talking about anything other than work. He also asked us to create weekly reports in a separate Google Doc to be shared with other members of the community. We used these reports to give updates and receive advice or any heads-ups. Both of us struggled during this stage at different places.

**Rahul**: At the start, I struggled a bit with following a standard workflow and using tools (including Git!) because I wanted to move fast. In hindsight, that helped us avoid future pains, so I am glad I learned them early on. The best advice I got from Alex was that it was our project, and we were free to make final decisions after his feedback. That gave me a sense of ownership, and I started experimenting more, creating more POCs, and bending specs to work with us. This change in attitude allowed me to implement features like visible logs and unique callouts that made integration testing easier and increased performance.

**Lahiru**: For me, the most irritating thing at the beginning was the steeper learning curve of the Rust programming language. When I started programming in Rust, I was mostly yelling at the compiler instead of writing code. But a few weeks later, we were slowly becoming friends. (I think the Rust compiler is more like an overprotective nanny. It has no interest in being your friend, but it will do everything it can to stop you from hurting yourself.) Also, there are vast differences among the Rust code written by a beginner, an intermediate, and an expert. These differences exist in other programming languages, like Java, Golang, and C++, but not to the same extent. So one of the challenges I had was implementing not only something that works but something that works in the most Rustic way possible.

## What we learned

If you want a list of things we learned that you can learn too if you participate in the Summer of Code, here it is:

- Collaboration: How to interact with the open source community, how to give context to a person new to your work
- Best practices for developing software: How to structure PRs and commits, how to set up and write integration or unit tests
- New technologies: Rust, Golang, Proxy-WASM, Envoy, etc.
- Soft skills: How to interact with senior engineers, how to introduce yourself
- Distributed computing theory in action and problem-solving skills in general

Google Summer of Code 2021 was an enriching experience for both of us. We got to interact with great engineers like Piotr Sikora (some say CPP is a language from hell, but he turns it into beautiful prose), Takeshi Yoneda (our savior when we needed it the most), David Ortiz (the myth, the legend, the co-creator of Limitador), and (obviously) Alex Martinez, along with the whole 3scale team. Without these people, we don't think we could have made it to the final stages and be listed on the GSoC website.
