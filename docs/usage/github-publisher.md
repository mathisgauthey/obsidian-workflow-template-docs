# Auto-upload to websites

## Setup

I encourage you to follow the [installation instructions](../getting-started/auto-upload-to-website.md) first.

## Usage

Notes are created with a YAML field called `share`. It is set to false by default. Change it to true.

Then select the command `Upload filename to DEFAULT` from the `More options` at the top right of your note.

Wait a little bit and your note will be uploaded to your website along with its attachments.

The posts will be sent to the `content/pos`t folder and the attachments to the `content/images` folder.

## Automated conversion regex

I configured some regex to convert my notes to Hugo's markdown format.

Images :

`/!\[\[([^[\]]+)\]\]/gi` → `![$1](/images/$1)`

Other notes links :

`/\[\[([^|\]]+)\|([^\]]+)\]\]|\[\[([^\]|]+)\]\]/gi` → `[$2$3]({{< ref "$1$3" >}})`
