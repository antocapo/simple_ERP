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
