# NFA to DFA Visualizer

Interactive web app implementing the full blueprint from `DFA.pdf`:
- Input + control panel
- Static NFA canvas + step-built DFA canvas
- Trace log
- `Build Graph`, `Next Step`, `Auto Play`, `Reset`
- Frame-based subset construction using core functions:
  - `lambda_closure(T)`
  - `move(T, a)`

## Run

Option 1:
- Open `index.html` directly in a browser.

Option 2 (recommended):
```powershell
cd "g:\Machine Learning\MRNet-v1.0\Project\dfa-visualizer"
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Input format

Use text like:
```text
start: q0
final: q3
alphabet: a,b
q0 -epsilon-> q1
q1 -a-> q1
q1 -b-> q2
q2 -a-> q3
```

Notes:
- Epsilon aliases supported: `epsilon`, `eps`, `λ`, `lambda`, `e`
- Transition format: `state -symbol-> state`
