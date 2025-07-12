# CKEditor 5 Custom Build

A custom CKEditor 5 build with essential plugins for rich text editing. This package provides a pre-configured CKEditor 5 editor with commonly used features.

## Installation

```bash
npm install @ssakibhossain10/ckeditor5-custom-build
```

## Usage

### Basic Usage

```javascript
import Editor from '@ssakibhossain10/ckeditor5-custom-build';

Editor
    .create(document.querySelector('#editor'))
    .then(editor => {
        console.log('Editor was initialized', editor);
    })
    .catch(error => {
        console.error(error);
    });
```

### With Custom Configuration

```javascript
import Editor from '@ssakibhossain10/ckeditor5-custom-build';

Editor
    .create(document.querySelector('#editor'), {
        toolbar: {
            items: [
                'heading',
                '|',
                'bold',
                'italic',
                'link',
                'bulletedList',
                'numberedList',
                '|',
                'outdent',
                'indent',
                '|',
                'imageUpload',
                'blockQuote',
                'insertTable',
                'mediaEmbed',
                'undo',
                'redo'
            ]
        },
        language: 'en',
        image: {
            toolbar: [
                'imageTextAlternative',
                'toggleImageCaption',
                'imageStyle:inline',
                'imageStyle:block',
                'imageStyle:side'
            ]
        },
        table: {
            contentToolbar: [
                'tableColumn',
                'tableRow',
                'mergeTableCells'
            ]
        }
    })
    .then(editor => {
        console.log('Editor was initialized', editor);
    })
    .catch(error => {
        console.error(error);
    });
```

### HTML Setup

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CKEditor 5 Custom Build</title>
</head>
<body>
    <div id="editor">
        <p>This is the initial content of the editor.</p>
    </div>
    
    <script src="path/to/your/bundle.js"></script>
</body>
</html>
```

## Features

This custom build includes the following plugins:

- **Autoformat** - Automatic text formatting
- **Bold** & **Italic** - Basic text styling
- **Block Quote** - Quote formatting
- **Cloud Services** - CKEditor Cloud Services integration
- **Essentials** - Core editor functionality
- **Heading** - Heading styles (H1-H6)
- **HTML Embed** - Embed raw HTML
- **Image** - Image insertion and editing
  - Image caption
  - Image styles (inline, block, side)
  - Image toolbar
  - Image upload
- **Indent** - Text indentation
- **Link** - Link insertion and editing with AutoLink
- **List** - Bulleted and numbered lists
- **Media Embed** - Embed media (YouTube, Vimeo, etc.)
- **Paragraph** - Paragraph formatting
- **Paste From Office** - Clean paste from Office applications
- **Table** - Table insertion and editing
- **Text Transformation** - Smart text transformations

## TypeScript Support

This package includes TypeScript definitions. You can use it in TypeScript projects without additional type packages.

```typescript
import Editor from '@ssakibhossain10/ckeditor5-custom-build';

Editor
    .create(document.querySelector('#editor')!)
    .then((editor: any) => {
        console.log('Editor was initialized', editor);
    })
    .catch((error: Error) => {
        console.error(error);
    });
```

## Browser Support

This editor build is compatible with modern browsers:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Links

- [CKEditor 5 Documentation](https://ckeditor.com/docs/ckeditor5/)
- [CKEditor 5 Framework](https://ckeditor.com/docs/ckeditor5/latest/framework/)
- [Report Issues](https://github.com/ssakibhossain10/ckeditor5-custom-build/issues)

## Author

Created by [Sakib Hossain](https://github.com/ssakibhossain10)
