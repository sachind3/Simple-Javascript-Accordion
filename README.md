# Simple-Javascript-Accordion
Pure Simple Javascript Accordion

// Javascript code
<code>
(function () {
    let accTitle = document.querySelectorAll('.acc-title');
    for (let i = 0; i < accTitle.length; i++) {
        accTitle[i].addEventListener('click', function () {
            [].forEach.call(accTitle, function (el) {
                el.classList.remove('active');
                el.nextElementSibling.classList.remove('active');
            });
            this.classList.toggle('active');
            this.nextElementSibling.classList.toggle('active');
        });
    }
})();
</code>
