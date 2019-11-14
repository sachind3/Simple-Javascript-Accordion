# Simple-Javascript-Accordion
Pure Simple Javascript Accordion
<div id="accordion">
        <div class="acc-panel">
            <div class="acc-title active">1. This is accordion heading</div>
            <div class="acc-content active">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores voluptatum, animi ad culpa quo,
                consequatur suscipit, sint inventore laudantium rerum impedit quam! Dicta, aliquam odit voluptatum
                consequatur ex pariatur totam!
            </div>
        </div>
        <div class="acc-panel">
            <div class="acc-title">2. This is accordion heading</div>
            <div class="acc-content">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores voluptatum, animi ad culpa quo,
                consequatur suscipit, sint inventore laudantium rerum impedit quam! Dicta, aliquam odit voluptatum
                consequatur ex pariatur totam!
            </div>
        </div>
        <div class="acc-panel">
            <div class="acc-title">3. This is accordion heading</div>
            <div class="acc-content">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores voluptatum, animi ad culpa quo,
                consequatur suscipit, sint inventore laudantium rerum impedit quam! Dicta, aliquam odit voluptatum
                consequatur ex pariatur totam!
            </div>
        </div>
        <div class="acc-panel">
            <div class="acc-title">4. This is accordion heading</div>
            <div class="acc-content">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores voluptatum, animi ad culpa quo,
                consequatur suscipit, sint inventore laudantium rerum impedit quam! Dicta, aliquam odit voluptatum
                consequatur ex pariatur totam!
            </div>
        </div>
    </div>
	<script>
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
    </script>
