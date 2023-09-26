# Project_Phone_Hunting.js

## Hosting Link:

# PhoneHuntingAPI
This is a simple web application for searching and displaying phone information. It allows users to search for phones and view their details.

### Step 1: HTML
The HTML code


```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Phone Hunting API</title>
    <link
      href="https://cdn.jsdelivr.net/npm/daisyui@3.6.2/dist/full.css"
      rel="stylesheet"
      type="text/css"
    />
    <link rel="stylesheet" href="https://cdn.tailwindcss.com" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="" />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&amp;display=swap"
      rel="stylesheet"
    />
  </head>
  <body>
    <nav class="nav">
      <h2>Hot Gadgets</h2>
      <button class="btn btn-primary">Sign Up</button>
    </nav>
    <header class="header">
      <h1>Apple Iphone 13 Pro Max</h1>
      <p>
        There are many variations of passages of Lorem Ipsum available, but the
        majority <br />
        have suffered alteration in some form, by injected humou.
      </p>
      <div>
        <button class="btn btn-primary">Buy Now</button>
      </div>
    </header>
    <section>
      <div
        class="img grid grid-cols-3 lg:flex lg:justify-center items-end relative bottom-80 -mb-72"
      >
        <img src="./images/pngwing 2 (1).png" alt="" />
        <img src="./images/pngwing 1.png" alt="" />
        <img src="./images/pngwing 2.png" alt="" />
      </div>
      <h1>Search Your Phone</h1>
    </section>
    <main>
      <section class="search">
        <input
          id="searchField"
          type="text"
          placeholder="e.g. oppo, samsung, iphone"
          class="input input-bordered"
        />
        <button onclick="searchHandler()" class="btn btn-primary">
          Search
        </button>
      </section>
      <section>
        <div class="text-center my-40 hidden" id="loading">
          <span class="loading loading-ring loading-lg"></span>
        </div>

        <div
          id="phone-container"
          class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 mx-8 my-5"
        ></div>
      </section>
      <div class="hidden flex justify-center my-8" id="showALLBtn">
        <button onclick="showBtn()" class="btn btn-primary text-white">
          Show All
        </button>
      </div>

      <!-- Modals -->
      <section>
        <!-- Open the modal using ID.showModal() method -->
        <dialog id="my_modal" class="modal modal-bottom sm:modal-middle">
          <form method="dialog" class="modal-box text-center">
            <div id="imgContainer" class="flex justify-center"></div>
            <h3 id="detailsPhoneName" class="font-bold text-lg mt-3"></h3>
            <h3 id="detailsBrand" class="py-4"></h3>
            <p id="detailsSpec"></p>
            <p id="releaseDate" class="my-2"></p>

            <div class="modal-action flex justify-center">
              <!-- if there is a button in form, it will close the modal -->
              <button class="btn bg-red-600 text-white">Close</button>
            </div>
          </form>
        </dialog>
      </section>
    </main>
    <footer class="footer">
      <div>
        <p class="font-bold">
          Hot Gadgets BD <br />Providing reliable tech items since 1992
        </p>
        <p>Copyright © 2023 - All rights reserved</p>
      </div>
      <div>
        <div class="svg-path">
          <a href="#"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              class="fill-current"
            >
              <path
                d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
              /></svg
          ></a>
          <a href="#"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              class="fill-current"
            >
              <path
                d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"
              /></svg
          ></a>
          <a href="#"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              class="fill-current"
            >
              <path
                d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"
              /></svg
          ></a>
        </div>
      </div>
    </footer>
    <script src="index.js"></script>
  </body>
</html>

```
### 2 . Style.css
```
body {
  font-family: "Poppins", sans-serif;
}
.nav {
  background: #0d6efd0d;
  padding: 10px 20px;
  display: flex;
  justify-content: space-between;
}
.nav h2 {
  font-size: 2rem;
  font-weight: bold;
}
.btn-primary {
  background-color: #007bff;
  color: white;
}
.header {
  background: #0d6efd0d;
  padding-bottom: 96px;
  text-align: center;
}
.header h1 {
  font-size: 4rem;
  font-weight: bold;
}
.header p {
  font-size: 1.2rem;
  margin-top: 6px;
}
.header button {
  margin-top: 20px;
  background-color: #007bff;
  color: white;
}
.search {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2px;
}
.input-bordered {
  width: 100%;
  max-width: 250px;
  margin: 5px 0;
}
.phone-card {
  margin: 40px auto;
  text-align: center;
}
.loading {
  display: none;
  justify-content: center;
  align-items: center;
  margin: 40px 0;
}
#phone-container {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
  margin: 5px 8px;
}
#showALLBtn {
  display: none;
  justify-content: center;
  margin: 8px 0;
}
.modal-box {
  text-align: center;
}
.modal-action {
  justify-content: center;
}

.footer {
  background: #0d6efd0d;
  color: black;
  padding: 10px 20px;
  text-align: center;
  margin-top: 20px;
  padding-top: 32px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer svg {
  width: 24px;
  height: 24px;
  margin: 5px;
  fill: currentColor; /* Use the current text color for the SVG fill */
}

.footer p {
  margin-top: 10px;
  font-weight: bold;
}
.svg-path {
  display: flex;
  justify-content: center;
}
h1 {
  font-size: 4rem;
  font-weight: bold;
  text-align: center;
}

.img {
  display: grid;
  grid-template-columns: repeat(3, 1fr); 
  gap: 20px; 
  justify-content: center;
  align-items: flex-end; 
  padding: 20px;
}
#phone-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  margin: 5px 8px;
}

```


### 3.  JavaScript

Create a JavaScript file and add the following code:

```
let searchText = "13";

function searchHandler(isShowAll) {
  loading(true);
  const searchField = document.getElementById("searchField");
  searchText = searchField.value;
  loadPhone(searchText, isShowAll);
}
const loading = (isLoading) => {
  const loading = document.getElementById("loading");
  if (isLoading) {
    loading.classList.remove("hidden");
  } else {
    loading.classList.add("hidden");
  }
};

const loadPhone = async (searchText, isShowAll) => {
  const res = await fetch(
    `https://openapi.programming-hero.com/api/phones?search=${searchText}`
  );

  const data = await res.json();
  const phones = data.data;

  displayPhones(phones, isShowAll);
};
loadPhone(searchText);
const displayPhones = (phones, isShowAll) => {
  //console.log(phones);
  const phoneContainer = document.getElementById("phone-container");
  phoneContainer.textContent = "";

  const showAll = document.getElementById("showALLBtn");
  if (phones.length > 12 && !isShowAll) {
    showAll.classList.remove("hidden");
  } else {
    showAll.classList.add("hidden");
  }
  //display first 10
  if (!isShowAll) {
    phones = phones.slice(0, 12);
  }

  phones.forEach((phone) => {
    //console.log(phone);
    //1 create a div
    const phoneCard = document.createElement("div");
    phoneCard.classList = `card bg-base-100 shadow-xl p-5`;
    phoneCard.innerHTML = `
        <figure class="px-10 pt-10">
                      <img src="${phone.image}" alt="phone" class="rounded-xl" />
                    </figure>
                    <div class="card-body items-center text-center">
                      <h2 class="card-title">${phone.phone_name}</h2>
                      <p>There are many variations of passages of available, but the majority have suffered</p>
                      <div class="card-actions">
                        <button onclick="showDetailsHandler('${phone.slug}')" class="btn btn-primary text-white">Show Details</button>
                      </div>
                    </div>

        `;
    phoneContainer.appendChild(phoneCard);
  });
};

// show All Button
function showBtn() {
  searchHandler(true);
}
// Show Details
const showDetailsHandler = async (id) => {
  //console.log(id);
  // load data
  const res = await fetch(
    `https://openapi.programming-hero.com/api/phone/${id}`
  );
  const data = await res.json();

  const phone = data.data;
  showPhoneDetails(phone);
  //console.log(phone);
};
const showPhoneDetails = (details) => {
  my_modal.showModal();
  const modelName = document.getElementById("detailsPhoneName");
  const brandName = document.getElementById("detailsBrand");
  const detailsSpec = document.getElementById("detailsSpec");
  const releaseDate = document.getElementById("releaseDate");
  const imageDiv = document.getElementById("imgContainer");

  imageDiv.innerHTML = `<img src="${details.image}" alt="">`;
  modelName.innerText = details.name;
  brandName.innerText = `Brand: ${details.brand}`;
  const features = details.mainFeatures;
  //console.log(features.storage);
  console.log(details.image);
  let string = "";
  for (const key in features) {
    //detailsSpec.innerHTML=`${features[key]} <br>`;

    //detailsSpec.innerText=`${features[key]} <br>`;
    //console.log(`${key}:${features[key]}`);
    string = string + `${key}: ${features[key]} \n`;
  }
  detailsSpec.innerText = string;
  releaseDate.innerText = `${details.releaseDate}`;
};

```
