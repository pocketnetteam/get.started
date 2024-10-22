<!--
-  [x] Update readme.md with what this repo is all about
-  [ ] Share this information with stakeholders
-->

<div align="center">
  <img src="bastyon-logo-256x256.png" alt="bastyon logo">
</div>

<div align="center">

# Get Started with Bastyon

</div>

Hello and welcome to Bastyon! We're excited to have you here and hope this project will excite you as much as it excites us!

Bastyon is on a mission to democratize how people communicate. Today, most communication is centralized. It's not an overstatement to say that anyone can get unplugged from any platform for any reason, forcing them to lose their ability to communicate with loved ones, create content, or access their own data. Bastyon is changing this.

>**Vision:**
Bastyon aims to create a resilient, decentralized ecosystem that empowers individuals with unrestricted access to communication, information, and personal data management. Our vision is to build a platform that stands strong against censorship and ensures user sovereignty in the digital realm.

This repo is meant to be an entry point into the project. It has descriptions and overview of other repos and how they are all connected.

If you know what you want to help with, you could jump straight to the [How To...?](#how-to) section.

> **Note:** But before you jump in, please make sure you check out [Contribution Guide](contribution.md). 

## 📝 Bastyon Architectural Overview

[Coming Soon - Detailed architectural documentation and diagrams will be added here]

The application flow architecture largerly depends on the content, users are interacting with.

### Text Content

```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser-based Bastyon App
    participant P as Proxy Server (SSL)
    participant N1 as Initial Blockchain Node
    participant NN as Other Blockchain Nodes
    
    rect rgb(245, 245, 245)
        note right of U: End User
    end
    rect rgb(230, 240, 250)
        note right of B: Client Layer
    end
    rect rgb(255, 245, 230)
        note right of N1: Blockchain Layer
    end
    rect rgb(255, 245, 230)
        note right of NN: Blockchain Layer
    end

    U->>+B: Creates text content
    B->>+P: Sends data over HTTPS
    Note over P: Process request
    P->>+N1: Forward processed request
    
    rect rgb(240, 248, 255)
        Note right of N1: Consensus Process
        N1->>NN: Broadcast content for validation
        activate NN
        NN->>N1: Return validation results
        deactivate NN
        Note over N1,NN: Content validated across network
    end

    N1->>-P: Confirm validation & receipt
    P->>-B: Return confirmation
    B->>-U: Display confirmation
```

### Images and Videos


### Bastyon Chat


## 🏗️ Bastyon Platform Structure

The Bastyon Platform consists of these main blocks:

- [Roadmap](#roadmap)
- [Documentation](#documentation)
- [Bastyon User Interfaces](#bastyon-user-interfaces)
- [Bastyon Protocols, Network, and Node Software](#bastyon-protocols-network-and-node-software)
- [Bastyon Integrations](#bastyon-integrations)

Below are the repositories for each respective platform component:

### 🗂️ Bastyon Project Overview

`This.repo`

An entry point that helps newcomers navigate the Bastyon project.

### 🛣️ Roadmap

This repo is used for submission, tracking, and discussion of new proposals. The conversations in this repo remain active until proposals either get approved (with a willing contributor) or rejected. In both cases, the natural end state for a proposal is to be archived with a decision note.

[https://github.com/pocketnetteam/roadmap](https://github.com/pocketnetteam/roadmap)

### ✍️ Documentation

This repo contains documentation files that power the Bastyon documentation site. They are expected to be evergreen and maintained by everyone, including developers who make observable changes that require documentation updates.

[https://github.com/pocketnetteam/documentation](https://github.com/pocketnetteam/documentation)

### 🎨 Bastyon User Interfaces

Bastyon Graphical User Interfaces include Mobile Apps, Desktop and Web Browser Apps across several repositories.

#### 🛠️ Bastyon Application UI

The `pocketnet.gui` repo holds the codebase for end-user applications. You can make changes and build and run locally for Desktop, Browser app, and Mobile Apps.

[https://github.com/pocketnetteam/pocketnet.gui](https://github.com/pocketnetteam/pocketnet.gui)

#### 🗨️ Bastyon Messenger UI

The messenger component of Bastyon, enabling secure, decentralized communication between users.

[https://github.com/pocketnetteam/bastyon-chat](https://github.com/pocketnetteam/bastyon-chat)

#### 📞💻 Bastyon Calls UI

The video calling and conferencing interface, providing peer-to-peer communication capabilities.

[https://github.com/pocketnetteam/bastyon-calls](https://github.com/pocketnetteam/bastyon-video)

#### 🔄 Barteron GUI

This repo contains the User Interface for Barteron - a decentralized marketplace.

https://github.com/pocketnetteam/barteron.gui

### 🖧🔒 Bastyon Protocols, Network, and Node Software

Back-End block (Node Software, Blockchain Explorer, Bastyon Platform API)

Core Protocol and Network Implementation:
[https://github.com/pocketnetteam/pocketnet.core](https://github.com/pocketnetteam/pocketnet.core)

Blockchain Explorer Interface:
[https://github.com/pocketnetteam/pocketnet.explorer](https://github.com/pocketnetteam/pocketnet.explorer)

Platform API Services:
[https://github.com/pocketnetteam/pocketnet-proxy-api](https://github.com/pocketnetteam/pocketnet-proxy-api)

Network Control and Management:
[https://github.com/pocketnetteam/pocketnet.control](https://github.com/pocketnetteam/pocketnet.control)

### 🧩 Bastyon Integrations

#### 🎬 Bastyon Video Implementation
This repo is a fork of PeerTube, a free, decentralized and federated video platform developed as an alternative to other platforms that centralize our data and attention, such as YouTube, Dailymotion or Vimeo. 🎬

It contains the integration code with Bastyon and the PeerTube code itself.

[https://github.com/pocketnetteam/bastyon-video](https://github.com/pocketnetteam/bastyon-video)


## How To

[Coming Soon - ]...

### How Do I contribute to the Bastyon Application Development?
### How Do I contribute to the Bastyon Node Development?
### How Do I contribute to Bastyon in Other Ways?
### How Do I contribute to the Bastyon Documentation?
### How Do I contribute to the Bastyon Documentation Translation?
### How Do I contribute to the Bastyon Chat Messenger?

