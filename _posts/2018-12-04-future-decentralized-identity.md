--- 
title: The Future of Decentralized Identity
published: false
---


# TLDR;

Hyperledger Indy is more than just a promising software package. It has deep roots within the internet identity standards community. Indy is a culmination of, and inter-related with, the work of numerous independent parties sharing a passion for the privacy-focused design of an Internet-wide identity layer. Support for this movement also comes from the blockchain community, government bodies, the United Nations, and the GDPR.

# Introduction

In May of 2017, the Hyperledger Foundation [received](https://www.hyperledger.org/blog/2017/05/02/hyperledger-welcomes-project-indy) the Sovrin codebase into its family of open-source tools and frameworks, dubbing it *Indy*:

> We’re excited to announce Indy, a new Hyperledger project for supporting independent identity on distributed ledgers. Indy provides tools, libraries, and reusable components for providing digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silo. -Phillip J. Windley, Ph.D., Chair, Sovrin Foundation

The problem with identity on the internet is that we are required to continually give away our personal information to engage with online services. That information ends up in data-silos that make attractive targets for hackers. Moreover, these services consistently collect more information than necessary for a given interaction.

It doesn’t require effort to realize that identity on the internet is broken, but why Indy? To know why I think Indy is a crucial component in replacing our current identity “solutions” let’s take a stroll through history:

![](https://i.imgur.com/Og8Qe0v.png)

## The IIW and the Data-Silo Paradox

In 2005, [Kaliya Young](https://identitywoman.net/), [Phil Windley](http://windley.com/), [Drummond Reed](https://evernym.com/), and [Doc Searls](https://twitter.com/dsearls) hosted [the first](https://identitywoman.net/announcing-the-internet-identity-workshop-iiw2005/) Internet Identity Workshop (IIW) to discuss proposals for internet-wide identity services. Since then, IIW has met bi-annually, supporting the development of identity standards such as [OpenID](http://wiki.openid.net/w/page/12995215/OpenID%20Authentication%202-1), [OAuth](https://en.wikipedia.org/wiki/OAuth), and [FIDO](https://fidoalliance.org/).

The IIW has a long history of working to protect user privacy while enabling organizations to verify identities with enterprise, entertainment, and State grade security assurances.

IIW participants began the effort towards creating a truly “[user centric identity](https://www.networkworld.com/article/2304596/access-control/what-is--user-centric--identity-.html),” in contrast to the dominant identity solutions who’s primary focus has been fulfilling the needs of the enterprise. However, these pioneers of decentralized identity have long struggled against the “identity silo paradox.” While the [identerati](https://www.zdnet.com/article/the-identity-silo-paradox/) continually work on solutions for breaking up identity data silos, the enterprise has had a strong financial incentive to keep them.

![](https://i.imgur.com/HUUYAfc.png)

# The Credentials Community Group of the W3C

The Credentials Community Group [was proposed](https://www.w3.org/community/credentials/charter-20140808/) by Manu Sporny of [Digital Bazaar](https://digitalbazaar.com/) (8/14):

> to forge a path for a secure, decentralized system of credentials that would empower both individual people and organizations on the Web to store, transmit, and receive digitally verifiable proof of qualifications and achievements.> The group was ratified in September of the same year, hosted by the World Wide Web Consortium (W3C), and began exploring the creation of common standards for decentralized identity.

![https://miro.medium.com/max/840/0*EnTfiPI0kteCi7G3.jpg](https://miro.medium.com/max/840/0*EnTfiPI0kteCi7G3.jpg)

## Blockchain and the UN Sustainable Development Goals

In September 2015, The United Nations agreed upon it’s [Agenda for Sustainable Development](https://sustainabledevelopment.un.org/post2015/transformingourworld) seeking to achieve “sustainable development in its three dimensions — economic, social and environmental — in a balanced and integrated manner.” This agenda included 17 Sustainable Development Goals (SDG), divided into 169 components.

> **Goal 16.9 By 2030, provide legal identity for all, including birth registration.**\n
> Providing legal identity to all helps ensure humanitarian aid is provided to those it is intended for. Furthermore, without legal identification, individuals are unable to access government services. Those individuals face even more of a challenge who don’t have a stable government to provide identification or any other services. A lot of energy towards blockchain identity solutions has come from the UN.

![https://miro.medium.com/max/636/0*x9RlfasJDJV25OXV.png](https://miro.medium.com/max/636/0*x9RlfasJDJV25OXV.png)

## Rebooting the Web of Trust

A few months after the UN released its SDGs, the first Rebooting the Web of Trust (RWoT) workshop [was held](http://www.weboftrust.info/event-2015-sf) attracting the likes of Vitalik Buterin, Peter Todd, Gregory Maxwell, Joel Dietz, and Jon Callas. Founded by Christopher Allen, the bi-annual RWoT [workshops are](http://www.kevinmarks.com/decentralweb2016-06-09.html) “like a hackathon for white papers” focused on creating next-gen web-of-trust based identity systems. Among the papers produced at that initial RWoT workshop was [Decentralized Public Key Infrastructure](https://github.com/WebOfTrustInfo/rebooting-the-web-of-trust/blob/master/final-documents/dpki.pdf), which is an essential component to the decentralized identity stack.

> The Web of Trust is a buzzword for a new model of decentralized self-sovereign identity. It’s a phrase that dates back almost twenty-five years, the classic definition derives from PGP […] the vibrant blockchain community is also drawing new attention to the concept we aim to reboot it.- Rebranding the Web of Trust

![https://miro.medium.com/max/714/0*upiI4rzmUtbXjJ7h.png](https://miro.medium.com/max/714/0*upiI4rzmUtbXjJ7h.png)

## ID2020 Summit

In April, of 2016, **Evernym** produced its [initial identity white paper](https://www.evernym.com/wp-content/uploads/2017/02/Identity-System-Essentials.pdf) describing the essential characteristics of Sovrin, the identity protocol they were creating.

May 20, 2016 [the first](https://press.pwc.com/News-releases/id2020-to-kick-start-digital-identity-summit-at-un-with-pwc-support./s/9fe11be5-cbd8-486b-b4d2-d798f486d0f2) ID2020 Summit for Digital Identity was held in alignment with the UN’s Sustainable Development Goals. In conjunction with, and immediately following the summit was [the second](https://www.eventbrite.com/e/id-2020-design-workshop-tickets-24611080404?ref=estw) RWoT design workshop. Evident by the [whitepapers](https://github.com/WebOfTrustInfo/ID2020DesignWorkshop/blob/master/topics-and-advance-readings/README.md) submitted, both Self Sovereign Identity and specifications for a decentralized identifier were on the minds those attending.

> 1.1 Billion people live without an officially recognized identity — This lack of recognized identification deprives them of protection, access to services, and basic rights. ID2020 is a public-private partnership dedicated to solving the challenges of identity for these people through technology. — id2020.org

> The original DID Whitepaper submitted to this design workshop aligns with the goals of the W3C Credentials Community Group: *“Decentralized Identifiers (DID) stored in a permissioned blockchain enable principals to directly control their own identities with cryptographic proofs and secure, addressable network endpoints.” —* [DID Whitepaper](https://github.com/WebOfTrustInfo/ID2020DesignWorkshop/blob/master/topics-and-advance-readings/DID-Whitepaper.md)

![https://miro.medium.com/max/716/1*PULVfmnQDsnqAHxzHXU2Kw.png](https://miro.medium.com/max/716/1*PULVfmnQDsnqAHxzHXU2Kw.png)

[Identity of the Blockchain: Perils and Promise](https://www.slideshare.net/ChristopherA/identity-of-the-blockchain-perils-and-promise)

### Self Sovereign Identity (SSI)

What was originally known as *user-centric* identity now sails under the banner *Self Sovereign Identity*, since the publication of Christopher Allen’s seminal work, The Path to Self-Sovereign Identity. Among the papers submitted to the ID2020/RWoT workshop, it details the history of internet identity standards, examines the current systems in place for identification. That paper outlines principles for SSI, made available for public collaboration [on GitHub](https://github.com/WebOfTrustInfo/ID2020DesignWorkshop/blob/master/topics-and-advance-readings/the-path-to-self-sovereign-identity.md):

## The 10 Principles of Self-Sovereign Identity

1. **Existence**: Users have an independent existence — they are never wholly digital.
2. **Control**: Users must have control over their own identities, celebrity, or privacy how they prefer.
3. **Access**: People must have access to their own data — no gatekeepers, nothing hidden.
4. **Transparency**: Systems and algorithms must be open and transparent.
5. **Persistence**: Identities should last for as long as the user wishes
6. **Portability**: Information and services about identity must be transportable by the user.
7. **Interoperability**: Identities should be as widely usable as possible, across borders and platforms
8. **Consent**: People must freely agree to how their identity information will be used
9. **Minimization**: The amount of data disclosed regarding an identity owner should be as little as possible for any interaction.
10. **Protection**: The rights of individual people must be protected against the powerful

Self-sovereign identity takes user-centric design philosophies to their logical conclusions, placing the user in charge of the administration of their own identity. An identity useful in multiple locations, and independent of the services which rely on identification for our use. This identity should be designed to protect against “human rights abuses by the powerful, supporting the rights of the individual.”

![https://miro.medium.com/max/752/0*uVmDqgtCxuoeylQ4.png](https://miro.medium.com/max/752/0*uVmDqgtCxuoeylQ4.png)

## Evernym Donates the Sovrin Codebase

For the Sovrin (now called Indy) code to power a truly decentralized global identity infrastructure, Evernym knew they must give it away. That [September](http://www.windley.com/archives/2016/09/announcing_the_sovrin_foundation.shtml) the Sovrin Foundation was announced: a private-sector, international non-profit established to govern a global public utility for self-sovereign identity.

The Sovrin ledger is operated by Stewards, trusted organizations within the ecosystem who have agreed to abide by the requirements in the Sovrin Trust Framework and operate the nodes maintaining an instance of the Sovrin ledger. Stewards also accept or reject changes to the open source code, which is now maintained by the Hyperledger Foundation. There are currently over 40 Sovrin Stewards including [Cisco](https://www.cisco.com/), [IBM](https://www.ibm.com/blogs/blockchain/2018/08/ibm-blockchain-trusted-identity-sovrin-steward-closed-beta-offering/), [Danube Tech](https://danubetech.com/), [Digital Bazaar](https://digitalbazaar.com/), [CULedger](http://culedger.com/), [iRespond](http://irespond.org/), [KYC Chain](https://kyc-chain.com/) [Tykn](https://tykn.tech/), [Aalto University](http://www.aalto.fi/), and [Global Consent](http://www.consent.global/).

Sovrin is a *public-permissioned* ledger, meaning anyone can read or transact upon it, but only Stewards can write upon it. Since the ledger is entirely public, no personally identifiable information is written on it. The ledger is designed to store DIDs, the decentralized identifiers under development by the W3C’s Credentials Community Group in conjunction with RWoT.

The ledger contains only public DIDs recorded by public institutions, accompanied by public keys, allowing anyone to verify credentials those institutions have attested to. Private DIDs are created and kept off-ledger, enabling identity owners to privately engage with other parties peer-to-peer, selectively disclosing information, and collecting credentials attested to by public parties.

## Decentralized Identity Foundation

Microsoft, uPort, Gem, Evernym, Blockstack, and Tierion [announced the formation](https://www.ethnews.com/decentralized-identity-foundation-announces-formation-at-consensus-2017)  of the Decentralized Identity Foundation (DIF), at Consensus 2017 to create a universal network for digital identification. The DIF supports the exploration of emerging standards, blockchain interoperability, open  source projects, and technical implementation.

[A Universal Resolver for self-sovereign identifiers](https://medium.com/decentralized-identity/a-universal-resolver-for-self-sovereign-identifiers-48e6b4a5cc3c) was published, and primarily developed by [Markus Sabadello](https://twitter.com/peacekeeper) in conjunction with the DIF, adding another essential piece of the decentralized identity stack.

![https://miro.medium.com/max/397/0*kXI_oKFuEq63dLY-.png](https://miro.medium.com/max/397/0*kXI_oKFuEq63dLY-.png)

[Uniresolver.io](https://uniresolver.io/) currently has methods for resolving the following DID types:

- did:sov, registered on the Sovrin distributed ledger
- did:btcr, registered on the Bitcoin blockchain
- did:stack, used by Blockstack
- did:uport, used by uPort
- did:ipid, using IPFS and IPNS
- did:v1, used by Veres One

The Decentralized Identity Foundation is composed of over 50 members, including [Microsoft](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE2DjfY), [uPort](https://github.com/uport-project/ethr-did/blob/develop/docs/index.md), [IBM](https://www.ibm.com/blogs/blockchain/2018/06/self-sovereign-identity-why-blockchain/), [Sovrin](https://github.com/sovrin-foundation/sovrin/blob/master/spec/did-method-spec-template.html), [SecureKey](https://www.ibm.com/blogs/blockchain/2018/05/self-sovereign-identity-our-recent-activity-as-a-sovrin-steward/), [Blockstack](https://github.com/blockstack/blockstack-core/blob/feature/docs-bns/docs/blockstack_naming_service.md#decentralized-identifiers-dids), [Evernym](https://www.evernym.com/wp-content/uploads/2017/07/What-Goes-On-The-Ledger.pdf), [Hyperledger](https://github.com/hyperledger/indy-sdk/blob/master/doc/getting-started/getting-started.md), [Civic](https://www.civic.com/solutions/kyc-services/), [Accenture](https://www.accenture.com/us-en/insight-blockchain-id2020), [ID2020](http://id2020.org/), [Mastercard](https://newsroom.mastercard.com/press-releases/mastercard-microsoft-join-forces-to-advance-digital-identity-innovations/), and others sharing the goal of creating a decentralized identity ecosystem.

## GDPR

On May 25, 2018, the GDPR, under development since 2016, was enacted into law. Now those who wish to do business with European citizens must comply with this new regulation. The GDPR shifts ownership of customer data to from the organizations to the individual. As required by the GDPR, Indy was built for “privacy by default” and “privacy by design.”

![https://miro.medium.com/max/840/0*gdi9WSuwlSKqwQG2.png](https://miro.medium.com/max/840/0*gdi9WSuwlSKqwQG2.png)

## Conclusion

If you’ve made it this far, then perhaps you understand why I believe Hyperledger Indy is a key component to the future of decentralized identity. Indy has deep roots within the internet identity standards community, and is a culmination of work from numerous independent parties sharing a passion for the privacy focused design of an internet-wide identity layer. Those roots reach back to 2005, when the IIW was formed, and even further to PGP’s [web of trust](https://en.wikipedia.org/wiki/Web_of_trust) from the 90s.

Indy isn’t just another blockchain identity application, but is born of a richly interwoven fabric stretching across the identity standards, cryptographic, blockchain, humanitarian, and enterprise ecosystems — similar to the network it was built to enable.

## Resources

- [The Hyperledger Project: 5 Frameworks, and 5 Tools](http://web.archive.org/web/20181205055115/https://medium.com/axiom-tech/getting-to-know-the-hyperledger-project-642fe25794df)
- [SSI - The ultimate GDPR Compliance Tool [1]](https://medium.com/evernym/is-self-sovereign-identity-ssi-the-ultimate-gdpr-compliance-tool-9d8110752f89) — [[2](https://medium.com/evernym/is-self-sovereign-identity-ssi-the-ultimate-gdpr-compliance-tool-40db94c1c437)] — [[3](https://medium.com/evernym/is-self-sovereign-identity-ssi-the-ultimate-gdpr-compliance-tool-7296a3b07769)]
- [What goes on the Ledger](http://web.archive.org/web/20181206060152/https://ernesto.net/ernesto-net-5-minute-course-on-indy-and-what-goes-on-the-blockchain-ledger/)
- [Hyperledger Indy Architecture](http://web.archive.org/web/20181206060151/https://www.ernesto.net/hyperledger-indy-architecture/)
- [infominer33/awesome-decentralized-id](https://github.com/infominer33/awesome-decentralized-id) — Self-Sovereign, and Blockchain ID Resources
- [wiki.hyperledger.org -Indy Documentation Index](https://wiki.hyperledger.org/projects/indy/documentation)
- [windley.com/tags/identity](http://www.windley.com/tags/identity.shtml)
- [/WebOfTrustInfo](https://github.com/WebOfTrustInfo/)
- [veres.one](https://veres.one/) — a permissionless platform built for the same purpose