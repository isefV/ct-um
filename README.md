# CT-UM

A Python implementation of an **Unlimited Register Machine (URM)** from Computability Theory, including a Gödel-number decoder for its instructions.

## Background

A URM program is a sequence of simple instructions over registers (variables), each one of:

- `Z <- Z`
- `Z <- Z + 1`
- `Z <- Z - 1`
- `IF Z != 0 GOTO L`

Instructions can be encoded as a single natural number via Gödel pairing, and a whole program as a list of such numbers. This project implements both directions:

- **`Decoder`** (`Decoder.py`) — decodes a Gödel-numbered instruction list back into readable URM instructions.
- **`UniversalMachine`** (`UM.py`) — a universal machine that decodes and *executes* a Gödel-numbered program against a set of inputs, producing a trace (snapshot) of register values at every step.

## Usage

Run the decoder, entering a space-separated list of instruction codes:

```bash
python Decoder.py
12 3 5
```

Run the universal machine, entering the program (instruction codes) on the first line and its inputs on the second:

```bash
python UM.py
12 3 5
2 3
```

## License

Released under the [MIT License](LICENSE).
