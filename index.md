```c
page->layout = "home";

global.url = "https://recepefee.github.io";
global.title = "Recep EFE";
global.description = "Elektrik-Elektronik Mühendisi";
global.favicon_path = "/sigorta_64x64.png";


ADD_SOCIAL("github", "https://github.com/Recepefee");
ADD_SOCIAL("linkedin", "https://www.linkedin.com/in/recep-efe/");

```

<br>

## PROJELER

<? sort_pages_alt(&global.posts); ?>
<? sort_pages_alt(&global.projects); ?>

<ul class="post-list">
    <? for (int i = 0; i < global.projects.count; i++) { ?>
        <li>
            <a href="<? STR(global.projects.items[i]->url) ?>">
                <? STR(global.projects.items[i]->title)?>
            </a>
        </li>
    <? } ?>
</ul>

## NASIL?
<ul class="post-list">
    <? for (int i = 0; i < global.posts.count; i++) { ?>
        <li>
            <a href="<? STR(global.posts.items[i]->url) ?>">
                <? STR(global.posts.items[i]->title) STR(" - ") ?> 
                <? STR(global.posts.items[i]->description) ?>
            </a>
        </li>
    <? } ?>
</ul>
