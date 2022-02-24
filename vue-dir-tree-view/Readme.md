# vue-dir-tree-view

Vue directory structure plugin
Render directories with files

Icons used: bootstrap icons

```bash
npm install vue-dir-tree-view
```

```javascript
import VueDirTreeView from 'vue-dir-tree-view'

export default {
components: {
    VueDirTreeView
},
data(){
    return {
        config: {
            options: null,
            data: <exampledata>
        }
    }
}

/*
exampledata: [
    {
        "title": "multi-depth-dir",
        "children": [
            {
                "title": "one",
                "isLeaf": false,
                "children": [
                    {"title": "image.jpg", "isLeaf": true},
                    {"title": "spreadsheet.xlsx", "isLeaf": true},
                    {"title": "file.pdf", "isLeaf": true}
                ]
            },
            {
                "title": "two",
                "children": [
                    {
                        "title": "three",
                        "isLeaf": false,
                        "children": [
                            {"title": "file_example_GIF_500kB.gif", "isLeaf": true},
                            {"title": "file_example_JPG_100kB.jpg", "isLeaf": true},
                            {"title": "file_example_SVG_20kB.svg", "isLeaf": true},
                            {"title": "file-sample_100kB.rtf", "isLeaf": true},
                            {"title": "file-sample_500kB.odt", "isLeaf": true}
                        ]
                    },
                    {"title": "file_example_GIF_500kB.php", "isLeaf": true},
                    {"title": "file_example_JPG_100kB.js", "isLeaf": true},
                    {"title": "file_example_PNG_500kB.pptx", "isLeaf": true},
                    {"title": "file_example_XLSX_100.xlsx", "isLeaf": true}
                ],
                "isLeaf": false
            },
            {"title": "file_example_GIF_500kB.vmv", "isLeaf": true},
            {"title": "file_example_SVG_20kB.docx", "isLeaf": true},
            {"title": "file_example_TIFF_1MB.tiff", "isLeaf": true}
        ],
        "isLeaf": false
    }
]
*/
```