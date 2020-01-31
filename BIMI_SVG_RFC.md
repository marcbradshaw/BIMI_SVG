%%%

   Title = "SVG Requirements for BIMI: SVG 1.2 BIMI"
   abbrev = "BIMI-SVG"
   category = "std"
   docName = "draft-bimi-svg-abrotman-01"
   ipr = "trust200902"
   area = "Applications"
   keyword = [""]

   date = 2020-01-30T00:00:00Z
   
   [[author]]
   initials="A."
   surname="Brotman"
   fullname="Alex Brotman"
   organization="Comcast, Inc"
     [author.address]
     email="alex_brotman@comcast.com"

%%%


.# Abstract

This document specifies SVG 1.2 BIMI -- An SVG profile to be used for
images that are meant to be displayed in conjunction with BIMI.

{mainmatter}

# Introduction

The Brand Indicators for Message Identification (BIMI) specification has 
a requirement that associated image files must be SVG documents. These
documents are meant to be self-contained and scalable.  SVG does allow
for elements that can create challenges.  By limiting BIMI-related SVG
documents to a subset of the overall SVG specification, this should make
the above goal more feasible.

SVG (Scalable Vector Graphics) has been developed by W3C, the World
Wide Web Consortium; its current standard is SVG 1.1 Full
[@W3C.REC-SVG11-20110816].  This document defines SVG 1.2 RFC, an SVG
profile (i.e., a subset of SVG) that is suitable for RFC line
drawings.

# SVG 1.2 BIMI

## Disallowed sections

Forbidden: Media, Interactivity, Linking, Scripting, Animation

## Permitted sections

Allowed: Path, Shapes, Text(?), Painting, Metadata

## Unadvised Sections

Advise against: Fonts

## Required Attributes

The attribites below are required for SVG 1.2 BIMI:

o title: This is a space where the title of the entity MUST be
 published. This may allow for individuals with disabilities 
 to have some knowledge about the image. For brevity, this SHOULD 
 be no more 64 characters.
 
 `<title>Example, Inc</title>`

o desc: A longer description would be permitted here, if necessary.

`<desc>BIMI logo intended for use with Example, Inc. messages</desc>`

o version: This tag MUST be set to "1.2".

`<version>1.2</version>`

o baseProfile: This tag MUST be set to "tiny".

`<baseProfile>tiny</baseProfile>`

o zoomAndPan: This tag MUST be set to disable, as it may cause issues in
 a user interface.

`<zoomAndPan>disable</zoomAndPan>`

o externalResourcesRequired: This attribute MUST be set to "false" so that
 external resources are not required for rendering.
 
`<externalResourcesRequired>false</externalResourcesRequired>`


## Disallowed Attributes

image

## Elements allowed in SVG 1.2 BIMI



### Notes

version = "1.0" | "1.1" | "1.2"
baseProfile = "none" | "full" | "basic" | "tiny"
preserveAspectRatio = ["defer"] <align> [<meet>]
zoomAndPan = "magnify" | "disable"
5.7 The 'image' element
externalResourcesRequired = "false" | "true"


# Security Considerations

# Contributors
TBD

# References
TBD



{backmatter}
