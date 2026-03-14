# councilleaders-org-static
This GitHub repository hosts a static HTML version of the Council Leaders website. ABLE's Council Leaders project has been inactive since at least 2020. The councilleaders.org website was a WordPress installation, which as of March 14, 2026, was version 5.4.11 and last updated in 2022. In March 2026, Stoil Stoilov exported a static HTML version of the last working WordPress installation using the WordPress plugin Simply Static, and uploaded it to be hosted forever for free on GitHub Pages.

## How to upload a Simply Static export to GitHub Pages

Hosting a static version of your WordPress website on GitHub Pages using the Simply Static plugin is an excellent way to get fast, free, and secure hosting.

Because the free version of Simply Static does not connect directly to GitHub via API (that is a Pro feature), you will generate the files and push them to your repository manually.

Here is the step-by-step guide on how to do this:

### Phase 1: Set Up Your GitHub Repository

Before generating your static files, you need to know what your final GitHub Pages URL will be.

1. **Create a GitHub Account:** If you don't have one, sign up at github.com.
2. **Create a New Repository:** * Click the **"+"** icon in the top right and select **New repository**.
* **Repository name:** If you want your URL to be `https://yourusername.github.io`, name the repository exactly **`yourusername.github.io`**. *(If you name it something else, like `my-site`, your URL will be `https://yourusername.github.io/my-site/`)*.
* Make the repository **Public**.
* Check **"Add a README file"** (this initializes the repository so you can upload files later).
* Click **Create repository**.


3. **Enable GitHub Pages:**
* Inside your new repository, click on the **Settings** tab.
* On the left sidebar, click on **Pages**.
* Under "Build and deployment", ensure the Source is set to **Deploy from a branch**.
* Under the "Branch" section, select **`main`** (or `master`) and save.
* *Note: It may take a minute, but GitHub will eventually show a message saying "Your site is live at [Your URL]". Copy this URL.*



---

### Phase 2: Configure Simply Static

Now, go to your WordPress Admin Dashboard to configure the plugin so it formats the website for your new GitHub URL.

1. Go to **Simply Static > Settings**.
2. **General Tab:**
* Under **Delivery Method**, select **ZIP Archive**. (This makes it easy to download all your files at once).


3. **URL Tab (Crucial Step):**
* Under **Destination URLs**, select **Absolute URLs**.
* In the **Absolute URL** field, paste the GitHub Pages URL you copied in Phase 1 (e.g., `https://yourusername.github.io/`).
* *Why? Simply Static will scan your entire WordPress site and replace your local development URLs with your new GitHub URL so images, CSS, and links work properly.*


4. Click **Save Changes**.

---

### Phase 3: Generate and Download Your Site

1. In the WordPress menu, go to **Simply Static > Generate**.
2. Click the big **Generate Static Files** button.
3. The plugin will scan your site. Once it finishes, a link will appear saying **"Click here to download"**.
4. Download the `.zip` file to your computer and **extract/unzip** it. You should see an `index.html` file along with folders like `wp-content` and `wp-includes`.

---

### Phase 4: Upload to GitHub

You now need to get these extracted files into your GitHub repository.

**Method A: Using the Browser (Best for small sites)**

1. Go to your repository on GitHub.
2. Click the **Add file** button and select **Upload files**.
3. Drag and drop all the extracted files and folders (do not upload the `.zip` file itself, upload its *contents*).
4. Add a commit message (e.g., "Initial site upload") and click **Commit changes**.
*(Note: GitHub's web interface has a 100-file limit per upload. If your site has more files, use Method B).*

**Method B: Using GitHub Desktop (Recommended for larger sites and updates)**

1. Download and install [GitHub Desktop](https://desktop.github.com/).
2. Log in with your GitHub account.
3. Click **File > Clone repository** and select the repository you created in Phase 1.
4. Open the folder on your computer where GitHub Desktop cloned the repository.
5. Copy all the extracted files from your Simply Static export and paste them into this cloned folder.
6. Go back to GitHub Desktop. You will see all your files listed as changes.
7. Enter a summary (e.g., "v1.0 static export") in the bottom left box and click **Commit to main**.
8. Click the **Push origin** button at the top to upload the files to GitHub.

---

### Phase 5: View Your Live Website

Once your files are pushed to the `main` branch, GitHub Actions will automatically start building your site.

Wait about 1–3 minutes, then visit your GitHub Pages URL (e.g., `https://yourusername.github.io/`). Your static WordPress site should now be live, secure, and loading incredibly fast!

*(Note: Every time you make changes to your WordPress site—like publishing a new blog post—you will need to repeat Phases 3 and 4 to update the live site).*

---

**Would you like me to explain how to handle contact forms or search functionality, since those typically rely on PHP and break when converted to a static site?**
