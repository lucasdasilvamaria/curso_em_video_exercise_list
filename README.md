# Curso em Video Exercises Generator

This project generates an interactive HTML page with exercises from the "Curso em Vídeo" YouTube course. It organizes the exercises into three worlds (Mundo 1, Mundo 2, Mundo 3) and provides an individual copy button for each exercise, making it easier to study and reference.

## Features

- Reads exercises from Excel files (`.xlsx`) for each world.
- Mundo 1 exercises are mandatory (`exercicios.xlsx`).
- Mundos 2 and 3 are optional (`mundo2.xlsx` and `mundo3.xlsx`). If the files are missing, a placeholder text is shown.
- Displays only the **first sentence** of the description for each exercise.
- Generates an HTML page with:
  - Tabs for Mundo 1, Mundo 2, and Mundo 3.
  - Each exercise in a separate block with title, YouTube link, and description.
  - Individual copy button for each exercise block.
- Automatically opens the generated HTML in the default browser.

## Installation

1. Clone this repository:

```bash
git clone https://github.com/lucasdasilvamaria/curso_em_video_exercise_list.git
cd curso_em_video_exercise_list
````

2. Make sure you have Python installed (>=3.7).

3. Install dependencies:

```bash
pip install openpyxl
```
## Generating the Excel Files

The Excel files for each world (`mundo1.xlsx`, `mundo2.xlsx`, `mundo3.xlsx`) can be generated automatically using the [YouTube Playlist Export project](https://github.com/lucasdasilvamaria/youtube-playlist-export) that we developed earlier.  

- Mundo 1: Export your main playlist as `mundo1.xlsx`.
- Mundo 2 and Mundo 3: You can export additional playlists and name them `mundo2.xlsx` and `mundo3.xlsx`.

Make sure each Excel file has three columns in the first sheet:

| Title | YouTube Link | Description |

## Usage

1. Put your Excel files in the project folder:

* Mundo 1: `mundo1.xlsx`
* Mundo 2: `mundo2.xlsx` (optional)
* Mundo 3: `mundo3.xlsx` (optional)

Each file should have three columns in the first sheet:

\| Title | YouTube Link | Description |

2. Run the generator script:

```bash
python gerar_html.py
```

3. The script will generate `curso_em_video.html` and open it in your default browser.
4. Mundo 2 and Mundo 3 will display placeholder text if the Excel files are not found.

## Example

An exercise block in the generated HTML looks like this:

```
# Título do vídeo: Introduction to Python
#
# Link do vídeo: https://youtube.com/xxxx
# Descrição: Learn the basic concepts of Python
```

Each block has its own **copy button**.

## License

This project is open-source and free to use.


