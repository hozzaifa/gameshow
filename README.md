import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const games = [
  {
    id: 1,
    title: "Endless Runner Car",
    description: "A fun endless runner game with a car!",
    image: "/game1.jpg",
    link: "#"
  },
  {
    id: 2,
    title: "Space Shooter",
    description: "Defend the galaxy from incoming enemies!",
    image: "/game2.jpg",
    link: "#"
  },
  {
    id: 3,
    title: "Puzzle Master",
    description: "Solve exciting puzzles and challenge your brain!",
    image: "/game3.jpg",
    link: "#"
  }
];

export default function GameShowcase() {
  return (
    <div className="p-6">
      <h1 className="text-3xl font-bold text-center mb-6">Game Showcase</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {games.map((game) => (
          <Card key={game.id} className="shadow-lg rounded-lg overflow-hidden">
            <img src={game.image} alt={game.title} className="w-full h-40 object-cover" />
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold">{game.title}</h2>
              <p className="text-gray-600 mb-4">{game.description}</p>
              <Button asChild>
                <a href={game.link} target="_blank" rel="noopener noreferrer">Play Now</a>
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}

