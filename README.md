# telegramBot
Telegram bot for my university group.

import telebot
from telebot import types
from datetime import datetime, timedelta

markup = types.ReplyKeyboardMarkup()
markup.row('ПН', 'ВТ')
markup.row('СР', 'ЧТ', 'ПТ')


# import request

bot = telebot.TeleBot('965290995:AAERpHF5_KlGvtt0VKZ-XDQLfOlNZjgQ1SM')


@bot.message_handler(content_types=['text'])
def get_text_messages(message):
    # bot.send_message(message.chat.id, "Bот, что я нашел:", reply_markup=markup)                                                                   ########
    if message.text.lower() == "расписание":
        bot.send_message(message.chat.id, "Here:"  '''
        Понедельник:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. ---
        11:30 -- 13:00      3. Дискретная математика[лекция](401).
        13:30 -- 15:00      4. Высшая / Дискретная математика[лекция](401).
        15:15 -- 16:45      5. Высшая математика[практика](203).

        Вторник: 

        08:00 -- 09:30      1. ---          
        09:45 -- 11:15      2. Базы данных и алгоритмы[лекция](310).
        11:30 -- 13:00      3. Экономика[лекция](310).
        13:30 -- 15:00      4. Физика[лекция](310).
	15:15 -- 16:45	    5. Физ-ра

        Среда:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. Рум.яз.(606 или 607).
        11:30 -- 13:00      3. Англ.яз.(611 или 519).
        13:30 -- 15:00      4. Экономика[лекция](310).
        15:15 -- 16:45      5. Экономика[семинар](201).
			    5. Экономика[семинар](202).

        Четверг:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. Базы данных и алгоритмы[лаба](513A).
			       Дискретная математика[лаба](513B).
        11:30 -- 13:00      3. Физика[лаба](303).
        13:30 -- 15:00      4. Высшая математика[лекция](310).
        
        Пятница:

        08:00 -- 09:30      1. Базы данных и алгоритмы[семинар](611).
        09:45 -- 11:15      2. Физика[семинар](312).
        11:30 -- 13:00      3. Физика[лекция](401).
        13:30 -- 15:00      4. ---
			    4. Дискретная математика[семинар](224).
        

''')

    elif message.text.lower() == 'расписание пн' or message.text.lower() == 'расписание понедельник' or message.text.lower() == 'пн':
        bot.send_message(message.chat.id, '''
        Понедельник:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. ---
        11:30 -- 13:00      3. Дискретная математика[лекция](401).
        13:30 -- 15:00      4. Высшая / Дискретная математика[лекция](401).
        15:15 -- 16:45      5. Высшая математика[практика](203).
        
    

''')

    elif message.text.lower() == 'расписание вт' or message.text.lower() == 'расписание вторник' or message.text.lower() == 'вт':
        bot.send_message(message.chat.id, '''
        Вторник: 

        08:00 -- 09:30      1. ---          
        09:45 -- 11:15      2. Базы данных и алгоритмы[лекция](310).
        11:30 -- 13:00      3. Экономика[лекция](310).
        13:30 -- 15:00      4. Физика[лекция](310).
	15:15 -- 16:45	    5. Физ-ра

''')
    elif message.text.lower() == 'расписание ср' or message.text.lower() == 'расписание среда' or message.text.lower() == 'ср':
        bot.send_message(message.chat.id, '''
        Среда:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. Рум.яз.(606 или 607).
        11:30 -- 13:00      3. Англ.яз.(611 или 519).
        13:30 -- 15:00      4. Экономика[лекция](310).
        15:15 -- 16:45      5. Экономика[семинар](201).
			    5. Экономика[семинар](202).

        ''')

    elif message.text.lower() == 'расписание чт' or message.text.lower() == 'расписание четверг' or message.text.lower() == 'чт':
        bot.send_message(message.chat.id, '''

        Четверг:

        08:00 -- 09:30      1. ---
        09:45 -- 11:15      2. Базы данных и алгоритмы[лаба](513A).
			       Дискретная математика[лаба](513B).
        11:30 -- 13:00      3. Физика[лаба](303).
        13:30 -- 15:00      4. Высшая математика[лекция](310).

''')

    elif message.text.lower() == 'расписание пт' or message.text.lower() == 'расписание пятница' or message.text.lower() == 'пт':
        bot.send_message(message.chat.id, '''

        Пятница:

        08:00 -- 09:30      1. Базы данных и алгоритмы[семинар](611).
        09:45 -- 11:15      2. Физика[семинар](312).
        11:30 -- 13:00      3. Физика[лекция](401).
        13:30 -- 15:00      4. ---
			    4. Дискретная математика[семинар](224).
        
        ''')
    elif message.text.lower() == 'maftei' or message.text.lower() == 'secret':
        bot.send_message(message.chat.id, 'Уже своё отжарил')

    elif message.text.lower() == 'luca':
        bot.send_message(message.chat.id, '7 этаж...')
        
    elif message.text.lower() == 'данила' or message.text.lower() == 'майстренко' or message.text.lower() == "#даниламайстренколох":
        bot.send_message(message.chat.id, '#ДанилаМайстренкоЛох')

    elif message.text.lower() == 'политех':
        bot.send_message(message.chat.id, 'Лучше х*** бить орехи, чем учиться в Политехе')

    elif message.text.lower() == 'расписание суббота' or message.text.lower() == 'расписание воскресенье':
        bot.send_message(message.chat.id, 'Ты что, е****тый(ая)? Дома сиди, выходной!')


    else:
        pass


bot.infinity_polling(none_stop=True)

