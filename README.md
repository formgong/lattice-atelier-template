# Lattice Atelier — windows and doors maker site with a Formgong form

**Live demo:** https://atelier.formgong.com · Download: the [latest release](https://github.com/formgong/lattice-atelier-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/lattice-atelier-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Flattice-atelier-template&project-name=lattice-atelier&repository-name=lattice-atelier)

Each button copies the site to your GitHub and publishes it. Then replace `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Шаблон сайту виробника вікон і дверей з формою Formgong

A variation of [Lattice](https://github.com/formgong/lattice-template). It keeps the core: every border sits on a faint grid line, frames draw from a corner and boxes slide in. On top of that it borrows the split hero of designer-window sites:

- Paper sits on the left and the photo bleeds off the right edge from a grid line.
- A stepped dark tab carries the category, and a white caption steps over the photo.
- Scrolling through the pinned hero changes the slide. The photo wipes up and every label rolls letter by letter.
- The page continues with a manifesto, collections, ateliers and the form, and ends on a dark footer.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace `fk_your_access_key` with that key.
3. Optional: put your Turnstile site key in `data-sitekey` on `<form id="fg-form">`.

The form sends `name`, `email`, `phone` (optional), `project`, `message` and `consent`. It shows "received" only when the server answers `success: true`.

**Edit**

- The hero slides are in the `SLIDES` array in the script. Their photos are the `<img>` tags in `.slides`, in the same order.
- The loader words are in `LOADER_WORDS`. The loader plays once per tab session and never with `prefers-reduced-motion: reduce`.
- The cell is 75px on wide screens and 56px below 1080px, where the page flows instead of using the split hero. Change it in `layout()`, not in CSS.
- Every section is a whole number of cells tall, so the grid scrolls with the content and stays aligned. Only the hero is pinned.

**Images.** All four were made for this template with FLUX.1 [schnell] (Apache 2.0), on the free Hugging Face Space and the AI Horde. You may use them in your own site. Replace them with photos of your own work, keeping the file names.

## Українська

Варіація Lattice для виробника вікон і дверей. Сітка, рамки з кута й виїзд блоків лишаються. Головний екран поділено: зліва папір, справа фото. Під час прокрутки слайди змінюються: фото «шторкою» йде вгору, а підписи перекочуються по літерах. Далі йдуть маніфест, колекції, ательє, форма й темний підвал.

**Форма:** замініть `fk_your_access_key` на ключ форми з кабінету Formgong. Форма надсилає ім'я, пошту, телефон, тип проєкту, повідомлення і згоду.

**Картинки:** усі згенеровано для цього шаблону моделлю FLUX.1 [schnell] (ліцензія Apache 2.0) через безкоштовні Hugging Face і AI Horde. Замініть їх фото своїх робіт, зберігши назви файлів.
