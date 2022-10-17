# LinCircuit-equation-solver
A jupyter notebook based Linear circuit equation solver and calculator. Used to symbolically analize linear circuits, especially in the complex frequency - s domain, but can also be used as a neat linear equation solver and substituter.

The needed libraries are: sympy and ipywidgets, which come by default when installing Anaconda and also antl3r, which you can install with pip.

All of the code is in the file Linsolve clean.ipynb 

Download [Anaconda for windows](https://www.anaconda.com/products/individual)


![Linear Circuit Equation claculator layout](readme_assets/linsolve-explanation.png)

## Description
1. Choose the number of equations you want to solve
2. You can write values or sympy expressions to substitute into the equations
3. Write your equations as LaTeX here (**This is bad:** <img src="https://latex.codecogs.com/svg.image?R_1(I_1&space;&plus;&space;2)" title="R_1(I_1 + 2)" /> This is good:<img src="https://latex.codecogs.com/svg.image?R_1\cdot(I_1&plus;2)" title="R_1\cdot(I_1+2)" />. **The bad way will result in incorrect parsing.**)
4. Buttons
    * Parse equations - read(parse) the equations form section 3.
    * LinSolve for I - solve the system of equations for current I
    * LinSolve for V - solve the system of equations for voltage V
      - To be able to solve a system of eqautions use current or voltage prefixes starting with 1.
    * Inverse laplace trans - Inverse laplace transform the resulting linsolve equations
    * Substitute in equations - substitute the values from section 2. into equations
    * Clear subs values - currently doesn't work
    * Clear Output - clears the outputted equations
5. You can write custom expressions.
    * For example if i want to add 2 to the first parsed equation I would enter: pEq[0] + 2.
    * I can also multiply the second parsed equation by 2: pEq[1] * 2.
    * I can multiply the first parsed equation with the second linsolve equation: pEq[0] * linEq[1]
6. Select into which equations you want to substitute values or from which equations you want to take the inverse laplace transform.



## Getting LaTeX equations from Microsoft Word
If you write your equations in Word you can directly copy them into this calculator. Just make sure you have selected the LaTex equation type in the Equation tab in Word.

Remember to write the equations in a way that the parser can understand correctly: <img src="https://latex.codecogs.com/svg.image?R_1\cdot(I_1&plus;2)" title="R_1\cdot(I_1+2)" />. (This is a bug. If you want to fix it feel free.)

Also, remember to use the \cdot symbol instead of the \bullet symbol. The wrong one is a square the correct a circle. If you look closely you can see the difference. If not take a magnifying lens and try again.

![Word Equations](readme_assets/word-latex.png)

Any improvements or tips appreciated! :)
