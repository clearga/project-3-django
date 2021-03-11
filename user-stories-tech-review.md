# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Project Tech Review: User Stories

**Elevator Pitch:** A tech review site where experts post reviews of tech products to inform their users of what to buy and what to skip. Users can post comments on reviews to share feedback or their own experiences.
---

## Sprint 1: Basic Auth & Profiles

**A user should be able to:**

1. Navigate to "/" and see a basic splash page with:

- The name of the website.
- Links to "Log In" and "Sign Up".

2. Sign up for an account.
3. Log in to their account if they already have one.
4. Be redirected to their public profile page after logging in.
5. On their public profile page, see their name, and their join date.
6. See the site-wide header on every page with:

- A link to "Log Out" if they're logged in.
- Links to "Log In" and "Sign Up" if they're logged out.

7. Update their profile by making changes to their name.
8. An admin user should be able to add a review to the site through the admin panel.

### Bonuses

**A user should be able to:**

1. See a "default" profile photo on their profile page before adding their own photo.
2. Update their profile photo (consider using Paperclip or Uploadcare).
3. See their profile photo next to their posts.
4. Receive a welcome email after creating an account.

---

## Sprint 2: CRUD

**A user should be able to:**

1. View a single review page (at "/reviews/1") including:

- The review title.
- The rating of the product.
- At least one high quality image of the product being reviewed.

2. View a list of reviews on the Home page:

- Sorted by newest first.
- With the review titles linked to the individual review "show" pages.

3. Use an "Add Comment" button on a single review page to pull up the new comment form.
4. Create a new comment for a review.
5. Click "Edit" on ANY individual comment, and be redirected to the edit form.
6. Click "delete" on ANY individual comment, then:

- See a pop-up that says: "Are you sure you want to delete this comment?"
- If the user confirms, delete the comment.

### Bonuses

**A user should be able to:**

1. Visit review pages via pretty urls, like "/reviews/iphone-x".
2. Visit user profile pages via pretty urls, like "/users/james".
3. On the homepage:

- See review content truncated to 1000 characters max, with a link to view more.
- See a relative published date, e.g. "2 days ago".

---

## Sprint 3: Validations & Authorization

**A user should be able to:**

1. Verify that a new comment they create is successfully published on the correct review page.

A user CANNOT save invalid data to the database, according to the following rules:

2. A user CANNOT sign up with an email (or username) that is already in use.
3. A comment must be between 1 and 240 characters.
4. A comment must not be empty.

A user is authorized to perform certain actions on the site, according to the following rules:

5. A user MUST be logged in to create/update/destroy resources.
6. A user may only edit their own profile and edit/delete their own comments.

#### Bonuses

**A user should be able to:**

1. View an error message when form validations fail, for the following validations:

- Title must be between 1 and 200 characters.
- Content must not be empty.

2. View only the 10 most recent reviews on the homepage (pagination), with

- A link/button to the "Next" 10.
- A link/button to the "Previous" 10.

3. See a list of review titles they've contributed comments to, on their public profile
4. See the number of comments they've written for each review, next to the review's title in their profile.
5. View all reviews by company name (i.e. filter reviews listed on the homepage by company name).

---

## Sprint 4: Admin Users

### Bonuses

**An admin user should be able to:**

1. Moderate comments on an individual review.
2. See the number of comments a review has on the review's "show" page.
3. Be able to create, edit, and delete reviews through the website rather than through the admin panel.
4. Admins should be able to upload and host their own image files to use in reviews on the site.
