This is an implemention of an ERP System in C++ using QT Builder Framework for the GUI and Oracle Database 


import React, { useState } from "react";

function ClickCounter() {
  const [count, setCount] = useState(0);

  const handleClick = () => {
    const newCount = count + 1;
    setCount(newCount);

    if (newCount === 5) {
      alert("Du hast 5 Mal geklickt!");
    }
  };

  const textStyle = {
    color: count > 5 ? "red" : "black",
    fontSize: "24px",
    marginBottom: "10px",
  };

  return (
    <div className="p-4">
      <div style={textStyle}>Anzahl Klicks: {count}</div>
      <button
        onClick={handleClick}
        className="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600"
      >
        Klicken
      </button>
    </div>
  );
}

export default ClickCounter;














import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      Counter: {count}
      <button onClick={increment}>Increment</button>
    </div>
  );
}




import React, { useState, useEffect } from 'react';

const Timer = () => {
  const [seconds, setSeconds] = useState(0);

  useEffect(() => {
    const intervalId = setInterval(() => {
      setSeconds((prevSeconds) => prevSeconds + 1);
    }, 1000);

    // Cleanup function to clear the interval when the component unmounts
    return () => clearInterval(intervalId);
  }, []); // Empty dependency array for initial setup only

  return <p>Seconds: {seconds}</p>;
};

export default Timer;







import React, { useState, useEffect } from 'react';

const DataFetcher = () => {
  const [data, setData] = useState(null);

  useEffect(() => {
    // Fetch data from an API
    fetch('https://api.example.com/data')
      .then((response) => response.json())
      .then((result) => setData(result))
      .catch((error) => console.error('Error fetching data:', error));
  }, []); // Empty dependency array means this effect runs once after the initial render

  return (
    <div>
      {data ? (
        <ul>
          {data.map((item) => (
            <li>{item.name}</li>
          ))}
        </ul>
      ) : (
        <p>Loading data...</p>
      )}
    </div>
  );
};

export default DataFetcher;





