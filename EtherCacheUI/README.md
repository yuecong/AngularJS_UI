1. Code Editor
 - Brackets (http://brackets.io/)

2. How to add a new page
 - Select a reference page from AngularJS Full Version or other pages in this project
 - `views/xxx.html` folder : Copy the html file into `views` folder
 - `js/config.js` : Add a new .state for the new page.
   - Copy the definition of .state from the reference page at first  
    - The first element will be used as entry point by `views/common/navigation.html`
     - <url> will be shown as #index/<url> 
      - <templateUrl> need to be the same name as the file below 'view' folder
 - `js/plugins/` : In case new plugs are defined in the <resolve> of newly added .state in `js/config.js`, copy those plugins from AngularJS full version folder
 - `js/controllder.js`: Register a new map for controller name and function name. This controller name will be used in `views/xxx.html`
 - `views/common/navigation.html`: Add a new item for the page in left navigation bar. the name for .state defined in `js/config.js` will be used here

3. Customize each view
  - Keep in mind all data are defined in `js/controller.js`. 
  - Customer UI component as your design. Using `<!-- -->` to have a try how each component is arranged in `views/xxx.html`
