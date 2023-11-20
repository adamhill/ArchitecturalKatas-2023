
# Notes from Videos

## Semi Finalist ***Videos*** from Previous Years
- 2021 Fall is on YT
  - [2021](https://www.youtube.com/watch?v=EicfaYa5nDg)

- 2022 is behind the O'Reilly Safari paywall but has a free trial
  - [2022 - Spring](https://www.oreilly.com/library/view/architectural-katas-spring/0636920743217/)
  - [2022 - Fall](https://www.oreilly.com/library/view/architectural-katas-fall/0636920824275/)

## Running notes for video based on notes below
Good ideas for us

- Different people read different bits
- Headshot on the slides at the beginning
- Use builds on slide - See if we can all use Keynote (Macs), then we could just do VO with a video Keynote slide, that can build as slow or fast as we like
- Make sure we have a a principals slide (Maybe our emphasis bits with another bullet point or two)
  - They really like the 3-4 circles Venn diagram
- Get the 97 things a software architect need to know book and skim it :-)
- Maybe we should stress our very event driven, very asynchronous architecture and have two diagrams. Show how resilient we are:
    - Flow with very little connectivity
        - Specifically call out store and forward all event if no connectivity
    - Flow with connectivity back to basecamp (LoraWAN & Mesh & Satellite)
    - They kindas liked medium level implementation details and the "Next Steps" (we kinda have that under the Expansions idea)
- They really liked the metadata for ADR (Proposed -> Acceptance)+2
  - This means they looked at file histories - We did start out as Proposed!
- **We need to make sure we set our ADR's once we are OK with them all to ACCEPTED**
- Tie our characteristics to the solution


## Fall 2021 - Pharmacy Family Problem - PII & HIPPA & Extension of a Previous Kata Solution

  
## Legend    
        Nothing == My comment 
        (J) == Judges comment 
        +number == number of times a judge mentioned it (there were 3 judges)

### Pentagram 2021
- Reading really fast - not good
- Text is really small
    - How do we get the text legible for diagrams? (I got a copy of Communication Patterns)
- (J) Good problem statement
- (J)Domain <-> Architecture isomorphism
    - Did not choose Microservices cause they are a startup and they might not be able to afford  / do it.
- (J)They used C4 diagramming
- (J) Neal nit picked them misspelling O’Reilly 
    - But they misspelled Wonderous Toys :-) 
- (J) ID strategic vs tactical, where to buy vs build
- (J) Diagrams not adapted for a presentation style (nice to have)

### Arch Angels (with a space)
- Good vision diagram
- They did a separate recording for each slide - no talking head
- **(!!!) They have a simple implementation plan (!!!)**
- They have team slide for the end
- **+2** (J) - Good problem statement
- **+2** (J) - Good showing the added bits versus existing bits 
- (J) - Like the Data Flow
- **+2** (J) - Next steps 
- (J) - ID architecture demonstration
- (J) - Good involvement of the team

### Berlin Bears
- Very non-technicalin the beginning (1 minute of exposition)
- Did a Customer-Journey-Map
- Used the zoomy web-javascript based Press
- Mentions open-source
- Implementation details (AWS, DynamoDB)
- They had picture slides
- **+3** (J) Liked the opening intro 
- (J) They liked a picture with pages, not speaking tho
- **+2** (J) Like including the whole team 
- (J) Liked addressing where all the data was going to go
- (J) Liked Vision -> Customer -> Architecture

### *3rd Place* - Architects++
- Good - Diagrams - Maps - great exposition in the beginning
- Added 2 other goals:
    - Empower people to improve own diets 
    - Meeting people where they are to get other services
- Made a Principals slide
- One person mainly read the repo - Scrolling thru the README and scrolling around the diagrams, zoomed in.
- Only two people read - Front bits and architecture
- (J) PO was good - First part a lot more business focus.
- (J) Neal liked the Preferred the left over the right discussion (from left over right) - NEED TO REWATCH
- **+2** (J) Not detailed, more of an overview 
- **+2** (J) Made a Principals slide 
- **-1** (J) Better 2nd bit transition to scrolling around the repo 
- **+2** (J) really liked the metadata for ADR (Proposed -> Acceptance) 
  - This means they looked at file histories - We did start out as Proposed!

## *1st Place* - ArchAngels (no space)
- Nice major ADR slide (us?)
- Context diagram vs Flow?
- Not any front matter
- Lots of tech - analyses of data storage types
    - Made a graph data diagram for PF!!!
- Did a deployment slide or two
- Only two people read
- **+2.5** (J) Liked the Excalidraw!!!!! 
    - Roughness good
- (J) Liked the domain separation
    - Good used of Event Driven architecture
- (J) Nice end bit with how good things will be
- (J) One judge liked the data breakdown & storage tech analysis

## *2nd Place* - Sever Crew
- Good Image & diagrammed  front matter
- More good requirements as pictures
- Nice animated transitions for Context.
    - Nice build while talking
- But big diagram is hard to read
- ADR intro - they have non-architecture ADR’s
    - And they talk about Webinars and Mobile!!
- Good non-diagrammy slides interspersed with diagrams
- Nice slide about handling change (evolving architectures)
- **+2** (J) Liked the manipulation of time (builds) in the slide 
    - Called out the zoom into the domains
- (J) Liked the constraints section
- (J) Liked all the explanation that told them the history of the ADRs **+2**
- **-2** (J) Did not use full time 
- (J) - Detailed explanation did not tie in

## Elephant on Cycle
- They are using Keynote IIRC - Cube rotate for each major section.
- Nice use of pictures and non-busy slides
- Liked meeting the team (this is at odd with the “dont include people”)
- **+2** (J) liked the tying the characteristics back to the solution 
- **-1** (J) A bit of ding for the multiple cloud claim 