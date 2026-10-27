
## 1. Aim

To create a complete responsive profile card using HTML and CSS. The profile card includes a profile image, name, role, description, skills, and a contact button. CSS Box Model properties, background colors, borders, rounded corners, and positioning are used to improve the design.

## 2. Project Structure

Create a folder named `Assignment-6.5` with these files:

```text
Assignment-6.5/
├── index.html
└── style.css
```

## 3. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Assignment 6.5 - Profile Card</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="page-header">
        <h1>My Profile Card</h1>
        <p>A responsive profile card built with HTML and CSS</p>
    </header>

    <main class="page-container">

        <section class="profile-card">

            <!-- Profile Badge -->
            <span class="profile-badge">STUDENT</span>

            <!-- Profile Image -->
            <div class="profile-image-container">
                <img
                    class="profile-image"
                    src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&w=400&q=80"
                    alt="Profile portrait"
                >
            </div>

            <!-- Name and Role -->
            <div class="profile-details">
                <h2 class="profile-name">Shubham Yadav</h2>
                <p class="profile-role">B.Tech CSE Student</p>

                <!-- Description -->
                <p class="profile-description">
                    I am a Computer Science Engineering student interested
                    in web development, programming, and learning new
                    technologies. I enjoy building websites and improving
                    my technical skills through practical projects.
                </p>

                <!-- Skills -->
                <h3 class="skills-heading">My Skills</h3>

                <div class="skills-list">
                    <span class="skill-tag">HTML</span>
                    <span class="skill-tag">CSS</span>
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">Java</span>
                    <span class="skill-tag">C++</span>
                    <span class="skill-tag">Git</span>
                </div>

                <!-- Contact Button -->
                <a
                    class="contact-button"
                    href="mailto:student@example.com"
                >
                    Contact Me
                </a>

                <p class="profile-footer">
                    Learning today, building tomorrow.
                </p>
            </div>

        </section>

    </main>

    <footer class="page-footer">
        <p>Assignment 6.5 | Web Development Practice</p>
    </footer>

</body>
</html>
```

## 4. CSS Code — `style.css`

```css
/* Universal Reset and Box Model */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* General Page Styling */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #1e293b;
    background-color: #f1f5f9;
}

/* Page Header */
.page-header {
    padding: 30px 20px;
    text-align: center;
    color: white;
    background: linear-gradient(135deg, #1e3a8a, #2563eb);
}

.page-header h1 {
    margin-bottom: 8px;
    font-size: 32px;
}

.page-header p {
    font-size: 15px;
}

/* Main Container */
.page-container {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100%;
    max-width: 1100px;
    min-height: 750px;
    margin: 0 auto;
    padding: 40px 20px;
}

/* Profile Card */
.profile-card {
    position: relative;

    width: 100%;
    max-width: 380px;
    padding: 30px;

    text-align: center;
    background-color: white;
    border: 1px solid #dbeafe;
    border-radius: 20px;

    box-shadow: 0 10px 30px rgba(15, 23, 42, 0.12);

    transition: transform 0.3s ease,
                box-shadow 0.3s ease;
}

/* Card Hover Effect */
.profile-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 35px rgba(15, 23, 42, 0.18);
}

/* Positioned Badge */
.profile-badge {
    position: absolute;
    top: 16px;
    right: 16px;
    z-index: 2;

    padding: 5px 12px;
    color: white;
    background-color: #0f766e;
    border-radius: 20px;

    font-size: 11px;
    font-weight: bold;
    letter-spacing: 1px;
}

/* Profile Image Container */
.profile-image-container {
    display: flex;
    justify-content: center;
    margin-bottom: 18px;
}

/* Profile Image */
.profile-image {
    display: block;

    width: 130px;
    height: 130px;
    max-width: 100%;

    object-fit: cover;
    border: 5px solid #dbeafe;
    border-radius: 50%;
}

/* Name */
.profile-name {
    margin-bottom: 5px;
    color: #1e3a8a;
    font-size: 27px;
}

/* Role */
.profile-role {
    margin-bottom: 18px;
    color: #0f766e;
    font-size: 15px;
    font-weight: bold;
}

/* Description */
.profile-description {
    margin-bottom: 22px;
    color: #475569;
    font-size: 14px;
    line-height: 1.8;
}

/* Skills Section */
.skills-heading {
    margin-bottom: 12px;
    color: #1e293b;
    font-size: 17px;
}

/* Skills Container */
.skills-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 8px;

    margin-bottom: 25px;
}

/* Individual Skill Tags */
.skill-tag {
    display: inline-block;

    padding: 6px 12px;
    color: #1d4ed8;
    background-color: #eff6ff;
    border: 1px solid #bfdbfe;
    border-radius: 20px;

    font-size: 12px;
    font-weight: bold;
}

/* Contact Button */
.contact-button {
    display: block;
    width: 100%;
    padding: 12px 18px;

    color: white;
    background-color: #2563eb;
    border: 2px solid #2563eb;
    border-radius: 10px;

    text-decoration: none;
    font-size: 15px;
    font-weight: bold;

    transition: background-color 0.3s ease;
}

.contact-button:hover {
    background-color: #1d4ed8;
    border-color: #1d4ed8;
}

/* Card Footer */
.profile-footer {
    margin-top: 18px;
    color: #64748b;
    font-size: 12px;
    font-style: italic;
}

/* Page Footer */
.page-footer {
    padding: 18px;
    color: white;
    background-color: #0f172a;
    text-align: center;
}

/* Responsive Design for Tablets and Phones */
@media (max-width: 600px) {
    .page-header h1 {
        font-size: 26px;
    }

    .page-container {
        min-height: auto;
        padding: 30px 16px;
    }

    .profile-card {
        max-width: 420px;
        padding: 25px 20px;
    }

    .profile-name {
        font-size: 24px;
    }

    .profile-image {
        width: 115px;
        height: 115px;
    }
}

/* Extra Small Screens */
@media (max-width: 350px) {
    .profile-card {
        padding: 25px 15px;
    }

    .profile-badge {
        top: 10px;
        right: 10px;
        font-size: 9px;
    }

    .profile-name {
        font-size: 21px;
    }
}
```

## 5. CSS Properties Used

| Property | Purpose |
|---|---|
| `padding` | Creates space inside the card and its elements. |
| `margin` | Creates space outside elements. |
| `box-sizing: border-box` | Includes padding and border in the specified dimensions. |
| `background-color` | Adds background colors to the page, card, and skill tags. |
| `border` | Adds a boundary around the card and image. |
| `border-radius` | Creates rounded card corners and a circular profile image. |
| `position: relative` | Establishes the positioning reference for the badge. |
| `position: absolute` | Places the STUDENT badge at the card's top-right corner. |
| `z-index` | Controls the badge's stacking order. |
| `max-width` | Prevents the card from becoming too wide. |
| `object-fit: cover` | Fits the image into the circular frame without distorting it. |
| `display: flex` | Aligns the card and skill tags. |
| `@media` | Adjusts the layout for smaller screens. |

## 6. How Positioning Works in This Project

The profile card uses `position: relative`, while the STUDENT badge uses `position: absolute`.

```css
.profile-card {
    position: relative;
}

.profile-badge {
    position: absolute;
    top: 16px;
    right: 16px;
    z-index: 2;
}
```

The badge is positioned relative to the card instead of the entire webpage. The `z-index` helps keep it above other card content.

## 7. How to Run the Project

1. Open Visual Studio Code.
2. Create a folder named `Assignment-6.5`.
3. Create `index.html` and `style.css` inside the folder.
4. Copy the HTML code into `index.html`.
5. Copy the CSS code into `style.css`.
6. Save both files.
7. Open `index.html` using the Live Server extension.
8. Check that the profile image loads and all card elements are visible.
9. Resize the browser window to test the responsive design.

**Note:** The profile image uses an online image URL, so an internet connection is required for it to load. The contact button opens the visitor's default email application. Replace `student@example.com` with your intended contact email if needed.

## 8. Responsive Testing

Test the profile card at the following viewport widths using Chrome DevTools:

- **Desktop:** 1200px
- **Tablet:** 768px
- **Mobile:** 375px
- **Small mobile:** 320px

To test:

1. Open the webpage in Chrome.
2. Right-click and select **Inspect**.
3. Click the **Toggle device toolbar** icon.
4. Select or enter the viewport widths listed above.
5. Check that the card fits the screen, the image stays circular, skill tags wrap onto new lines, and the contact button remains visible.

## 9. Screenshot Instructions

1. Open the finished webpage using Live Server.
2. Set the browser to a desktop-sized viewport.
3. Make sure the complete profile card is visible.
4. Take a screenshot using `Win + Shift + S`.
5. Save it as `profile-card.png`.
6. Optionally, take another screenshot at a mobile viewport and save it as `profile-card-mobile.png`.

Include the screenshot with both source files in your submission.

## 10. Expected Output

The webpage displays a profile card with:

- A circular profile image.
- Name: Shubham Yadav.
- Role: B.Tech CSE Student.
- A short description.
- Six skill tags.
- A Contact Me button.
- A STUDENT badge positioned at the top-right corner.
- A responsive layout with a colored background, rounded corners, and a subtle shadow.

## 11. Result

A responsive profile card was created successfully using HTML and CSS. The project demonstrates the CSS Box Model, background colors, borders, rounded corners, meaningful class names, and positioning. The layout can be tested at different screen widths.

## 12. Conclusion

Profile cards are useful components for personal portfolios and professional websites. HTML provides the structure, while CSS controls the appearance, spacing, and layout. Responsive design ensures that the card remains usable on desktops, tablets, and mobile devices.

## 13. Submission Checklist

- [ ] `index.html`
- [ ] `style.css`
- [ ] `profile-card.png`
- [ ] Profile image, name, role, description, and skills
- [ ] Contact button
- [ ] Background, border, and rounded corners
- [ ] Positioned badge
- [ ] Responsive testing at different screen widths
- [ ] Result and conclusion
