# Gradewing Guide

This project provides documentation and setup instructions for the Gradewing Guide.

## Setup

1. Ensure Python 3.13 is installed.
2. Create a virtual environment:
   ```
   python3.13 -m venv .venv
   ```
3. Activate the virtual environment:
   ```
   source .venv/bin/activate
   ```
4. Upgrade pip:
   ```
   python -m pip install --upgrade pip
   ```
5. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Live server
    ```
   mkdocs serve --livereload
   ```

## Usage

Refer to the documentation in the `docs/` folder for usage instructions.

## Project Structure

- `.venv/` — Python virtual environment
- `requirements.txt` — Python dependencies
- `docs/` — Project documentation
