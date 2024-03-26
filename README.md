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

## Guide on how to achieve this (_will completely update this soon_)

1. Blazor Web App provide us with a default sidebar on the Startup page which is inside the MainLayout.razor and NavMenu.razor. So all we need to do is just locate both files and thier respective css files and start editing.
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/a75b0bef-eb4b-40fc-8240-fbbd3564114a" width="200" height=auto>

2. Start with removing the sidebar class in __MainLayout.razor__ and its respective css code inside __MainLayout.razor.css__.
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/633e41ae-5a46-4b54-b060-ec849e83b99d" width="500" height=auto>
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/e12cda7f-a63e-41d6-9f1f-ad9bb3283aa2" width="500" height=auto>
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/c443dd41-c4c2-431f-a1af-058770ac6baa" width="500" height=auto>

3. Add the sidebar class into __NavMenu.razor__ class and its respective css as well.
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/01029cf1-f3d4-401a-811a-d0e71307faae" width="300" height=auto>
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/727c4b2d-bad3-4431-b754-a7361a1b22f3" width="300" height=auto>
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/0e4f11a2-497b-4939-840f-67eab8cd4ff6" width="300" height=auto>

5. Create a Method to hold the state of the button. This will allow you to later set the style based on the toggle state. And create a style SidebarContainer to the sidebar in __NavMenu.razor__ and set the width to change based on the isNarrow method inside the code section.
<img src="https://github.com/Amirularif/Blazor-Collapsible-Sidebar/assets/57553676/f8ed831c-3638-46f0-80d1-591d707079f0" width="700" height=auto>

7. Now, add an if-statement on each nav-link to show extra label when not narrow and to only show icons when is narrow.
8. In my case, I added an if-else statement for the buttons and the nav-brand to change the button type, either arrow-left or arrow-right based on toggle, and to show only Text of nav-brand when the sidebar is not narrow and Icon when the sidebar is narrow.
9. Now all left is adding and editing css. In my case :
    + I removed sidebar class from MainLayout.razor.css, added them into NavMenu.
    + Add a transition property in sidebar class.
    + Add a bottom-row class and nav-label class.
    + Edit the margin on bi class.
  
10. And you are set ◡̈ 
