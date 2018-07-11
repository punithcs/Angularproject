# HTML Style Guide
----

## 1. Code structure

Coding should be well structured. ie, proper indentation and comments should be provided.

#### Example

#### Incorrect

    <div class="search-data-container">
        <div class="search-data-list">
            <div class="user-details-holder">
        <div class="user-name">User name</div>
        <div class="user-email">Email Address</div>
            </div>
        </div>
        </div>

#### Correct

    <!-- search area starts here -->
    <div class="search-data-container">
        <div class="search-data-list">
            <div class="user-details-holder">
                <div class="user-name">User name</div>
                <div class="user-email">Email Address</div>
            </div>
        </div>
    </div>
    <!-- search area ends here -->

NOTE: The above mentioned practices are suggested for development and programming phase, once the website/application is moved to production, all the comments and spaces will be removed as part of minifying.

## 2. Minimal code

Use minimum <div>s to make the code lite weighted.
   
    Don’t use unnecessary <div>s to wrap the elements and content.

## 3. Only one ID

Any element should not have more than 1 ID as per W3C standards.

## 4. ID/Class names

ID/Class names should not start with numbers.

#### Example

#### Incorrect

    <div class=”1-banner-section”>…</div>

#### Correct

    <div class=”banner-block”>…</div>
        

## 5. Unique IDs

A page cannot have a same ID more than once.


## 6. IDs for controls

All the actionable elements(textboxes, buttons, radiobuttons, checkoxes, dropdowns etc..,) should have        unique IDs.

## 7. Avoid inline styles.

Inline styles, while they have a purpose, generally are not the best way to maintain your website.

#### Example

#### Incorrect

    <div style="width:100px; height:55px; margin-top:20px;">
    </div>

#### Correct

    <div class="search-data-container">
    </div>

## 8. Close your tags.

Closing all your tags is a W3C specification. Some browsers may still render your pages correctly (under Quirks mode), but not closing your tags is invalid under standards.

## 9. A <div> tag should have a class or ID.

A div without class name or ID is not really necessary.

## 10. Use lower case markup.

It is an industry-standard practice to keep your markup lower-cased. Capitalizing your markup will work and will probably not affect how your web pages are rendered, but it does affect code readability.


#CSS Style Guide
----

## 1. Create readable CSS

#### Example

#### Incorrect

    .example { background: #cc0000;padding: 10px;border: 1px solid black;}

#### Correct

    .example {
        background: #cc0000;
        padding: 10px;
        border: 1px solid black;
    }
            

## 2. Use comments whenever needed.

#### Example

    // Styles for header starts here
    .hedaer-container {
        width: 1000px;
        height: 100px;
    }
    // Styles for header ends here

## 3. Combine CSS elements with common properties

Elements during a stylesheet typically share properties. Rather than re-writing previous code, simply mix them

#### Example

    h1, h2, h3 {
        font-family: verdana;
        color: #e1e1e1;
    }

## 4. Use appropriate naming convention

#### Example

#### Incorrect

    .right-div {
        width: 250px;
        padding: 10px;
    }

#### Correct

    .vision-container {
        width: 250px;
        padding: 10px;
    }


## 5. Use shorthand CSS.

#### Example

#### Incorrect

    .vision-container {
        margin-top: 5px
        margin-right: 10px
        margin-bottom: 5px;
        margin-left: 10px;
    }

#### Correct

    .vision-container {
        margin: 5px 10px 5px 10px;
    }
            

## 6. Make use of generic classes.

You'll find that there are certain styles that you're applying over and over. Instead of adding that particular style to each ID/class, you can create generic classes and add them to the IDs or other CSS classes.

#### Example

#### Incorrect

###### CSS
    .vision-container {
        margin: 0 auto;
        width: 200px;
        height: 55px;
    }

    .mission-container {
        margin: 0 auto;
        width: 300px;
        height: 65px;
    }

###### HTML 
    <div class="vision-container"></div>
    <div class="mission-container"></div>

#### Correct

###### CSS 
    .vision-container {
        width: 200px;
        height: 55px;
    }

    .mission-container {
        width: 300px;
        height: 65px;
    }

    .center-it {
        margin: 0 auto;
    }

###### HTML 
    <div class="vision-container center-it"></div>
    <div class="mission-container center-it"></div>
            

## 7. Use nested css only when necessary.

#### Reference links

    https://www.sitepoint.com/beware-selector-nesting-sass/
    http://thesassway.com/intermediate/avoid-nested-selectors-for-more-modular-css
    https://css-tricks.com/strategies-keeping-css-specificity-low/

## 8. Use SASS variable and mixins whenever possible.

## 9. Keep a library of helpful CSS classes

#### Example

    .width-100 {
        width: 100%;
    }

    .center-it {
        margin: 0 auto;
    }

## 10. Proper separation

Try to use "-" (hyphen) instead of "_" (underscore) for separating names in classes.

## 11. Try OOCSS or SMACSS

Try to use OOCSS or SMACSS guidelines to separate stylesheets by category.

#### Reference links

    http://oocss.org/
    https://smacss.com/
    http://thesassway.com/intermediate/using-object-oriented-css-with-sass
    https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/