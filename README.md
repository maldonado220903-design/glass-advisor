export default function VidrieriaWeb() {
  const chatMessages = [
    {
      from: 'ia',
      text: 'Hola 👋 Bienvenido a Vidriería Premium. ¿En qué puedo ayudarte hoy?'
    },
    {
      from: 'user',
      text: 'Quiero cotizar un cancel de baño.'
    },
    {
      from: 'ia',
      text: 'Claro. ¿Podrías decirme las medidas aproximadas y el tipo de vidrio que deseas?'
    }
  ];
  const services = [
    {
      title: 'Vidrio Templado',
      desc: 'Instalación de vidrio templado para hogares, oficinas y negocios.'
    },
    {
      title: 'Canceles de Baño',
      desc: 'Diseños modernos y personalizados para baños residenciales.'
    },
    {
      title: 'Espejos',
      desc: 'Espejos decorativos y funcionales a medida.'
    },
    {
      title: 'Fachadas de Vidrio',
      desc: 'Soluciones elegantes y resistentes para exteriores.'
    }
  ];

  const gallery = [1,2,3,4,5,6];

  return (
    <div className="min-h-screen bg-zinc-950 text-white font-sans">
      {/* Navbar */}
      <header className="fixed top-0 left-0 w-full bg-black/70 backdrop-blur-md border-b border-zinc-800 z-50">
        <div className="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
          <h1 className="text-2xl font-bold tracking-wide">
            Vidriería <span className="text-cyan-400">Premium</span>
          </h1>

          <nav className="hidden md:flex gap-8 text-sm">
            <a href="#inicio" className="hover:text-cyan-400 transition">Inicio</a>
            <a href="#servicios" className="hover:text-cyan-400 transition">Servicios</a>
            <a href="#galeria" className="hover:text-cyan-400 transition">Galería</a>
            <a href="#contacto" className="hover:text-cyan-400 transition">Contacto</a>
          </nav>
        </div>
      </header>

      {/* Hero */}
      <section
        id="inicio"
        className="h-screen flex items-center justify-center px-6 bg-gradient-to-br from-zinc-950 via-zinc-900 to-cyan-950"
      >
        <div className="max-w-4xl text-center">
          <h2 className="text-5xl md:text-7xl font-extrabold leading-tight mb-6">
            Diseño y Calidad
            <span className="block text-cyan-400">en Vidrio</span>
          </h2>

          <p className="text-zinc-300 text-lg md:text-xl mb-10">
            Especialistas en vidrio templado, canceles, espejos y fachadas modernas.
          </p>

          <div className="flex flex-col md:flex-row gap-4 justify-center">
            <button className="bg-cyan-400 text-black px-8 py-4 rounded-2xl font-semibold hover:scale-105 transition">
              Solicitar Cotización
            </button>

            <button className="border border-zinc-700 px-8 py-4 rounded-2xl hover:bg-zinc-900 transition">
              Ver Trabajos
            </button>
          </div>
        </div>
      </section>

      {/* Servicios */}
      <section id="servicios" className="py-24 px-6 max-w-7xl mx-auto">
        <div className="text-center mb-16">
          <h3 className="text-4xl font-bold mb-4">Nuestros Servicios</h3>
          <p className="text-zinc-400 max-w-2xl mx-auto">
            Soluciones profesionales para proyectos residenciales y comerciales.
          </p>
        </div>

        <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          {services.map((service, index) => (
            <div
              key={index}
              className="bg-zinc-900 border border-zinc-800 rounded-3xl p-8 hover:border-cyan-400 transition shadow-xl"
            >
              <div className="w-14 h-14 rounded-2xl bg-cyan-400/20 flex items-center justify-center mb-6">
                <div className="w-6 h-6 rounded-full bg-cyan-400"></div>
              </div>

              <h4 className="text-2xl font-semibold mb-4">{service.title}</h4>
              <p className="text-zinc-400">{service.desc}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Galería */}
      <section id="galeria" className="py-24 px-6 bg-zinc-900">
        <div className="max-w-7xl mx-auto">
          <div className="text-center mb-16">
            <h3 className="text-4xl font-bold mb-4">Galería</h3>
            <p className="text-zinc-400">Ejemplos de nuestros trabajos recientes.</p>
          </div>

          <div className="grid md:grid-cols-3 gap-6">
            {gallery.map((item) => (
              <div
                key={item}
                className="aspect-square rounded-3xl bg-gradient-to-br from-cyan-400/20 to-zinc-800 border border-zinc-700 flex items-center justify-center text-zinc-400 text-lg"
              >
                Imagen Proyecto {item}
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Contacto */}
      <section id="contacto" className="py-24 px-6">
        <div className="max-w-5xl mx-auto grid md:grid-cols-2 gap-12 items-center">
          <div>
            <h3 className="text-4xl font-bold mb-6">
              Cotiza tu proyecto
            </h3>

            <p className="text-zinc-400 text-lg mb-8">
              Contáctanos para recibir atención personalizada y una cotización rápida.
            </p>

            <div className="space-y-4 text-zinc-300">
              <p>📍 Chihuahua, México</p>
              <p>📞 +52 614 000 0000</p>
              <p>✉️ contacto@vidrieria.com</p>
            </div>
          </div>

          <div className="bg-zinc-900 border border-zinc-800 rounded-3xl p-8 shadow-2xl">
            <div className="space-y-5">
              <input
                type="text"
                placeholder="Nombre"
                className="w-full bg-zinc-950 border border-zinc-700 rounded-2xl px-5 py-4 outline-none focus:border-cyan-400"
              />

              <input
                type="email"
                placeholder="Correo"
                className="w-full bg-zinc-950 border border-zinc-700 rounded-2xl px-5 py-4 outline-none focus:border-cyan-400"
              />

              <textarea
                rows="5"
                placeholder="Cuéntanos sobre tu proyecto"
                className="w-full bg-zinc-950 border border-zinc-700 rounded-2xl px-5 py-4 outline-none focus:border-cyan-400"
              ></textarea>

              <button className="w-full bg-cyan-400 text-black py-4 rounded-2xl font-bold hover:scale-[1.02] transition">
                Enviar Cotización
              </button>
            </div>
          </div>
        </div>
      </section>

      {{/* Chatbot IA */}
      <section className="fixed bottom-6 right-6 z-50">
        <div className="w-[340px] bg-zinc-900 border border-zinc-700 rounded-3xl shadow-2xl overflow-hidden">
          <div className="bg-cyan-400 text-black px-5 py-4 font-bold flex items-center justify-between">
            <span>🤖 Asistente IA</span>
            <span className="text-sm font-medium">En línea</span>
          </div>

          <div className="h-[320px] overflow-y-auto p-4 space-y-4 bg-zinc-950">
            {chatMessages.map((msg, index) => (
              <div
                key={index}
                className={`flex ${msg.from === 'user' ? 'justify-end' : 'justify-start'}`}
              >
                <div
                  className={`max-w-[80%] px-4 py-3 rounded-2xl text-sm ${
                    msg.from === 'user'
                      ? 'bg-cyan-400 text-black'
                      : 'bg-zinc-800 text-zinc-200'
                  }`}
                >
                  {msg.text}
                </div>
              </div>
            ))}
          </div>

          <div className="p-4 border-t border-zinc-800 bg-zinc-900 flex gap-3">
            <input
              type="text"
              placeholder="Escribe un mensaje..."
              className="flex-1 bg-zinc-950 border border-zinc-700 rounded-2xl px-4 py-3 outline-none focus:border-cyan-400 text-sm"
            />

            <button className="bg-cyan-400 text-black px-5 rounded-2xl font-semibold hover:scale-105 transition">
              Enviar
            </button>
          </div>
        </div>
      </section>

      {/* Footer */}}
      <footer className="border-t border-zinc-800 py-8 text-center text-zinc-500">
        © 2026 Vidriería Premium — Página creada con React + Firebase.
      </footer>
    </div>
  );
}

