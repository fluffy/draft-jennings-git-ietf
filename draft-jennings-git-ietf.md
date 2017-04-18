%%%

    #
    # SRTP Double Encryption Procedures
    #
    # Generation tool chain:
    #   mmark (https://github.com/miekg/mmark)
    #   xml2rfc (http://xml2rfc.ietf.org/)
    #

    Title = "Thoughts on Using GitHUb for IETF work"
    abbrev = "GitHub at IETF"
    category = "std"
    docName = "draft-jennings-git-ietf-03"
    ipr= "trust200902"
    area = "Internet"
    keyword = ["GitHub"]

    [pi]
    symrefs = "yes"
    sortrefs = "yes"
    compact = "yes"

    [[author]]
    initials = "C."
    surname = "Jennings"
    fullname = "Cullen Jennings"
    organization = "Cisco Systems"
      [author.address]
      email = "fluffy@iii.ca"

%%%

.# Abstract


Discusses a few of the issues and proposed solutions for using GitHub for IETF draft development. 


{mainmatter}



# Introduction

This draft is purely meant to propose a few things worth discussing when using GitHub for IETF work.


## Everything under one org

Anyone doing a IETF spec in Github should be encouraged to use put it under the IETF organization. This makes is much easier to ensure it gets archived, does not disappear, and can reflect changes to IETF policy over time.

## One repo per draft

The PERC WG experiment with one repo for WG. It did not work out well primarily because issues end not associated with the specific draft they apply to.

## Also a repo per WG

This can mange minutes, general issues, charter tracking over time etc. It might work to import the WG doc repos into this so that people can easily find all the documents for a WG.

## No black magic

The current templates used in may repo do not work for a large number of contributors. Prefer something simple that worked for a variety of users or even a template where were different things for different OSs but the one appropriate for that OS reliably worked to build drafts

## Trivial repo creation

I think it would be easy to make a tool where if someone created a -00 draft, and if one of the authors had an email that part of the IETF team on git, then a git repo for that draft was automatically created. 

## All contributions compliant with IPR BCPs

I do not want our specification to have anonymous contributions. I do not think that is compatible with our patent policy. My goal would be to take the same level of identity we use in going an IETF and bring that to Github. 

Anyone with commit access to to a repo in the IETF Github org would need to be in the IETF org team have agreed to the things you need to agree to to attend an IETF along with linking their Github account to the same level of identity verification we use for IETF registration.

All PR would have an automated tool that ran and marked the PR as coming from someone who was not in the IETF team as potentially not compliant with the BCP. Editors could decide if they wanted to merge that or not. The W3C uses a tool that marks if a PR comes from an W3C member or not and it is really nice to use. 


## Archive 

The IETF should archive all Github repo by closing them to IETF servers and should archive all PR, issues, and comments by using the email subscription. The ability to look through this information 20 years from now is one of will be one of the primary tools used to show their was prior are on some of the patents we will be dealing with. One of the risk of doing patents in the open at IETF vs in  closed form at other SDOs is that people can file patents on the ideas in the standard before it is published. Mailing list and GitHub information can be used to mitigate this risk by showing others had the ideas and publicly discussed it before the patent was filed. 


## Huge problems with issue discussion

At some level, having both a mailing list and issue tracker is the worst of both worlds. The 5 people that are most involved with the drafts love the issue tracker. No one else reads it or participates. Discussions on Github dramatically reduce the number of people involved with the dissolution. If you just wish no one would object to your brilliant idea, use the issue tracker.

It is hard for chairs to call any form of consensus on a conversation across email and issue trackers. This is similar to our issues of calling consensus from a room discussion but then saying the somewhat funny phrase "will confirm it on the list" which often ends up not meaning that.

I'd be interested in seeing what happens with a WG that tried to do random discussion of clarifying questions in a Slack channel but any real dissolution proposing a changes or arguing something needed to happen was done in issue tracker.

I't be interested in seeing an experiment with a WG where all the discussion happens on the mailing list and *only* the editors of a draft can create an issue or add comments to it.

## Formats

Markdown is much easier to use than XML for writing drafts. It makes it easier for people who don't so IETF XML to create pull requests. The mmark tool at https://github.com/miekg/mmark works better than the kramdown-rfc2629 The IETF should define a way to put the meta data in the markdown. 


{backmatter}

