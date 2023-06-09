<frontmatter>
  title: QR Code Component
</frontmatter>

<br>

## Example of QR Code Component Usage in Markdown

In your XML or HTML file, you can include the QR code element like this:

<qr-code 
    data="https://markbind.org/"
    size="10"
    margin="4"
    ec-level="H"
    color="red"
    background="white"
    type="svg"
    alt="Markbind QR Code"
    caption="Markbind QR Code"
    style="width:100%;height:100%;border:2px solid black;"
></qr-code>

This will generate a QR code with the following characteristics:
- The encoded data is the URL `https://markbind.org/`.
- The size of the QR code is 10.
- The margin around the QR code is 4.
- The error correction level is `H`.
- The QR code is red, on a white background.
- The QR code is output as an SVG.
- The alternative text for the QR code (for screen readers) is "Spirify QR Code".
- The caption underneath the QR code is "Spirify QR Code".
- The QR code is styled with a width and height of 100%, and a 2px solid black border.

## Source Code for the `QrCodeProcessor` class

The `QrCodeProcessor` class is responsible for generating the QR code based on the parameters passed in the QR code element. Here is the source code:

```xml
import cheerio from 'cheerio';
import { NodeOrText } from '../utils/node';
import qr from 'qr-image';

class QrCodeProcessor {
    process(node: NodeOrText) {
        node.name = 'div';
        if (node.attribs && node.attribs.data) {
            const data = node.attribs.data;
            const options = {
                size: parseInt(node.attribs.size) || 10,
                margin: parseInt(node.attribs.margin) || 4,
                ecLevel: node.attribs.ecLevel || 'H',
                color: node.attribs.color || 'black',
                background: node.attribs.background || 'white',
                caption: node.attribs.caption || '',
                alt: node.attribs.alt || '',
            };
            const qrSvg = this.generateQRCodeSync(data, options);
            let styles = {
                textAlign: 'center',
                ...node.attribs.style
            };
            let stylesString = Object.entries(styles).map(([prop, value]) => `${prop}: ${value}`).join('; ');
            const $wrapper = cheerio.load(`<div style="${stylesString}"></div>`);
            $wrapper('div').append(qrSvg);
            if (options.caption) {
                $wrapper('div').append(`<p>${options.caption}</p>`);
            }
            cheerio(node).append($wrapper.html());
            return node;
        }
        return node;
    }
    generateQRCodeSync(data: string, options: any) {
        if (typeof data !== 'string') {
            data = JSON.stringify(data);
        }
        let qrSvg = qr.imageSync(data, { type: 'svg', size: options.size, margin: options.margin, ec_level: options.ecLevel });
        let $ = cheerio.load(qrSvg, { xmlMode: true });
        $('path').attr('fill', options.color);
        qrSvg = $.html();
        return qrSvg;
    }
}
export default QrCodeProcessor;
```




## Different QR Code Usages in Markdown

### 1. URL QR Code with Default Settings

<qr-code 
    data="https://markbind.org/"
></qr-code>

This will generate a default QR code encoding the URL `https://markbind.org/`.

### 2. Text QR Code with Custom Size and Margin

<qr-code 
    data="Hello, MarkBind!"
    size="15"
    margin="2"
></qr-code>

This will generate a QR code encoding the text `Hello, MarkBind!` with a size of 15 and a margin of 2.

### 3. URL QR Code with Custom Colors and Error Correction Level

<qr-code 
    data="https://github.com/MarkBind"
    ec-level="Q"
    color="blue"
    background="yellow"
></qr-code>

This will generate a QR code encoding the URL `https://github.com/MarkBind` with an error correction level of `Q`, a blue color code, and a yellow background.

### 4. Text QR Code with Custom Caption

<qr-code 
    data="MarkBind rocks!"
    caption="Scan to see a cool message!"
></qr-code>

This will generate a QR code encoding the text `MarkBind rocks!` and a caption that says `Scan to see a cool message!`.
