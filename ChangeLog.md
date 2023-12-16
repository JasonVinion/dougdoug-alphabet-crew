### Change Log

V 1.5.0

**1. Mode Switching Feature**
   - Added a global variable `mode` to switch between different modes: `icon`, `nameChange`, and `normalName`.
   - Implemented a browser message listener to change the mode based on user selection from the popup.

**2. Enhanced Username Modification Functionality**
   - `modifyUsername` function now handles three modes:
     - `icon`: Appends an icon to the original username.
     - `nameChange`: Modifies the username to either 'A Crew' or 'Z Crew'.
     - `normalName`: Resets to the original username.
   - Stores the original username in `data-originalUsername` attribute to ensure consistent source of original username.
   - Clears existing username display before applying new mode.

**3. Enhanced Username Determination Logic**
   - Added `determineCrewIconName` function to determine 'A_Crew' or 'Z_Crew' based on the username's first letter.

**4. Improved Dynamic Content Handling**
   - Updated the MutationObserver to handle dynamic content and apply the current mode to new chat messages.
   - Ensured original usernames are stored and retrieved correctly for dynamic content.

**5. Popup HTML and Script**
   - Added a popup interface with buttons to switch modes: `Normal Name`, `Icon Mode`, and `Name Change Mode`.
   - Integrated event listeners in popup script to send the selected mode to the content script.

**6. Manifest Updates**
   - Added permissions for `storage` and `tabs` to support mode switching and popup functionality.
   - Included `web_accessible_resources` for icon handling in `icon` mode.
   - Configured `browser_action` to use the newly created popup.

