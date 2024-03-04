---
id: 64de4bccf5becb208a48ca97
title: Крок 13
challengeType: 20
dashedName: step-13
---

# --description--

In the Tower of Hanoi puzzle, you can identify the three rods according to their purpose:

- The first rod is the source, where all the disks are stacked on top of each other at the beginning of the game.
- The second rod is an auxiliary rod, and it helps in moving the disks to the target rod.
- The third rod is the target, where all the disks should be placed in order at the end of the game.

Наразі функція `move()` не приймає жодних параметрів. Змініть оголошення функції, щоб вона приймала 4 параметри: `n`, `source`, `auxiliary` та `target`. Then, pass `NUMBER_OF_DISKS` and the strings `'A'`, `'B'`, and `'C'` as arguments to your function call. Порядок має значення.

# --hints--

Your `move()` function should have `n`, `source`, `auxiliary`, and `target` as the parameters. Порядок має значення.

```js
({ test: () => assert(__pyodide.runPython(`
      import inspect
      str(inspect.signature(__locals.get('move'))) == '(n, source, auxiliary, target)'    
  `))
})
```

Передайте `NUMBER_OF_DISKS` і рядки `'A'`, `'B'` та `'C'` до `move()`. Порядок має значення.

```js
({test: () => assert.match(code, /^move\(\s*NUMBER_OF_DISKS\s*,\s*('|")A\1\s*,\s*('|")B\2\s*,\s*('|")C\3\s*\)/m)
})
```

# --seed--

## --seed-contents--

```py
NUMBER_OF_DISKS = 3
number_of_moves = 2**NUMBER_OF_DISKS - 1
rods = {
    'A': list(range(NUMBER_OF_DISKS, 0, -1)),
    'B': [],
    'C': []
}

--fcc-editable-region--
def move():
    print(rods)

move()
--fcc-editable-region--
```
