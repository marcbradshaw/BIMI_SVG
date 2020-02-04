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

Currently, the SVG standard is at version 1.1 [W3C.REC-SVG11-20110816], 
while SVG Tiny is at 1.2  [W3C.REC-SVGTiny12-20081222], 
and these are both W3C standards.  The definition below will outline 
SVG 1.2 BIMI, an SVG profile that is suitable for use with BIMI.  This new
profile will use SVG Tiny as a base.




# SVG 1.2 BIMI

## Permitted sections

These attributes described in the sections listed below are permitted
to be used in SVG 1.2 BIMI:

* 8 Paths

* 9 Basic Shapes

* 10 Text

* 11 Painting 

## Disallowed sections

THe attributes described in the sections below are expressly
forbidden from use in SVG 1.2 BIMI:

* 12 Multimedia

* 13 Interactivity

* 14 Linking

* 15 Scripting

* 16 Animation

* 18 Metadata

## Unadvised Sections

The sections below are of questionable value to the documents, but
are not expressly forbidden.

* 17 Fonts

## Required Attributes

The attribites below are required for SVG 1.2 BIMI.  These should be declared
in the base `<svg>` tag.

* title: This is a space where the title of the entity MUST be
  published. This may allow for individuals with disabilities 
  to have some knowledge about the image. For brevity, this SHOULD 
  be no more 64 characters.
 
* desc: A longer description would be permitted here, if necessary.

* version: This attribute MUST be set to "1.2".

* baseProfile: This attribute MUST be set to "tiny".

* zoomAndPan: This attribute MUST be set to disable, as it may cause issues in
 a user interface.

* externalResourcesRequired: This attribute MUST be set to "false" so that
 external resources are not required for rendering.

* preserveAspectRatio: This should be set to xMidYMid, and should center the image
 in the viewbox when the size is changed.

`<svg width="1cm" height="1cm" version="1.2" baseProfile="tiny" zoomAndPan="disable"`
`         externalResourcesRequires="false" perserveAspectRatio="xMidYMid"`

## Elements allowed in SVG 1.2 BIMI

```Do we want to explicitly state which tags are permitted?```

# Notes

https://www.w3.org/TR/2011/REC-SVG11-20110816/

https://www.w3.org/TR/2008/REC-SVGTiny12-20081222/

Comparison: https://tools.ietf.org/html/rfc7996
  (esp note App A: RNC for validation)

# Security Considerations

N/A

# Contributors

TBD

# References

TBD

{backmatter}
