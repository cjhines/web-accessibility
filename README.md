# Web Accessibility (A11y)
Cliff notes of Google's Web Accessibility course. You can access the course, and other Web Accessibility resources from Google in the link below.

[Web Accessibility fundamentals by Google](https://developers.google.com/web/fundamentals/accessibility).

## What is Web Accessibility?
In short, accessibility is about making sure that the content and websites we create is usable to people with various impairments or abilities. In its narrowest sense, addressing accessibility issues very often improves the user experience for everyone.

**Example**: A checkbox is not correctly associated with its label.  
**Specific issue**: A screen reader user may struggle to figure out the association.  
**Universal issue**: Users must click the small checkbox, rather than the label.  

## Understanding the diversity of users

### Blindness
Modern web technologies make it very easy for developers to make websites that are difficult to use for blind users. If a user has no vision they will likely be using a screen reader or Braille to allow them to read information displayed on the screen. Many websites are visual in their nature and lack keyboard navigation, which is essential for blind people to navigate.

### Visual impairments
In general, it is safe to assume there are more people with visual impairments - people with **some** sight - as opposed to people that are completely blind. Such people may use large-print text, magnification, or adjusted colour contrast when using the computer.

### Colour vision impairments
People with poor colour vision may have difficulty distinguishing red and green, or blue and yellow. This accounts for 9% of men and 1% of women.

### Motor/dexterity impairments
A wide range of common illnesses and accidents mean a huge number of people may be using only the keyboard, head or eye tracking software, switches, or voice dictation.

### Hearing impairments
Some users may be completely deaf, while others have some hearing. This means that content that uses sound should provide some visual alternative.

### Cognitive impairments
Users with conditions such as ADD, dyslexia, and autism may require diverse accomodations such as magnified content, or minimal design to minimize cognitive load.

### Temporary challenges
Circumstances such as using a screen in the sun, or using a laptop on a shaky train mean that users without disabilities may also encounter circumstances where they struggle to use their devices as they usually would.

## Web Content Accessibility Guidelines (WCAG) 2.0
WCAG is a set of guidelines and best practices which have been put together by web accessibility experts to try and answer the question of what accessibility means in a methodical way. WCAG is organised around four core principles, known as **POUR**:

* Perceivable
* Operable
* Understandable
* Robust

While these guidelines supply a framework for thinking about accessibility, there may be places where they're incomplete or even give advice which is outdated.
