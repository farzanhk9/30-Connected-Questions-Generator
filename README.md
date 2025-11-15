# -*- coding: utf-8 -*-
"""
30 Connected Questions Generator (English Only)
Generates a logical, flowing, 30-question conversation about any topic.

Run:
    python question_generator_en.py
"""

def generate_questions(topic: str):
    topic = topic.strip() if topic else "this topic"

    templates = [
        "What does {} truly mean to you?",
        "What is the first thing that comes to your mind when you hear about {}?",
        "Why do you think {} has become important in today's world?",
        "Where do you believe the roots of {} originally come from?",
        "What personal experience do you have related to {}?",
        "What is the biggest misunderstanding people often have about {}?",
        "If you had to explain {} to a child in a simple way, how would you do it?",
        "Do you think {} is more about emotion or logic? Why?",
        "What fears or concerns do people usually have regarding {}?",
        "What do you think is the biggest advantage of {}?",
        "And what do you consider the biggest downside or risk of {}?",
        "If someone disagrees with {}, what do you believe their strongest argument could be?",
        "Do you personally agree with that argument or not? Why?",
        "How do you think {} will change over the next 10 years?",
        "What role does technology play in shaping the future of {}?",
        "How is society influencing {} today, and how is {} influencing society in return?",
        "What values or beliefs lie behind people's opinions about {}?",
        "If you wanted to use {} for self-improvement, how would you apply it?",
        "What is a common mistake people make when dealing with {}?",
        "What would be the first practical step to fix that mistake?",
        "What difficult or unanswered question do you personally have about {}?",
        "If you could ask one expert a single question about {}, what would you ask?",
        "How do you think media is shaping the public perception of {}?",
        "Which movie, book, or series, in your opinion, represents {} well? And why?",
        "If you were to write a book about {}, what would the title be?",
        "In what way do you think your own perspective about {} might be incomplete or biased?",
        "How do you think the next generation will judge or understand {}?",
        "If {} didn’t exist, what would take its place in people’s lives?",
        "After thinking about {}, what is one thing you feel motivated to change in yourself?",
        "In one sentence, what is the most important lesson you take from reflecting on {}?",
    ]

    questions = [t.format(topic) for t in templates]
    return questions


def main():
    print("🧠 30 Connected Questions Generator (English)")
    print("---------------------------------------------")
    topic = input("Enter a topic (e.g., freedom, AI, love, fear, leadership): ")
    questions = generate_questions(topic)

    print("\nHere are 30 connected questions about", topic or "this topic", ":\n")
    for i, q in enumerate(questions, start=1):
        print(f"{i}. {q}")


if __name__ == "__main__":
    main()

