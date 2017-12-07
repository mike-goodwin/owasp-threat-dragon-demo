# Demo Threat Model

__Owner:__ Mike Goodwin

__Reviewer:__ Jane Smith

__Contributors:__ Tom Brown, Albert Moneypenny

A sample model of a web application, with a queue-decoupled background process.

---

# Main Request Data Flow #

*insert image here*

---
  
## Browser (Actor) ##

|Property|Value|
|:---|:---|
|Provides Authentication|False|

### Threats ###

*None*

## Web Response ##

|Property|Value|
|:---|:---|
|Protocol|HTTP/S|
|Is Encrypted|True|
|Is Over Public Network|True|

### Threats ###

|Title|Data flow should use HTTP/S|
|:---|:---|
|Type|Information Disclosure|
|Status|Mitigated|
|Severity|High Severity|
|Description|These responses are over the public internet and could be intercepted by an attacker.|
|Mitigations|The requests should require HTTP/S. This will provide confidentiality and integrity. HTTP should not be supported.|
