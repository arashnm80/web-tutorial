```

Here’s a list of 30 commonly used JavaScript codes in HTML and CSS contexts, sorted by their general usage and relevance:

### DOM Manipulation
1. Selecting Elements  
   document.querySelector('#id')  
   document.querySelectorAll('.class')

2. Adding Event Listeners  
   element.addEventListener('click', function)  
   element.addEventListener('mouseenter', function)

3. Modifying Element Styles  
   element.style.property = 'value'  
   element.classList.add('class')  
   element.classList.remove('class')

4. Changing Element Content  
   element.innerHTML = 'new content'  
   element.textContent = 'new content'

5. Creating and Inserting Elements  
   let newElement = document.createElement('div')  
   parent.appendChild(newElement)

6. Removing Elements  
   element.remove()  
   parent.removeChild(child)

7. Toggling Classes  
   element.classList.toggle('class')

8. Changing Input Values  
   input.value = 'new value'

### CSS Manipulation via JavaScript
9. Changing Inline Styles  
   element.style.backgroundColor = 'red'

10. Adding CSS via `style` Tag  
   let style = document.createElement('style'); style.innerHTML = 'css code'; document.head.appendChild(style)

11. Set CSS Variables (CSS Custom Properties)  
   document.documentElement.style.setProperty('--main-color', 'red')

### Animation & Transitions
12. Using CSS Transitions  
   element.style.transition = 'all 0.3s ease'

13. Using CSS Animations  
   element.style.animation = 'fadeIn 1s forwards'

14. Adding Keyframes via JavaScript  
   @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

15. Triggering Animations  
   element.classList.add('animate')

### AJAX and Fetch Requests
16. Using Fetch API  
   fetch('/data').then(response => response.json()).then(data => console.log(data))

17. Using XMLHttpRequest (legacy)  
   let xhr = new XMLHttpRequest(); xhr.open('GET', '/data'); xhr.send();

18. Async/Await with Fetch  
   const response = await fetch('/data'); const data = await response.json();

19. POST Requests with Fetch  
   fetch('/submit', { method: 'POST', body: JSON.stringify(data) })

### Timers and Intervals
20. Using `setTimeout()`  
   setTimeout(function() { alert('Hello!'); }, 1000)

21. Using `setInterval()`  
   let interval = setInterval(() => { console.log('Interval'); }, 1000)

22. Clearing a Timeout or Interval  
   clearTimeout(timeoutId)  
   clearInterval(intervalId)

### Form Handling
23. Form Validation  
   if (input.value === '') { alert('Field is empty') }

24. Getting Form Data  
   let formData = new FormData(formElement)  
   let value = formData.get('inputName')

25. Submitting Forms with JavaScript  
   formElement.submit()

### Utility Functions
26. Debouncing Function  
   function debounce(func, delay) { let timeout; return function() { clearTimeout(timeout); timeout = setTimeout(func, delay) } }

27. Throttling Function  
   function throttle(func, limit) { let lastFunc, lastTime; return function() { const now = new Date().getTime(); if (now - lastTime >= limit) { func(); lastTime = now; } } }

28. Checking Element Visibility  
   if (element.getBoundingClientRect().top < window.innerHeight) { console.log('Element is in view') }

### Local Storage & Session Storage
29. Saving Data to Local Storage  
   localStorage.setItem('key', 'value')

30. Retrieving Data from Local Storage  
   let value = localStorage.getItem('key')

These JavaScript functionalities are commonly used in conjunction with HTML and CSS to enhance interactivity, manage data, and handle user input.

```
