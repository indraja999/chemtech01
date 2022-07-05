#Service-oriented architecture (SOA):
(Excerpt from [Stevey's Google Platform rant](https://gist.github.com/chitchcock/1281611))
- All teams will henceforth expose their data and functionality through service interfaces.

- Teams must communicate with each other through these interfaces.

- There will be no other form of interprocess communication allowed: no direct linking, no direct reads of another team's data store, no shared-memory model, no back-doors whatsoever. The only communication allowed is via service interface calls over the network.

- It doesn't matter what technology they use. HTTP, Corba, Pubsub, custom protocols -- doesn't matter. Bezos doesn't care.

- All service interfaces, without exception, must be designed from the ground up to be externalizable. That is to say, the team must plan and design to be able to expose the interface to developers in the outside world. No exceptions.

##Learnings to include in this transition:
- pager escalation gets way harder, because a ticket might bounce through 20 service calls before the real owner is identified. If each bounce goes through a team with a 15-minute response time, it can be hours before the right team finally finds out, unless you build a lot of scaffolding and metrics and reporting.

- every single one of your peer teams suddenly becomes a potential DOS attacker. Nobody can make any real forward progress until very serious quotas and throttling are put in place in every single service.

- monitoring and QA are the same thing. You'd never think so until you try doing a big SOA. But when your service says "oh yes, I'm fine", it may well be the case that the only thing still functioning in the server is the little component that knows how to say "I'm fine, roger roger, over and out" in a cheery droid voice. In order to tell whether the service is actually responding, you have to make individual calls. The problem continues recursively until your monitoring is doing comprehensive semantics checking of your entire range of services and data, at which point it's indistinguishable from automated QA. So they're a continuum.

- if you have hundreds of services, and your code MUST communicate with other groups' code via these services, then you won't be able to find any of them without a service-discovery mechanism. And you can't have that without a service registration mechanism, which itself is another service. So Amazon has a universal service registry where you can find out reflectively (programmatically) about every service, what its APIs are, and also whether it is currently up, and where.

- debugging problems with someone else's code gets a LOT harder, and is basically impossible unless there is a universal standard way to run every service in a debuggable sandbox.

