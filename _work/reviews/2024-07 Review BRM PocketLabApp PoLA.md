## Suggestions
- Software Tests
- CI / CD
- Look at requirements for JOSS (an interesting alternative outlet)
- Documentation website
- Google Play Store
- F-Droid et al
- semver

## ToCheck
- AI Features do seem a bit odd, welcome that they're out of the MS, could be more distinguished from the rest of the software in documentation as well
- Was not able to test software
- Does it also trigger by itself?
- Any line w/o command is ignored?
	- Not a good idea in terms of software design


- Page 7 L 46 in "the" Kotlin
- Page 7 L 49 no citation for 56%
- pinning app to screen is not mentioned in documentation
- not suitable for EMA?
- instructions could be more clear?
- how are interruptions / crashes handled?
- lack of configuration? TIMER with e.g. only vibration
- restrictions on lab phone screen size etc?
- tab separated values should be saved as tsv?
- why is data only available on request?


## Review

I want to thank the author for their submission. I believe there is significant value in new research software and greatly appreciate their choice in releasing it as open source software.

-- Brief Summary --
The author presents a new software application named Pocket Lab App (PoLA) for in-the-field data collection using android smartphones. They describe several of the benefits of its design. The author further presents data from a study supporting its unobtrusiveness during data collection and illustrating how it has successfully been tested in a field-study.

As I do not own an Android smartphone I want to mention that I did not personally test the app itself, although I examined some of the codebase / documentation on GitHub.

-- Overall Evaluation --
I am not convinced that PoLA fills a wide enough gap in its current form to warrant publication in Behavior Research Methods. I am open to be convinced otherwise, if the author can make a compelling argument in a potential revision. I also found the manuscript to be quite one-sided in its current form, largely praising the application without a more nuanced discussion of its perks, shortcomings and alternative software.

I also recommend the Journal of Open Source Software to the author, either as a potential alternative for publication or as inspiration, as some of the critiques and suggestions I voice are formal requirements of the journal and the software would greatly benefit by fulfilling them.

--  Major Points --
I find the section on "Addressing Limitations of Current Mobile Research Applications" to be lacking (1) a comparison and overview of prior work (this should be present in the manuscript or at the very least the appendix) and (2) a clear positioning of PoLA within this space of other apps in light of its strengths and weaknesses. This would be an excellent opportunity to explain why PoLA was designed the way it was and how it fills a particular niche / gap in the ecosystem. Ecological momentary assessments and whether or not PoLA is suitable for the collection of these should be mentioned.

I noticed at least one entry in the references (Vaswani et. al., 2017) which was not referenced in the main body of the manuscript and it seems that the name of one citation is also frequently misspelled (Meer et al. vs. Meers et al). I therefore strongly recommend a thorough check of the references and citations in the manuscript. (If not used already, I recommend the use of citation software such as Zotero)

While I did not review the earlier version of the manuscript, I second the previous reviewers' points on clearly separating HeLA and PoLA. I appreciate the author's effort in updating the manuscript in this regard and would ask them to do the same for the application's documentation. If HeLA is to be part of the PoLA documentation, the text describing it should also be slightly reworked to more clearly highlight potential issues with AI generated studies and what to look out for. A clear separation between HeLA and PoLA is also important, as HeLA is clearly neither free nor open source.

Regarding the software side of the application, I question the author's choice of treating any text that is not a command as a comment. This means, that if I were to do a last minute change in my PoLA experiment switching an INSTRUCTION to a TAP__INSTRUCTION (accidentally adding a double underscore), that PoLA will happily run my study without any warnings and just treat the line as a comment. Having explicit comment markers such as // and --- would be better here. I further believe that research software which is used for data collection should ideally also have some automated tests to verify and test its function.

It is important that the app is able to reliably store data and I would appreciate it if the author could briefly comment on the app's ability to store partial data when it is accidentally closed or crashes.

-- Minor Points --
Overall some of the language on "ease of use" and "straightforwardness" could be turned down a bit and the article would benefit in general from a slightly more neutral and nuanced description, rather than "praising" or "selling" the application.

p.3 L 12: Complimentary and free seem to be synonymous
p.4 L 22: "Conducting field experiments comes with technical challenges that may discourage many researchers and suppress a broader adoption of field research.", I would appreciate some examples or a citation here, also in regards to how and which challenges are eased by mobile technology.
p.4 L 60: The author mentions that the use of text over graphical interfaces reduces the learning curve for new users. I am not convinced by this claim and would like to see proper proof / citations for it. Naively I would think that the opposite may be the case.
p.7 Fig. 1. would benefit from improved typesetting, esp. consistent alignment of text.
p.7 L 46 "the" Kotlin
p.7 L 49 56% of devices - citation needed, 56% of which devices is this referring to, the complete global mobile market or just android devices?
p.12 L 10: I would drop the word "extensively" here if it was only tested in a single study, same on p.15 L 6.
p. 17 L 30: Is there a good reason data is only available upon request?

GitHub
- The versions of the documentation (ver. 13.03.2024) and the release (v0.1) are mismatched, these should at least have a clear correspondence to each other. I would suggest potentially switching to semantic versioning instead.
- The instructions in the documentation should match the paper, as e.g. pinning the app to avoid navigating out of it is not mentioned in the GitHub documentation.

-- Optional Suggestions --
- A built version of the software could be released on the Google Play Store or the open source app store F-Droid for easier installation.
- The PoLA documentation could be put on a small static website via documentation generators e.g. mkdocs or vitepress, that can be hosted for free with GitHub Pages.
- Setting up a CI/CD pipeline (via e.g. GitHub Actions) for automated testing (and maybe even building) of the software could aid in future maintenance.
- It would be beneficial to have a way of validating a PoLA protocol.txt file on a desktop computer.
- As data is saved as tab separated values, tsv might be more suitable as an extension than csv.
- The author could eventually generate a citeable code archive of their software using Zenodo


