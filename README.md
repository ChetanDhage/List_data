# My React Project with Tailwind CSS

This is a simple React application that uses Tailwind CSS for styling. The project displays a list of students and allows users to clear the list.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Components](#components)
- [Contributing](#contributing)
- [License](#license)

## Installation

To get started with this project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2. Install the dependencies:

    ```bash
    npm install
    ```

3. Start the development server:

    ```bash
    npm run dev
    ```

4. Open your browser and navigate to `http://localhost:5173`.

## Usage

This project consists of a simple React application that displays a list of students. Each student has a name, age, and image. Users can clear the list by clicking the "Clear All" button.

### App Component

The main component that handles the state and renders the list of students.

### List Component

A functional component that receives the list of students as props and renders each student's details.

### Data File

A simple data file that contains the list of students.

## Components

### App.jsx

```jsx
import React, { useState } from 'react';
import Data from './components/data.jsx';
import List from './components/list.jsx';
import './index.css';

function App() {
  const [people, setPeople] = useState(Data);

  return (
    <div className="container mx-auto p-4">
      <h3 className="text-2xl font-bold mb-4">{people.length} Students</h3>
      <List people={people} />
      <button
        className="mt-4 px-4 py-2 bg-red-500 text-white rounded"
        onClick={() => setPeople([])}
      >
        Clear All
      </button>
    </div>
  );
}

export default App;
