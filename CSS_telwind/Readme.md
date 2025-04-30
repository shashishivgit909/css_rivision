1. group :  utility is used to apply styles to child elements when a parent element is in a specific state (like hover, focus, etc.). You add the group class to a parent element, then inside its children, you can use classes like group-hover:, group-focus:, etc., to apply styles when the parent is in that state.

🧪 Example:
html
Copy
Edit
<div class="p-4 group hover:bg-gray-100">
  <h2 class="text-lg font-bold group-hover:text-blue-500">
    Hover over this box
  </h2>
  <p class="text-sm group-hover:underline">
    This text changes when you hover the parent
  </p>
</div>

=> group on the parent allows children to detect its hover state.
=> group-hover:text-blue-500 and group-hover:underline apply styles to the children when the parent is hovered.



2. in tailwind

