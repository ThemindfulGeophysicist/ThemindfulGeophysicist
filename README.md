## Hi there 👋

<!--
**ThemindfulGeophysicist/ThemindfulGeophysicist** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
// Interactive Personal Website - Shatakshi Goyal's World
import React, { useState } from "react";

export default function HomePage() {
  const [activeTab, setActiveTab] = useState("Cooking");

  const tabs = ["Cooking", "Exercise", "Stories", "Children Work"];

  const content = {
    Cooking: (
      <div>
        <h2 className="text-xl font-semibold mb-2">🍰 Magical Bakes & Brews</h2>
        <p className="mb-2">I experiment with baking, gut-friendly cooking, and a touch of 🍷 homemade wine magic!</p>
        <ul className="list-disc list-inside">
          <li>Studio Ghibli-inspired Mushroom Quiche 🍄</li>
          <li>Vegetarian Lasagna – Totoro-approved!</li>
          <li>Homebrewed Hibiscus Wine – slightly enchanted ✨</li>
        </ul>
      </div>
    ),
    Exercise: (
      <div>
        <h2 className="text-xl font-semibold mb-2">💪 Dancing with Gravity</h2>
        <p>I like to keep moving with strength, stillness, and smiles:</p>
        <ul className="list-disc list-inside">
          <li>Yoga under a banyan tree 🌳</li>
          <li>Resistance bands with a side of Studio Ghibli soundtrack 🎵</li>
          <li>Mindful walks that spark story ideas ✨</li>
        </ul>
      </div>
    ),
    Stories: (
      <div>
        <h2 className="text-xl font-semibold mb-2">📚 Tales from a Storyteller</h2>
        <p>Science, whimsy, and wonder mix in my stories like soot sprites in a candy jar.</p>
        <ul className="list-disc list-inside">
          <li><strong>The Curious Papaya</strong> – A fruit’s quest for self-expression 🥭</li>
          <li><strong>The Forest’s Whisper</strong> – Silence, trees, and secrets 🌲</li>
          <li><strong>Volcano Dreams</strong> – A geoscientist’s bedtime tale 🌋</li>
        </ul>
      </div>
    ),
    "Children Work": (
      <div>
        <h2 className="text-xl font-semibold mb-2">🎨 Kids + Science = Magic</h2>
        <p>I'm a science educator and workshop host who believes every child is a little Hayao Miyazaki in disguise.</p>
        <ul className="list-disc list-inside">
          <li>Hands-on storytelling with a geoscience twist 🔬</li>
          <li>Natural crafts and laughter-powered experiments 🎈</li>
          <li>Reading clubs and imagination explosions 📖</li>
        </ul>
      </div>
    ),
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-yellow-100 via-pink-100 to-purple-100 p-6 animate-fadeIn">
      <div className="max-w-4xl mx-auto bg-white rounded-2xl shadow-xl p-6 border-4 border-pink-300">
        <h1 className="text-4xl font-bold text-center mb-4 text-purple-700">🎥 Shatakshi Goyal’s Magical World</h1>
        <p className="text-center text-gray-600 text-lg mb-6">Geoscientist | Storyteller | Science Educator | Wine Maker | Movie Buff | Book Lover</p>
        <div className="flex justify-center gap-4 mb-6 flex-wrap">
          {tabs.map((tab) => (
            <button
              key={tab}
              onClick={() => setActiveTab(tab)}
              className={`px-4 py-2 rounded-xl transition-all duration-300 font-medium shadow-md ${
                activeTab === tab
                  ? "bg-pink-500 text-white scale-105"
                  : "bg-yellow-200 text-gray-800 hover:bg-pink-200"
              }`}
            >
              {tab}
            </button>
          ))}
        </div>
        <div className="p-4 bg-white rounded-xl border-2 border-yellow-300">
          {content[activeTab]}
        </div>
      </div>
    </div>
  );
}


