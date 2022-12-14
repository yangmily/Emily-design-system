---
title: Text inputs
layout: variation
section: components
status: Released
description: 'Text fields give users the ability to enter text. They can be
  single-line or multi-line (textarea inputs).  '
variation_groups:
  - variation_group_name: Standard text inputs
    variations:
      - variation_code_snippet: >
          <!--States are shown for demonstration purposes only-->

          <label class="a-label a-label__heading" for="textinput-example-default">

          Default

          </label>

          <input class="a-text-input"
                type="text"
                id="textinput-example-default"
                placeholder="Enter text…"
                value="Placeholder text">
          <br><br>

          <label class="a-label a-label__heading" for="textinput-example-hover">

          Hover

          </label>

          <input class="a-text-input hover"
                 type="text"
                 id="textinput-example-hover"
                 placeholder="Enter text…"
                 value="Placeholder text">
          <br><br>

          <label class="a-label a-label__heading" for="textinput-example-focus">

          Focus

          </label>

          <input class="a-text-input focus"
                 type="text"
                 id="textinput-example-focus"
                 placeholder="Enter text…"
                 value="Lorem ipsum">
          <br><br>

          <label class="a-label a-label__heading" for="textinput-example-disabled">

          Disabled

          </label>

          <input class="a-text-input"
                 type="text"
                 id="textinput-example-disabled"
                 placeholder="Enter text…"
                 value="Lorem ipsum"
                 disabled>
        variation_specs: |-
          #### Default
          - Border: 1 px, Gray 60 (#919395)
          - Height: 35 px
          - Padding: 7px
          - Avenir Next Regular, 16px, Gray (#5a5d61)
          - Text should be in sentence case

          #### Hover
          - Border: 2 px, Pacific (#0072ce)

          #### Focus
          - Border: 2 px, Pacific (#0072ce)
          - Outline: Dotted 1px, Pacific (#0072ce)
          - Outline offset: 1px

          #### Disabled
          - Background: Gray 10 (#e7e8e9)
        variation_name: Single-line text inputs
        variation_description:
          Use to input single lines of text, for example email
          addresses, names, or search queries. The length of the input field
          should be proportional to the expected user input, so that the user
          can see what they've typed without having to scroll to reveal hidden
          content. See the guidelines section below for more information.
      - variation_name: Multi-line textarea inputs
        variation_description:
          Use for long-form answers that are more than a single
          word or two. Make sure the input size is big enough that the user can
          see what they've typed without having to scroll to reveal hidden
          content, and small enough that the user doesn't have  to navigate the
          viewport in order to see the entire field at once.
        variation_code_snippet: >-
          <label class="a-label a-label__heading"
          for="textarea-example-default">
              Label
          </label>

          <textarea class="a-text-input"
                    id="textarea-example-default"
                    placeholder="Enter text…">Placeholder text</textarea>
        variation_specs: |-
          * Border: 1 px, Gray 60 (#919395)
          * Avenir Next Regular, 16 px, Gray (#5a5d61)
    variation_group_description: ''
  - variation_group_name: Variations
    variations:
      - variation_name: Full-width text inputs
        variation_code_snippet: >-
          <div class="m-form-field">
              <label class="a-label a-label__heading" for="full-textinput-example">
                  Label
              </label>
              <input class="a-text-input a-text-input__full"
                    type="text"
                    id="full-textinput-example"
                    value="Placeholder text">
          </div>
      - variation_name: Full-width textarea inputs
        variation_code_snippet: >-
          <div class="m-form-field">
              <label class="a-label a-label__heading" for="full-textarea-example">
                  Label
              </label>
              <textarea class="a-text-input a-text-input__full"
                        id="full-textarea-example">Placeholder text</textarea>
          </div>
      - variation_name: Datepicker inputs
        variation_code_snippet: |-
          <div class="m-form-field">
              <label class="a-label a-label__heading" for="datepicker-example">
                  Label
              </label>
              <input class="a-text-input"
                    type="date"
                    id="datepicker-example"
                    placeholder="mm/dd/yyyy">
          </div>
      - variation_name: Text input with a button
        variation_description: These are used for simple forms where a full filter isn’t necessary.
        variation_code_snippet: |-
          <div class="o-form__input-w-btn">
              <div class="o-form__input-w-btn_input-container">
                  <input class="a-text-input" type="text" title="Test input">
              </div>
              <div class="o-form__input-w-btn_btn-container">
                  <button class="a-btn">Search</button>
              </div>
          </div>
      - variation_name: Button inside a text input
        variation_code_snippet: >-
          <div class="m-btn-inside-input">
              <input type="text"
                  value="This is some really long text to make sure that the button doesn't overlap the content in such a way that this input becomes unusable."
                  title="Test input"
                  class="a-text-input">
              <button class="a-btn a-btn__link">
                  {% include icons/error.svg %}
                  <span class="u-visually-hidden">Clear</span>
              </button>
          </div>
        variation_description:
          These offer the user an action to take related to the
          input, typically to clear the input.
      - variation_name: Button inside a text input with another button
        variation_description:
          This example combines both of the previous patterns,
          creating a typical site search form.
        variation_code_snippet: >-
          <div class="o-form__input-w-btn">
              <div class="o-form__input-w-btn_input-container">
                  <div class="m-btn-inside-input">
                      <input type="text"
                          value="This is some really long text to make sure that the button doesn't overlap the content in such a way that this input becomes unusable."
                          title="Test input"
                          class="a-text-input">
                      <button class="a-btn a-btn__link">
                          {% include icons/error.svg %}
                          <span class="u-visually-hidden">Clear</span>
                      </button>
                  </div>
              </div>
              <div class="o-form__input-w-btn_btn-container">
                  <button class="a-btn">Search</button>
              </div>
          </div>
use_cases: ''
guidelines: >-
  ### Stylistic guidelines


  Choose the appropriate width for text input fields so they match the kind of information requested. This makes it easier for users to quickly grasp what’s being asked.


  For example, it’s hard to understand at a glance that a single 1,000 px-wide text field is asking for your phone number or birth date. When possible, be even more explicit with the width by dividing it into known character counts. For instance, social security number should be three characters, then two, then four. Be mindful of not getting too restrictive, however. This approach could work for phone numbers, but only if international numbers are not permitted.


  These types of inputs should always be smaller widths:


  * Middle initial

  * Date, month, or year

  * State abbreviation


  ### Content guidelines


  Text should be in sentence case.


  Use placeholder text for formatting examples only. Don’t use for instructions. Placeholder text disappears once a user begins typing in the field. For more information, see [Design System guidance on placeholder text](https://cfpb.github.io/design-system/components/helper-text#placeholder-text-1).
behavior: As the screen size gets smaller, break multi-column inputs into a
  single, stacked column. Fields that are next to each other on a large screen,
  should stack at smaller screen sizes. When possible, fields should span the
  entire width of the screen at the smallest screen sizes.
accessibility: >-
  Inputs should always be paired with a `label` for accessibility reasons.


  Users of screen readers use the tab key to move focus from one form control to another. Make sure that tab focus order reflects the way you would like users to navigate through the form. Consider whether tabs should move a user down or across the page.
research: ''
related_items: "* [Text input
  variables](https://cfpb.github.io/design-system/development/variables#forms-1\
  )"
last_updated: 2020-01-28T15:55:47.394Z
eyebrow: Form elements
---
