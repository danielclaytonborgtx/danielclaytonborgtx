# 🛠️ Meu Stack de Tecnologias

## 📋 Visão Geral

```js
"use client";

const meuStack = ["HTML", "CSS", "React", "Next.js", "Node.js", "PostgreSQL", "TypeScript", "JavaScript"];

export default function Home() {
  return (
    <main className="min-h-screen flex flex-col items-center justify-center bg-gray-900 text-white p-6 text-center">
      <h1 className="text-3xl font-bold mb-2">👨‍💻 Daniel</h1>
      <p className="text-gray-300 mb-6">Desenvolvedor Fullstack</p>

      <h2 className="text-lg font-semibold mb-3">🚀 Stack</h2>
      <div className="flex flex-wrap justify-center gap-2 max-w-md">
        {meuStack.map((tech) => (
          <span key={tech} className="bg-gray-700 px-3 py-1 rounded-lg text-sm">
            {tech}
          </span>
        ))}
      </div>

      <div className="mt-8">
        <p className="text-gray-400">
          📬{" "}
          <a href="mailto:danielclaitul@gmail.com" className="text-blue-400 underline">
            Contato
          </a>{" "}
          |{" "}
          <a href="https://github.com/danielclaytonborgtx" target="_blank" className="text-blue-400 underline">
            GitHub
          </a>
        </p>
      </div>
    </main>
  );
}

