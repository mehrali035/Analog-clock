# Analog-clock
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            width: 100vw;
            height: 100vh;
            background: linear-gradient(60deg, rgb(58, 4, 13) 30%, rgb(36, 34, 36) 70%);
        }

        .clock {
            width: 25rem;
            height: 25rem;
            background: black;
            border-radius: 50%;
            border: solid white 1rem;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 30px 5px black;
        }

        svg {

            height: 100%;
            width: 100%;
        }

        #hourhand {
            height: 6rem;
            width: 0.4rem;
            background: rgb(47, 255, 193);
        }

        #minhand {
            height: 7rem;
            width: 0.3rem;
            background: red;

        }

        #sechand {
            height: 7rem;
            width: 0.1rem;
            background:rgb(68, 47, 255);
        }
        #hourhand{
            position: absolute;
            margin-left: 180px;
            margin-top: 92px;
            z-index: -1;
            border-radius: 1rem;
            transform-origin: bottom;
        }
        #minhand{
            position: absolute;
            margin-left: 180px;
            margin-top: 74px;
            z-index: -1;
            border-radius: 1rem;
            transform-origin: bottom;
        }
        #sechand{
            position: absolute;
            margin-left: 183px;
            margin-top: 75px;
            z-index: -1;
            border-radius: 1rem;
            transform-origin: bottom;
        }
        path{
            fill: rgb(251, 255, 0) !important;
        }
    </style>
</head>

<body>
    <div class="clock">
        <div id="hourhand"></div>
        <div id="minhand"></div>
        <div id="sechand"></div>
        <svg id="Layer_1" data-name="Layer 1" width="320" height="320" viewBox="0 0 320 320">

            <title>clock new temp</title>

            <circle cx="160" cy="160" r="160" style="fill: none" />

            <g>

                <path
                    d="M90.41829,46.56813l5.40956-3.12228c3.66372,6.36569,7.30721,12.69624,11.01555,19.13948l-5.40783,3.1334Z"
                    style="fill: #fff" />

                <path
                    d="M63.82572,103.36729,60.74883,108.796,41.60629,97.8415,44.69,92.43065C51.07971,96.08258,57.38641,99.68705,63.82572,103.36729Z"
                    style="fill: #fff" />

                <path
                    d="M101.45571,258.35751c1.88379,1.08545,3.5949,2.0714,5.41266,3.11878-3.66,6.36731-7.2817,12.66808-10.97572,19.09463l-5.44582-3.043C94.12876,271.1164,97.76594,264.78275,101.45571,258.35751Z"
                    style="fill: #fff" />

                <path
                    d="M225.17634,43.69783c1.84207,1.05807,3.55478,2.04183,5.40949,3.10718l-11.08332,19.12-5.37464-3.1643C217.80213,56.42121,221.46346,50.104,225.17634,43.69783Z"
                    style="fill: #fff" />

                <path
                    d="M275.58741,232.09351c-6.436-3.71452-12.7328-7.34863-19.12046-11.03525,1.07107-1.82437,2.0849-3.55131,3.16364-5.38875l19.09655,11.025C277.67729,228.49981,276.67215,230.22819,275.58741,232.09351Z"
                    style="fill: #fff" />

                <path
                    d="M45.2884,232.626l-3.10166-5.42688,19.01835-11.11293c1.07566,1.84659,2.08195,3.57412,3.13731,5.38585Z"
                    style="fill: #fff" />

                <path
                    d="M275.56452,91.88642c1.07864,1.87784,2.0608,3.58763,3.10882,5.4121L259.56711,108.361c-1.03017-1.82147-2.015-3.56272-3.0717-5.43122Z"
                    style="fill: #fff" />

                <path
                    d="M214.13,261.22387l5.41128-3.12022c3.68242,6.34842,7.34868,12.669,11.06216,19.071-1.8268,1.07453-3.5612,2.09471-5.36191,3.15387Z"
                    style="fill: #fff" />

                <text transform="translate(149.2113 298.5818)"
                    style="font-size: 42.23796081542969px;fill: #fff;font-family: WorkSans-Regular, Work Sans">6</text>

                <path
                    d="M160.19628,170.99376a9.94806,9.94806,0,0,1-9.944-9.96613,9.86362,9.86362,0,0,1,19.71948-.17825A10.01217,10.01217,0,0,1,160.19628,170.99376Z"
                    style="fill: #fff" />

                <text transform="translate(24.27283 178.11598)"
                    style="font-size: 42.23796081542969px;fill: #fff;font-family: WorkSans-Regular, Work Sans">9</text>

                <text transform="translate(272.33728 178.11598)"
                    style="font-size: 42.23796081542969px;fill: #fff;font-family: WorkSans-Regular, Work Sans">3</text>

                <text transform="translate(138.97937 57.27126)"
                    style="font-size: 42.23796081542969px;fill: #fff;font-family: WorkSans-Regular, Work Sans">12</text>

            </g>

        </svg>
    </div>
    <script>
        let hourhand = document.getElementById('hourhand');
        let minhand = document.getElementById('minhand');
        let sechand = document.getElementById('sechand');


        setInterval(() => {

            let time = new Date();
            let hour = time.getHours();
            let min = time.getMinutes();
            let sec = time.getSeconds();

            let hr = hour*30 + min/2;
            let mr = min*6;
            let sr = sec*6;

            hourhand.style.transform = `rotate(${hr}deg)`;
            minhand.style.transform = `rotate(${mr}deg)`;
            sechand.style.transform = `rotate(${sr}deg)`;

        }, 1000);
    </script>


    </script>
</body>

</html>
