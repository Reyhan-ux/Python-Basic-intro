{  
 "cells": [  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "# Python Crash Course\n",  
    "### By [Your Name]\n",  
    "\n",  
    "A no-fluff guide to Python fundamentals with practical examples. Covers everything from basic syntax to intermediate tricks.\n",  
    "\n",  
    "**Topics:**\n",  
    "- Input/Output\n",  
    "- Data Types & Variables\n",  
    "- Control Flow\n",  
    "- Functions & Lambda\n",  
    "- File Handling\n",  
    "- List Comprehensions\n",  
    "- Final Project: To-Do List App"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 1. Input & Output\n",  
    "\n",  
    "### Getting User Input\n",  
    "Python’s `input()` function always returns a string. Convert it if needed:"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "# Basic input\n",  
    "name = input(\"What's your name? \")\n",  
    "age = int(input(\"Your age? \"))  # Convert to integer\n",  
    "\n",  
    "# F-strings (Python 3.6+)\n",  
    "print(f\"Hello {name}! You’re {age} years old.\")\n",  
    "\n",  
    "# Old-school formatting (still works)\n",  
    "print(\"Next year, you’ll be {}.\".format(age + 1))"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 2. Data Types\n",  
    "\n",  
    "**Common Types:**\n",  
    "- `int`: 42\n",  
    "- `float`: 3.14\n",  
    "- `str`: \"hello\"\n",  
    "- `bool`: True/False\n",  
    "- `list`: [1, 2, 3]\n",  
    "- `dict`: {\"key\": \"value\"}\n",  
    "\n",  
    "**Type Checking & Conversion:**"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "# Check type\n",  
    "x = 42\n",  
    "print(type(x))  # <class 'int'>\n",  
    "\n",  
    "# Convert types\n",  
    "y = str(3.14)  # \"3.14\"\n",  
    "z = float(\"10\")  # 10.0"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 3. Control Flow\n",  
    "\n",  
    "### If-Else Statements\n",  
    "Python uses indentation (4 spaces) instead of braces:"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "score = 85\n",  
    "\n",  
    "if score >= 90:\n",  
    "    print(\"A\")\n",  
    "elif score >= 80:\n",  
    "    print(\"B\")  # This runs\n",  
    "else:\n",  
    "    print(\"C\")"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "### Loops\n",  
    "**`for` Loop:**"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "fruits = [\"apple\", \"banana\", \"cherry\"]\n",  
    "\n",  
    "for fruit in fruits:\n",  
    "    print(f\"I like {fruit}!\")"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "**`while` Loop:**"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "count = 0\n",  
    "\n",  
    "while count < 3:\n",  
    "    print(f\"Count: {count}\")\n",  
    "    count += 1"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 4. Functions & Lambda\n",  
    "\n",  
    "### Basic Function"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "def greet(name):\n",  
    "    return f\"Hey {name}!\"\n",  
    "\n",  
    "print(greet(\"Alice\"))"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "### Lambda (Anonymous Function)"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "square = lambda x: x * x\n",  
    "print(square(5))  # 25"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 5. File Handling\n",  
    "\n",  
    "**Read a File:**"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "with open(\"example.txt\", \"r\") as file:\n",  
    "    content = file.read()\n",  
    "    print(content)"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "**Write to a File:**"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "with open(\"output.txt\", \"w\") as file:\n",  
    "    file.write(\"Hello, file!\")"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 6. List Comprehensions\n",  
    "\n",  
    "A concise way to create lists:"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "# Traditional way\n",  
    "squares = []\n",  
    "for i in range(5):\n",  
    "    squares.append(i ** 2)\n",  
    "\n",  
    "# With list comprehension\n",  
    "squares = [i ** 2 for i in range(5)]\n",  
    "print(squares))  # [0, 1, 4, 9, 16]"  
   ]  
  },  
  {  
   "cell_type": "markdown",  
   "metadata": {},  
   "source": [  
    "---\n",  
    "## 7. Final Project: To-Do List\n",  
    "\n",  
    "A simple CLI to-do list app:"  
   ]  
  },  
  {  
   "cell_type": "code",  
   "execution_count": null,  
   "metadata": {},  
   "outputs": [],  
   "source": [  
    "tasks = []\n",  
    "\n",  
    "while True:\n",  
    "    print(\"\\nTo-Do List:\")\n",  
    "    for i, task in enumerate(tasks, 1):\n",  
    "        print(f\"{i}. {task}\")\n",  
    "    \n",  
    "    action = input(\"\\nAdd/Remove/Quit? \").lower()\n",  
    "    \n",  
    "    if action == \"add\":\n",  
    "        tasks.append(input(\"Task: \"))\n",  
    "    elif action == \"remove\":\n",  
    "        tasks.pop(int(input(\"Task number: \")) - 1)\n",  
    "    elif action == \"quit\":\n",  
    "        break"  
   ]  
  }  
 ],  
 "metadata": {  
  "kernelspec": {  
   "display_name": "Python 3",  
   "language": "python",  
   "name": "python3"  
  },  
  "language_info": {  
   "name": "python",  
   "version": "3.8.5"  
  }  
 },  
 "nbformat": 4,  
 "nbformat_minor": 4  
}  
