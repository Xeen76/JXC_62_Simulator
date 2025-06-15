# JXC-62 Assembly Simulator

A web-based assembly language simulator that helps students understand and visualize the execution of assembly code. The simulator provides step-by-step execution, register state visualization, and AI-powered code analysis.

## Features

- **Interactive Assembly Code Execution**: Write and execute assembly code in real-time
- **Step-by-Step Execution**: Visualize each instruction's effect on registers and memory
- **Register State Tracking**: Monitor changes in PC, ACC, B, MAR, MDR, IR, and NF registers
- **RAM Visualization**: View and modify RAM contents with labels and values
- **AI-Powered Analysis**: Get detailed explanations of code execution using Google's Gemini AI
- **Modern Web Interface**: Clean and intuitive user interface for code editing and execution

## Supported Instructions

The simulator supports the following assembly instructions:

- `MBA` - Move Accumulator to B register
- `LDA` - Load value from memory into Accumulator
- `STA` - Store Accumulator value to memory
- `ADD` - Add B register to Accumulator
- `SUB` - Subtract B register from Accumulator
- `JMP` - Jump to specified address
- `JN` - Jump if Negative flag is set
- `HLT` - Halt program execution

## Prerequisites

- Python 3.10 or higher
- pip (Python package installer)
- Google Gemini API key

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/jaycee-62.git
cd jaycee-62
```

2. Install dependencies:
```bash
pip install flask google-generativeai python-dotenv
```

3. Create a `.env` file in the `jxc_62` directory with your Gemini API key:
```
GEMINI_API_KEY=your_api_key_here
```

## Running the Application

1. Navigate to the project directory:
```bash
cd jxc_62
```

2. Start the Flask server:
```bash
python flask_jc.py
```

3. Open your web browser and go to:
```
http://localhost:5000
```

## Project Structure

```
jaycee-62/
├── jxc_62/
│   ├── flask_jc.py          # Main Flask application
│   ├── processor.py         # Assembly processor simulator
│   ├── templates/           # HTML templates
│   ├── static/             # Static assets (CSS, JS)
│   └── __init__.py
├── tests/                  # Test files
├── pyproject.toml          # Project dependencies
└── README.md              # This file
```

## Usage

1. **Writing Code**:
   - Enter your assembly code in the editor
   - Use labels to reference memory locations
   - Each instruction should be on a new line

2. **Executing Code**:
   - Click "Submit" to load your code
   - Use "Step" to execute one instruction at a time
   - Use "Run" to execute all instructions
   - Use "Reset" to clear the simulator state

3. **Viewing State**:
   - Monitor register values in real-time
   - View RAM contents and their labels
   - See instruction execution steps

4. **AI Analysis**:
   - Get detailed explanations of your code
   - Understand execution flow and register changes
   - Receive optimization suggestions

## Example Code

```assembly
LDA x    ; Load value from memory location 'x'
ADD      ; Add B register to Accumulator
STA y    ; Store result in memory location 'y'
HLT      ; Halt execution
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Google Gemini AI for providing the AI analysis capabilities
- Flask framework for the web interface
- All contributors who have helped improve the project
