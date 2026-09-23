### Ciao, mi chiamo Gianfranco 👋

> Tinkerer ✦ Software Developer ✦ Dog father 🐶

- ☀️ I'm living in sunny Madrid, Spain 🌞
- Tech Stack: `Next.js | TypeScript | React | Python | Node.js | PostgreSQL | MongoDB | AWS | Vercel | Generative AI (text and audio) | Agentic systems`
- Blog:
  - <https://gian.cool>
- Socials:
  <!-- - <img src="https://cdn.jsdelivr.net/gh/gianpaj/gianpaj@1.6/youtube.svg" style="height: 1rem"> [YouTube](https://www.youtube.com/@gianpaj) -->
  - <img src="https://cdn.jsdelivr.net/gh/gianpaj/gianpaj@1.6/twitter-x.svg" style="height: 1rem"> [Twitter/X](https://x.com/gianpaj)
  - <img src="https://cdn.jsdelivr.net/gh/gianpaj/gianpaj@1.6/linkedin.svg" style="height: 1rem"> [LinkedIn](https://linkedin.com/in/gianpaj)
  - <img src="https://cdn.jsdelivr.net/gh/gianpaj/gianpaj@1.6/goodreads.svg" style="height: 1rem"> [Goodreads](https://www.goodreads.com/user/show/10470860-gianfranco)
- ⚡ Fun fact:
  - My first computer was a Compaq Presario in 1995 in Ecuador – I was 8 years old. It came with Windows 3.1, but you could install Windows '95. I was amazed by the possibilities of computers and the internet (dial-up). I still cherish those memories 🕹️😊

## Businesses

- ☎️ [HolaBrisa](https://holabrisa.com) - a thoughtful text and voice AI receptionist that gives every hotel guest an immediate, personal welcome.
- 🎙️ [SexyVoice.ai](https://sexyvoice.ai) ([repo](https://github.com/gianpaj/sexyvoice)) - Text to Speech and Voice cloning platform. Perfect for content creators, developers, and storytellers

## Onova 🇺🇦

[Onova.co](https://www.onova.co/) was our startup in Ukraine, active until September 2019. It was a mobile marketplace where people bought and sold clothes and accessories, built their own brand and grew an audience of buyers. Payments went through UAPay and were held in escrow until the buyer collected the package. We also launched Drop, a spin-off where sellers scheduled a batch of items to go on sale at a set date and time.

The iOS and Android apps were built with React Native, and the web apps with React and TypeScript. A set of small Node.js services ran on a single AWS Lightsail instance and shared one MongoDB database:

- `server.data`: the Express REST API behind the apps and the web app
- `server.push`: push notifications through Firebase Cloud Messaging
- `server.chat`: buyer–seller chat on Pusher ChatKit, with auth and polling for notifications
- Agenda: a MongoDB-backed job scheduler for order deadlines and notifications
- Forest Admin: the back office
- A Google AutoML image classifier for tagging items listed for sale

<details><summary>Details</summary>
<p>




```mermaid
flowchart LR
  subgraph lightsail["AWS Lightsail instance"]
    webapp(["webapp<br/>:3000"])
    data(["server.data<br/>:4040"])
    agenda{"Agenda job scheduler"}
    push(["server.push"])
    chatPoll(["server.chat<br/>push notif. polling"])
    chatAuth(["server.chat<br/>Pusher auth REST API<br/>:8142"])
    mongo[("MongoDB")]
  end

fcm["Firebase Cloud Messaging"]
chatkit["Pusher ChatKit"]
backup[("MongoDB cloud backup")]

webapp --> data
data <--> mongo
data <--> agenda
agenda <--> mongo
agenda <--> push
agenda <--> chatPoll
push --> mongo
push --> fcm
chatPoll --> chatkit
chatAuth <--> chatkit
mongo --> backup
```


</p>
</details> 

## Side projects 👨‍💻

- 🔥 [Walnut.tv](https://walnut.tv) ([repo](https://github.com/gianpaj/walnut.tv)) - Discover trending videos from Reddit and curated YouTube channels
- 📞 [agentcaller.io](https://agentcaller.io) ([repo](https://github.com/gianpaj/agentcaller-io)) - AgentCaller.io lets your AI agent (e.g. OpenClaw) call businesses — booking a restaurant, etc.
- 🎯 [3dvibegame.com](https://3dvibegame.com) ([repo](https://github.com/gianpaj/3dvibegame)) - 3d multiplayer game where you can create any 3d object, move around and manipulate objects with text. My first game
- ⚽️ [football_analysis_yolo](https://github.com/gianpaj/football_analysis_yolo) - A Machine Learning project using YOLO and OpenCV to automate soccer match analysis, player tracking, and performance insights from live or pre-recorded video footage.

<!-- - 🤖 [Call Me Now Please app](https://github.com/gianpaj/call-me-please) - A mobile application that lets users schedule AI-powered voice calls. -->
<!-- - [CoverLetter.work](https://coverletter.work) - Get a tailored cover letter in seconds, for FREE! 🤖 -->

<!-- - **CoMaking Malaga** - An upcoming Hackerspace / Makerspace for meeting new people and making cool stuff. -->

```

```
