# 🚀  Backend UI-Stack Template

## Screenshots
### 〰️ Empty State
![Empty State Picture]()

### 🚫 Error State
![Error State Picture]()

### ⏳ Loading State
![Loading State Picture]()


## Code 
HTML:
```html
<div class="preloader-wrapper">
  <span class="preloader"></span>
</div>
```

JavaScript:
```javascript
// Preloader
const preLoaderWrapper = document.querySelector(".preloader-wrapper");

// Fetch API data
fetch(apiUrl)
  .then((res) => {

    if (res.status >= 200 && res.status <= 299) {
      preLoaderWrapper.classList.add("hide");
      return res.json();
    } else {
      preLoaderWrapper.classList.add("hide");
    }
  })

  // Filter data to specific person
  .then((res) => {
    const boudewijnData = res.data.find((student) => student.memberId === 18);

    // Put data into HTML

    // Title
    nameTitle.textContent = `${boudewijnData.name} ${boudewijnData.surname}`;

    // Bio
    bioText.textContent = boudewijnData.bio;
  })
```


  
## Licentie

![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).
