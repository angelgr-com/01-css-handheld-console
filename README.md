# Project 1: Handheld videogame console with CSS

## Description 📌

Recreate with CSS the front side of our favorite portable videogame console.

## Objectives 📋

Use HTML and CSS3 with flexbox layout technique:

- **Git / github**
  - **Readme**. Includes project description and at least two sections with details.
  - **Git / github**. More than three commits with a excellent readability and a developed README file.
- **Frontend**
  - **Design + user experience**. Excelent presentation besides originality while trying to push the limits.
  - **Extra features**. Include sound, video o javascript for a more dynamic interaction.
  - **Flex**. Proper use of flex layout tecnique while trying to use it in a non-redundant way.
  - **Components and folder structure**. Use folders to separate files by type. HTML and README in root and JS + CSS in their corresponding folders.
  - **Naming and clean code**. Naming of variables, functions, HTML and CSS elements is clear, accurate and, above all, scalable. The code has quality and instructive comments.

## Development details

- **Start date**: Saturday, 22 January 2022
- **End date**: Sunday, 23 January 2022

### Shell layout

- In order to use flexbox in a relatively complex layout, it is advisable to plan ahead before typing the html code. For that, I used GIMP and divided the shell into 1 row and 6 columns. It was very helpful this outline to be able to match the shape of the shell. I placed it as a background image:

  > segaretro.org | GameGear outline | CC BY 4.0
  >
  > https://segaretro.org/images/2/20/Gamegear_outline.svg

  ![](https://github.com/angelgr-com/01-css-handheld-console/blob/main/readme/01.jpg?raw=true)

- Then I advanced subdividing every column into more rows. The curves were defined using **border-radius** property and some **rotate()** function when needed.

  ![](https://github.com/angelgr-com/01-css-handheld-console/blob/main/readme/02.jpg?raw=true)

  ```css
  body {
      background-image: url("../media/Gamegear_outline.svg");
      background-repeat: no-repeat;
      background-size: 60em 31em;
  }
  
  #_12 {
      height: 10.2em;
      width: 2em;
      background: rgba(255, 166, 0, 0.5);
      border-radius: 100% 0 0 0;
      transform: rotate(1.5deg);
  }
  ```

- To reduce as much as possible duplicated code, I defined some classes to apply them to various div elements:

  ```css
  .flex {
      display: flex;
  }
  
  .flex-end {
      align-items: flex-end;
      justify-content: flex-end;
  }
  
  .row {
      flex-direction: row;
  }
  
  .column {
      flex-direction: column;
  }
  ```
