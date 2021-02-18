---
title: "[Draft] Module 7: Rich Applications"
nav_title: "Rich Applications"
permalink: /curricula/developer-modules/rich-applications/
ref: /curricula/developer-modules/rich-applications/
lang: en
github:
  repository: w3c/wai-curricula
  path: content/developer/rich-applications.md
license: creative-commons
acknowledgements: /curricula/acknowledgements/
changelog: /curricula/changelog/
footer: >
  <p><strong>Date:</strong> Updated @@ Month 2021. First published December 2019. CHANGELOG</p>
  <p><strong>Editors:</strong> Daniel Montalvo and <a href="http://www.w3.org/People/shadi/">Shadi Abou-Zahra</a>. Contributors: <a href="https://www.w3.org/WAI/EO/EOWG-members">EOWG Participants</a>. ACKNOWLEDGEMENTS lists contributors and credits.</p>
  <p>Developed by the Education and Outreach Working Group (<a href="http://www.w3.org/WAI/EO/">EOWG</a>). Developed with support from the <a href="https://www.w3.org/WAI/about/projects/wai-guide/">WAI-Guide Project</a> funded by the European Commission (EC) under the Horizon 2020 program (Grant Agreement 822245).</p>
parent_in_h1: 
  - ref: /curricula/developer-modules/
    name: nav_title
  - ref: /curricula/
    name: "Curricula"
navigation:
  previous: /curricula/developer-modules/custom-widgets/
---

## Introduction
{:.no-display}

Courses based on this module should:

* demonstrate how people with disabilities rely on structures, navigate, operate, and interact with rich applications, including Single Page Applications (SPA) and others generated by JavaScript
* explain coding techniques to provide rich applications with appropriate structures and relationships, keyboard and focus interactions, and concurrent notifications

## Learning Outcomes for Module

Students should be able to:

* explain how appropriate structures and relationships, keyboard and focus interactions, and concurrent notifications enable people with disabilities to navigate, operate, and interact with rich applications
* explain how assistive technologies communicate generated content changes, such as change of screens in Single Page Applications (SPA), as opposed to page reloads
* write code to communicate coherent overall structure and relationships across rich application widgets that are perceived by people with disabilities
* write code to communicate coherent reading and keyboard focus order to navigate within rich applications using different types of input devices
* write code for prioritization of notifications and updates that allow people with disabilities to check them at their pace and convenience
* describe related requirements for content authors and designers to ensure applications are operable and understandable

{% include excol.html type="all" %}

## Competencies

Skills required for this module:

{% include excol.html type="start" %}

### Students

{% include excol.html type="middle" %}

* [Prerequisites for Students](/curricula/developer-modules/#prerequisites-for-students)
* Prior [Developer Modules](/curricula/developer-modules/)
* Knowledge of [HTML5 living standard](https://html.spec.whatwg.org/multipage/)

{% include excol.html type="end" %}

{% include excol.html type="start" %}

### Instructors

{% include excol.html type="middle" %}

* Applied expertise in teaching:
  * [WCAG 2 Success Criterion 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships)
  * [WCAG 2 Success Criterion 1.3.2 Meaningful Sequence](https://www.w3.org/WAI/WCAG21/quickref/#meaningful-sequence)
  * [WCAG 2 Success Criterion 2.1.1 Keyboard](https://www.w3.org/WAI/WCAG21/quickref/#keyboard)
  * [WCAG 2 Success Criterion 1.4.13 Content on Hover or Focus](https://www.w3.org/WAI/WCAG21/quickref/#content-on-hover-or-focus)
  * [WCAG 2 Success Criterion 2.2.2 Pause, Stop, Hide](https://www.w3.org/WAI/WCAG21/quickref/#pause-stop-hide)
  * [WCAG 2 Success Criterion 2.4.2 Page Titled](https://www.w3.org/WAI/WCAG21/quickref/#page-titled)
  * [WCAG 2 Success Criterion 2.4.6 Headings and Labels](https://www.w3.org/WAI/WCAG21/quickref/#headings-and-labels)
  * [WCAG 2 Success Criterion 2.4.10 Section Headings](https://www.w3.org/WAI/WCAG21/quickref/#section-headings)
  * [WCAG 2 Success Criterion 2.5.1 Pointer Gestures](https://www.w3.org/WAI/WCAG21/quickref/#pointer-gestures)
  * [WCAG 2 Success Criterion 3.2.1 On Focus](https://www.w3.org/WAI/WCAG21/quickref/#on-focus)
  * [WCAG 2 Success Criterion 4.1.1 Parsing](https://www.w3.org/WAI/WCAG21/quickref/#parsing)
  * [WCAG 2 Success Criterion 4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG21/quickref/#name-role-value)
  * [WCAG 2 Success Criterion 4.1.3 Status Messages](https://www.w3.org/WAI/WCAG21/quickref/#status-messages)
  * [HTML5 Living Standard {% include_cached icon.html name="external-link" %}](https://html.spec.whatwg.org/multipage/)
  * [DOM Living Standard {% include_cached icon.html name="external-link" %}](https://dom.spec.whatwg.org/)
  * [WAI-ARIA specification](https://www.w3.org/TR/wai-aria/)
  * [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices/)
* In-depth knowledge of:
  * [Prerequisites for Students](/curricula/developer-modules/#prerequisites-for-students)
  * Prior [Developer Modules](/curricula/developer-modules/)

{% include excol.html type="end" %}

## Topics to Teach

 Topics to achieve the learning outcomes:

{% include excol.html type="start" %}

### Topic: Structure and Relationships

{% include excol.html type="middle" %}

Refer back to [Module 1: Page Structure](/curricula/developer-modules/page-structure/) and explain the importance of proper structures and semantics within applications just as within less dynamic web pages. Demonstrate how assistive technologies rely on clearly identifiable sections and regions. Explain how content that is dynamically generated, for example through JavaScript, needs to be properly reflected in the DOM.

#### Learning Outcomes for Topic

Students should be able to:

* explain how structures and semantics enable people with disabilities to orient themselves and navigate within applications
* ensure that applications and dynamically generated content have appropriate markup structures and semantics, including:
  * sections, regions, and corresponding identifiers for these
  * sections of content, such as lists, paragraphs, and tables
  * widgets, including menu bars, form controls, and custom widgets
* identify and write code for any relationships between different sections of content within the application, for example groups of widgets that share the same purpose
* ensure that the order of content within the application follows a meaningful sequence in the DOM and visually, including when content is added, removed, hidden, and displayed
* ensure recognizable and consistent naming of widgets, including widget states, in particular when they appear multiple times within an application
* describe the impact of large amounts of client side code on assistive technologies and older computer technologies that some people with disabilities may be using
* describe related requirements for content authors and designers to provide clear layout and designs that support different viewport sizes

#### Teaching Ideas for Topic

Optional ideas to teach the learning outcomes:

* Demonstrate navigation between several widgets in an application using assistive technologies, such as text-to-speech and voice interaction. Explain how these components show and hide depending on user action. For example, when the user goes to the menu bar, the main text area, or a toolbar, another application widget may be hidden or greyed out. Emphasize that these states need to be programmatically marked up by updating, adding, and removing the corresponding elements from the DOM.
* Demonstrate the use of voice commands, keystrokes, and gestures provided by assistive technologies and adaptive strategies to query for applications titles, headings, and regions. Explain that such elements need to be updated using DOM management techniques to reflect the current state of the application, such as when a new view has been selected.
* Demonstrate overall interaction with rich applications using assistive technologies. Compare examples where assistive technologies communicate the elements that are displayed with other examples where assistive technologies may access information that is not currently on screen. Emphasize that document object model layers should be added and removed depending on the application view, so that assistive technologies only access the ones that are visible.
* Discuss different mechanisms to hide content from view, from the accessibility tree, and from both, such as the WAI-ARIA attribute `aria-hidden`, the HTML attribute `hidden`, and the CSS property `display:none`. Explain that code needs to reflect the current state of each of the application widgets.

#### Ideas to Assess Knowledge for Topic

Optional ideas to support assessment:

* Practical &mdash; Give students a rich application containing different views and ask students to code mechanisms to update titles,  headings, and regions depending on the currently visible section. Assess students' knowledge of how to code updates for application structural components.
* Practical &mdash; Give students a rich application containing different views that show and hide based on user interaction and ask students to update the DOM structure accordingly. Assess students' knowledge of how to provide a coherent DOM structure depending on the  displayed application widgets.
* Practical &mdash; Give students an application with content that can be shown to and hidden from the user; for example, an application to create presentation slides. Ask students to ensure that the code reflects the shown and hidden states of the content; for example, by using the WAI-ARIA attribute `aria-hidden`, the HTML attribute `hidden`, and the CSS property `display: none`. Assess students' knowledge of how to code `displayed` and `hidden` states of application views.

{% include excol.html type="end" %}

{% include excol.html type="start" %}

### Topic: Keyboard and Focus Interactions

{% include excol.html type="middle" %}

Build on the [Topic Keyboard and Focus Management in Module 6](/curricula/custom-widgets/#topic-keyboard-and-focus-management) to extend the concept to entire applications with multiple widgets. Demonstrate the importance of consistent keyboard commands and predictable behavior across the entire application. Explain how change of screens in Single Page Applications (SPA) and modal dialogs require particular focus management.

#### Learning Outcomes for Topic

Students should be able to:

* explain how people with different types of disabilities interact with widgets, including keyboard only and voice interaction users, and how keyboard commands, including tab, arrow, and shortcut keys, are used to operate widgets
* explain how people with different types of disabilities rely on focus indicators that are provided in the code and visually
* write code to enable applications to be operated using the keyboard only and other input devices, such as voice interaction
* ensure consistent use of keyboard commands, including tab, arrow, and shortcut keys, across the entire application
* ensure that navigating through different parts of the application does not initiate change of context without prior notice
* ensure that the focus is placed appropriately when new screens are generated in Single Page Applications (SPA); for example, at the beginning of the content to replicate the behavior of page reloads for assistive technologies
* ensure that the focus is placed appropriately when inline error messages are generated for application form controls
* write code to place focus in modal dialogs at the beginning of the dialog, to confine focus to the dialog until it is closed, and to return the focus  to the appropriate place in the main content after the dialog is closed
* identify when changes in applications, such as adding, removing, and updating content, impact the current focus and sequence of content, and write code to restore appropriate focus and meaningful sequence when such changes occur
* describe related requirements for content authors and designers to provide distinguishable styles for focus indicators

#### Teaching Ideas for Topic

Optional ideas to teach the learning outcomes:

* Explain that the tab sequence needs to be preserved so that keyboard users can navigate across the different widgets and content areas of applications, such as different toolbars and menus. Emphasize that native HTML elements are recommended regardless of the nature of the application in use, as they inherit all the necessary semantic properties that make them usable with the keyboard.
* Demonstrate use of common shortcut keys for rich applications, such as to create a new message in a web-based email client or to move to the menu bar in a web-based word processor. Explain that these shortcut keys should avoid any conflict with key combinations of both browsers and assistive technologies. Emphasize that application functionality should rely as much as possible on standard keyboard conventions and on expected navigational mechanisms, as non-standard keyboard shortcuts may sometimes be difficult to remember for some users or impossible to use due to their specific configurations.
* Demonstrate assistive technology interaction with rich applications such as Single Page Applications (SPA). Explain that assistive technologies may not perceive content changes by default unless there is a page reload. Emphasize that each time the view changes, a message indicating the currently selected view should be provided to assistive technologies via a live region.
* Explain techniques to set focus to the most relevant place in an application, such as a newly loaded screen, a form control containing input errors, the default button in a dialog, and the control that originated a modal dialog. Mention that coding keyboard and focus interactions is a developer's responsibility, whereas defining such interactions is a responsibility shared with the designer.
* Demonstrate the use of mechanisms to communicate information about the available keyboard shortcuts in rich applications, such as web-based email clients, spreadsheets, and word processors. Explain that when an application makes extensive use of non-standard keyboard shortcuts, a mechanism that provides users with information about these shortcuts is necessary. Mention that  coding these messages is a developer's responsibility, whereas providing them is a responsibility shared with the designer.
* Demonstrate accessible and inaccessible modal dialogs. Emphasize how focus remains within the boundaries of the dialogs when they have been coded appropriately. Explain that content that is not part of the modal dialog should not be focusable as long as the modal dialog is displayed.

#### Ideas to Assess Knowledge for Topic

Optional ideas to support assessment:

* Practical &mdash; Give students a Single Page Application (SPA) with several screens that show and hide based on user interaction. Ask students to set focus to the specific displayed widget. Assess students' knowledge of how to place focus on a specific application widget based on its state or relevance.
* Practical &mdash; Give students an application that makes extensive use of non-standard keyboard shortcuts and ask students to code a help widget that explains such keyboard shortcuts. Assess students' knowledge of how to provide specific help based on the implemented application keyboard shortcuts.
* Practical &mdash; Give students an application containing modal dialogs and ask students to set focus to the most relevant place based on user interaction. Assess students' knowledge of how to set focus to the dialog when it appears and to the element that originated it when it disappears.

{% include excol.html type="end" %}

{% include excol.html type="start" %}

### Topic: Concurrent Notifications

{% include excol.html type="middle" %}

Build on the [Topic: Notifications in Module 5](/curricula/developer-modules/forms/#topic-notifications) to extend the concept to entire applications with multiple widgets. Explain how notifications from different parts of the application need to be queued and prioritized to avoid overloading and confusing users. Demonstrate how unobtrusive and coordinated notifications benefit people using different types of assistive technologies.

#### Learning Outcomes for Topic

Students should be able to:

* explain how multiple concurrent notifications could occur in applications and describe ways to prioritize such notifications
* identify and write code for the appropriate values `polite`, `assertive`, and `off` for WAI-ARIA `aria-live` regions across entire applications
* identify and write code for relevant updates using the WAI-ARIA attribute `aria-relevant` with the values `additions`, `removals`, and `all`
* identify and write code for status messages that may originate from any particular widget or part of the application using the WAI-ARIA `role="status"`
* write code for alerts using WAI-ARIA `role="alert"` and identify situations in which it is appropriate to interrupt users
* write code for messages containing non-essential information using the WAI-ARIA `role="log"`, and `role="marquee"`,
* write code for numerical counters using the WAI-ARIA `role="timer"`
* write code to switch notifications on and off to avoid conflicts with assistive technologies presenting several notifications at the same time
* describe related requirements for content authors and designers to provide clear and concise notifications

#### Teaching Ideas for Topic

Optional ideas to teach the learning outcomes:

* Demonstrate interaction to request data from applications, such as making a data request for new emails and operating an address lookup. Explain that these data exchanges could be skipped by users of assistive technologies if they are not marked up correctly. Emphasize that live regions to indicate that new data is being loaded and that there is a waiting time should be provided so that users are aware of what is going on.
* Compare accessible and inaccessible examples of applications confirmation messages warning about critical errors that can cause data loss, and progress bars indicating timeouts. Explain that, when these messages are populated, these should be given high priority in the list of the live regions so that users can take action to avoid data loss and to solve the problem.

#### Ideas to Assess Knowledge for Topic

Optional ideas to support assessment:

* Practical &mdash; Ask students to code an alert to prevent users from quitting a word processor without saving changes. Assess students' knowledge of how to use assertive live regions to provide such alerts.
* Practical &mdash; Give students a Single Page Application (SPA) with several views and ask students to code the messages for assistive technologies to indicate what is the currently loaded view. Assess students' knowledge of how to use polite live regions to provide individual notifications based on the currently selected application view

{% include excol.html type="end" %}

## Ideas to Assess Knowledge for Module

Optional ideas to support assessment:

* Practical &mdash; Supervise students using different mechanisms that assistive technologies provide to navigate within rich applications, such as move through headings, regions, and interact with updates and notifications. Assess students’ knowledge of mechanisms of assistive technologies to interact and operate rich applications.
* Portfolio &mdash; Students build an accessible single page application. Assess students' knowledge of how to communicate structural elements state changes, keyboard and focus interactions, notifications, and updates to assistive technologies.

## Teaching Resources

Suggested resources to support your teaching:

* [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices/) &mdash; Provides readers with an understanding of how to use WAI-ARIA 1.1 to create accessible rich internet applications.
* [How People with Disabilities Use the Web](/people-use-web/) &mdash; Provides stories of people with disabilities using the Web; describes types of disabilities and some of the barriers that people encounter using the Web; and introduces types of assistive technologies and adaptive strategies that some people use.
* [Notifications and Feedback (Web Accessibility Perspectives)](https://www.w3.org/WAI/perspective-videos/notifications/) &mdash; Is one of the Web accessibility perspectives videos that show accessibility features and how they impact people with disabilities.
* [Keyboard Compatibility (Web Accessibility Perspectives)](https://www.w3.org/WAI/perspective-videos/keyboard/) &mdash; Is one of the Web accessibility perspectives videos that show accessibility features and how they impact people with disabilities.
* [Text to Speech (Web Accessibility Perspectives)](https://www.w3.org/WAI/perspective-videos/speech/) &mdash; Is one of the Web accessibility perspectives videos that show accessibility features and how they impact people with disabilities.
* [Clear Layout and Design (Web Accessibility Perspectives)](https://www.w3.org/WAI/perspective-videos/layout/) &mdash; Is one of the Web accessibility perspectives videos that show accessibility features and how they impact people with disabilities.
* [WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/) &mdash; Address accessibility of web content on desktops, laptops, tablets, and mobile devices.
* [WAI-ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) &mdash; Describes the roles, states, and properties that define accessible user interface elements and can be used to improve the accessibility and interoperability of web content and applications.
* [HTML5 living standard {% include_cached icon.html name="external-link" %}](https://html.spec.whatwg.org/multipage/) &mdash; The core markup language for the web.
* [DOM Living Standard {% include_cached icon.html name="external-link" %}](https://dom.spec.whatwg.org/)