# 🛠️ Meu Stack de Tecnologias

## 📋 Visão Geral

```js
"use client";

import { motion } from "framer-motion";

const meuStack = {
  fundamentos: ["HTML", "CSS"],
  frontend: ["React", "Next.js", "Hooks", "Context API"],
  backend: ["Node.js", "Express.js", "APIs REST", "Autenticação"],
  bancoDados: ["MySQL", "PostgreSQL", "ORM (Prisma)", "FireBase"],
  linguagens: ["TypeScript", "JavaScript"]
};

export default function Home() {
  return (
    <main className="min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 text-white p-6">
      {/* Header */}
      <section className="text-center my-10">
        <h1 className="text-4xl font-bold">👨‍💻 Olá, eu sou Daniel</h1>
        <p className="text-lg mt-2 text-gray-300">
          Desenvolvedor Fullstack apaixonado por criar soluções modernas
        </p>
      </section>

      <section className="max-w-4xl mx-auto mt-10">
        <h2 className="text-2xl font-semibold mb-6">🚀 Meu Stack</h2>
        <div className="grid md:grid-cols-2 gap-6">
          {Object.entries(meuStack).map(([categoria, tecnologias]) => (
            <motion.div
              key={categoria}
              className="bg-gray-800 rounded-2xl p-5 shadow-lg"
              whileHover={{ scale: 1.05 }}
            >
              <h3 className="text-xl font-bold capitalize mb-3">{categoria}</h3>
              <ul className="space-y-2">
                {tecnologias.map((tech) => (
                  <li
                    key={tech}
                    className="bg-gray-700 px-3 py-1 rounded-lg inline-block text-sm"
                  >
                    {tech}
                  </li>
                ))}
              </ul>
            </motion.div>
          ))}
        </div>
      </section>

      <section className="max-w-4xl mx-auto mt-16">
        <h2 className="text-2xl font-semibold mb-6">📂 Projetos</h2>
        <div className="grid md:grid-cols-2 gap-6">
          <div className="bg-gray-800 rounded-2xl p-5 shadow-lg">
            <h3 className="text-lg font-bold">Sistema de Imóveis</h3>
            <p className="text-gray-400 mt-2">
              App para cadastro e listagem de imóveis, integrado ao backend com autenticação.
            </p>
          </div>
          <div className="bg-gray-800 rounded-2xl p-5 shadow-lg">
            <h3 className="text-lg font-bold">Dashboard Financeiro</h3>
            <p className="text-gray-400 mt-2">
              Controle de receitas e despesas, com gráficos interativos (React + Recharts).
            </p>
          </div>
        </div>
      </section>

      <section className="text-center mt-16">
        <h2 className="text-xl font-semibold">📬 Vamos conversar?</h2>
        <p className="text-gray-400 mt-2">
          Entre em contato pelo{" "}
          <a href="danielclaitul@gmail.com" className="text-blue-400 underline">
            email
          </a>{" "}
          ou me encontre no{" "}
          <a href="https://github.com/danielclaytonborgtx" target="_blank" className="text-blue-400 underline">
            GitHub
          </a>.
        </p>
      </section>
    </main>
  );
}

