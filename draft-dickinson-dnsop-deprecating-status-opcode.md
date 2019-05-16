%%%
    Title = "Deprecating the DNS Status OpCode"
    abbrev = "Deprecating the DNS Status OpCode"
    category = "std"
    docName= "draft-dickinson-dnsop-deprecating-status-opcode-01"
    ipr = "trust200902"
    area = "Internet"
    workgroup = "dnsop"
    keyword = ["DNS"]
    date = 2019-05-13T00:00:00Z
    toc = "yes"
    compact = "yes"
    symrefs = "yes"
    sortrefs = "yes"
    subcompact = "no"
    updates = [1035]
    [[author]]
    initials="J."
    surname="Dickinson"
    fullname="John Dickinson"
    organization = "Sinodun IT"
      [author.address]
      email = "jad@sinodun.com"
      [author.address.postal]
      streets = ["Magdalen Centre", "Oxford Science Park"]
      city = "Oxford"
      code = "OX4 4GA"
%%%

.# Abstract
This document updates RFC1035 to depreciate the Status DNS OpCode.

{mainmatter}

# Introduction

The Status OpCode was given the value of 2 in [@!RFC1035]. However, no RFC defines what it means or how it should be used. This document makes the Status OpCode obsolete.

# Terminology
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in BCP 14 [@!RFC2119] [@!RFC8174] when, and only when, they appear in all capitals, as shown here.

# Implementation Status

To the author's knowledge there is no implementation of the Status OpCode. A quick test shows inconsistent responses to a Status request with different DNS server implementations returning NotImp, Refused or giving no response at all.

# Deprecating the Status OpCode

The Status OpCode MUST be marked OBSOLETE.

The correct response to the Status OpCode MUST be NotImp.

# Security Considerations

None

# IANA Considerations

This documents updates the IANA registry "Domain Name System (DNS) Parameters OpCode registry" [@DNS-IANA].

OpCode | Name | Reference
:------|:-----|:---------
2 | Status (OBSOLETE) | This Document

# Acknowledgments

Thanks to Mark Andrews, Matt Pounsett, Roy Arends and all the people at IETF 104 that I asked if they knew of any usage of this OpCode. Also thanks to Shane Kerr for reminding me to write this document.

<reference anchor='DNS-IANA' target='https://www.iana.org/assignments/dns-parameters/dns-parameters.xhtml#dns-parameters-5'>
    <front>
        <title>Domain Name System (DNS) Parameters OpCode registry</title>
        <author>
            <organization>IANA</organization>
        </author>
        <date year=''/>
    </front>
</reference>

{backmatter}