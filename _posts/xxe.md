---

title: "Egyptian Bank Of Knowledge"
date: "2020-01-9"
layout: single
permalink: /ekb/
tags:
- Bugs
categories:
- Notes
---


Welcome Everyone, Today our report gonna be about
List of Bugs :
 1. Reflected XSS 
 2. Open Redirection 
 3. XXE 


# Reflected XSS

  After usual subdomain enumeration we've got assessment.ekb.eg that has login .. mmmm suspicious i like login panels
  Run our **PageCrap** script to search for links, after 10 seconds we've got resetPasswordRequest.svc?emailAddress=
  Mmm nice lets try our email resetPasswordRequest.svc?emailAddress=omarbadraan@cybershit.com .. it gets printed
  and no mail received as we didn't signup our email so lets try printing html content before [*@cybershit.com*] and
  boom reflected xss, but wait thats old as shit .. does it even check if @ is there on the mail ? .. nope it doesn't
  so final payload is [OmarBadraan](https://assessment.ekb.eg/pearson/login/resetPasswordRequest.svc?emailAddress=%3Cscript%3Ealert(%22OmarBadraan%22);%3C/script%3E)

# Open Redirection

  I just ran my 2 scripts together and they got it i'm not gonna get into details as it has login, scraping, same as above
  so here is the final link
  [OmarBadraan](https://sandboxlms.ekb.eg/api/knowledgetree/resources/ba58f381-a4a0-406c-b0d4-3a03596e99c2/launch?url=https://omarmohamedsc.github.io/)
  

# XXE 
Private for now
