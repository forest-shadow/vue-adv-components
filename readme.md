# Collection of custom Vue components

## 01. Controlled Toggle Component
Make `ToggleInput` component. Considering usage of Vue's `v-model` feature with custom event emitting.

## 02. DatePicker Component
Make `DatePicker` Component using 3rd party js library. Considered `mounted()` hook as a good place for js libraray initiation.

## 03. Modal Component
Considered number encapsulating behavior methods for Modal Component implementation.

### 03.01. Global events
Considered adding globla events for handling Modal closing on `Esc` key.

### 03.02. Direct DOM manipulations
Dynamically adding `.open-modal` class to root element `<div id="app">` for disabling background scrolling.

### 03.03. Portals
Use common block for displaying different Modal instances with help of `vue-portal` plugin.

## 12. Compound Accordion Compoenent
Made with usage of Vue's Provide/Inject feature.

<b>Provide/Inject</b> - works as a secret back-channel where parent can provide data to any of its children no matter how deep them nested without necessity to pass down these data explicitly by props.

Decision of making element of array active made by `AccordionList` component.

## 13. Compound Draggable Contacts List component
Made using several conception discovered before: Compund Components, Provide/Inject, using 3rd-party library, scoped slots.