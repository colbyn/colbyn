# Timeline

## 2016

- Discovered functional programming and formal verification in general, I later quit my paying dev job and became a passionate FP zealot.
    - Overall, learned a lot about things that had absolutely no job prospects but life was great.
    - Read Category Theory For Programmers.
    - Considered myself an ammeter compiler engineer (which as an FP zealot was just par for the course lol 🙂) with knowhow on the design and implementation of typed lambda calculus based languages including hindley milner type inference.
    - Probably the most practical experienced I got from this whole ordeal was parsing knowhow and the ability to make my own monadic parser combinator frameworks.

## 2018

### Worked on a secret startup project
- Didn't go anywhere. But I learned a lot about visual compression and decided to turn my attention towards image processing.

## 2019

- The beginning of my open source endeavors.

- According to GitHub in 2019 I made 1,323 contributions.

  To put this in perspective: according to this [data source](https://web.archive.org/web/20200415010317/https://gist.github.com/paulmillr/2657075/), from from December 2016 to December 2017, the 256th person (at the end of the list) made 1,322 total contributions. **So I literally beat the 256th person by a single contribution.** 



### [Imager Project]( https://github.com/imager-io )

Site performance tools for efficiently distributing media on the web. Notably includes a [tool]( https://github.com/imager-io/imager ) for optimizing the binary encoding of images in a brute force trial ’n error sorta manner, using a new ML based perceptual quality metric designed to be a more accurate model of human perception compared to prior formulaic approaches. 

## 2020

In absolute terms everything hitherto was a waste of time. Which lead to the following events,
- I decided to attend a university, with a desire to get outta programming as a profession and into something new.
- My aspiration was to find a niche that itself wasn't a programming profession but where my background as a programmer was valuable. 
    - The aspiration was partly inspired by a talk on precision medicine by a guy with a background in formal verification (which resonated with me).
    - I was also under the impression that theres finite demand and preferring security I wanted to explore other options.

## Regarding My University Studies

- Took an entry level programming class.
    - The instructor said my code was beautiful (which was surprising since it was in Python).
    - Afterwards I found myself a grader for the class.
    - As a grader for an entry level class, the standard among the students was not what I was expecting.
- I took trig and calculus concurrently which was a lot.
- Overall I did well in all calculus classes but for me calculus was nothing more than algebra, which itself was nothing more than a symbolic medium that played well with my very discrete mindset.

### Regarding my School Notes

- My digital notes were growing in complexity and sophistication from rendered PDFs to webpages—which I preferred because I could quickly navigate from one resource to an other via hyperlinks.
- By the end of the year I have a well developed [toolchain]( https://github.com/subscript-publishing/subscript-html ) for automating its complication, I referred to it as **Content Publishing using Web Technologies** with tons of conveniences such as rendering Desmos graphs as shown the following:
    ```html
    <include src="../template/base.html">
        <h1>My Book</h1>
        
        <include src="../content/chapter1.html"></include>
        <include src="../content/chapter2.html"></include>
        <include src="../content/chapter3.html"></include>

        <!--
        NOTE: SEE HTML SYNTAX HIGHLIGHTING EXTENSION FOR VS-CODE
            (MAKES MIXING LATEX/HTML MORE BEARABLE)
        -->
        <h2>Graph of <tex>y = x^2</tex></h2>
        <desmos>
            <expr>y = x^2</expr>
        </desmos>
    </include>
    ```
- The above tool lead to the culmination of [colbyn's math notes]( https://colbyn.github.io/school-notes-spring-2020/ ). Which I used to great effect and yet such left much to be desired.
    What I wanted was:

    - Seamless support for typeset and hand drawn notes.
  
    - More practically, the after a point the nesting so much LaTeX math in HTML was becoming very difficult to read and manage.
      Even after releasing a VSCode extension that basically hacked in LaTeX Math Syntax Highlighting.
    
  What I needed was a new markup format that allowed for:
    
    1. The sophisticated layout as see in my personal [math notes]( https://colbyn.github.io/school-notes-spring-2020/ ) (i.e. try resizing the browser window if you're on a desktop).
        - Layout is important because I want notes to be as compact as possible for any given viewport. 
    2. With support for the expression of math in a super convenient manner. 
    3. In a manner that accommodates autocomplete and syntax lighting in as robust and efficient a manner as possible. 
        - On a tangent, one thing I absolutely loved was this concept called rainbow parentheses. 
            - [See here for an early prototype]( https://github.com/subscript-publishing/subscript-compiler )
            - This was later cleaned up with a somewhat better version:
                - [example 1]( images/Screenshot 2023-11-03 at 11.04.54 PM.png )
                - [example 2]( images/Screenshot 2023-11-03 at 11.20.12 PM.png )


- At the same time I was starting to think about how to integrate hand drawn notes into such a toolchain which first manifested as a simple app prototype that I used—as a proof of concept—in my chemistry classes.
    - See here for the [root index]( https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/index.html ) of the chemistry notebook. 
    - Where this differs from other note taking apps is its ability to support giant autogenerated **tables of contents** from the root notebook down to the individual pages.
        - [see here for an example]( https://colbyn.github.io/old-school-chem-notes/dev/chemistry-1010---fall-2021/overview.html )
        - In a later version this was expanded to support arbitrary hierarchical page layout.
    - Overall I was very happy with the work. But on a sad note, my original chemistry notes were compiled at a time when the app lacked support for dark mode. In a later version I added support for such in the autogenerated HTML/SVG markup but I lost the original model file for the chem notebook—so all I have left are the rendered webpages. 😔 
    - Also on a tangent, the development of the native note taking app is what got me into iOS development.
- **The code for all my note taking explorations culminated into the mono repo over at [subscript-publishing/subscript](https://github.com/subscript-publishing/subscript)**

- On an random but interesting tangent, some recruiter reached out to me saying that I'm at the top of some list he compiled of rust developers based on their GitHub activity. Nowadays the idea of companies paying other people to find needed talent is unfathomable. 

## In the aftermath of COVID

### The Time Of Personal Trial

- My overall health and wellbeing was in a terrible state and I was clearly on the decline at this point. 
- After taking a leave of absence, I later transferred to a different university.
    - Perhaps I was hoping to just resume where I left off in life but in a manner where I was closer to my original end goal; but perhaps as well, such was too little too late. 
    - I could no longer perform at the level I expected of myself.
    - Something was clearly wrong, yet my instinct was to just push on regardless. I think this was a mistake, As they say,
        > "better to retreat a foot than to advance by only an inch"
    
      From a book that I absolutely disliked previously (had to read and write about it in a dumb honors class)… Which I was now reading it as if divine scripture. Such a change in literary preference was itself very inauspicious from my perspective, compounding my belief that I broke somewhere along the way. 
      
      But what to do?
      
        - For context, when I was younger I had solved many hard problems via sheer brute force, including the implementation of a hindley milner type inference system for a type lambda calculus like language that I designed myself as a toy project. Something I had no formal training on yet I was able to see firsthand (after much trial and error) how types substituted with other types and how general constraints unified with less general constraints in such a beautifully elegant manner that afterwards I though much of myself with regard to solving abstract problems, which only happened after applying 100% of my energies into its solution. So from my perspective brute force can solve all immediate problems. 
        - But at the same time the real world was taking on a rosy red hue as I began to process my experiences with regard to that thing that college students are stereotypically known for (shockingly too—from my perspective—by the opposite gender).
    - Seemingly, I was at an impasse with fate itself but again what to do? 
    - Later on I came across this concept in asian philosophy called "wu wei" which—as I interpreted it—caused me to reconsider my hitherto brute force approach to life. 
        
**Ultimately I completely washed out of higher education.**
- I guess such is what happens from prolonged indecision where problems under pressure are never resolved. But at this point I was completely committed to just relenting to any and all problems and complete inaction in general.
- Devoid of any aim in life I went on a prolonged *'trip'*. 

**Technically while on an indefinite leave of absence:**

- Okay I'm now a certified dropout and as such, perhaps I should just return to IT as a day job?
    
  After all, as one may say, it's been that "all giving tit" for millennials who championed the "learn to code" slogan.
  
  But oh no!
  
  Turns out that the IT job market has completely crashed. Apparently it was not the panacea we all thought. At this point I was now completely disillusioned with regard to white collar professions in general and higher education in particular.

**Sometime in the aftermath of me falling from grace:**
- Clearly I was no longer the person I thought I was. 
- The meaning of the expression:
  
  > fate is a cruel mistress

  Now seemed very real, as life now seemed like nature as found in the wild.

**Time to get my life back together:**
- Whatever identity I had of myself was no longer so I may as well start from scratch. 
- Time to get my life back; all options are on the tables.
- All I really wanted at this point was stability wherever that may be found.

### By 2023
- I had moved back in with my parents.

  Not necessarily a bad thing. When I was a teenager I may have technically lived at this house, but I was never around in favor of one social outlet or another.
  
  But I soon discovered that the times have changed even down here. Over time it dawned on me that there was no going back, and there is no repeating what once worked.

  In a way, I began to idolize my unhealthy teenage lifestyle, which socially speaking I now longed for. Clearly I was feeling particularly lonely.
- I had taken up a janitorial job.
  
  As inspired by that "wu wei" epiphany I had where I happily went with the least effort option in my life.
  
  Which by now had completely changed my perspective on career options:
    - Honestly I enjoyed being physically active which was probably one of the better decisions in my life.
    - To add to my sense of burnout I was starting to regret even touching a computer.

## 2024

### In the beginning
- Getting my life back together is still an ongoing task but things are different.
- Long term career objectives still very uncertain.
    - In the beginning I decided to double down as an indie developer since I was certain that no company would want someone with my résumé.
    - But secretly I was considering jumping ship altogether and going into some blue collar trade where I didn't have to think about computers.
    - For the first time in my life I found myself conscious of the fact that I'm growing older, which lead to some conflicting thoughts:
        - Restarting a life is a young man's game and therefore if I'm going to do it I better make up my mind sooner than later.
        - At the same time I was hesitant:
            - I knew much and my mindset was such that I very self sufficient at solving technical problems.
            - A guy I met at college who was super smart in quantitative terms said I was a better developer in general.
            - In a way I paid a price for these things and who wants to just waste such an expenditure? 
- Mentally speaking:
    - At one point in my life I was certain that my brain was permanently fried. Akin to some homeless people I've met.
    - But at this time it was like some hitherto unknown brain fog was beginning to lift. (If so perhaps the brain's fault tolerance capacity took effect in my case.)
    - Loneliness was no longer something I wanted to cure.

### Sometime Afterwards
- **Long term break from all computer/online activities:**
    - Began with no expectations. My life was such that it just happened. 
    - Suddenly I found myself reading up to a thousand pages a week as if I was 15 again.
        - I learned that Stormlight Archive is super overrated. (Although I really liked the first book. Perhaps if the author was less ambitious my opinion would be different.)
    - Later on I found myself falling asleep without the aid of drugs.
    - Soon afterwards I stopped taking any and all meds, I also found myself in complete sobriety overall.

- Overall I concluded 2024 in such a way that,
    - **In extrinsic terms:** little to no change.
    - **In intrinsic terms:** significant change, in terms of me as a person and in my personal relations. 
        - In a way, while I always saw myself as that nice guy, at the same time I was no longer that *[insert expletive]* I once was.
        - I no longer felt lonely, in any way, and such has been the case ever since.
        - I regained confidence in myself but in a newfound manner.
          
          In a way I was somewhat inspired Xi Jinping's trials as a young man (not that I idolize who he has become) as discussed in this biography I found.

          ***As one may say to another who's starved of something: "eat bitterness".***

## Post 2024

While I’m a little ways away from my thirties, my immediate goal from here to there is to be on-par with this statement by Confucius, a statement that really resonated with me at a very dark time in my life:

> “CHAP. IV. 1. The Master said, 'At fifteen, I had my mind bent on learning. 2. 'At thirty, I stood firm. 3. 'At forty, I had no doubts. 4. 'At fifty, I knew the decrees of Heaven. 5. 'At sixty, my ear was an obedient organ for the reception of truth. 6. 'At seventy, I could follow what my heart desired, without transgressing what was right.”

