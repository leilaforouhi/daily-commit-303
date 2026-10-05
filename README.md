def extract_numbers(text):
    numbers = []
    current = ""

    for char in text:
        if char.isdigit():
            current += char
        elif current:
            numbers.append(int(current))
            current = ""

    if current:
        numbers.append(int(current))

    return numbers


if __name__ == "__main__":
    text = "Python 3 is used in 12 projects and 5 scripts."

    print("Text:", text)
    print("Numbers found:", extract_numbers(text))
