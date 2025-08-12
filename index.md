---
global.url = "https://recepefee.github.io";
global.title = "Recep EFE";
global.description = "Elektrik-Elektronik Mühendisi";
global.favicon_path = "/kafam.png";

ADD_PROJECT("bitirme projesi", "bir şeyler yaptım", "/proje/bitirme");
ADD_PROJECT("ikinci proje", "açıklama", "/post/ikinci_proje_postu");

ADD_SOCIAL("github", "https://github.com/Recepefee");
ADD_SOCIAL("linkedin", "https://www.linkedin.com/in/recep-efe/");

page->layout = "home";
---

<br>

## Projeler

<ul class="post-list">
    <? for (int i = 0; i < global.projects.count; i++) { ?>
        <li>
            <a href="<? STR(global.projects.items[i]->url) ?>">
                <? STR(global.projects.items[i]->title) STR(" - ") ?> 
                <? STR(global.projects.items[i]->description) ?>
            </a>
        </li>
    <? } ?>
</ul>



