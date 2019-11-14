# Simple-Javascript-Accordion
Pure Simple Javascript Accordion
Codepen URl https://codepen.io/sachindesai/pen/GRRYEwR

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: sans-serif;
            padding: 30px;
        }

        .acc-title {
            padding: 0.8rem 1.2rem;
            background: #232323;
            border-bottom: 1px solid #111;
            color: #fff;
            cursor: pointer;
        }

        .acc-title.active {
            background: brown;
            border-bottom: 1px solid #ddd;
        }

        .acc-content {
            padding: 0.8rem 1.2rem;
            background: #f1f1f1;
            display: none;
        }

        .acc-content.active {
            display: block;
        }
    </style>



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
