# Admin-Dashboard
Admin Dashboard for the FullStack JavaScript module on The Odin Project.


[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#github.com/yxuan1996/Admin-Dashboard)

To preview this webpage, run a server
```
python -m http.server 8000
```

![Alt text](src/dashboard-project.png "Dashboard")

## Development Notes
#### Tehnologies Used
- HTML
- CSS (Grid and Flexbox, Tailwind)
- JS

#### Layout
Throughout this project, we will strive to use Tailwind and DaisyUI components. This is to minimize clutter in the CSS file and make the project more readable. 

We start by creating a vertical sidebar with collapsible menu items. The sidebar should be responsive and collapse on mobile views. 

We use Flexbox and Grid to position the main layout. We start from the outermost layout and go inward using nested flexbox and grid. 

#### Fixed Sidebar, Scrollable Content Box
To ensure that the sidebar is fixed, we use fixed positioning. However, this ruins other layouts, since bootstrap columns, flexbox and grid all use relative positionning. 

Solution: If we are using bootstrap columns, use fixed positioning for the sidebar, then apply an offset to the scrollable content. 

```HTML
<div class="row">
    <div class="col-lg-3" style="position:fixed">
        Fixed content
    </div>
    <div class="col-lg-9 col-lg-offset-3">
        Normal scrollable content
    </div>
</div>
```

Source: https://stackoverflow.com/questions/21868610/make-column-fixed-position-in-bootstrap

#### Icons and Images
We use SVG for icons and images. There are 2 ways to insert SVG:
- Directly into HTML. This can get messy, a better way to organize would be this: https://stackoverflow.com/questions/27954250/moving-to-svg-icons-how-to-separate-them-from-the-code
- Download SVG file and import as an image