## About this project

<b>Genealogy</b> (family tree) application to record family members.

<img src="https://genealogy.kreaweb.be/img/genealogy-01.webp" alt="Genealogy-01"/>
<img src="https://genealogy.kreaweb.be/img/genealogy-02.webp" alt="Genealogy-02"/>

This application is PHP 8.1 compatible and build using :
<ul>
    <li><a href="https://laravel.com/" target="_blank">Laravel 10</a> (featuring <a href="https://vitejs.dev/" target="_blank">Vite</a>)</li>
    <li><a href="https://jetstream.laravel.com/" target="_blank">Laravel Jetstream 4 (Teams)</a></li>
    <li><a href="https://livewire.laravel.com/" target="_blank">Livewire 3</a></li>
    <li><a href="https://tailwindcss.com/" target="_blank">Tailwind CSS</a></li>
    <li><a href="https://tw-elements.com/" target="_blank">Tailwind Elements</a></li>
    <li><a href="https://tabler-icons.io/" target="_blank">Tabler Icons</a></li>
</ul>

### Logic Concept
1. A person can have 1 biological father (1 person, based on <b>father_id</b>)
2. A person can have 1 biological mother (1 person, based on <b>mother_id</b>)
3. A person can have 1 set of parents, biological or not (1 couple of 2 people, based on <b>parents_id</b>)

4. A person can have 0 to many biological children (n people, based on father_id/mother_id)

5. A person can have 0 to many partners (n people), being part of 0 to many couples (opposite or same biological sex)
6. A person can be part of a couple with the same partner multiple times (remarriage or reunite)

7. A couple can have 0 to many children (based on parents_id as a couple or father_id/mother_id individually)
8. A couple can be married or not, still together or separated in the meantime

### Requirements

<ul>
    <li>At least <a href="https://www.php.net/" target="_blank">PHP 8.1</a></li>
</ul>

### License

<p>Open source under MIT License.</p>

## Demo

<p><a href="https://genealogy.kreaweb.be/" target="_blank">https://genealogy.kreaweb.be/</a></p>

<p>e-mail : <b>administrator@genealogy.test</b><br/>password : <b>password</b></p>

## Features

<ul>
    <li>Light/Dark/System theme</li>
    <li>Fully responsive</li>
    <li>Multi-language, English and Dutch already implemented, language setting saved in authenticated users profile</li>
    <li>Multi-tenancy by Jetstream Teams</li>
    <li>Security through Jetstream Teams Roles & Permissions, 2FA & API can be enabled</li>
    <li>Offcanvas menu</li>
    <li>Image upload with possibility of watermarking</li>
</ul>

### Special features

<p>This application has a built-in <b>Backup Manager</b> :
    <ul>
        <li>Backups can be initiated and managed manually</li>
        <li>Backups can be scheludeld by issuing a cron job on your development or production server</li>
        <li>An e-mail will be send after each backup</li>
   </ul>
</p>

<p>This application has a built-in <b>Log Viewer</b> showing :
    <ul>
        <li>INFO    : All scheduled backups</li>
        <li>DEBUG   : All executed database queries, but only in local development mode</li>
        <li>WARNING : All detected N+1 queries, but only in local development mode</li>
        <li>ERROR   : All detected errors</li>
   </ul>
</p>

<p>This application has a built-in <b>User logging</b> :
    <ul>
        <li>User statistics by country of origin</li>
        <li>User statistics by date</li>
   </ul>
</p>

### To do ...

<ul>
    <li>Allow uploading extra images for people</li>
    <li>Write documentation</li>
    <br/>
    <li>GEDCOM import and export (help needed)</li>
</ul>

## Basic idea (2017)

<p>This application is based on an original implementation by <a href="https://github.com/nafiesl/silsilah" target="_blank">nafiesl</a>.<br/>Thanks for your excellent work.</p>

## Design & Development (2024)

<p>This Laravel application is designed and developed by <a href="https://www.kreaweb.be" target="_blank">kreaweb.be</a>.</p>