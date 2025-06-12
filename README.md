# glasstk-css
CSS for a glassmorphic Tab UI

## Usage
### Classes:
row: Creates a flexbox row using the item it is applied to as the parent

vertical: Same as row, but it uses a column.

tab: For use in a div of id tabs. Use on p with onclick to opening function. Creates a template for a tab button, or any button, but name tab kept from when it was exclusivley for tabs.

popuptext: Centers text. Can be removed if not used.

header: Deprecated but kept for compatibility. Makes text color #fff.

prompt: A closed modal popup. Usage example provided below.

promptOpen: An open modal popup. Refer to examples.

tabon: Use to indicate an open tab.

badge: This is tab but it doesn't have cues to click. Use for noninteractive messages, like Made by viewer in my site.
### IDs:
tabs: Use with a div. Is row but has a gap of 4px.

content: Use this on a div. The div will contain all of your objects for body. Left aligns and makes the page a column.

break: This should be a class but it isn't because i didn't expect to use it many times. So... compatibility. Use for ```<hr>```.

page: Use to contain page content (not popups)

## Examples

### Prompt

HTML (excluding boilerplate):

```html
<div id="content">
<div id="page">
<p class="tab" onclick="openModal();">Click to open a modal</p>
</div>
<div id="modal" class="prompt"> <!-- Note modal is not a glasstk id. !-->
<h1>Pressed!</h1>
<p class="tab" onclick="closeModal();">Close</p>
</div>
</div>
```

Javascript
```js
let modal = document.getElementById("modal");
function openModal() {
    modal.classList = "promptOpen";
}
function closeModal() {
    modal.classList = "prompt";
}
```

## How do I get it?
Download from the repo and include it as a stylesheet. Background not set automatically
## Notes
The content is centered by default.