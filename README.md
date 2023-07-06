# calc-action

```yml
name: Your Workflow
on: push
jobs:
  calculate:
    runs-on: ubuntu-latest
    steps:
      - id: calc
        uses: DaleSchool/calc-action@v1
        with:
          x: 12
          y: 3
      - name: print results
        run: |
          echo "x + y = ${{ steps.calc.outputs.plus }}"
          echo "x - y = ${{ steps.calc.outputs.minus }}"
```
