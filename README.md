# password-maker

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A web-based tool for generating multiple strong passwords with a customizable composition. Its key feature is the display of Japanese phonetic readings (yomigana) for each character, making passwords easier to read and communicate verbally.

## Demo

[**Live Demo**](https://code4fukui.github.io/password-maker/)

The user interface allows you to configure the password structure by setting the number of digits, uppercase letters, lowercase letters, and symbols. You can also specify the total number of passwords to generate before clicking the "パスワードを生成する" (Generate Passwords) button.

## Features

-   **Customizable Composition:** Specify the exact number of digits, uppercase letters, lowercase letters, and symbols for each password.
-   **Batch Generation:** Generate a large number of passwords at once (defaults to 200).
-   **Phonetic Readings (Yomigana):** Each character in the generated passwords is displayed with its Japanese phonetic reading using HTML ruby annotations (`<ruby>`), making them easy to convey verbally.

## How to Use

1.  Open the [live demo](https://code4fukui.github.io/password-maker/).
2.  Adjust the number of characters for each type (数字: Numbers, アルファベット大文字: Uppercase, etc.) using the number input fields. The total length updates automatically.
3.  Set the desired quantity of passwords in the "パスワード生成数" (Number of passwords to generate) field.
4.  Click the **パスワードを生成する** button.
5.  The list of generated passwords will appear on the page.

## Technical Details

This tool is a self-contained HTML file with no build process required.

-   **Dependencies:** It utilizes two external JavaScript modules from `js.sabae.cc`:
    -   [CSV.js](https://js.sabae.cc/CSV.js) for parsing character data.
    -   [rnd.js](https://js.sabae.cc/rnd.js) for random character selection.
-   **Data Source:** Character-to-reading mappings are loaded from local CSV files (`num_d-yomi.csv`, `symbol-yomi.csv`, etc.), which follow a simple `char,yomi` format (e.g., `-,ハイフン`).

## License

MIT License