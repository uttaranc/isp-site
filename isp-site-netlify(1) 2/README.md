# Institutional Signal Press website (free Netlify version)

## One-time setup (about 20 minutes)
1. Create a free GitHub account at github.com. Make a new repository called `isp-site` (Private is fine).
2. On the repository page choose "uploading an existing file" and drag in everything inside this folder (keep the folders). Commit.
3. Edit `admin/config.yml` in GitHub: replace `YOUR-GITHUB-USERNAME` with your GitHub username.
4. Create a free Netlify account at netlify.com and sign in with GitHub. Choose "Add new site" > "Import an existing project" > GitHub > `isp-site`. Leave the build settings empty and deploy. Your site appears at a free address such as `something.netlify.app` (rename it under Site configuration > Change site name).
5. Turn on posting login: in GitHub go to Settings > Developer settings > OAuth Apps > New. Homepage URL = your Netlify address; Authorization callback URL = `https://api.netlify.com/auth/done`. Copy the Client ID and generate a Client secret. In Netlify go to Site configuration > Access & security > OAuth > Install provider > GitHub, and paste them in. Update `site_url` in `admin/config.yml` to your Netlify address.
6. Forms: in Netlify go to Forms and enable form detection, then redeploy. Under Forms > Form notifications add an email notification to uttaranc@gmail.com for both "contact" and "newsletter".

## Posting an update
Go to `your-site.netlify.app/admin`, log in with GitHub, open Site content > Book updates, add an update, and press Publish. The site refreshes in about a minute. You can edit books, covers, store links and imprint details the same way.

## Newsletter
Sign-ups are collected in Netlify > Forms > newsletter (free plan: 100 submissions a month across both forms). Export them as CSV when you send a newsletter, for example with Buttondown or Substack (both free).

## Before going public
- The site is hidden from search engines (`robots.txt`). Delete that file once the imprint name has cleared trademark, business-name and domain checks.
- The name appears in the logo image and in Imprint details. If it changes, replace `images/logo.png` and edit Imprint details.
- To use your own domain later: Netlify > Domain management > Add a domain.
