# The Odin Project: Sign-up Form

## Steps I made

1. I'll be using flexbox for the layout. Setting up the container div.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Project Odin Sign-up Form</title>
        <link rel="stylesheet" href="./styles.css" />
    </head>
    <body>
        <div class="flex-container">test</div>
    </body>
</html>
```

2. Basic CSS and setting up some fonts.

```css
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100..900;1,100..900&display=swap");

@font-face {
    font-family: "norse";
    src: url("./public/Norse-Bold.otf"), format("opentype");
}

* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    font-family: "Noto Sans", sans-serif;
    width: 100%;
    height: 100vh;
}

.flex-container {
    display: flex;
    margin: 0 auto;
    width: 66%;
    height: 100%;
}
```

3. Adding the logo section (left side) and the form section (right side).

```html
<div class="flex-container">
    <div class="logo-container">logo</div>
    <div class="form-container">form</div>
</div>
```

4. The logo container has the logo in the middle upper area and the credits at the bottom.

```html
<div class="logo-container">
    <div class="logo">ODIN</div>
    <div class="credits-for-background">
        <small>
            Photo by
            <a
                href="https://unsplash.com/@haliewestphoto?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
                >Halie West</a
            >
            on
            <a
                href="https://unsplash.com/photos/green-leaf-plant-in-close-up-photography-25xggax4bSA?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash"
                >Unsplash</a
            >
        </small>
    </div>
</div>
```

5. In the form side, there are hero section and the form section.

```html
<div class="form-container">
    <div class="hero-container">hero</div>
    <div class="form-container">form</div>
</div>
```

6. Going back to the logo, adding the logo and changing the font.

```html
<div class="logo">
    <img src="./public/odin-lined.png" alt="odin logo" />
    <span>ODIN</span>
</div>
```

```css
.logo {
    font-family: "norse", system-ui;
    font-size: 5rem;
    color: white;
    background-color: rgba(0, 0, 0, 0.5);
}
```

7. Adding the background image and some adjustments.

```css
.logo-container {
    background: url("./public/halie-west-25xggax4bSA-unsplash.jpg");
    background-size: cover;
}
```

8. Background image credit is hard to read.

```css
.credits-for-background small,
.credits-for-background small a {
    color: white;
}
```

9. Resize logo.

```css
.logo {
    font-family: "norse", system-ui;
    font-size: 5rem;
    color: white;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2rem 10rem;
    margin-top: 20vh;
}

.logo img {
    width: 4rem;
    height: 6rem;
}
```

10. Pushing down the background image credits.

```css
.logo-container {
    background: url("./public/halie-west-25xggax4bSA-unsplash.jpg");
    background-size: cover;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
```

11. Hero section.

```html
<div class="hero-container">
    <p>
        This is not a real online service! You know you need something like this
        in your life to help you realize your deepest dreams. Sign up
        <em>now</em> to get started.
    </p>
    <p>You <em>know</em> you want to.</p>
</div>
```

12. Style it a little bit.

```css
.hero-container {
    font-size: 1.5rem;
    font-weight: bold;
    margin: 15vh 5rem 2rem 5rem;
}

.hero-container p + p {
    margin-top: 1rem;
}
```

13. Basic structure of the form.

```html
<div class="form-main">
    <span>Let's do this!</span>
    <form action="" method="post">
        <section class="first-last-name">
            <div class="form-row">
                <label for="first-name">FIRST NAME</label>
                <input id="first-name" name="first-name" type="text" />
            </div>
            <div class="form-row">
                <label for="last-name">LAST NAME</label>
                <input id="last-name" name="last-name" type="text" />
            </div>
        </section>

        <section class="email-phone">
            <div class="form-row">
                <label for="email">EMAIL</label>
                <input id="email" name="email" type="email" />
            </div>
            <div class="form-row">
                <label for="phone">PHONE NUMBER</label>
                <input id="phone" name="phone" type="tel" />
            </div>
        </section>

        <section class="password">
            <div class="form-row">
                <label for="password">PASSWORD</label>
                <input id="password" name="password" type="password" />
            </div>
            <div class="form-row">
                <label for="password-conform">CONFIRM PASSWORD</label>
                <input
                    id="password-conform"
                    name="password-conform"
                    type="password"
                />
            </div>
        </section>
    </form>
    <button type="submit">Create Account</button>
    <p>Already have an account? <a href="">Log in</a></p>
</div>
```
