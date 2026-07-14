---
tags:
  - website-requirements
  - user-experience
  - loading-speed
  - technical
  - design
  - strategy
---

# GENERAL REQUIREMENTS

+-----+----------------------------------------------------------------+
| 1\. | The website must provide a seamless and consistent user        |
|     | experience across the following devices and operating systems: |
|     |                                                                |
|     | -   *Mobile devices:*                                          |
|     |                                                                |
|     |     -   iOS, Android (latest stable release and one previous   |
|     |         version)                                               |
|     |                                                                |
|     | -   *Tablet devices:*                                          |
|     |                                                                |
|     |     -   iOS, Android (latest stable release and one previous   |
|     |         version)                                               |
|     |                                                                |
|     | -   *Desktop & mobile browsers:*                               |
|     |                                                                |
|     |     -   Google Chrome                                          |
|     |                                                                |
|     |     -   Safari                                                 |
|     |                                                                |
|     |     -   Mozilla Firefox                                        |
|     |                                                                |
|     |     -   Microsoft Edge                                         |
|     |                                                                |
|     |     -   The website should support the latest stable version   |
|     |         and 2 previous versions.                               |
|     |                                                                |
|     | -   The website must be responsive and adaptive to the         |
|     |     following screen sizes and resolutions:                    |
|     |                                                                |
|     |     -   Mobile devices: Small screens (up to 480px wide),      |
|     |         medium screens (481px to 768px wide)                   |
|     |                                                                |
|     |     -   Tablet devices: Medium to large screens (769px to      |
|     |         1024px wide)                                           |
|     |                                                                |
|     |     -   Desktop devices: Large screens (1025px and above)      |
+-----+----------------------------------------------------------------+
| 2\. | The UI design should consider different user types and meet    |
|     | international accessibility standards such as W3C WCAG2.       |
+-----+----------------------------------------------------------------+
| 3\. | The website should load within \<2 seconds on average across   |
|     | all supported devices and browsers, even under moderate        |
|     | network conditions (3G/4G for mobile; 50 Mbits/sec).           |
|     |                                                                |
|     | Acceptance test to be performed at the key markets:            |
|     |                                                                |
|     | -   US                                                         |
|     |                                                                |
|     | -   Colombia                                                   |
|     |                                                                |
|     | -   Mexico                                                     |
|     |                                                                |
|     | -   Peru                                                       |
|     |                                                                |
|     | -   EU                                                         |
|     |                                                                |
|     | If load, re-load and update time takes more than 2 seconds and |
|     | it is approved by JVL, the page should utilise level-of-detail |
|     | and/or load-by-priority practices, supported with 'loading'    |
|     | animations.                                                    |
+-----+----------------------------------------------------------------+
| 4\. | The system should be accessible by 10000 users with a high     |
|     | concurrency ratio that could reach up to 100 concurrent users  |
|     | in the following 5 years without any impact on the             |
|     | performance.                                                   |
+-----+----------------------------------------------------------------+
| 5\. | By default, new pages should open in a new browser tab unless  |
|     | specified otherwise.                                           |
+-----+----------------------------------------------------------------+
| 6\. | The website should include breadcrumb navigation on all pages  |
|     | except the landing page to help users understand their         |
|     | location within the site\'s hierarchy and easily navigate back |
|     | to previous sections.                                          |
+-----+----------------------------------------------------------------+
| 7\. | The website must comply with relevant data protection          |
|     | regulations, ensuring that all user data is handled securely   |
|     | and with respect to user privacy.                              |
+-----+----------------------------------------------------------------+
| 8\. | Website to be designed, implemented and deployed with the      |
|     | understanding that at further stages it will be constantly     |
|     | populated with new type of content, functionality and          |
|     | features.                                                      |
|     |                                                                |
|     | Architecture and Design solution should allow all updates and  |
|     | expansions in a cost- and technically effective way            |
+-----+----------------------------------------------------------------+
| 9\. | Website data and content should be designed and implemented in |
|     | the way allowing it to be used for SEO purposes.               |
|     |                                                                |
|     | The major SEO website area is considered 'Blog' rich-text and  |
|     | images pages.                                                  |
+-----+----------------------------------------------------------------+

# FUNCTIONAL REQUIREMENTS

## 

## EPIC-1: LANDING PAGE

+-----------------------------------------------------------------------+
| ## \[LANDING PAGE\] Add website header with the main menu items       |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to see a header  |
| with the menu items at the top of each website page so that I can     |
| easily access different sections of the website.                      |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  A header should be present at the top of all website pages.       |
|                                                                       |
| 2.  The header should contain the JVL logo.                           |
|                                                                       |
| 3.  Clicking on the JVL logo should redirect the user to the landing  |
|     page.                                                             |
|                                                                       |
| 4.  The header should include the following menu items:               |
|                                                                       |
| -   Games                                                             |
|                                                                       |
| -   About JVL                                                         |
|                                                                       |
| -   Contact                                                           |
|                                                                       |
| 5.  Each menu item should be a clickable link that redirects to the   |
|     corresponding page.                                               |
|                                                                       |
| 6.  On smaller screens, the header should be collapsed into hamburger |
|     menus.                                                            |
|                                                                       |
| 7.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605915113527&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[LANDING PAGE\] View JVL info section on the Landing Page         |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to view the      |
| information about JVL on the landing page so that I can learn more    |
| about the company.                                                    |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The landing page should display the following content about JVL:  |
|                                                                       |
|     a.  Card with a JVL intro video with the ability to play straight |
|         on the page                                                   |
|                                                                       |
|     b.  2-3 cards with the game image and text description            |
|                                                                       |
|     c.  1 'latest news' (meet us at the conference) card with the     |
|         image and text description                                    |
|                                                                       |
|     d.  Clicking on the card should redirect to the relevant page     |
|                                                                       |
|     e.  Cards should be played automatically                          |
|                                                                       |
|     f.  Each card should have a clear call to action                  |
|                                                                       |
|     g.  \[Welcome to JVL!\] text company description                  |
|                                                                       |
|         i.  It should be possible to apply basic formatting to the    |
|             description                                               |
|                                                                       |
| 2.  The content of this section should be managed in CMS.             |
|                                                                       |
| 3.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605914730700&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \                                                                  |
| [LANDING PAGE\] View "Discover Our Games" section on the Landing Page |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to view the list |
| of available game categories on the landing page so that I can choose |
| the category I am interested in before viewing the list of related    |
| games.                                                                |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The "Discover Our Games" section should be displayed on the       |
|     landing page.                                                     |
|                                                                       |
| 2.  The section should display the game themes defined in the CMS.    |
|                                                                       |
| 3.  Each game theme on the list should have an image and a name       |
|     representing it.                                                  |
|                                                                       |
|     a.  Custom list order should be applied based on the FE layout    |
|         and size of the theme image.                                  |
|                                                                       |
| 4.  Clicking on the game theme should redirect the user to the Games  |
|     page with the list of games pre-filtered by the theme.            |
|                                                                       |
| 5.  The user should be able to redirect to the list of all games from |
|     the "Discover Our Games" section.                                 |
|                                                                       |
| 6.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605914730685&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[LANDING PAGE\] Add website footer                                |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to see a footer  |
| at the bottom of each website page so that I can access additional    |
| information and links.                                                |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The footer should be present at the bottom of every website page. |
|                                                                       |
| 2.  The footer should include the following elements:                 |
|                                                                       |
|     a.  LinkedIn logo with the redirect to LinkedIn portal            |
|                                                                       |
|     b.  Youtube logo with the redirect to Youtube portal              |
|                                                                       |
|     c.  18+ logo                                                      |
|                                                                       |
|     d.  Text information about licenses                               |
|                                                                       |
|     e.  Copyright notice                                              |
|                                                                       |
|     f.  3-4 additional logos with the redirects to external portals   |
|                                                                       |
| 3.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605914730786&cot=10> |
+-----------------------------------------------------------------------+

# EPIC-2: GAMES SECTION

+-----------------------------------------------------------------------+
| ## \[GAMES\] View games list                                          |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to see a list of |
| games on the Games page so that I can easily browse through all       |
| available games.                                                      |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  New item "Games" should be added to the main menu.                |
|                                                                       |
| 2.  When the user opens the Games page, the system should display the |
|     list of all available games as defined by the CMS.                |
|                                                                       |
|     a.  The criteria of "available game" is to be defined once the    |
|         CMS is selected.                                              |
|                                                                       |
| 3.  Each game on the list should be represented with the game\'s name |
|     and logo set in CMS.                                              |
|                                                                       |
| 4.  The total number of games should be displayed at the top of the   |
|     list.                                                             |
|                                                                       |
| 5.  The list should include pagination to navigate through multiple   |
|     pages of games.                                                   |
|                                                                       |
| 6.  Each page should display 20 games.                                |
|                                                                       |
| 7.  The list should be sorted based on the date of adding the game to |
|     CMS from the oldest to newest or based on the game list position  |
|     set in CMS (preferred option, if available in CMS).               |
|                                                                       |
| 8.  Clicking on the game logo should navigate to a single game view   |
|     page.                                                             |
|                                                                       |
| 9.  The page should be implemented in such a way that it supports     |
|     adding sub-items (All, Cabinet, Online, Skill) in future.         |
|                                                                       |
| 10. UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605917692259&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[GAMES\] View featured game                                       |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to see a         |
| featured game at the top of the Games page so that I can quickly view |
| and start playing the highlighted game.                               |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The featured game should be displayed at the top of the Games     |
|     section.                                                          |
|                                                                       |
| 2.  The featured game should be configurable via CMS.                 |
|                                                                       |
| 3.  The featured game should include the game\'s name, description,   |
|     and an image.                                                     |
|                                                                       |
| 4.  There should be a \"Let\'s Go\" button associated with the        |
|     featured game.                                                    |
|                                                                       |
| 5.  Clicking the \"Let\'s Go\" button should redirect the user to the |
|     single game view page.                                            |
|                                                                       |
| 6.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605917692261&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[GAMES\] Search for a game                                        |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to search for a  |
| game by name through the games list on the Games page so that I can   |
| quickly find a specific game I am interested in.                      |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The Games list should include a search bar.                       |
|                                                                       |
| 2.  Users should be able to search for a game by name.                |
|                                                                       |
| 3.  The system should start showing results starting from the 2nd     |
|     character input.                                                  |
|                                                                       |
| 4.  The search results should display games that match the entered    |
|     query.                                                            |
|                                                                       |
| 5.  The search should support partial matches (e.g., searching for    |
|     \"pok\" should return \"Poker\" and \"Video Poker\").             |
|                                                                       |
| 6.  The search results should be displayed in the same format as the  |
|     games list.                                                       |
|                                                                       |
| 7.  The search component should be implemented in such a way it is    |
|     re-usable on other pages.                                         |
|                                                                       |
| 8.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605917692262&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[GAMES\] Filter games list                                        |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to filter the    |
| games list by various criteria so that I can find games that match my |
| preferences.                                                          |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The Games section should include filters for the following        |
|     criteria:                                                         |
|                                                                       |
| -   Theme                                                             |
|                                                                       |
|     -   List of themes from CMS                                       |
|                                                                       |
|     -   Multiselect                                                   |
|                                                                       |
| -   Features                                                          |
|                                                                       |
|     -   List of features from CMS                                     |
|                                                                       |
|     -   Multiselect                                                   |
|                                                                       |
| -   Volatility                                                        |
|                                                                       |
|     -   List of volatilities from CMS                                 |
|                                                                       |
|     -   Multiselect                                                   |
|                                                                       |
| 2.  Users should be able to apply multiple filters simultaneously.    |
|                                                                       |
| 3.  If any filters have been applied prior to initiating a search,    |
|     the search should be conducted within the filtered dataset.       |
|                                                                       |
| 4.  The search results should only display games that match both the  |
|     search query and the applied filter criteria.                     |
|                                                                       |
| 5.  If the user tries to apply the filter after performing a search,  |
|     the system should apply the filters to the search results.        |
|                                                                       |
| 6.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605917692264&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[GAMES\] View single game                                         |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to view detailed |
| information about a single game so that I can decide if I want to     |
| play it.                                                              |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The user should be able to access the single game view from the   |
|     games list on the "Games" page.                                   |
|                                                                       |
| 2.  The system should display the following information on a single   |
|     game view page:                                                   |
|                                                                       |
| -   Video of the game with the ability to play in the view window     |
|                                                                       |
|     -   Video source can be either Youtube or an internal server      |
|                                                                       |
| -   5-4 game screens (in the same window as the Youtube video)        |
|                                                                       |
| -   Game general info                                                 |
|                                                                       |
|     -   Icon                                                          |
|                                                                       |
|     -   Name                                                          |
|                                                                       |
|     -   Subtitle                                                      |
|                                                                       |
| -   Game theme - text, 1 game can have multiple themes                |
|                                                                       |
| -   Game volatility                                                   |
|                                                                       |
| -   Reels configuration - text, 1 game can have 1 config              |
|                                                                       |
| -   Paylines - text, 1 game can have 1 payline configuration          |
|                                                                       |
| -   Game 5 first features as added in CMS, where each feature will    |
|     have:                                                             |
|                                                                       |
|     -   Name                                                          |
|                                                                       |
|     -   Description                                                   |
|                                                                       |
|     -   Optional image                                                |
|                                                                       |
| -   Game description:                                                 |
|                                                                       |
|     -   Title                                                         |
|                                                                       |
|     -   Body                                                          |
|                                                                       |
|     -   Image space (optional)                                        |
|                                                                       |
|         -   Title                                                     |
|                                                                       |
|         -   Body                                                      |
|                                                                       |
|         -   Image itself                                              |
|                                                                       |
| -   Reviews list                                                      |
|                                                                       |
|     -   Reviewer name                                                 |
|                                                                       |
|     -   URL                                                           |
|                                                                       |
|     -   Image                                                         |
|                                                                       |
| 3.  The user should be able to redirect to the next game or to the    |
|     previous game on the list of all games from the single game view  |
|     page.                                                             |
|                                                                       |
| 4.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605919244735&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[GAMES\] Add Play the Game to the single game view page           |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to have the      |
| option to test the game before making a purchase, so that I can       |
| ensure it meets my expectations and decide if it\'s the right choice  |
| for me.                                                               |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  When the user navigates to a single game view page, then they     |
|     should see an option to access a demo version of the game.        |
|                                                                       |
| 2.  Given the user clicks on the demo option, then the demo version   |
|     of the game should load within an iFrame embedded on the same     |
|     game page or a designated demo page.                              |
|                                                                       |
| 3.  The link to the demo for a game should be configurable in CMS.    |
+-----------------------------------------------------------------------+

# EPIC-3: GENERAL INFO PAGES (ABOUT US, CONTACT US, PARTNERS)

+-----------------------------------------------------------------------+
| ## \[ABOUT US\] Add About Us information to the JVL portal            |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to access        |
| \'About Us\' information on the website so that I can learn more      |
| about the company\'s history, awards and partners.                    |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  When a visitor navigates to the JVL public portal, then they      |
|     should be able to find and access an "About Us" page from the     |
|     main navigation menu.                                             |
|                                                                       |
| 2.  The "About Us" page should include sections for:                  |
|                                                                       |
|     a.  Title                                                         |
|                                                                       |
|     b.  Company history timeline, where each milestone should be      |
|         represented with                                              |
|                                                                       |
|         i.  Year                                                      |
|                                                                       |
|         ii. Description                                               |
|                                                                       |
|         iii. Image                                                    |
|                                                                       |
|     c.  Mission                                                       |
|                                                                       |
|     d.  Values                                                        |
|                                                                       |
|     e.  Partners section with (assumed will be managed in CMS):       |
|                                                                       |
|         i.  Section title                                             |
|                                                                       |
|         ii. List of partner brands where each brand is represented    |
|             with a logo                                               |
|                                                                       |
|             1.  Logo contains a url link to the partners website      |
|                                                                       |
|         iii. General description for the partners brands sub-section  |
|                                                                       |
|         iv. List of media partners where each brand is represented    |
|             with a logo                                               |
|                                                                       |
|         v.  General description for the media partners sub-section    |
|                                                                       |
| 3.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605921578740&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[CONTACT US\] Add company Contact Us form to the JVL portal       |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to access the    |
| company contact information and use specific contact forms so that I  |
| can communicate my inquiries or feedback appropriately.               |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  When a visitor navigates to the JVL public portal, then they      |
|     should be able to find and access an "Contact Us" page from the   |
|     main navigation menu.                                             |
|                                                                       |
| 2.  The \"Contact Us\" page should display the company\'s main        |
|     contact information, including the company's address, phone       |
|     number, email, and social media links.                            |
|                                                                       |
| 3.  The \"Contact Us\" page should provide options to select one of   |
|     the four types of contact forms:                                  |
|                                                                       |
|     a.  Casino                                                        |
|                                                                       |
|     b.  Platform                                                      |
|                                                                       |
|     c.  Media Partner                                                 |
|                                                                       |
|     d.  General                                                       |
|                                                                       |
| 4.  When the user selects the \"Casino\" contact form, the system     |
|     should capture the following fields:                              |
|                                                                       |
|     a.  Name                                                          |
|                                                                       |
|     b.  Casino name                                                   |
|                                                                       |
|     c.  Email                                                         |
|                                                                       |
|     d.  Description                                                   |
|                                                                       |
| 5.  When the user selects the \"Platform\" contact form, the system   |
|     should capture the following fields:                              |
|                                                                       |
|     a.  Name                                                          |
|                                                                       |
|     b.  Platform name                                                 |
|                                                                       |
|     c.  Email                                                         |
|                                                                       |
|     d.  Description                                                   |
|                                                                       |
| 6.  When the user selects the \"Media Partner\" contact form, the     |
|     system should capture the following fields:                       |
|                                                                       |
|     a.  Name                                                          |
|                                                                       |
|     b.  Media platform name                                           |
|                                                                       |
|     c.  Email                                                         |
|                                                                       |
|     d.  Description                                                   |
|                                                                       |
| 7.  When the user selects the \"General\" contact form, the system    |
|     should capture the following fields:                              |
|                                                                       |
|     a.  Name                                                          |
|                                                                       |
|     b.  Email                                                         |
|                                                                       |
|     c.  Description                                                   |
|                                                                       |
| 8.  Submission of any form described above should trigger an          |
|     automatic lead creation in the integrated CRM.                    |
|                                                                       |
| 9.  After submitting any contact form, the visitor should see a       |
|     confirmation message on the screen indicating that their request  |
|     has been either successfully submitted or that an error occurred  |
|     with the instruction on the next action expected from the         |
|     visitor.                                                          |
|                                                                       |
| 10. Each contact form should include validation to ensure all         |
|     required fields are completed and that the information entered is |
|     in the correct format (e.g., valid email address).                |
|                                                                       |
|     a.  All fields in the forms above are required.                   |
|                                                                       |
| 11. Error messages should be displayed for any invalid or incomplete  |
|     fields.                                                           |
|                                                                       |
| 12. All form submissions should be securely transmitted and handled   |
|     in accordance with data privacy regulations.                      |
|                                                                       |
| 13. The \"Contact Us\" page content and form configurations should be |
|     manageable through the CMS.                                       |
|                                                                       |
| 14. UI and Content ref: <https://yggdrasilgaming.com/contact>         |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[PARTNERS\] View all JVL partners                                 |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to view all JVL  |
| partners, including different types of partners so that I can         |
| understand the scope and diversity of JVL\'s partnerships.            |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  When a visitor navigates to the JVL public portal, then they      |
|     should be able to find and access the "Partners" page from the    |
|     main menu (between About Us and Contact items).                   |
|                                                                       |
| 2.  The \"Partners\" page should list all JVL partners, categorized   |
|     by the types of partners configured in CMS.                       |
|                                                                       |
| 3.  Each partner entry should include the partner\'s logo and URL     |
|     leading to the partner's website.                                 |
|                                                                       |
| 4.  The \"Partners\" page should have clear sections for each type of |
|     partner, with appropriate headings for each category.             |
|                                                                       |
| 5.  Within each category, partners should be listed based on their    |
|     list position set in CMS.                                         |
|                                                                       |
| 6.  Each partner\'s entry should be visually consistent, maintaining  |
|     the same format for all partners.                                 |
|                                                                       |
| 7.  The \"Partners\" page content should be manageable through the    |
|     CMS.                                                              |
|                                                                       |
| 8.  The "Partners" page should also contain the link to the Contact   |
|     Us page with the description.                                     |
|                                                                       |
| 9.  UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764571380866460&cot=14> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[LATEST NEWS\] View latest news on the landing page               |
+-----------------------------------------------------------------------+
| As a visitor to the JVL public client portal, I want to see the       |
| latest news section on the landing page so that I can stay updated    |
| with recent developments and information.                             |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The latest news section should be displayed on the landing page.  |
|                                                                       |
| 2.  The section should be presented in the form of cards.             |
|                                                                       |
| 3.  The section should display up to 4 cards.                         |
|                                                                       |
| 4.  If there are more than 4 cards to display, a horizontal scroll    |
|     should be applied to the list.                                    |
|                                                                       |
| 5.  If there is nothing to display, the section should be hidden.     |
|                                                                       |
| 6.  Each news card should include the following required elements:    |
|                                                                       |
|     a.  Title                                                         |
|                                                                       |
|     b.  Image                                                         |
|                                                                       |
|     c.  Date of publication                                           |
|                                                                       |
|     d.  First part of the news description which fits the card,       |
|         ending with "\..."                                            |
|                                                                       |
|     e.  A source link that directs to the full article                |
|                                                                       |
| 7.  Clicking on the title or image of a news piece should open the    |
|     full article in a new tab.                                        |
|                                                                       |
| 8.  Administrators should be able to add, edit, or remove news pieces |
|     through the CMS.                                                  |
|                                                                       |
| 9.  The CMS should allow the upload of the main image, title, date of |
|     publication, descriptions, images to descriptions and links to    |
|     the full article.                                                 |
|                                                                       |
| 10. UI example:                                                       |
|     <https://miro                                                     |
| .com/app/board/uXjVNeAZgHw=/?moveToWidget=3458764605923319323&cot=10> |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[BLOG\] View blog page                                            |
+-----------------------------------------------------------------------+
| As a JVL marketing specialist, I want to have a dedicated blog page   |
| on the JVL public website so that I can use these blog articles for   |
| Google indexation.                                                    |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The blog page should be accessible from the main navigation menu  |
|     of the website.                                                   |
|                                                                       |
| 2.  The blog page should display articles cards based on the grid     |
|     layout.                                                           |
|                                                                       |
| 3.  Each card should include the following elements:                  |
|                                                                       |
|     a.  Title                                                         |
|                                                                       |
|     b.  Date of publication                                           |
|                                                                       |
|     c.  Image                                                         |
|                                                                       |
|     d.  Short description                                             |
|                                                                       |
|     e.  Description limited by the card size and user display size.   |
|                                                                       |
|     f.  Link to the original source (optional)                        |
|                                                                       |
| 4.  The blog page should display up to \[X\] blog cards per page.     |
|                                                                       |
| 5.  The cards should be displayed in a chronological order from the   |
|     newest to the oldest.                                             |
|                                                                       |
| 6.  It should be possible to sort the cards by the publication date.  |
|                                                                       |
| 7.  Pagination or infinite scrolling should be implemented to manage  |
|     the display of additional blog articles.                          |
|                                                                       |
| 8.  The blog page should support content from the internal blog       |
|     managed by the CMS.                                               |
|                                                                       |
| 9.  Administrators should be able to add, edit, or remove blog        |
|     articles through the CMS.                                         |
|                                                                       |
| 10. The CMS should allow the upload of images, entry of titles,       |
|     descriptions, and links to the full articles.                     |
|                                                                       |
| 11. Each blog article should be optimized for search engines with     |
|     appropriate meta tags, keywords, and descriptions.                |
|                                                                       |
| 12. The blog page and articles should have a clear and logical URL    |
|     structure that supports Google indexation.                        |
|                                                                       |
| 13. The CMS should allow administrators to add meta tags, keywords,   |
|     and descriptions to each blog article.                            |
|                                                                       |
| 14. UI and Content ref: <https://yggdrasilgaming.com/news>            |
+-----------------------------------------------------------------------+

# EPIC-4: ONLINE USER ROLE

+-----------------------------------------------------------------------+
| ## \[ONLINE USER ROLE\] Sign in / sign out for registered users       |
+-----------------------------------------------------------------------+
| As a registered user of the JVL website, I want to be able to sign in |
| and sign out of my account so that I can access content that is       |
| available only to registered users.                                   |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The user should be able to navigate to the sign-in page from the  |
|     main menu.                                                        |
|                                                                       |
| 2.  The user should be able to sign in with their email and password. |
|                                                                       |
| 3.  The email field should accept only valid email addresses.         |
|                                                                       |
| 4.  The password field should mask the input to ensure privacy.       |
|                                                                       |
| 5.  Upon clicking the sign-in button, the system should validate the  |
|     provided credentials against the users existing in the database.  |
|                                                                       |
|     a.  *The users will be added to the database manually with one    |
|         role "Online". In future, there will be other roles required  |
|         (e.g., Cabinets Viewer role)*                                 |
|                                                                       |
| 6.  If the credentials are correct, the user should be redirected to  |
|     the lending page or the previously intended page.                 |
|                                                                       |
| 7.  If the credentials are incorrect, a relevant error message should |
|     be displayed:                                                     |
|                                                                       |
|     a.  Invalid email format                                          |
|                                                                       |
|     b.  Incorrect email or password                                   |
|                                                                       |
|     c.  Unregistered email addresses                                  |
|                                                                       |
| 8.  A signed-in user should be able to sign out from the main menu.   |
|                                                                       |
| 9.  The system should automatically sign out the signed in user after |
|     \[X\] time of inactivity.                                         |
|                                                                       |
| 10. UI ref: <https://slotmatrix.com/login/>                           |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[ONLINE USER ROLE\] Add landing page for registered users         |
+-----------------------------------------------------------------------+
| As a registered user of the JVL website, I want to access a landing   |
| page that displays game assets and general JVL assets available only  |
| for registered users so that I can easily find and utilize the        |
| resources available to me.                                            |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The user is automatically directed to the landing page after      |
|     signing in.                                                       |
|                                                                       |
| 2.  The landing page should display the following sections:           |
|                                                                       |
|     a.  All Games Assets                                              |
|                                                                       |
|     b.  General Assets                                                |
|                                                                       |
|     c.  Games List                                                    |
|                                                                       |
| 3.  The **All Games Assets** section should display the following     |
|     list of assets:                                                   |
|                                                                       |
|     a.  Asset Package                                                 |
|                                                                       |
|     b.  Game Rules                                                    |
|                                                                       |
|         i.  All                                                       |
|                                                                       |
|         ii. English                                                   |
|                                                                       |
|         iii. Finnish                                                  |
|                                                                       |
|         iv. German                                                    |
|                                                                       |
|         v.  etc.                                                      |
|                                                                       |
|     c.  Game Sheet                                                    |
|                                                                       |
|     d.  Help Screens                                                  |
|                                                                       |
| 4.  The **General Assets** section should display the following list  |
|     of assets:                                                        |
|                                                                       |
|     a.  Master Game List                                              |
|                                                                       |
|     b.  Supported Currencies                                          |
|                                                                       |
|     c.  RGS Materials                                                 |
|                                                                       |
|     d.  JVL Vendor Materials                                          |
|                                                                       |
| 5.  The **Games List** should display the same list of games as on    |
|     the landing page for non-registered users with the possibility to |
|     redirect to the list of all games on the Games page.              |
|                                                                       |
| 6.  Each asset without sub-assets should be displayed as a name with  |
|     a link to either view or download the asset.                      |
|                                                                       |
| 7.  Each asset with sub-assets should be displayed as a name with a   |
|     link to view sub-assets.                                          |
|                                                                       |
| 8.  The user should be able to download each asset separately.        |
|                                                                       |
| 9.  Each asset file should be created and located to the storage      |
|     where it will be available for retrieval and made accessible on   |
|     the JVL website by the JVL team.                                  |
|                                                                       |
| 10. A game asset should be a single file. The expected sizes may      |
|     vary, but should support up to 30 GB per file.                    |
+-----------------------------------------------------------------------+
| For the page structure refer to the following reference:              |
|                                                                       |
| a.  https://slotmatrix.com/clients-area/games/                        |
|                                                                       |
| b.  User: <andreik@jvl.ca>                                            |
|                                                                       |
| c.  Pass: ***REMOVED***                                   |
|                                                                       |
| This part requires contractor's assistance with wireframes and        |
| specification.                                                        |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| ## \[ONLINE                                                           |
| USER ROLE\] View game attributes available only for registered users  |
+-----------------------------------------------------------------------+
| As an online user with a registered account on the JVL website, I     |
| want to view detailed game attributes that are available exclusively  |
| for registered users, so that I can make informed decisions and have  |
| a better understanding of the games.                                  |
+-----------------------------------------------------------------------+
| **Acceptance criteria:**                                              |
|                                                                       |
| 1.  The following additional game attributes and sections should be   |
|     displayed only for registered users on a single game view page:   |
|                                                                       |
|     a.  Game ID (unique, required for each game)                      |
|                                                                       |
|     b.  Category                                                      |
|                                                                       |
|     c.  Game Assets                                                   |
|                                                                       |
|     d.  Volatility                                                    |
|                                                                       |
|     e.  RTPs                                                          |
|                                                                       |
|     f.  Max Win                                                       |
|                                                                       |
|     g.  Min Bet                                                       |
|                                                                       |
|     h.  Max Bet                                                       |
|                                                                       |
|     i.  Certificates                                                  |
|                                                                       |
|         i.  List of files available for download                      |
|                                                                       |
|         ii. Should include the file name and link for download        |
+-----------------------------------------------------------------------+
| For the page structure refer to the following reference:              |
|                                                                       |
| a.  https://slotmatrix.com/clients-area/games/                        |
|                                                                       |
| b.  User: <andreik@jvl.ca>                                            |
|                                                                       |
| c.  Pass: ***REMOVED***                                   |
|                                                                       |
| This part requires contractor's assistance with wireframes and        |
| specification.                                                        |
+-----------------------------------------------------------------------+
