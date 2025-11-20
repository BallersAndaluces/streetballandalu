import React from 'react';
import { motion } from 'framer-motion';
import { Mail, Instagram, MapPin } from 'lucide-react';

const App = () => {
  const fadeInUp = {
    initial: { opacity: 0, y: 30 },
    animate: { opacity: 1, y: 0 },
    transition: { duration: 0.6 }
  };

  const staggerContainer = {
    animate: {
      transition: {
        staggerChildren: 0.15
      }
    }
  };

  return (
    <div className="min-h-screen bg-white text-gray-900 font-sans">
      {/* Hero Section */}
      <section className="relative bg-gradient-to-r from-orange-500 to-orange-600 text-white py-20 px-4 sm:px-6 lg:px-8">
        <div className="max-w-4xl mx-auto text-center">
          <motion.h1
            className="text-4xl md:text-6xl font-bold mb-4"
            variants={fadeInUp}
            initial="initial"
            animate="animate"
          >
            StreetBall Andaluz
          </motion.h1>
          <motion.p
            className="text-xl md:text-2xl font-light mb-8"
            variants={fadeInUp}
            initial="initial"
            animate="animate"
          >
            Vuelve la calle. Vuelve el basket.
          </motion.p>
          <motion.p
            className="text-lg md:text-xl opacity-90 max-w-2xl mx-auto mb-10"
            variants={fadeInUp}
            initial="initial"
            animate="animate"
          >
            Bienvenido a la nueva era del baloncesto callejero en Andalucía.
          </motion.p>
          <motion.div
            variants={fadeInUp}
            initial="initial"
            animate="animate"
          >
            <a
              href="#contacto"
              className="inline-block bg-white text-orange-600 font-semibold px-8 py-4 rounded-full text-lg shadow-lg hover:bg-gray-100 transition-all duration-300"
              aria-label="Contactar con StreetBall Andaluz"
            >
              Únete a la comunidad
            </a>
          </motion.div>
        </div>
        <motion.div
          className="mt-12 flex justify-center"
          variants={fadeInUp}
          initial="initial"
          animate="animate"
        >
          <img
            src="https://placehold.co/800x300/111111/FFFFFF?text=Jugando+3x3+en+la+calle"
            alt="Jugadores compitiendo en una cancha de streetball urbana"
            className="rounded-xl shadow-2xl w-full max-w-5xl"
            width="800"
            height="300"
          />
        </motion.div>
      </section>

      {/* ¿Quiénes somos? */}
      <section id="quienes-somos" className="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div className="max-w-6xl mx-auto">
          <motion.div
            className="text-center mb-16"
            variants={fadeInUp}
            initial="initial"
            animate="animate"
          >
            <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">¿Quiénes somos?</h2>
            <div className="w-24 h-1 bg-orange-500 mx-auto rounded-full"></div>
          </motion.div>
          <motion.div
            variants={staggerContainer}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true, margin: "-100px" }}
            className="grid md:grid-cols-2 gap-12 items-center"
          >
            <div>
              <img
                src="https://placehold.co/600x400/222222/FFFFFF?text=Cancho+urbano+3x3"
                alt="Cancha de baloncesto callejero con aros metálicos y paredes de ladrillo"
                className="rounded-xl shadow-lg w-full"
                width="600"
                height="400"
              />
            </div>
            <div>
              <h3 className="text-2xl font-bold mb-4">StreetBall Andaluz</h3>
              <p className="text-lg text-gray-700 leading-relaxed">
                Nacimos en 2024 como una iniciativa para impulsar el baloncesto callejero en Andalucía. Creamos eventos y torneos donde la pasión, la comunidad y el deporte urbano se unen en una experiencia auténtica.
              </p>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Misión y Visión */}
      <section className="py-20 px-4 sm:px-6 lg:px-8">
        <div className="max-w-6xl mx-auto">
          <div className="grid md:grid-cols-2 gap-12">
            <motion.div
              variants={fadeInUp}
              initial="initial"
              whileInView="animate"
              viewport={{ once: true }}
              className="bg-gradient-to-br from-orange-50 to-white p-8 rounded-2xl shadow-md border border-orange-100"
            >
              <h3 className="text-2xl font-bold text-orange-600 mb-4">misión</h3>
              <p className="text-gray-800 text-lg">
                Promover el streetball como deporte y cultura urbana, fomentando valores de respeto, inclusión y superación personal.
              </p>
            </motion.div>
            <motion.div
              variants={fadeInUp}
              initial="initial"
              whileInView="animate"
              viewport={{ once: true }}
              className="bg-gradient-to-br from-gray-50 to-white p-8 rounded-2xl shadow-md border border-gray-200"
            >
              <h3 className="text-2xl font-bold text-gray-900 mb-4">visión</h3>
              <p className="text-gray-800 text-lg">
                Convertirnos en la referencia autonómica en eventos 3×3, con torneos de calidad, impacto social y proyección nacional.
              </p>
            </motion.div>
          </div>
        </div>
      </section>

      {/* Más que un torneo */}
      <section className="py-20 px-4 sm:px-6 lg:px-8 bg-gray-900 text-white">
        <div className="max-w-4xl mx-auto text-center">
          <motion.h2
            className="text-3xl md:text-4xl font-bold mb-6"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            StreetBall Andaluz es más que un torneo
          </motion.h2>
          <motion.p
            className="text-xl opacity-90 mb-10 max-w-3xl mx-auto"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            Traemos de vuelta la esencia del 3x3: espontaneidad, creatividad, rivalidad sana y hermandad en la cancha.
          </motion.p>
          <motion.img
            src="https://placehold.co/700x250/000000/FF6B00?text=Autenticidad+en+cada+duelo"
            alt="Jugadores celebrando después de un partido intenso en la calle"
            className="rounded-xl w-full max-w-3xl mx-auto shadow-2xl"
            width="700"
            height="250"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          />
        </div>
      </section>

      {/* Comunidad */}
      <section className="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div className="max-w-4xl mx-auto text-center">
          <motion.h2
            className="text-3xl md:text-4xl font-bold text-gray-900 mb-6"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            Nuestra Comunidad
          </motion.h2>
          <motion.p
            className="text-lg text-gray-700 max-w-3xl mx-auto leading-relaxed"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            Somos amantes del baloncesto que queremos revivir esos tiempos en los que competir y disfrutar del juego nos motivaba a seguir adelante y dar lo mejor de nosotros en la cancha. Aquí no hay estrellas: todos somos parte del mismo equipo.
          </motion.p>
        </div>
      </section>

      {/* Inversión */}
      <section className="py-20 px-4 sm:px-6 lg:px-8">
        <div className="max-w-4xl mx-auto">
          <motion.div
            className="text-center mb-12"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Inversión responsable</h2>
            <p className="text-lg text-gray-700">
              Financiado 100% con capital propio. Transparencia y compromiso.
            </p>
          </motion.div>

          <motion.div
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
            className="bg-white p-6 rounded-xl shadow-md"
          >
            <div className="text-center mb-4">
              <span className="text-2xl font-bold text-orange-600">120 €</span>
              <p className="text-gray-600">Total invertido</p>
            </div>

            <div className="space-y-4 max-w-md mx-auto">
              {[
                { label: 'Material deportivo', value: 60, color: 'bg-orange-500' },
                { label: 'Organización logística', value: 40, color: 'bg-orange-400' },
                { label: 'Publicidad', value: 20, color: 'bg-orange-300' },
                { label: 'Alquiler de instalaciones', value: 0, color: 'bg-gray-300' }
              ].map((item, i) => (
                <div key={i}>
                  <div className="flex justify-between text-sm mb-1">
                    <span className="font-medium">{item.label}</span>
                    <span>{item.value} €</span>
                  </div>
                  <div className="h-3 bg-gray-200 rounded-full overflow-hidden">
                    <motion.div
                      className={`h-full ${item.color}`}
                      initial={{ width: 0 }}
                      whileInView={{ width: `${(item.value / 60) * 100}%` }}
                      viewport={{ once: true }}
                      transition={{ duration: 0.8, delay: i * 0.2 }}
                    />
                  </div>
                </div>
              ))}
            </div>

            <motion.p
              className="mt-6 text-center text-gray-700 italic"
              variants={fadeInUp}
              initial="initial"
              whileInView="animate"
              viewport={{ once: true }}
            >
              Este modelo de inversión reducida nos permite ofrecer eventos de calidad de forma sostenible.
            </motion.p>
          </motion.div>
        </div>
      </section>

      {/* Equipo */}
      <section className="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div className="max-w-5xl mx-auto">
          <motion.div
            className="text-center mb-16"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Equipo de Gestión</h2>
            <p className="text-lg text-gray-700 max-w-3xl mx-auto">
              Personas comprometidas, apasionadas y con experiencia en eventos deportivos.
            </p>
          </motion.div>

          <div className="grid md:grid-cols-2 gap-10">
            {[
              {
                name: 'Víctor Manuel Espejo Luna',
                role: 'Organizador de torneos',
                duties: ['Comunicación y redes sociales', 'Logística y montaje en las pistas'],
                img: 'https://placehold.co/300x300/111111/FFFFFF?text=V%C3%ADctor'
              },
              {
                name: 'Jean Carlo Espejo Prieto',
                role: 'Co-organizador',
                duties: ['Gestión de inscripciones', 'Supervisión de torneos', 'Logística y montaje'],
                img: 'https://placehold.co/300x300/222222/FFFFFF?text=Jean+Carlo'
              }
            ].map((person, i) => (
              <motion.div
                key={i}
                variants={fadeInUp}
                initial="initial"
                whileInView="animate"
                viewport={{ once: true }}
                className="bg-white p-6 rounded-2xl shadow-md hover:shadow-lg transition-shadow duration-300"
              >
                <div className="flex flex-col md:flex-row gap-6 items-center">
                  <img
                    src={person.img}
                    alt={`Foto de ${person.name}, miembro del equipo de StreetBall Andaluz`}
                    className="w-32 h-32 rounded-full object-cover"
                    width="128"
                    height="128"
                  />
                  <div className="text-center md:text-left">
                    <h3 className="text-2xl font-bold text-gray-900 mb-1">{person.name}</h3>
                    <p className="text-orange-600 font-semibold mb-3">{person.role}</p>
                    <ul className="text-gray-700 space-y-1">
                      {person.duties.map((duty, j) => (
                        <li key={j} className="flex items-center">
                          <span className="w-1.5 h-1.5 bg-orange-500 rounded-full mr-2 inline-block"></span>
                          {duty}
                        </li>
                      ))}
                    </ul>
                  </div>
                </div>
              </motion.div>
            ))}
          </div>

          <motion.div
            className="mt-16 text-center"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            <p className="text-lg text-gray-700 mb-4">
              Apoyados por colaboradores locales y pequeñas empresas comprometidas con el deporte base.
            </p>
            <img
              src="https://placehold.co/800x100/EEE/333?text=Colaboradores:+tiendas+deportivas,+colegios,+ayuntamientos"
              alt="Logo de colaboradores locales que apoyan StreetBall Andaluz"
              className="mx-auto rounded-lg"
              width="800"
              height="100"
            />
          </motion.div>
        </div>
      </section>

      {/* Contacto */}
      <section id="contacto" className="py-20 px-4 sm:px-6 lg:px-8 bg-gray-900 text-white">
        <div className="max-w-4xl mx-auto text-center">
          <motion.h2
            className="text-3xl md:text-4xl font-bold mb-6"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            ¿Quieres formar parte?
          </motion.h2>
          <motion.p
            className="text-xl opacity-90 mb-10"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            Escríbenos, síguenos o ven a jugar. La cancha te espera.
          </motion.p>

          <motion.div
            className="grid md:grid-cols-3 gap-6 mb-12"
            variants={staggerContainer}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            <div className="p-6 bg-gray-800 rounded-xl">
              <Mail className="w-8 h-8 text-orange-400 mx-auto mb-4" />
              <p className="font-mono text-lg">streetballandaluz@gmail.com</p>
            </div>
            <div className="p-6 bg-gray-800 rounded-xl">
              <Instagram className="w-8 h-8 text-orange-400 mx-auto mb-4" />
              <p className="font-bold text-lg">@streetball_andaluz_</p>
            </div>
            <div className="p-6 bg-gray-800 rounded-xl">
              <div className="w-8 h-8 text-orange-400 mx-auto mb-4 flex items-center justify-center">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" className="w-6 h-6">
                  <path fillRule="evenodd" d="M12 2.25c-5.385 0-9.75 4.365-9.75 9.75s4.365 9.75 9.75 9.75 9.75-4.365 9.75-9.75S17.385 2.25 12 2.25zm-2.625 6c-.54 0-.828.419-.936.634a1.96 1.96 0 00-.189.866c0 .298.059.605.189.866.108.215.395.634.936.634.54 0 .828-.419.936-.634.13-.26.189-.568.189-.866 0-.298-.059-.605-.189-.866-.108-.215-.395-.634-.936-.634zm4.314.634c.108-.215.395-.634.936-.634.54 0 .828.419.936.634.13.26.189.568.189.866 0 .298-.059.605-.189.866-.108.215-.395.634-.936.634-.54 0-.828-.419-.936-.634a1.96 1.96 0 01-.189-.866c0-.298.059-.605.189-.866zm-4.34 7.964a.75.75 0 01-1.061-1.06 5.236 5.236 0 013.73-1.538 5.236 5.236 0 013.695 1.538.75.75 0 11-1.061 1.06 3.736 3.736 0 00-2.639-1.098 3.736 3.736 0 00-2.664 1.098z" clipRule="evenodd" />
                </svg>
              </div>
              <p className="font-bold text-lg">@streetball_andaluz_</p>
              <p className="text-xs mt-1 text-gray-300">(TikTok)</p>
            </div>
          </motion.div>

          <motion.div
            className="flex flex-col items-center"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          >
            <MapPin className="w-6 h-6 text-orange-400 mb-2" />
            <p className="text-lg">Sevilla, Andalucía, España</p>
          </motion.div>

          <motion.img
            src="https://placehold.co/700x200/000000/FF6B00?text=As%C3%AD+se+vive+el+basket+en+la+calle"
            alt="Momento épico de un partido de streetball: mate en la cancha urbana"
            className="mt-12 rounded-xl w-full max-w-3xl mx-auto shadow-2xl"
            width="700"
            height="200"
            variants={fadeInUp}
            initial="initial"
            whileInView="animate"
            viewport={{ once: true }}
          />
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-800 text-gray-400 py-8 px-4 sm:px-6">
        <div className="max-w-6xl mx-auto text-center">
          <p className="text-sm">
            © {new Date().getFullYear()} StreetBall Andaluz. Todos los derechos reservados.
          </p>
          <p className="text-xs mt-2">
            Diseñado con pasión por la comunidad del streetball.
          </p>
        </div>
      </footer>
    </div>
  );
};

export default App;

