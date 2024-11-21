# Importing libraries
import random

# Маълумоти савол ва ҷавобҳои оддӣ
qa_database = {
    "Салом": ["Салом! Чӣ тавр метавонам кӯмак кунам?", "Салом! Саволи худро гӯед."],
    "Чӣ гуна кор мекунӣ?": ["Ман як бот ҳастам ва ҳамеша омодаам кӯмак кунам!", "Ман хубам, ташаккур!"],
    "Ту кистӣ?": ["Ман як боти оддии Python ҳастам, ки барои кӯмак сохта шудааст."],
    "Ташаккур": ["Хуш омадед!", "Шумо ҳамеша метавонед ба ман муроҷиат кунед."],
}

# Функсияи ҷавоб додан
def get_response(user_input):
    for question in qa_database:
        if question in user_input:
            return random.choice(qa_database[question])
    return "Мутаассифона, ман ин саволро намефаҳмам. Лутфан саволи дигарро санҷед."

# Барномаи асосӣ
def chatbot():
    print("Салом! Ман боти кӯмакрасон ҳастам. Саволҳои худро бипурсед ё 'Хайр' нависед, то барномаро қатъ кунед.")
    while True:
        user_input = input("Шумо: ")
        if user_input.lower() in ["хайр", "худо ҳофиз"]:
            print("Бот: Худо ҳофиз! Бо шумо сӯҳбат кардан хуб буд!")
            break
        response = get_response(user_input)
        print(f"Бот: {response}")

# Иҷро кардани бот
if __name__ == "__main__":
    darsii.hayot.bot()
