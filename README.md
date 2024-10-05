<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Градієнтний фон з анімацією</title>
    <style>
        body {
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(to bottom, #001f3f, #b03060);
            color: white;
            font-size: 2em;
            text-align: center;
            transition: background 0.5s;
            overflow: hidden;
        }

        .emoji {
            position: absolute;
            font-size: 48px;
        }

        #cat {
            top: 10%;
            left: 10%;
            animation: moveCat 3s infinite alternate ease-in-out;
        }

        #hearts {
            bottom: 10%;
            right: 10%;
            animation: moveHearts 3s infinite alternate ease-in-out;
        }

        #heart {
            display: none;
            font-size: 48px;
            position: absolute;
            bottom: 20%;
            left: 50%;
            transform: translateX(-50%);
        }

        @keyframes moveCat {
            from {
                transform: translate(0, 0);
            }
            to {
                transform: translate(50px, 50px);
            }
        }

        @keyframes moveHearts {
            from {
                transform: translate(0, 0);
            }
            to {
                transform: translate(-50px, -50px);
            }
        }
    </style>
</head>
<body>
    <div id="text">Просто нажимай на екран 🤍</div>

    <div id="cat" class="emoji">🐈‍⬛🤍🐈‍⬛🤍🐈‍⬛🤍</div>
    <div id="hearts" class="emoji">🤍🐈‍⬛🤍🐈‍⬛🤍🐈‍⬛</div>
    <div id="heart" class="emoji">❤️</div>

    <script>
        const texts = [
"Так що це і з чим його їдять) натискай на екран і читай повідомлення) ",
"Ти завжди була для мене моєю головною підтримкою. ❤️ ",
"Дякую за це. 🌷",
"Мамо, твої обійми числі потім тоді, коли нічого не боюся. 🤗",
"Я часто думаю, як ти встигаєш бути такою сильною. 💪",
"Твої слова - як теплий чай після холодного дня. 🍵",
"Ти завжди знаєш, що сказати, коли мені потрібна порада. 💬",
"Без тебе моє життя було б зовсім іншим. 🌍",
"Ти завжди підтримуєш мене, навіть коли я сама в собі не впевнена. 🤝",
"Ти найлюбляча та терпляча людина, яку я знаю. 💖",
"Мамо, ти найбільший рецепт щастя. 🥰",
"Немає нічого кращого, ніж чути твій сміх. 😄",
"Твої поради - це як GPS для життя, завжди показують правильний шлях. 🗺️",
"Мамо, я просто хотіла сказати, що ти найкраща. 🌟",
"Навіть якщо я далеко, ти завжди поруч у моїх думках. 💭",
"Дякую, що завжди бачиш краще у мені, навіть коли я сама це не бачу. 🌈",
"Кожен день я вдячна, що у мене є така мама, як ти.",
"Дякую за все тепло, яке ти даруєш мені щодня. 🔥",
"Ти завжди знаєш, як зробити будь-який день кращим. 🌞",
"Ти мій головний наставник у житті. 📚",
"Я ніколи не можу віддячити тобі за все, що ти для мене зробила. 💖",
"Ти навчила мене, що важливо завжди залишатися собою. 🌿",
"Мамо, я обожнюю наші маленькі традиції. 🎉",
"Мамо, ти - моя щоденна мотивація бути кращою людиною. 🌈",
"Я намагаюся бути такою ж сильною, як ти, і це дуже надихає. 💪",
"Твої слова зігрівають, як тепла ковдра. 🛏️",
"Мамо, ти - моя головна гордість. 🏆",
"Твої смішні історії завжди піднімають мені настрій. 😂",
"Ти вмієш перетворити будь-яку буденність на свято. 🎉",
"Мамо, з тобою навіть прості речі стають особливими. 🌷",
"Ти завжди знаєш, що робити в будь-якій ситуації. 🧭",
"Ти навчила мене, що любов - це завжди бути поруч. 💕",
"Дякую за всі ті рази, коли ти допомагала мені впоратися з труднощами. 💪",
"Ти - мій головний приклад для наслідування. 🌱",
"Я люблю тебе більше, ніж можна сказати словами. 💖",
"Мамо, дякую за все. Ти - моя найрідніша людина. ❤️",
"З любов'ю Юля ❤️",


        ];

        let index = 0;
        const textElement = document.getElementById('text');
        const heartElement = document.getElementById('heart');

        document.addEventListener('click', () => {
            if (index < texts.length) {
                textElement.innerText = texts[index];
                index++;
            } else {
                textElement.innerText = ""; // Сховати текст
                heartElement.style.display = 'block'; // Показати серце
                index = 0; // Скидаємо index для повторного перегляду
            }
        });
    </script>
</body>
</html>

         
