## For css flex box : Go this docs: https://css-tricks.com/snippets/css/a-guide-to-flexbox/   (recommneded by chai with code).


## Default Flex Direction
    Default Value: row
    Effect: Flex items are arranged in a row, starting from the left.
    Nested Flex Containers
    When you have a parent flex container and a child that is also a flex container, the flex-direction property of the parent does not affect the flex-direction property of the child. Each flex container has its own independent set of flex properties.



## Transition Property:   (By Shradha didi)
=> Elements have different states (eg: active , hover   we can see it in inspect). 


## VVI : Margin Note: 
1. 
{
    width: 70%;
    margin: 0 auto;
}

=> By margin: auto in left right (above ): Browser first calculate the space avaliable in width and then it divides the remaining space equally as left and right margin so element comes in centre.

2.  Whem we give margin then element  make seperation  either from parent of siblings both . if a div is inside a a div and give margin  to inner div to 20px then  it takes  seperation from  parent div . if gives margin negative value it comes outside of that parent div and takes that specified outside that parent div . 


## VVI: Default brhaiour of block level elemnets in flexbox
=> Block level elements in flexbox behavave different than it is being  outside flexbox. In flexbox , child div or other block level elemnts takes only that much space required by its content intstead of full width .


## Flex-item property:
1.flex-grow

=> Purpose: Controls how much a flex item should grow relative to the other flex items inside the same container when there is extra space available.
Default Value: 0 (The item will not grow to fill the available space).
Behavior: When flex-grow is set to a positive value (e.g., 1), the flex item will grow to fill the available space in the container. If multiple items have a flex-grow value, they will grow relative to each other according to their flex-grow values.

2.flex-shrink:

=>Purpose: Controls how much a flex item should shrink relative to the other flex items inside the same container when there is not enough space.
Default Value: 1 (The item will shrink if necessary).
Behavior: When flex-shrink is set to a positive value (e.g., 1), the flex item will shrink when the container is smaller than the combined size of the flex items. If multiple items have a flex-shrink value, they will shrink relative to each other according to their flex-shrink values.

## note : VVI: 
=>flex-grow: Deals with how items expand in size when there's extra space in the container. Items with higher flex-grow values will take up more space.

=> flex-shrink: Deals with how items reduce in size when the container is too small. Items with higher flex-shrink values will shrink more.

EG: code: 
.container {
  display: flex;
  width: 100%;
}

.item-1 {
  flex-grow: 2;
  flex-shrink: 1;
  background-color: lightblue;
}

.item-2 {
  flex-grow: 1;
  flex-shrink: 1;
  background-color: lightgreen;
}

.item-3 {
  flex-grow: 1;
  flex-shrink: 2;
  background-color: lightcoral;
}

=> Item 1 will grow twice as much as Item 2 and Item 3 when there is extra space, but will shrink at the same rate as Item 2 when space is tight.
Item 2 will grow and shrink evenly compared to others.
Item 3 will grow like Item 2 but will shrink twice as much as Item 1 and Item 2.


## ####################   ####################       ####################    ####################    #################### 
<!--    TAILWIND CSS  -->

1. dist folder goes to production and we write our code to src .
2. when ever we apply property fpr state then we need to apply by "state: property"    eg: hover:text-white  hover:bg-red
3. tailwind follow mobile first Approach : so what ever wee write css that is good for mobile : 













<!-- NOt NEEDED TO  LEARN THIS , NEED TO HAVE IDEA ABOUT THIS: -->

<!-- Pligins -->

// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      // Customizations here
    },
  },
  plugins: [
    function ({ addUtilities }) {
      const newUtilities = {
        '.text-shadow': {
          textShadow: '2px 2px 4px rgba(0, 0, 0, 0.1)',
        },
        '.text-shadow-md': {
          textShadow: '3px 3px 6px rgba(0, 0, 0, 0.2)',
        },
        '.text-shadow-lg': {
          textShadow: '4px 4px 8px rgba(0, 0, 0, 0.3)',
        },
      }

      addUtilities(newUtilities, ['responsive', 'hover'])
    }
  ],
}
