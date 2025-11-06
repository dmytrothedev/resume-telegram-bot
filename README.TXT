# 🤖 Resume Telegram Bot

A **personal Telegram bot** built with Python and the `python-telegram-bot` library.  
It introduces me — **Dmytro Khmeliuk** — as a developer and provides interactive information via inline buttons.

---

## 🧠 About the Project

This bot allows users to:
- View my **contacts**, **projects**, and **personal info**
- Interact via **inline buttons** with a clean asynchronous flow
- Get instant responses without delay thanks to **async handlers**
- Navigate smoothly using callback logic

The bot was designed as a personal “digital business card” and runs entirely on Python.

---

## 🧩 Technologies Used

- **Python 3.11+**
- **python-telegram-bot** (v20+)
- **Asyncio**
- Inline keyboards and callback handlers

---

## 🧱 Code Example

```python
async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    keyboard = [
        [InlineKeyboardButton("Contacts", callback_data="contacts")],
        [InlineKeyboardButton("Projects", callback_data="projects")],
        [InlineKeyboardButton("Who is Dmytro Khmeliuk?", callback_data="me")]
    ]
    reply_markup = InlineKeyboardMarkup(keyboard)
    await update.message.reply_text(
        "Hi! This is the bot of Dmytro Khmeliuk. Choose what you want to know:",
        reply_markup=reply_markup
    )
