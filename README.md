
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Plant Diseases | Community Service Project</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #f7fbea;
    color: #284b2d;
    line-height: 1.7;
}

/* NAVIGATION BAR */
nav {
    background: #174d2a;
    color: white;
    padding: 17px 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    position: sticky;
    top: 0;
    z-index: 100;
}

nav h2 {
    font-size: 23px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 25px;
    flex-wrap: wrap;
}

nav a {
    text-decoration: none;
    color: white;
    font-weight: bold;
}

nav a:hover {
    color: #f5e99b;
}

/* HOME SECTION */
.hero {
    min-height: 470px;
    background:
    linear-gradient(rgba(10,60,25,.76),rgba(10,60,25,.76)),
    url("https://images.unsplash.com/photo-1497250681960-ef046c08a56e?w=1600")
    center/cover;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
    padding: 45px 20px;
}

.hero h1 {
    font-size: 55px;
    margin-bottom: 15px;
    letter-spacing: 2px;
}

.hero p {
    max-width: 800px;
    font-size: 19px;
}

.main-btn {
    margin-top: 25px;
    padding: 13px 30px;
    background: #f5e99b;
    color: #174d2a;
    border: none;
    border-radius: 30px;
    font-weight: bold;
    cursor: pointer;
    font-size: 16px;
}

/* GENERAL SECTIONS */
section {
    padding: 65px 7%;
    scroll-margin-top: 75px;
}

.section-title {
    text-align: center;
    color: #17602e;
    font-size: 33px;
    margin-bottom: 18px;
}

.section-subtitle {
    text-align: center;
    max-width: 900px;
    margin: 0 auto 35px;
    font-size: 17px;
}

/* INTRODUCTION */
.introduction {
    background: white;
}

.intro-content {
    max-width: 1050px;
    margin: auto;
}

.intro-content h3 {
    color: #28753a;
    margin: 25px 0 10px;
    font-size: 23px;
}

.intro-content p {
    text-align: justify;
    margin-bottom: 15px;
}

.info-box {
    background: #f0f7df;
    padding: 25px;
    border-left: 5px solid #378b43;
    border-radius: 12px;
    margin: 25px 0;
}

.info-box h3 {
    margin-top: 0;
}

/* CAUSES */
.causes {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin-top: 30px;
}

.cause-card {
    background: #f7fbea;
    border-radius: 13px;
    padding: 25px 17px;
    text-align: center;
    box-shadow: 0 3px 12px #00000010;
}

.cause-card h3 {
    color: #26763c;
    margin-bottom: 10px;
}

/* GALLERY */
.gallery-section {
    background: #eef5df;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(6, 200px);
    gap: 18px;
    overflow-x: auto;
    padding: 12px 5px 20px;
}

.photo-card {
    background: white;
    padding: 10px;
    border-radius: 12px;
    text-align: center;
    box-shadow: 0 3px 12px #00000015;
}

.photo-card img {
    width: 100%;
    height: 185px;
    object-fit: cover;
    border-radius: 9px;
    display: block;
}

.photo-card p {
    color: #26763c;
    padding: 10px 0;
    font-weight: bold;
}

.upload-area {
    background: white;
    text-align: center;
    padding: 30px;
    border-radius: 15px;
    margin-top: 30px;
}

.upload-btn {
    display: inline-block;
    background: #23763b;
    color: white;
    padding: 14px 30px;
    border-radius: 30px;
    cursor: pointer;
    margin: 15px;
    font-weight: bold;
}

.upload-btn:hover {
    background: #145328;
}

#photoUpload {
    display: none;
}

/* TEAM MEMBERS */
.team-section {
    background: white;
}

.team-container {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
    margin-top: 35px;
}

.team-card {
    background: #f1f7e5;
    border-radius: 15px;
    text-align: center;
    padding: 28px 12px;
    border-bottom: 5px solid #438b4c;
    box-shadow: 0 3px 12px #00000010;
    overflow-wrap: anywhere;
}

.team-number {
    background: #26763c;
    color: white;
    width: 45px;
    height: 45px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto 15px;
    font-weight: bold;
}

.team-card h3 {
    color: #216b34;
    margin-bottom: 10px;
}

/* EDIT TEAM PANEL */
.edit-panel {
    background: #f0f7df;
    padding: 25px;
    border-radius: 15px;
    margin-top: 30px;
    display: none;
}

.edit-panel h3 {
    text-align: center;
    margin-bottom: 20px;
    color: #17602e;
}

.edit-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 15px;
}

.edit-card {
    background: white;
    padding: 15px;
    border-radius: 10px;
}

.edit-card label {
    display: block;
    font-weight: bold;
    margin: 10px 0 5px;
}

.edit-card input {
    width: 100%;
    padding: 10px;
    border: 1px solid #aaa;
    border-radius: 7px;
}

.edit-buttons {
    text-align: center;
    margin-top: 25px;
}

.edit-btn {
    background: #e6c84c;
    color: #24452b;
    margin: 20px 0;
}

.save-btn {
    background: #23763b;
    color: white;
}

.cancel-btn {
    background: #777;
    color: white;
    margin-left: 10px;
}

button {
    padding: 12px 25px;
    border: none;
    border-radius: 25px;
    font-weight: bold;
    cursor: pointer;
    transition: .3s;
}

button:hover {
    opacity: .85;
    transform: translateY(-2px);
}

/* FOOTER */
footer {
    background: #174d2a;
    color: white;
    text-align: center;
    padding: 28px;
}

/* RESPONSIVE DESIGN */
@media(max-width: 950px) {
    .causes {
        grid-template-columns: repeat(2, 1fr);
    }

    .team-container,
    .edit-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 600px) {
    nav {
        justify-content: center;
    }

    nav ul {
        justify-content: center;
        gap: 13px;
    }

    .hero h1 {
        font-size: 35px;
    }

    .hero p {
        font-size: 16px;
    }

    section {
        padding: 45px 5%;
    }

    .causes,
    .team-container,
    .edit-grid {
        grid-template-columns: 1fr;
    }

    .section-title {
        font-size: 27px;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->
<nav>
    <h2>🌿 PLANT DISEASES</h2>

    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#team">Our Team</a></li>
    </ul>
</nav>

<!-- HOME -->
<div class="hero" id="home">

    <h1>PLANT DISEASES</h1>

    <p>
        A Community Service Project to understand plant diseases,
        identify their causes, study their effects and create
        awareness about crop protection among farmers.
        Protect Plants, Protect Nature, Protect Our Future!
    </p>

    <button class="main-btn"
    onclick="document.getElementById('introduction').scrollIntoView()">
        Explore More
    </button>

</div>

<!-- INTRODUCTION -->
<section class="introduction" id="introduction">

    <h2 class="section-title">INTRODUCTION</h2>

    <div class="intro-content">

        <h3>🌱 What Are Plant Diseases?</h3>

        <p>
            Plant diseases are abnormal conditions that affect
            the normal growth, development and functioning of
            plants. A healthy plant normally grows, produces
            flowers, fruits and seeds. However, when a plant is
            affected by a disease, its normal activities are
            disturbed. The disease may damage different parts
            of the plant, including roots, stems, leaves,
            flowers and fruits.
        </p>

        <p>
            Plant diseases are mainly caused by harmful
            microorganisms such as fungi, bacteria and viruses.
            They can also develop due to unfavourable
            environmental conditions such as extreme
            temperatures, lack of nutrients, excess water
            and drought. Some diseases spread through soil,
            seeds, insects, water, wind and infected plant
            materials.
        </p>

        <p>
            Common symptoms of plant diseases include yellow
            leaves, brown spots, wilting, leaf curling,
            rotting, unusual growth and premature falling
            of leaves. These symptoms can affect the
            productivity and quality of agricultural crops.
        </p>

        <h3>🌾 Importance of Identifying Plant Diseases</h3>

        <p>
            Identifying plant diseases at an early stage is
            very important in agriculture. When farmers
            recognize disease symptoms early, they can take
            suitable preventive and control measures before
            the disease spreads to other plants.
        </p>

        <p>
            Early identification reduces crop losses,
            improves the quality of agricultural products,
            saves farming expenses and protects farmers'
            income. It also helps in reducing unnecessary
            pesticide usage and supports environmentally
            friendly farming practices.
        </p>

        <div class="info-box">

            <h3>🌿 Why Should We Protect Crops?</h3>

            <p>
                Agriculture is an important source of food
                and livelihood for millions of people.
                Protecting crops from diseases helps maintain
                food production, improve farmers' economic
                conditions and support food security.
                Healthy crops also contribute to a healthy
                environment and sustainable agriculture.
            </p>

        </div>

        <h3>🔬 Common Causes of Plant Diseases</h3>

        <p>
            Plant diseases can occur due to different
            biological and environmental factors. The
            following are some of the major causes.
        </p>

        <div class="causes">

            <div class="cause-card">
                <h3>🍄 Fungi</h3>
                <p>
                    Fungi are common plant disease-causing
                    organisms. They can cause rust, powdery
                    mildew, leaf spots, blights and root rot.
                </p>
            </div>

            <div class="cause-card">
                <h3>🦠 Bacteria</h3>
                <p>
                    Bacterial infections may cause leaf spots,
                    bacterial wilt, soft rot and other plant
                    tissue damage.
                </p>
            </div>

            <div class="cause-card">
                <h3>🌿 Viruses</h3>
                <p>
                    Plant viruses can cause mosaic patterns,
                    yellowing, leaf curling, stunted growth
                    and reduced crop production.
                </p>
            </div>

            <div class="cause-card">
                <h3>☀️ Environment</h3>
                <p>
                    Drought, excess moisture, poor soil
                    drainage, nutrient deficiency and
                    extreme temperatures can damage plants.
                </p>
            </div>

        </div>

        <h3>🌻 Prevention and Control of Plant Diseases</h3>

        <div class="info-box">
            <p>
                1. Use healthy and disease-free seeds.<br>
                2. Maintain proper irrigation and drainage.<br>
                3. Remove and safely dispose of infected plant parts.<br>
                4. Maintain cleanliness in agricultural fields.<br>
                5. Follow crop rotation practices.<br>
                6. Use disease-resistant plant varieties.<br>
                7. Control insect pests that spread plant viruses.<br>
                8. Consult agricultural experts for correct treatment.
            </p>
        </div>

        <h3>🌱 Objective of Our Community Service Project</h3>

        <p>
            The main objective of our Community Service
            Project is to create awareness among farmers and
            local communities about different plant diseases,
            their symptoms, causes, prevention and management.
            Through field visits, observations and interaction
            with farmers, we aim to understand the challenges
            faced in crop protection and share useful
            information about maintaining healthy plants.
        </p>

    </div>
</section>

<!-- PHOTO GALLERY -->
<section class="gallery-section" id="gallery">

    <h2 class="section-title">OUR PROJECT GALLERY</h2>

    <p class="section-subtitle">
        Photographs of our CSP field visits, plant observations,
        farmer interactions and awareness activities.
    </p>

    <!-- EXACTLY SIX PHOTO SLOTS -->
    <div class="gallery" id="photoGallery">

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+1" alt="Project photo 1">
            <p>Project Photo 1</p>
        </div>

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+2" alt="Project photo 2">
            <p>Project Photo 2</p>
        </div>

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+3" alt="Project photo 3">
            <p>Project Photo 3</p>
        </div>

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+4" alt="Project photo 4">
            <p>Project Photo 4</p>
        </div>

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+5" alt="Project photo 5">
            <p>Project Photo 5</p>
        </div>

        <div class="photo-card">
            <img src="https://placehold.co/400x300/e8f2dc/276b37?text=Photo+6" alt="Project photo 6">
            <p>Project Photo 6</p>
        </div>

    </div>

    <!-- UPLOAD PHOTOS -->
    <div class="upload-area">

        <h3>📸 UPLOAD YOUR OWN PROJECT PHOTOS</h3>

        <p>
            Select exactly 6 photographs from your computer.
            JPG, JPEG and PNG formats are supported.
        </p>

        <label for="photoUpload" class="upload-btn">
            + UPLOAD PHOTOS
        </label>

        <input
            type="file"
            id="photoUpload"
            accept=".jpg,.jpeg,.png,image/jpeg,image/png"
            multiple
        >

        <p id="photoMessage" aria-live="polite"></p>

    </div>

</section>

<!-- TEAM MEMBERS -->
<section class="team-section" id="team">

    <h2 class="section-title">OUR TEAM MEMBERS</h2>

    <p class="section-subtitle">
        Our four team members working together to complete
        the Plant Diseases Community Service Project.
    </p>

    <!-- EDIT THESE FOUR DETAILS USING THE EDIT BUTTON -->
    <div class="team-container" id="teamContainer"></div>

    <div style="text-align:center">

        <button class="edit-btn" onclick="openEditor()">
            ✏️ EDIT TEAM DETAILS
        </button>

    </div>

    <!-- TEAM EDITING PANEL -->
    <div class="edit-panel" id="editPanel">

        <h3>EDIT STUDENT DETAILS</h3>

        <div class="edit-grid" id="editGrid"></div>

        <div class="edit-buttons">

            <button class="save-btn" onclick="saveTeam()">
                💾 SAVE DETAILS
            </button>

            <button class="cancel-btn" onclick="closeEditor()">
                CANCEL
            </button>

        </div>

        <p id="teamMessage" style="text-align:center;margin-top:15px;"></p>

    </div>

</section>

<!-- FOOTER -->
<footer>

    <h3>🌿 PLANT DISEASES - CSP PROJECT</h3>

    <p>Community Service Project</p>

    <p>Protect Plants, Protect Nature, Protect Our Future!</p>

    <p>© 2026 All Rights Reserved</p>

</footer>

<script>

/* =========================================
   PHOTO GALLERY UPLOAD

   Select exactly 6 JPG, JPEG or PNG photos.
   Photos will immediately appear on website.

   To change photos, click UPLOAD PHOTOS and
   select your new set of six photographs.
========================================= */

const photoUpload = document.getElementById("photoUpload");

photoUpload.addEventListener("change", function(event) {

    const files = Array.from(event.target.files);
    const message = document.getElementById("photoMessage");

    if (files.length !== 6) {
        message.textContent = "Please select exactly 6 photos.";
        photoUpload.value = "";
        return;
    }

    const valid = files.every(file =>
        ["image/jpeg", "image/png"].includes(file.type)
    );

    if (!valid) {
        message.textContent =
        "Only JPG, JPEG and PNG images are allowed.";

        photoUpload.value = "";
        return;
    }

    const gallery = document.getElementById("photoGallery");

    gallery.innerHTML = "";

    files.forEach((file, index) => {

        const reader = new FileReader();

        reader.onload = function(e) {

            const card = document.createElement("div");
            card.className = "photo-card";

            const img = document.createElement("img");
            img.src = e.target.result;
            img.alt = "CSP Photo " + (index + 1);

            const caption = document.createElement("p");
            caption.textContent = "Project Photo " + (index + 1);

            card.appendChild(img);
            card.appendChild(caption);

            gallery.appendChild(card);

        };

        reader.readAsDataURL(file);

    });

    message.textContent =
    "Your 6 project photographs have been selected!";

    photoUpload.value = "";

});


/* =========================================
   TEAM MEMBER DETAILS

   Change the names and roll numbers here,
   or use EDIT TEAM DETAILS on the website.
========================================= */

let students = [

    {name: "B. Raagni", roll: "24JNA05112"},

    {name: "Student 2", roll: "24JNA05140"},

    {name: "Student 3", roll: "24JNA05091"},

    {name: "Student 4", roll: "24JNA05114"}

];


/* DISPLAY FOUR STUDENT CARDS */

function displayTeam() {

    const container =
    document.getElementById("teamContainer");

    container.innerHTML = "";

    students.forEach((student, index) => {

        const card = document.createElement("div");
        card.className = "team-card";

        const number = document.createElement("div");
        number.className = "team-number";
        number.textContent = String(index + 1).padStart(2, "0");

        const name = document.createElement("h3");
        name.textContent = student.name;

        const roll = document.createElement("p");

        const bold = document.createElement("b");
        bold.textContent = "Roll No: ";

        roll.appendChild(bold);
        roll.appendChild(document.createTextNode(student.roll));

        card.appendChild(number);
        card.appendChild(name);
        card.appendChild(roll);

        container.appendChild(card);

    });

}


/* OPEN EDIT PANEL */

function openEditor() {

    const panel = document.getElementById("editPanel");
    const grid = document.getElementById("editGrid");

    grid.innerHTML = "";

    students.forEach((student, index) => {

        const card = document.createElement("div");
        card.className = "edit-card";

        const heading = document.createElement("h4");
        heading.textContent = "Student " + (index + 1);

        const nameLabel = document.createElement("label");
        nameLabel.textContent = "Student Name";

        const nameInput = document.createElement("input");
        nameInput.id = "name" + index;
        nameInput.value = student.name;

        const rollLabel = document.createElement("label");
        rollLabel.textContent = "Roll Number";

        const rollInput = document.createElement("input");
        rollInput.id = "roll" + index;
        rollInput.value = student.roll;

        card.appendChild(heading);
        card.appendChild(nameLabel);
        card.appendChild(nameInput);
        card.appendChild(rollLabel);
        card.appendChild(rollInput);

        grid.appendChild(card);

    });

    panel.style.display = "block";

    panel.scrollIntoView({
        behavior: "smooth",
        block: "center"
    });

}


/* SAVE EDITED STUDENT DETAILS */

function saveTeam() {

    const updatedStudents = [];

    for (let i = 0; i < 4; i++) {

        const name =
        document.getElementById("name" + i).value.trim();

        const roll =
        document.getElementById("roll" + i).value.trim();

        if (!name || !roll) {

            document.getElementById("teamMessage").textContent =
            "Please fill all four student details.";

            return;
        }

        updatedStudents.push({
            name: name,
            roll: roll
        });

    }

    students = updatedStudents;

    try {
        localStorage.setItem(
            "cspStudents",
            JSON.stringify(students)
        );
    } catch (error) {
        document.getElementById("teamMessage").textContent =
        "Unable to save details in this browser.";
        return;
    }

    displayTeam();

    document.getElementById("teamMessage").textContent =
    "Student details saved successfully!";

    closeEditor();

}


/* CLOSE EDIT PANEL */

function closeEditor() {

    document.getElementById("editPanel").style.display = "none";

}


/* LOAD PREVIOUSLY SAVED DETAILS */

try {

    const savedStudents = localStorage.getItem("cspStudents");

    if (savedStudents) {

        const parsed = JSON.parse(savedStudents);

        if (
            Array.isArray(parsed) &&
            parsed.length === 4 &&
            parsed.every(student =>
                student &&
                typeof student.name === "string" &&
                typeof student.roll === "string"
            )
        ) {

            students = parsed;

        }

    }

} catch (error) {

    console.log("Using default team details.");

}

displayTeam();

</script>

</body>
</html>

