# Instructions 
1. Copy the HTML Code [HTML Code](#html-code) & Insert in the HTML Page
2. Copy tbe CSS Code [CSS Code](#css-code) & Insert before `</head>`
<br> P.S: If the CSS will be placed inside an existing CSS file, remove `<style>` & `</style>` and just add the CSS code
3. Add JQuery Library [JQuery Library](#jquery-library) Before `</body>`
4. Add JQuery Code [JQuery Code](#jquery-code) After the JQuery Library
<br> P.S: If the JQuery will be placed inside an existing JS file, remove `<script>` & `</script>` and just add the CSS code


### HTML Code
```
<div class="question boxme" id="q1">
    <h2>Do you make under $50,000 a year?</h2>
    <p class="cta_btn_container"><a class="cta_btn q1-btn">Yes</a></p>
    <p class="cta_btn_container"><a class="cta_btn q2-btn">No</a></p>
</div>

<div class="question boxme" id="q2">
    <h2>Are you on Medicare or Medicaid?</h2>
    <p class="cta_btn_container"><a class="cta_btn q2-btn">Yes</a></p>
    <p class="cta_btn_container"><a class="cta_btn q2-btn">No</a></p>
</div>

<div id="loading1" class="loading boxme">
    <div class="dot-falling"></div>
    Reviewing Your Answers
</div>

<div id="loading2" class="loading boxme">
    <div class="dot-falling"></div>
    Searching For Spots Available
</div>

<div id="loading3" class="loading boxme">
    <div class="dot-falling"></div>
    Eligibility Confirmation
</div>

<div id="qualify" class="boxme">
    <div class="qualifyHeadline">Congratulations!</div>

    <div class="loadingCopy"> You Prequalify for
        <b>
            <font color="ff0000"> Special Offer #1:</font>
        </b> this special offers gives you <strong style="color: # 2fbdaa;"> bold text!</strong>
    </div>
    <p style="font-size:18px;">
        Call Us Now Before The Spots Run Out!
    </p>
    <h2><strong>TOUCH TO CALL</strong></h2>
    <p><a href="tel:+11341441555" class="cta_btn">(134) 144-1555</a></p>
    <p style="text-align: center; font-size:18px; font-weight:bold">Act quickly! This Claim expires in
        <strong style="color: #E90E0E;"><span id="countingItem">02:00</span></strong>
    </p>
</div>
```
### CSS Code

```
<style>
a {
    text-decoration: none !important;
}

.question {
    text-align: center;
}

.hidden {
    display: none;
}

.inlineBlock {
    display: inline-block;
}

.cta_btn {
    text-align: center;
    background-color: var(--fbox-main-color);
    border-radius: 3px;
    padding: 15px 0px;
    margin-top: 10px;
    color: white;
    font-weight: bold;
    font-size: 1.5rem;
    text-decoration: none !important;
    display: block;
}

.cta_btn:hover {
    color: white;
    box-shadow: inset 0 2px 2px 0 rgba(255, 255, 255, 0.22), 0 233px 233px 0 rgba(255, 255, 255, 0.12) inset;
    cursor: pointer;
}

.boxme {
    text-align: center;
    padding: 40px 34px;
    background-color: #fff;
    border-top: 5px solid var(--fbox-main-color);
    font-size: 14px;
    line-height: 1.75;
    font-weight: 400;
    box-shadow: 0 0 7px 0 rgba(0, 0, 0, .2);
    transition: all .2s ease;
}

.survey {
    text-align: center;
}

.loading {
    font-size: 24px;
    font-weight: bold;
}

.qualifyHeadline {
    font-size: 32px;
    font-weight: bold;
    color: ff0000;
    margin-bottom: 20px;
}

.loadingCopy {
    font-size: 22px;
    margin-bottom: 25px;
}

#q2,
#q3,
#q4,
#q5,
#q6,
#loading1,
#loading2,
#loading3,
#qualify {
    display: none;
}

.result-p {
    font-size: 18px;
    font-weight: 600;
    text-align: left;
}

.row {
    display: flex;
}

#qualify .card .row .column i {
    margin-right: 5px;
}

.column {
    flex: 50%;
    display: flex;
    align-items: center;
    font-size: 16px;
}

.column h3 {
    font-weight: bold;
}

.end {
    justify-content: end;
}

.fa {
    color: #1aae9f !important;
}

.card {
    padding: 24px;
    border-radius: 10px;
    box-shadow: 1px 5px 10px #888888;
    margin: 25px;
}

#qualify .card .row:nth-child(3) {
    margin-top: 10px;
}

@media(max-width:860px) {
    .column {
        flex: 100%;
        display: flex;
        align-items: center;
        font-size: 13px;
    }

    .row {
        display: block;
    }

    .column h3 {
        font-weight: bold;
        font-size: 19px;
    }

    .result-p {
        font-size: 13px;
        font-weight: 600;
        text-align: left;
    }

    .card {
        padding: 15px;
        box-shadow: 1px 5px 10px #888888;
        margin: 0px;
        margin-top: 20px;
        margin-bottom: 20px;
    }

    .boxme {
        padding: 35px 20px;
    }
}

@keyframes fade-in {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

@keyframes fade-out {
    0% {
        opacity: 1;
    }

    100% {
        opacity: 0;
    }
}

.fade-in {
    animation: fade-in;
    animation-duration: .5s;
}

.fade-out {
    animation: fade-out;
    animation-duration: .5s;
}



.cta-button {
    color: #fff;
    max-width: 349px;
    margin: auto;
    width: 100%;
    padding: 18px 23px 18px 50px;
    display: inline-block;
    border-radius: 70px;
    position: relative;
    text-align: center;
    text-decoration: none;
    border: 2px solid #092251;
    transition: .4s all
}

.cta-button b {
    font-size: 18px;
    color: #fff;
    font-weight: 500
}

.cta-button span {
    letter-spacing: 1.1px
}

.cta-button small {
    font-size: 15px;
    letter-spacing: 0;
    margin-top: 4px;
    display: block
}

.cta-button img {
    position: absolute;
    left: 25px;
    top: 50%;
    transform: translatey(-50%)
}

.cta-button:before {
    content: "";
    -webkit-animation: ripple .6s linear infinite;
    animation: ripple .6s linear infinite;
    border-radius: 100%;
    -webkit-filter: brightness(0) invert(1);
    filter: brightness(0) invert(1);
    position: absolute;
    width: 2px;
    height: 2px;
    left: 29px;
    top: 50%;
    transform: translatey(-50%);
    -webkit-transform: translatey(-50%);
    border-radius: 50%
}

.phone_wave:before {
    left: 12px;
    top: 20px
}

@-webkit-keyframes ripple {
    0% {
        box-shadow: 0 0 0 0 rgba(255, 255, 255, .12), 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12)
    }

    100% {
        box-shadow: 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12), 0 0 0 80px transparent
    }
}

@keyframes ripple {
    0% {
        box-shadow: 0 0 0 0 rgba(255, 255, 255, .12), 0 0 0 20px rgba(255, 255, 255, .1), 0 0 0 40px rgba(255, 255, 255, .1), 0 0 0 60px rgba(255, 255, 255, .1)
    }

    100% {
        box-shadow: 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12), 0 0 0 80px transparent
    }
}

.bottom-bar p {
    margin-bottom: 0px;
}

.bg-orange {
    background-color: #092251;
}

.bottom-bar {
    position: fixed;
    bottom: 0;
    left: 0;
    top: auto;
    width: 100%;
    padding-top: 5px;
    padding-bottom: 10px;
    background-color: #fff;
    text-align: center;
    z-index: 10000020;
    box-shadow: 10px 5px 5px #575757;
}

.bottom-bar__text {
    font-size: 16px;
    font-weight: 600;
    display: inline-block;
    margin-right: 5px
}

.bottom-bar__text:before {
    content: "";
    background-color: #bd9a38;
    width: 6px;
    height: 6px;
    border-radius: 50%;
    display: inline-block;
    margin-bottom: 1px;
    margin-right: 6px
}

.bottom-bar .cta-button b {
    font-size: 16px
}

.bottom-bar .cta-button {
    margin-top: 5px;
    padding: 6px 11px 6px 30px;
    width: auto
}

.bottom-bar .cta-button img {
    display: inline-block;
    width: 10px;
    left: 12px;
    top: 52%
}

.bottom-bar .cta-button:before {
    left: 13px
}

@media only screen and (min-width:800px) {
    footer {
        padding-top: 45px;
        padding-bottom: 35px
    }

    .footer-links {
        margin-bottom: 16px
    }

    .footer-links a {
        display: inline-block
    }

    .footer-links a:nth-child(1) {
        margin-right: 24px
    }

    .footer-links a:nth-child(2) {
        margin-right: 24px
    }

    .bottom-bar {
        padding-top: 10px;
        padding-bottom: 15px
    }

    .bottom-bar__text {
        font-size: 16px
    }

    .bottom-bar__text:before {
        width: 8px;
        height: 8px;
        margin-bottom: 2px
    }
}

@media only screen and (max-width:768px) {
    .bottom-bar #cta-bottom {
        text-align: center;
        flex-direction: column-reverse;
        flex-direction: column-reverse;
        -webkit-flex-direction: column-reverse;
        -webkit-align-items: center;
        align-items: center;
        display: -webkit-box;
        display: -moz-box;
        display: -ms-flexbox;
        display: -webkit-flex;
        display: flex
    }

}

/**
 * ==============================================
 * Dot Falling
 * ==============================================
 */
 .dot-falling {
    position: relative;
    left: -10000px;
    width: 10px;
    height: 10px;
    border-radius: 5px;
    animation: dot-falling 1s infinite linear;
    animation-delay: 0.1s;
  }
  .dot-falling::before, .dot-falling::after {
    content: "";
    display: inline-block;
    position: absolute;
    top: 0;
  }
  .dot-falling::before {
    width: 10px;
    height: 10px;
    border-radius: 5px;
    background-color: #9880ff;
    color: #9880ff;
    animation: dot-falling-before 1s infinite linear;
    animation-delay: 0s;
  }
  .dot-falling::after {
    width: 10px;
    height: 10px;
    border-radius: 5px;
    background-color: #9880ff;
    color: #9880ff;
    animation: dot-falling-after 1s infinite linear;
    animation-delay: 0.2s;
  }
  
  @keyframes dot-falling {
    0% {
      box-shadow: 10000px -10px 0 0 var(--fbox-main-color);
    }
    25%, 50%, 75% {
      box-shadow: 10000px 0 0 0 var(--fbox-main-color);
    }
    100% {
      box-shadow: 10000px 10px 0 0 var(--fbox-main-color);
    }
  }
  @keyframes dot-falling-before {
    0% {
      box-shadow: 9985px -10px 0 0 var(--fbox-main-color);
    }
    25%, 50%, 75% {
      box-shadow: 9985px 0 0 0 var(--fbox-main-color);
    }
    100% {
      box-shadow: 9985px 10px 0 0 var(--fbox-main-color);
    }
  }
  @keyframes dot-falling-after {
    0% {
      box-shadow: 10005px -10px 0 0 var(--fbox-main-color);
    }
    25%, 50%, 75% {
      box-shadow: 10005px 0 0 0 var(--fbox-main-color);
    }
    100% {
      box-shadow: 10005px 10px 0 0 var(--fbox-main-color);
    }
  }

/**
 * ==============================================
 * Centering Falling Dots
 * ==============================================
 */

  .loading {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

:root {
    --fbox-main-color: #F4405E;
}

p:has(.cta_btn) {
    display: flex;
    align-items: center;
    justify-content: center;
    /* flex-direction: column;
    text-align: center; */
}

.cta_btn {
    width: 50%;
}
</style>

```

### JQuery Library
```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```


### JQuery Code
```
<script>
let isOver64 = false;
let isUSA = false;

$(document).ready(function () {
    $(".q1-btn").on("click", function () {
        if ($(".q1-btn").text === "Yes") {
            isOver64 = true;
        } else {
            isOver64 = false;
        }
        $("#q1").fadeOut(500);
        $("#q2").delay(500).fadeIn(500);
    });

    $(".q2-btn").on("click", function () {
        if ($(".q2-btn").text === "Yes") {
            isUSA = true;
        } else {
            isUSA = false;
        }
        waitingInfo()
    });
});

function waitingInfo() {
    q2.style.display = "none";
    loading1.style.display = 'flex';
    loading1.classList.add('fade-in');
    window.setTimeout(function () {
        loading1.classList.add('fade-out');
        window.setTimeout(function () {
            loading1.style.display = 'none';
            loading2.style.display = 'flex';
            loading2.classList.add('fade-in');
            window.setTimeout(function () {
                loading2.classList.add('fade-out');
                window.setTimeout(function () {
                    loading2.style.display = 'none';
                    loading3.style.display = 'flex';
                    loading3.classList.add('fade-in');
                    window.setTimeout(function () {
                        loading3.classList.add('fade-out');
                        window.setTimeout(function () {
                            loading3.style.display = 'none';
                            qualify.style.display = 'block';
                            qualify.classList.add('fade-in');
                            //counting();
                            countdown();
                        }, 500);
                    }, 1700);
                }, 500);
            }, 1700);
        }, 500);
    }, 1700);
}

var interval;

function countdown() {
    clearInterval(interval);
    interval = setInterval(function () {
        var timer = $('#countingItem').html();
        timer = timer.split(':');
        var minutes = timer[0];
        var seconds = timer[1];
        seconds -= 1;
        if (minutes < 0) return;
        else if (seconds < 0 && minutes != 0) {
            minutes -= 1;
            seconds = 59;
        } else if (seconds < 10 && length.seconds != 2) seconds = '0' + seconds;
        else if (minutes < 1) minutes = '00';

        $('#countingItem').html(minutes + ':' + seconds);

        if (minutes == 0 && seconds == 0) clearInterval(interval);
    }, 1000);
}
</script>
```


Full Example
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        a {
            text-decoration: none !important;
        }
        
        .question {
            text-align: center;
        }
        
        .hidden {
            display: none;
        }
        
        .inlineBlock {
            display: inline-block;
        }
        
        .cta_btn {
            text-align: center;
            background-color: var(--fbox-main-color);
            border-radius: 3px;
            padding: 15px 0px;
            margin-top: 10px;
            color: white;
            font-weight: bold;
            font-size: 1.5rem;
            text-decoration: none !important;
            display: block;
        }
        
        .cta_btn:hover {
            color: white;
            box-shadow: inset 0 2px 2px 0 rgba(255, 255, 255, 0.22), 0 233px 233px 0 rgba(255, 255, 255, 0.12) inset;
            cursor: pointer;
        }
        
        .boxme {
            text-align: center;
            padding: 40px 34px;
            background-color: #fff;
            border-top: 5px solid var(--fbox-main-color);
            font-size: 14px;
            line-height: 1.75;
            font-weight: 400;
            box-shadow: 0 0 7px 0 rgba(0, 0, 0, .2);
            transition: all .2s ease;
        }
        
        .survey {
            text-align: center;
        }
        
        .loading {
            font-size: 24px;
            font-weight: bold;
        }
        
        .qualifyHeadline {
            font-size: 32px;
            font-weight: bold;
            color: ff0000;
            margin-bottom: 20px;
        }
        
        .loadingCopy {
            font-size: 22px;
            margin-bottom: 25px;
        }
        
        #q2,
        #q3,
        #q4,
        #q5,
        #q6,
        #loading1,
        #loading2,
        #loading3,
        #qualify {
            display: none;
        }
        
        .result-p {
            font-size: 18px;
            font-weight: 600;
            text-align: left;
        }
        
        .row {
            display: flex;
        }
        
        #qualify .card .row .column i {
            margin-right: 5px;
        }
        
        .column {
            flex: 50%;
            display: flex;
            align-items: center;
            font-size: 16px;
        }
        
        .column h3 {
            font-weight: bold;
        }
        
        .end {
            justify-content: end;
        }
        
        .fa {
            color: #1aae9f !important;
        }
        
        .card {
            padding: 24px;
            border-radius: 10px;
            box-shadow: 1px 5px 10px #888888;
            margin: 25px;
        }
        
        #qualify .card .row:nth-child(3) {
            margin-top: 10px;
        }
        
        @media(max-width:860px) {
            .column {
                flex: 100%;
                display: flex;
                align-items: center;
                font-size: 13px;
            }
        
            .row {
                display: block;
            }
        
            .column h3 {
                font-weight: bold;
                font-size: 19px;
            }
        
            .result-p {
                font-size: 13px;
                font-weight: 600;
                text-align: left;
            }
        
            .card {
                padding: 15px;
                box-shadow: 1px 5px 10px #888888;
                margin: 0px;
                margin-top: 20px;
                margin-bottom: 20px;
            }
        
            .boxme {
                padding: 35px 20px;
            }
        }
        
        @keyframes fade-in {
            0% {
                opacity: 0;
            }
        
            100% {
                opacity: 1;
            }
        }
        
        @keyframes fade-out {
            0% {
                opacity: 1;
            }
        
            100% {
                opacity: 0;
            }
        }
        
        .fade-in {
            animation: fade-in;
            animation-duration: .5s;
        }
        
        .fade-out {
            animation: fade-out;
            animation-duration: .5s;
        }
        
        
        
        .cta-button {
            color: #fff;
            max-width: 349px;
            margin: auto;
            width: 100%;
            padding: 18px 23px 18px 50px;
            display: inline-block;
            border-radius: 70px;
            position: relative;
            text-align: center;
            text-decoration: none;
            border: 2px solid #092251;
            transition: .4s all
        }
        
        .cta-button b {
            font-size: 18px;
            color: #fff;
            font-weight: 500
        }
        
        .cta-button span {
            letter-spacing: 1.1px
        }
        
        .cta-button small {
            font-size: 15px;
            letter-spacing: 0;
            margin-top: 4px;
            display: block
        }
        
        .cta-button img {
            position: absolute;
            left: 25px;
            top: 50%;
            transform: translatey(-50%)
        }
        
        .cta-button:before {
            content: "";
            -webkit-animation: ripple .6s linear infinite;
            animation: ripple .6s linear infinite;
            border-radius: 100%;
            -webkit-filter: brightness(0) invert(1);
            filter: brightness(0) invert(1);
            position: absolute;
            width: 2px;
            height: 2px;
            left: 29px;
            top: 50%;
            transform: translatey(-50%);
            -webkit-transform: translatey(-50%);
            border-radius: 50%
        }
        
        .phone_wave:before {
            left: 12px;
            top: 20px
        }
        
        @-webkit-keyframes ripple {
            0% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, .12), 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12)
            }
        
            100% {
                box-shadow: 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12), 0 0 0 80px transparent
            }
        }
        
        @keyframes ripple {
            0% {
                box-shadow: 0 0 0 0 rgba(255, 255, 255, .12), 0 0 0 20px rgba(255, 255, 255, .1), 0 0 0 40px rgba(255, 255, 255, .1), 0 0 0 60px rgba(255, 255, 255, .1)
            }
        
            100% {
                box-shadow: 0 0 0 20px rgba(255, 255, 255, .12), 0 0 0 40px rgba(255, 255, 255, .12), 0 0 0 60px rgba(255, 255, 255, .12), 0 0 0 80px transparent
            }
        }
        
        .bottom-bar p {
            margin-bottom: 0px;
        }
        
        .bg-orange {
            background-color: #092251;
        }
        
        .bottom-bar {
            position: fixed;
            bottom: 0;
            left: 0;
            top: auto;
            width: 100%;
            padding-top: 5px;
            padding-bottom: 10px;
            background-color: #fff;
            text-align: center;
            z-index: 10000020;
            box-shadow: 10px 5px 5px #575757;
        }
        
        .bottom-bar__text {
            font-size: 16px;
            font-weight: 600;
            display: inline-block;
            margin-right: 5px
        }
        
        .bottom-bar__text:before {
            content: "";
            background-color: #bd9a38;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            display: inline-block;
            margin-bottom: 1px;
            margin-right: 6px
        }
        
        .bottom-bar .cta-button b {
            font-size: 16px
        }
        
        .bottom-bar .cta-button {
            margin-top: 5px;
            padding: 6px 11px 6px 30px;
            width: auto
        }
        
        .bottom-bar .cta-button img {
            display: inline-block;
            width: 10px;
            left: 12px;
            top: 52%
        }
        
        .bottom-bar .cta-button:before {
            left: 13px
        }
        
        @media only screen and (min-width:800px) {
            footer {
                padding-top: 45px;
                padding-bottom: 35px
            }
        
            .footer-links {
                margin-bottom: 16px
            }
        
            .footer-links a {
                display: inline-block
            }
        
            .footer-links a:nth-child(1) {
                margin-right: 24px
            }
        
            .footer-links a:nth-child(2) {
                margin-right: 24px
            }
        
            .bottom-bar {
                padding-top: 10px;
                padding-bottom: 15px
            }
        
            .bottom-bar__text {
                font-size: 16px
            }
        
            .bottom-bar__text:before {
                width: 8px;
                height: 8px;
                margin-bottom: 2px
            }
        }
        
        @media only screen and (max-width:768px) {
            .bottom-bar #cta-bottom {
                text-align: center;
                flex-direction: column-reverse;
                flex-direction: column-reverse;
                -webkit-flex-direction: column-reverse;
                -webkit-align-items: center;
                align-items: center;
                display: -webkit-box;
                display: -moz-box;
                display: -ms-flexbox;
                display: -webkit-flex;
                display: flex
            }
        
        }
        
        /**
         * ==============================================
         * Dot Falling
         * ==============================================
         */
         .dot-falling {
            position: relative;
            left: -10000px;
            width: 10px;
            height: 10px;
            border-radius: 5px;
            animation: dot-falling 1s infinite linear;
            animation-delay: 0.1s;
          }
          .dot-falling::before, .dot-falling::after {
            content: "";
            display: inline-block;
            position: absolute;
            top: 0;
          }
          .dot-falling::before {
            width: 10px;
            height: 10px;
            border-radius: 5px;
            background-color: #9880ff;
            color: #9880ff;
            animation: dot-falling-before 1s infinite linear;
            animation-delay: 0s;
          }
          .dot-falling::after {
            width: 10px;
            height: 10px;
            border-radius: 5px;
            background-color: #9880ff;
            color: #9880ff;
            animation: dot-falling-after 1s infinite linear;
            animation-delay: 0.2s;
          }
          
          @keyframes dot-falling {
            0% {
              box-shadow: 10000px -10px 0 0 var(--fbox-main-color);
            }
            25%, 50%, 75% {
              box-shadow: 10000px 0 0 0 var(--fbox-main-color);
            }
            100% {
              box-shadow: 10000px 10px 0 0 var(--fbox-main-color);
            }
          }
          @keyframes dot-falling-before {
            0% {
              box-shadow: 9985px -10px 0 0 var(--fbox-main-color);
            }
            25%, 50%, 75% {
              box-shadow: 9985px 0 0 0 var(--fbox-main-color);
            }
            100% {
              box-shadow: 9985px 10px 0 0 var(--fbox-main-color);
            }
          }
          @keyframes dot-falling-after {
            0% {
              box-shadow: 10005px -10px 0 0 var(--fbox-main-color);
            }
            25%, 50%, 75% {
              box-shadow: 10005px 0 0 0 var(--fbox-main-color);
            }
            100% {
              box-shadow: 10005px 10px 0 0 var(--fbox-main-color);
            }
          }
        
        /**
         * ==============================================
         * Centering Falling Dots
         * ==============================================
         */
        
          .loading {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        
        :root {
            --fbox-main-color: #F4405E;
        }
        
        p:has(.cta_btn) {
            display: flex;
            align-items: center;
            justify-content: center;
            /* flex-direction: column;
            text-align: center; */
        }
        
        .cta_btn {
            width: 50%;
        }
        </style>
        
</head>
<body>
    <div class="question boxme" id="q1">
        <h2>Do you make under $50,000 a year?</h2>
        <p class="cta_btn_container"><a class="cta_btn q1-btn">Yes</a></p>
        <p class="cta_btn_container"><a class="cta_btn q2-btn">No</a></p>
    </div>
    
    <div class="question boxme" id="q2">
        <h2>Are you on Medicare or Medicaid?</h2>
        <p class="cta_btn_container"><a class="cta_btn q2-btn">Yes</a></p>
        <p class="cta_btn_container"><a class="cta_btn q2-btn">No</a></p>
    </div>
    
    <div id="loading1" class="loading boxme">
        <div class="dot-falling"></div>
        Reviewing Your Answers
    </div>
    
    <div id="loading2" class="loading boxme">
        <div class="dot-falling"></div>
        Searching For Spots Available
    </div>
    
    <div id="loading3" class="loading boxme">
        <div class="dot-falling"></div>
        Eligibility Confirmation
    </div>
    
    <div id="qualify" class="boxme">
        <div class="qualifyHeadline">Congratulations!</div>
    
        <div class="loadingCopy"> You Prequalify for
            <b>
                <font color="ff0000"> Special Offer #1:</font>
            </b> this special offers gives you <strong style="color: # 2fbdaa;"> bold text!</strong>
        </div>
        <p style="font-size:18px;">
            Call Us Now Before The Spots Run Out!
        </p>
        <h2><strong>TOUCH TO CALL</strong></h2>
        <p><a href="tel:+11341441555" class="cta_btn">(134) 144-1555</a></p>
        <p style="text-align: center; font-size:18px; font-weight:bold">Act quickly! This Claim expires in
            <strong style="color: #E90E0E;"><span id="countingItem">02:00</span></strong>
        </p>
    </div>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script>
        let isOver64 = false;
        let isUSA = false;
        
        $(document).ready(function () {
            $(".q1-btn").on("click", function () {
                if ($(".q1-btn").text === "Yes") {
                    isOver64 = true;
                } else {
                    isOver64 = false;
                }
                $("#q1").fadeOut(500);
                $("#q2").delay(500).fadeIn(500);
            });
        
            $(".q2-btn").on("click", function () {
                if ($(".q2-btn").text === "Yes") {
                    isUSA = true;
                } else {
                    isUSA = false;
                }
                waitingInfo()
            });
        });
        
        function waitingInfo() {
            q2.style.display = "none";
            loading1.style.display = 'flex';
            loading1.classList.add('fade-in');
            window.setTimeout(function () {
                loading1.classList.add('fade-out');
                window.setTimeout(function () {
                    loading1.style.display = 'none';
                    loading2.style.display = 'flex';
                    loading2.classList.add('fade-in');
                    window.setTimeout(function () {
                        loading2.classList.add('fade-out');
                        window.setTimeout(function () {
                            loading2.style.display = 'none';
                            loading3.style.display = 'flex';
                            loading3.classList.add('fade-in');
                            window.setTimeout(function () {
                                loading3.classList.add('fade-out');
                                window.setTimeout(function () {
                                    loading3.style.display = 'none';
                                    qualify.style.display = 'block';
                                    qualify.classList.add('fade-in');
                                    //counting();
                                    countdown();
                                }, 500);
                            }, 1700);
                        }, 500);
                    }, 1700);
                }, 500);
            }, 1700);
        }
        
        var interval;
        
        function countdown() {
            clearInterval(interval);
            interval = setInterval(function () {
                var timer = $('#countingItem').html();
                timer = timer.split(':');
                var minutes = timer[0];
                var seconds = timer[1];
                seconds -= 1;
                if (minutes < 0) return;
                else if (seconds < 0 && minutes != 0) {
                    minutes -= 1;
                    seconds = 59;
                } else if (seconds < 10 && length.seconds != 2) seconds = '0' + seconds;
                else if (minutes < 1) minutes = '00';
        
                $('#countingItem').html(minutes + ':' + seconds);
        
                if (minutes == 0 && seconds == 0) clearInterval(interval);
            }, 1000);
        }
        </script>
</body>
</html>
```
