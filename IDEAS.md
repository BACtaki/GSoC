Google Summer Of Code Matrix Ideas list
=======================================

Google Summer Of Code Matrix Ideas list
=======================================

### Matrixcraft

There are many minecraft clones available e.g. [https://github.com/fogleman/Minecraft](https://github.com/fogleman/Minecraft) - but none of these are networked in any way. The aim of this project is to design and implement a protocol which can allow multiple minecraft players to play together, through Matrix.

**Expected results**: Able to have 2+ players building structures together

**Difficulty**: Hard. Getting sensible chunking algorithms for rooms is Hard. There is huge scope to build on this both feature wise (e.g. PvP, monster AI) and protocol wise (reliability, masking latency hiccups, etc)

**Knowledge pre-req**: Python (assuming fogleman/Minecraft is used as a base)

**Potential mentor**: Kegan Dougal
   

### Tumblr gateway
Tumblr has a public API which you can use to extract and submit posts. It would be great if you could join a room alias like #tumblr_username and see a complete feed of their posts in Matrix, optionally responding to them from any Matrix client. This can be done use the Application Services API in Matrix.

**Expected results**: Able to join a room alias for any tumblr user and see a feed (even if it's just text) of their posts. Bonus points for gifs/videos/etc, and the ability to post comments on the posts and/or reblog.

**Difficulty**: Moderate.

**Knowledge pre-req**: Good knowledge of HTTP/REST APIs in general.

**Potential mentor**: Kegan Dougal
    
### Etherpad clone
  Etherpad allows real-time text collaboration and we use it frequently internally. The aim of this project is to recreate Etherpad using Matrix.

**Expected results**: Able to have at least 10 people collaborating (typing) on a single document, and to have the document in sync across all people.

**Difficulty**: Hard. Made harder by needing to storing and synchronising document snapshots efficiently

**Knowledge pre-req**: Python/Twisted for server-side extensions; Client-side development (Javascript/HTML/CSS or Android or iOS), HTTP/JSON APIs, basic awareness of Operational Transform theory

**Potential mentor**: Kegan Dougal

### Matrix Powered Microblogging
Matrix-powered, open and federated microblogging platform.

**Expected results**: User can log in, choose some users to follow, get an aggregated feed of 'tweets' from users they follow, and post 'tweets'.  Messages should be sendable and consumable by both generic Matrix clients as well as the microblog-specific optimised user experience.

**Difficulty**: Moderate

**Knowledge pre-req**: HTML, CSS, Javascript

**Potential mentor**: David Baker

### Location based Chat
A mobile app that shows you a list of chat rooms "around you". People could create chat rooms fixed in one place (a Café could have a room, for example) or you could create a chat room that follows you around as you walk around using the app.

**Expected Results**: An app and backend where you can log in, create a room, find and join rooms near you and chat.

**Difficulty**: Moderate

**Knowledge pre-req**: Android/iOS, probably python and SQL for the backend.

**Potential mentor**: David Baker (iOS), Kegan Dougal (Android)

### HTML Embeddable Matrix Chat Rooms
A Matrix-powered engine for comments boxes.

**Expected Results**: A javascript/HTML SDK of some form that a website author can download, embed and skin into their website to make comments work with minimal work to integrate. Could require user to log in with a matrix account to post (so your Matrix account would let you post comments on any website which used this).  VoIP and Video calling support would be an added bonus.

**Difficulty**: Easy/Moderate

**Knowledge pre-req**: HTML, Javascript

**Potential mentor**: David Baker

### Clustered Homeservers
Whilst Matrix itself is a global eventually consistent database, the current server implementations have no horizontal scaling or high availability per homeserver node.  As a result, it's impossible for a single homeserver to scale beyond a single core currently.  This project would extend the Synapse (Python) or Pallium (Golang) homeserver implementations to support simple clustering by letting the multiple instances run concurrently, sharing distributed state over the network such that clients can connect to arbitrary nodes within the cluster.

**Expected Results**: Clients can connect per-request to one of many active/active nodes in the same homeserver cluster, and experience a consistent view of the homeserver state.  Nodes may fail in the cluster without impacting client experience.

**Difficulty**: Moderate/Hard

**Knowledge pre-req**: Python/Twisted or Golang.  Experience of clustering strategies a plus.

**Potential mentor**: Erik Johnson

