
Basic Details :
1. App Name : ThunderNotes
2. Package name : com.thundernotes
3. App icon : A large thunder icon in center with red background.
3. Primary Device : Oneplus Pad 2
4. Other Devices : Any tablet with screen size larger than 12 inch.
5. Max App Size : 5GB
6. Network Connection : Required only for Snipping via API.

6. Interface : It has similar looking interface like the mock ui(screenshots). But it shouldn't try to replicate it pixel by pixel. It's just for reference. Also the mock ui may contain ambiguity. Its the job of the developer to interpret them correctly.

7. Stylus & Palm Rejection : Stylus should work properly and be optimized for oneplus pad series. In some note apps there is a weird bug of producing an electric / vibration like noise when we write on canvas. Our app shouldn't have this issue. All the demo apps(specially Notein) I have uploaded don't have this issue so you can try to copy their implementation. Palm Rejection should be automatically activated by default and should work properly.

Important Features :
1. Reliability : The app should be reliable and must not stop working after an year. It should only integrate reliable third party services which won't stop working in future.
2. Functionality: The app must meet user requirements and perform intended operations accurately. However the developer is free to add more features & functionalities which he finds relevant given that such features doesn't create bugs.
3. Efficiency : The app optimizes system resources such as stylus, CPU, and RAM of tablet. It delivers performance and responsiveness without excessive overhead or slow execution times.
4. Flexibility : The app should be adaptable to changing requirements and can be easily modified to incorporate new functions. It should support **PLUGINS**.
5. Portability(Tablet First Design) : The app is only intended to work on android tablets having screen-size > 12 inch. Our main target device is Onplus Pad 2+ series but it should support other 12in+ tablets. There is no plan to use it on mobile or other operating systems.
6. Security : Since it is a completely free app, there is no extra headache of security. So even if source code becomes visible its not a big issue. So you shouldn't take extra headache of source code hiding or android obfuscation.
7. App-size : File size is not an issue, it can be as large as 5GB given it performs well with great accuracy(OCR). So performance > app-size.

Priority of Features :
    Reliability(most priority) > Efficiency(performance) = Functionality = Flexibility > Portability(12in+ android tablet) > App-size = Security(least priority).

Strategy :
As this is a quite complex app so creating everything from scratch is quite hard. For that reason, I have decompiled some similar note apps from playstore using apktool, jadx and ghidra and uploaded their source codes. The Notein app has 75% common features to the app we are trying to build. So you can copy as much of its code as you want. You can also copy necessary components from other apps if you can locate them. The reason why I recommend it is because such apps are already functional and have no bugs, so copying them reduces the hurdle of debugging in later phases.

**CAUTION** : Don't blindly start copying. First make a proper plan and design and then copy relevant components instead of trying to copy first and then discover the copied code is not flexible enough and start writing spaghetti code to forcefully include features at any cost. Also copy only when you are sure such code will work and work create severe bugs.

Decompiled Demo App Links :
    Mock UI + Souce Code Repository Link : TBD
    Notein Souce Code Repository Link : TBD
    MyScript Souce Code Repository Link : TBD
    SamsungNotes Souce Code Repository Link : TBD
    Notewise Souce Code Repository Link : TBD

Account Details :
    Classic Access Token(will be changed after the app is ready) : TBD

Pages :
1. ThunderHomePage : Nothing much to say, very clear from the mock ui. Still some important components explained :
    i. Templates(sidebar) : It will open a interface displaying lots coverpages for engineering subjects which can be downloaded for free and used in our notes.
    ii. Plugins(sidebar) : It is put there just to tell the developer to build the app in such a flexible way that it can support plugins in future if some more feature needs to be added in the app like snipping chemistry reactions etc. For now only make one very simple plugin(text translator(any -> english) for testing. When we click the Plugins button it should open an interface showing that single plugin only. More plugins are to be added in future.
    iii. Upgrade to Premium : Our app is completely free so that popup is just for advertisement and can be safely ignored. Subscription & Cloud features might be added in future so its not our concern now.

2. NotesLibraryPage : Again nothing much to say, very clear from the mock ui. Still some important components explained :
    i. All notes user has created should be displayed here.
    ii. I forgot to include one essential thing to the mock ui is to show which folder a note is in while displaying the file cards. So please add that in actual app.
    iii. If you click three dots of a folder card there should be 7 functions : Rename, Change Cover, Move(folder change), Export, Bookmark, Information(file-name, file-size, date-created etc) Trash. You may add more functions if you find relevant.
    iv. Export Feature : It supports two types of exports - Native(.thunder extension) export for local backup and PDF for compatibility. The .thunder format is to be decided by you when you implement the app. For example, I have included native exports of some similar apps like Notein. Study them and decide native export format for our app.

3. FoldersLibraryPage : Again nothing much to say, very clear from the mock ui. I feel its self explanatory so no components needs to be discussed separately.

4. BookmarksPage : Its quite trivial that is why I haven't created any mock ui for it. It will just display all bookmarked files and folders with some basic functions.

5. TrashPage : Its again quite trivial that is why I haven't created any mock ui for it. It will just display all trashed files and folders with some basic functions like Restore, Delete, Empty Trash, Restore All etc.

6. CreateNotePage : Again its quite clear from the mock ui. Our app will support two types of pages - Blank and Lined and two types of orientation - Portrait and Landscape. The Infinite Canvas is not required for now. It may be available in future. If user clicks it then just add a popup to indicate the user that such feature is not available right now but may be added later.

7. CreateFolderPage : There is nothing much to say. Its almost clear from the mock ui.

8. CoverSelectionPage : Again nothing much to say, very clear from the mock ui. There will be atleast 50 pre-downloaded coverpages for engineering subjects(math, electrical, physics, cse etc). User will download the rest from Template Library. Again ignore the infinite canvas.

9. ImportFilePage : Its very trivial and that is why I haven't created anu mock ui for it. It will just tell user to select a .thunder file from their local storage and import it to thundernotes gallery. Error message to be displayed if user tries to import pdf or some other types of files.

10. Canvas Pages(4 pages) : Here comes the main thing - the canvas. In the four canvas pages (CanvasLayoutPage, CanvasCustomizationPage, CanvasUtilityPage, CanvasSettingsPage), I have tried my best to explain each and every single feature of canvas however as you know its not possible to describe everything from images I will write here about some important features. I am explaining everything from top-bottom and left-right in the mock ui.
    i. Row 1 (top-left): Here two files are opened side by side. Both will be native(.thunder) files. So user can open as many native files side by side as he wants.
    ii. Row 1 (top-right): Main thing here is the theme toggle button. **NOTE**: The toggle theme is only for the canvas area and not for our app-level settings(always dark). If user toggles theme it will change canvas area(drawings, shapes, textbox etc) from dark to light and vice-versa while preserving their base colors. So a pen-stroke in black will become white, a pen-stroke in dark red become light red, a pen-stroke in dark blue become light blue in canvas area if user switches from dark mode to light. Here smart color inversion should be applied so they preserve their base colors i.e. red(#FF0000) pen-stroke should not become cyan(#00FFFF) during theme switch.
    iii. Row 2 (top-left) : Just basic page counts, undo, redo and paste buttons. Clear from the mock ui.
    iv. Row 2 (top-center) : Four buttons are there :
        a. Textbox : Adds textbox in canvas area. Explained in more detail later.
        b. Image : Adds images from user's gallery.
        c. Scale : Clicking it opens a long marked ruler on canvas for drawing quick lines. The ruler can be rotated.
        d. Gridline : Clicking it opens a bold m ⨯ n gridline layout on canvas. It should have the magnetic feature i.e. shapes such as line, rectangle should be automatically attracted / sticked to its lines. This auto-fitting geometry feature is used by many note apps. 
    v. Row 2 (top-right) : Nine buttons - Bookmark, Read Mode, Fullscreen Mode(Hides the topmost file explorer row), Lock Canvas(canvas can't be moved by fingers), Change Page Margin, Chnage Cover Page, Add a new page(added next to current page), Settings(discussed later), Page Minimap View(discussed later).
    vi. Row 3 (top-left) : The penset section. It has six components :
        a. Fountain Pen : Have 4 function (shown in canvasCustomizationPage) - Brush Thickness, Line Type(straight, dotted, dashed), Pressure Sensitivity, Color Picker.
        b. Ballpoint Pen : Similar to fountain pen. Only stroke type different.
        c. Highliter : Have 4 function - Brush Thickness, Line Type(straight, dotted, dashed), Color Picker.
        d. Eraser : Have 2 function - Type(area eraser & shape eraser), Size.
        e. Lasso : 2 types of Lasso (shown in canvasCustomizationPage) - Random lasso, Rectangular Lasso.
        f. Filler : Used to fill enclosed areas. Have 2 options - Fill Color, Fill Opacity.
        **NOTE** : Icon / svg of all these items are available from the source-code of mock ui. You can re-adjust them for android and use them.

    vii. Row 3 (top-center-left) : The color-palate section. Only three color-palates are available and all support 8 different colors :
        a. ThunderDark (shown in canvasCustomizationPage) : Default color-set for pens
        b. ThunderLight (shown in canvasCustomizationPage) : Default color-set for highlighter
        c. Sunflower (shown in canvasCustomizationPage) : A user created color-set. Can be renamed.

    ix. Row 3 (top-center-right) : This generalized area for displaying clickable options. It will display three stroke sizes for pens under normal condition. It will display random and lasso eraser when lasso is clicked, it will display grid options m=? ⨯ n=?(user can adjust it) when gridline button is clicked and so on.

    x. Row 3 (top-right) : The diagram section. It has 7 buttons :
        a. Shape Picker : It has 4 function (shown in canvasCustomizationPage) : Shape Types, Border width, Line Type (8 types of lines shown in canvasCustomizationPage), Corner Radius, Border Color, Fill Color(can be set to None), Fill Opacity.
        b. Table Maker : It has 7 options - Border Visibility, Border Thickness, Border Color, Header Color, Rows(integer), Columns(integer), Alternative Row Color(If enabled a two color picker for odd rows and even rows)
        c. Add Extra Writing Space : It adds / removes space within the canvas by dragging a fat blue arrow (shown in canvasCustomizationPage). More about it is discussed later.
        d. Vertical Shifter : When user lasso some canvas area and clicks it then the whole lasso selected item reposition itself at y(0%-100%) distance from top margin. The value of y can be changed in settings(shown in canvasCustomizationPage).
        e. Horizontal left Shift : When user lasso some canvas area and clicks it then the whole lasso selected item reposition itself at almost 0(0%) distance from left margin.
        f. Horizontal Shifter : When user lasso some canvas area and clicks it then the whole lasso selected item reposition itself at x(0%-100%) distance from left margin. The value of x can be changed in settings(shown in canvasCustomizationPage).
        g. Finger / Stylus Mode : This button helps to instantly switch between finger and stylus only mode. **Note** : Palm rejection is on by default in this app.

    xi. Canvas Area : Here user makes notes using pens, highlighter, shapes etc.
        - This is the only area which supports adaptive theme change(dark <-> light) feature.
        - **Note** : There should be no gap between two different pages, only a dotted line as separator as shown in canvasLayoutPage. This is to give the user a feel of an infinite vertical canvas which is great for engineering note making.
        Also page number of each page should be properly displayed like a small side black strip with page number written in white at center similar to Notein.
        - The AI snipping button stays at the left / right side for snipping activity (discussed later).
        - The 100 Fit button should also be there to indicate zoom level of the canvas.
    
Individual Components :

    i. Textbox : User can place typed things in canvas using textbox. It has a global settings(shown in canvasSettingsPage) and local change(shown in canvasUtilityPage) for its theme. The options are : Bold, Italic, Underline(thin, thick, dashed and wavy), font-size, font-family, fill color(background color of textbox).
        Font-Family : There should be 10 pre-defined fonts : 2 serif font, 2 san-serif font, 6 handwriting font. The handwritten fonts should be selected such that they are : not too bent, not too wavy, neat, clean, has good support for both text and equations and integrates well to android ecosystem.
    
    ii. Lasso : We can lasso any area within canvas having mixed type content(pen-stroke+textbox+shape) and move it freely anywhere. It supports 9 functions as shown in canvasUtilityPage : Cut, Copy, Rotate, Enlarge/Reduce, Change Color, Horizontal Flip, Vertical Flip, <I forgot it, check source code of the mock ui >, Delete.


    ii. AI Snipping Button : It is a button for AI snipping tasks. It's a floating button which can be dragged to anywhere. It remains active as long as ThunderNotes is open and can stay on other apps if ThunderNotes is minimized but running in background. So overlay on other apps permission is granted. It supports capturing area from both inside Notein and from other apps for performing OCR but **FINAL RESULT(OUTPUT) IS ONLY SAVED TO THUNDERNOTES MEMORY FOR PASTING IN CANVAS**. It supports 4 types of snipping : Text, Equation, Code, Diagram. After snipping, text & code should appear as textbox whereas equation & diagram as native pen-stroke(erasable) as final result after pasting into canvas.

        i. Text Snip : Area captured -----> Confirmation -----> Sent for text OCR -----> OCR result produced -----> result converted to native ThunderNotes handwriting font -----> copied to app's clipboard -----> click paste button[Row 2 (top-left)] -----> Final output appears as floating textbox that user moves to place at desired location.

        ii. Equation Snip : Area captured -----> Confirmation -----> Sent for equation OCR -----> OCR result produced -----> OCR result rendered to user with LaTeX code -----> user may edit LaTeX and re-render(shown in canvasSettingsPage) -----> Again Confirmation -----> result(or user's edit result) converted to native ThunderNotes handwriting font -----> copied to app's clipboard -----> click paste button[Row 2 (top-left)] -----> Final output appears as floating lasso that user moves to place at desired location.

        **Note** : The equation snip should be able to handle multi-line equations like an entire solution of a math problem and correctly convert it into native pen stroke before final paste.

        iii. Code Snip : Area captured -----> Confirmation -----> Sent for text OCR -----> OCR result produced -----> sent to some code formatter engine -----> formatted code with proper tabs & colors is copied to app's clipboard -----> click paste button -----> Final output appears as floating textbox that user moves to place at desired location.

        **Note** : No need to match color of formatted code with thundernote's predefined color-palate.

        iv. Diagram Snip : Area captured -----> Confirmation -----> Sent for Tracing -----> Traced result is converted to native pen stroke copied to app's clipboard -----> click paste button -----> Final output appears as floating lasso that user moves to place at desired location.
    
        **Note** : During tracing strokes should be considered separate if and only if they have **SHARP POINT OR DIFFERENT COLOR** otherwise they should be considered same pen stroke. 
        
**Note** : The workflow is not strict and developer can add more steps in between or slightly change the existing workflow if it suites better for integration into the app.

    iii. Software required for snipping :
        i. Text Snip : TBD
        ii. Equation Snip : TBD
        iii. Code Snip : TBD
        iv. Diagram Snip : TBD
    
    iv. Add Extra Writing Space : As said before it adds / removes space within the canvas by dragging a fat blue arrow (shown in canvasCustomizationPage). But it should be implemented in a way so it don't starts to lag when dealing with large files(100+ pages). If you try to shift entire content up / down across pages pages, it may hang for large files. So a cunning data structure / plan has to be crafted to deal with such issue beforehand.
    **Note** : If the document has more than 1000 pages then we won't take guarantee of it not hanging during Add / Delete writing space(it may slightly hang) but document lesser than 1000 pages shouldn't hang during this operation.

    v. Settings : I think its very clear from canvasSettingsPage (right-side). One important thing is mentioned :
        Brush Thickness : If constant scaling is enabled then the thickness of the penstroke won't change if any lasso selected area is enlarged or reduced. if its off then the stroke thickness will increase(or decrease) proportionately as they shape is increased(or decreased) 

    **Note** : The developer is free to add new settings other than the ones mentioned if he finds them relevant.
        

    vi. Page minimap : I think its very clear from canvasUtilityPage (right-side) and needs no further detailing.
    
Conclusion : I have tried my best to describe every feature of this app through this prompt and mock ui's but even after that if something is missed it should be smartly guessed by the developer.
