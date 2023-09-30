# Raffler: A raffle app for communities

At deep south devs we luuuurve raffles. Attendees _must_ leave our events
with knowledge, connections _and swag_, donated by our partner companies.
Managing these raffles is arduous—entering, doing the draw, ensuring peeps
get their prizes—so we developed this app to smooth the experience for
attendees entering the raffles and organisers administering them.

## Usage

A Node.js (or compatible) runtime must be available in the environment.
Try [NVM](https://github.com/nvm-sh/nvm/blob/master/README.md) if you don't have one already.

Clone the repo:

    git clone git@github.com:deepsouthdevs/raffle-helper-v2.git

Install dependencies:

    npm install

To connect the existing Supabase backend:

- go to Project Settings > API on Supabase
- copy the project URL
- copy the anon/public API key
- rename the dotenv file (`mv .env.example .env`)
- in the dotenv file, assign the project URL to `SUPABASE_URL` and the API key to `SUPABASE_KEY`

Run the app in dev mode:

    npm start

## Collaborating

The master branch is deployed to Vercel at https://raffler-eight.vercel.app/

For now, we collaborate using [trunk-based development](https://trunkbaseddevelopment.com/).
We can assess if this strategy meets our needs in time.

Create a branch, add your changes and create a pull request (PR). Once merged, the changes
will be deployed to Vercel.

Note: there is no CI set up. If you would like to sponsor CI minutes, please reach out.
For now, please run test locally before requesting a review.

    npm test

### PR guidelines

When collaborating over code, we value direct communication with a factual yet light-hearted tone.
Assume the best intentions. Re-read your comments before submitting them, as though you were the
other party reading them for the first time.

Be charitable, eager to learn and grow, and eager to contribute.

Remember: coding is a team sport that requires both individual brilliance and tight teamwork
to happen in concert. Kind of like football :)

#### Creating a PR

The **PR description** should explain _what_ the change is and the _context_ (or _why_ it's needed).
It should have instructions for using the feature. A screenshot or screen recording might do well,
if appropriate (e.g. for new UI features).

Add as many **reviewers** as you like. Reviews are optional, i.e. just because a review is requested,
does not mean that person must provide feedback.

**Assign** the PR to a developer for review. This should not be a surprise to them! I.e. make sure
they're expecting the review using accepted communication channels.

#### Reviewing a PR

The main question to ask as the reviewer is:

> Does this change improve the product?

The keyword is **improve**. If the change adds a nice feature but introduces a security risk, it might
not be an improvement. If it adds a great feature but the code is a mess, it might well be an improvement.
Use your judgement. The downside of messy code is that subsequent developers have to do more work to
change the code, or iterate the feature. These are trade-offs that only the developer involved can make
as the situation arises, and we back you to make the right call. Just keep in mind the maxim:

> Does this change improve the product?

Engineers are often tempted to leave many comments that have no bearing on the product whatsoever,
such as style and formatting preferences, arbitrary refactors and the like. Try resist this urge.

If the change does not improve the product, a review isn't necessary. Take the conversion off Github
and address the deeper issues.

If the change has risks but is otherwise solid, leave a 'Request changes' review. Once the risks
have been addressed, approve the PR.

If the change improves the product but there are more minor concerns, approve the PR and leave comments.

#### Responding to PR reviews

As the change author, you are in control of the PR. Once approved, merge at will. If there
are comments to address, you may address them in the current PR, or a subsequent PR, or not at all.
If changes have been requested, address these as a priority.