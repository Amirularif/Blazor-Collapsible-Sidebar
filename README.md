# Blazor Collapsible Sidebar

This project provides a simple implementation of a collapsible sidebar for the default Blazor Web App Sidebar. The sidebar can be toggled between a full (expand state) and a minimal width (collapse state). I was trying to find a way on how to achieve this online but couldn't find one, so I tried myself and managed. I'm sharing this simple trick to help people who are trying to achieve this too.

> [!TIP]
> This simple task is completed for learning purposes. Feel free to use it and let me know ◡̈

## Outcome
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/9c3bee3f-ef66-4904-8a54-807707f72ff3" width="400" height=auto>
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/4288877c-08ef-4374-8d32-1764c85e31f9" width="400" height=auto>

## Features

- **Expandable and Collapsible:** Click to collapse the sidebar to a minimal icon view. And expand for a full sidebar view.
- **Smooth Transitions:** Animated transitions for expanding and collapsing the sidebar.

## Guide on how to achieve this

1. Blazor Web App provide us with a default sidebar on the Startup page which is inside the MainLayout.razor and NavMenu.razor. So all we need to do is just locate both files and thier respective css files and start editing.
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/a75b0bef-eb4b-40fc-8240-fbbd3564114a" width="200" height=auto>

2. Start with removing the sidebar class in MainLayout.razor and its respective css code inside MainLayout.razor.css.
3. Add the sidebar class into NavMenu.razor class and its respective css as well.
4. Create a Method to hold the state of the button. This will allow you to later set the style based on the toggle state.
5. Create a style SidebarContainer to the sidebar in NavMenu.razor and set the width to change based on the isNarrow method inside the code section.
6. Now, add an if-statement on each nav-link to show extra label when not narrow and to only show icons when is narrow.
7. In my case, I added an if-else statement for the buttons and the nav-brand to change the button type, either arrow-left or arrow-right based on toggle, and to show only Text of nav-brand when the sidebar is not narrow and Icon when the sidebar is narrow.
8. Now all left is adding and editing css. In my case :
    + I removed sidebar class from MainLayout.razor.css, added them into NavMenu.
    + Add a transition property in sidebar class.
    + Add a bottom-row class and nav-label class.
    + Edit the margin on bi class.
  
9. And you are set ◡̈ 
