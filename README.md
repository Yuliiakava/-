<!DOCTYPE html>
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
         "Таксь что это и с чем его едят) нажимай на екран и чтай сообщения) ",
         "Ты всегда была для меня моей главной поддержкой. ❤️ ",
         "Спасибо за это. 🌷",
         "Мама, твои объятия числе потом тогда, когда ничего не боюсь. 🤗",
         "Я часто думаю, как ты успеваешь быть такой сильной. 💪",
         "Твои слова - как теплый чай после холодного дня. 🍵",
         "Ты всегда знаешь, что сказать, когда мне нужен совет. 💬",
         "Без тебя моя жизнь была бы совсем другой. 🌍",
         "Ты всегда поддерживаешь меня, даже когда я сама в себе не уверена. 🤝",
         "Ты самый любящий и терпеливый человек, которого я знаю. 💖",
         "Мама, ты самый большой рецепт счастья. 🥰",
         "Нет ничего лучше, чем слышать твой смех. 😄",
         "Твои советы - это как GPS для жизни, всегда показывают правильный путь. 🗺️",
         "Мама, я просто хотела сказать, что ты самая лучшая. 🌟",
         "Даже если я далеко, ты всегда рядом в моих мыслях. 💭",
         "Спасибо, что всегда видишь лучшее во мне, даже когда я сама это не вижу. 🌈",
         "Каждый день я благодарна, что у меня есть такая мама, как ты.",
         "Спасибо за все тепло, которое ты даришь мне каждый день. 🔥",
         "Ты всегда знаешь, как сделать любой день лучше. 🌞",
         "Ты мой главный наставник в жизни. 📚",
         "Я никогда не могу отблагодарить тебя за все, что ты для меня сделала. 💖",
         "Ты научила меня, что важно всегда оставаться собой. 🌿",
         "Мама, я обожаю наши маленькие традиции. 🎉",
         "Мама, ты - моя ежедневная мотивация быть лучшим человеком. 🌈",
         "Я стараюсь быть такой же сильной, как ты, и это очень вдохновляет. 💪",
         "Твои слова согревают, как теплое одеяло. 🛏️",
         "Мама, ты - моя главная гордость. 🏆",
         "Твои смешные истории всегда поднимают мне настроение. 😂",
         "Ты умеешь превратить любую обыденность в праздник. 🎉",
         "Мама, с тобой даже простые вещи становятся особенными. 🌷",
         "Ты всегда знаешь, что делать в любой ситуации. 🧭",
         "Ты научила меня, что любовь - это всегда быть рядом. 💕",
         "Спасибо за все те разы, когда ты помогала мне справиться с трудностями. 💪",
         "Ты - мой главный пример для подражания. 🌱",
         "Я люблю тебя больше, чем можно сказать словами. 💖",
         "Мама, спасибо за все. Ты - мой самый родной человек. ❤️",
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

         
