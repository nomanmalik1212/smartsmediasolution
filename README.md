import { Canvas } from "@react-three/fiber";
import { Float, OrbitControls, Sphere, MeshDistortMaterial } from "@react-three/drei";

function FloatingOrb() {
  return (
    <Float speed={2} rotationIntensity={2} floatIntensity={3}>
      <Sphere args={[1.5, 100, 200]} scale={2.2}>
        <MeshDistortMaterial
          color="#22d3ee"
          attach="material"
          distort={0.4}
          speed={2}
          roughness={0}
        />
      </Sphere>
    </Float>
  );
}

function ThreeScene() {
  return (
    <Canvas camera={{ position: [0, 0, 5] }}>
      <ambientLight intensity={1.2} />
      <directionalLight position={[2, 2, 5]} intensity={2} />

      <FloatingOrb />

      <OrbitControls
        enableZoom={false}
        autoRotate
        autoRotateSpeed={1.5}
      />
    </Canvas>
  );
}

export default function SmartsMediaSolution() {
  return (
    <div className="bg-[#050816] text-white min-h-screen overflow-x-hidden font-sans">
      {/* Background Glow */}
      <div className="fixed inset-0 -z-10 overflow-hidden">
        <div className="absolute top-[-200px] left-[-100px] w-[500px] h-[500px] bg-cyan-500/20 blur-3xl rounded-full animate-pulse"></div>
        <div className="absolute bottom-[-250px] right-[-150px] w-[600px] h-[600px] bg-blue-600/20 blur-3xl rounded-full animate-pulse"></div>
      </div>

      {/* Navbar */}
      <header className="fixed top-0 left-0 w-full z-50 backdrop-blur-xl bg-black/20 border-b border-white/10">
        <div className="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
          <div className="flex items-center gap-3">
            <img
              src="/SMS Logo New.jpg"
              alt="Smarts Media Solution"
              className="w-12 h-12 object-contain"
            />
            <div>
              <h1 className="text-xl font-bold tracking-wide">Smarts Media Solution</h1>
              <p className="text-cyan-400 text-sm">Visuals That Speak</p>
            </div>
          </div>

          <nav className="hidden md:flex gap-8 text-sm tracking-wide">
            <a href="#home" className="hover:text-cyan-400 transition">Home</a>
            <a href="#about" className="hover:text-cyan-400 transition">About</a>
            <a href="#services" className="hover:text-cyan-400 transition">Services</a>
            <a href="#portfolio" className="hover:text-cyan-400 transition">Portfolio</a>
            <a href="#contact" className="hover:text-cyan-400 transition">Contact</a>
          </nav>
        </div>
      </header>

      {/* Hero */}
      <section
        id="home"
        className="relative h-screen flex items-center justify-center text-center px-6"
      >
        <video
          autoPlay
          muted
          loop
          playsInline
          className="absolute inset-0 w-full h-full object-cover opacity-20"
        >
          <source src="/hero-video.mp4" type="video/mp4" />
        </video>

        <div className="absolute inset-0 bg-gradient-to-b from-black/60 to-[#050816]"></div>

        {/* Real Three.js 3D Scene */}
        <div className="absolute inset-0 opacity-80">
          <ThreeScene />
        </div>

        {/* Floating UI Elements */}
        <div className="absolute top-20 left-10 w-32 h-32 border border-cyan-400/30 rounded-full animate-spin"></div>
        <div className="absolute bottom-20 right-20 w-20 h-20 bg-cyan-400/10 backdrop-blur-xl rounded-2xl rotate-12 animate-bounce"></div>

        <div className="relative z-10 max-w-5xl">
          <p className="uppercase tracking-[8px] text-cyan-400 mb-4 text-sm">
            Premium Production House
          </p>

          <h1 className="text-5xl md:text-7xl font-black leading-tight mb-6">
            We Create
            <span className="text-cyan-400"> Cinematic </span>
            Visual Experiences.
          </h1>

          <p className="text-gray-300 text-lg max-w-2xl mx-auto mb-10 leading-relaxed">
            Smarts Media Solution delivers commercials, corporate visuals,
            documentaries, podcasts, and cinematic content engineered for modern
            brands.
          </p>

          <div className="flex flex-wrap justify-center gap-4">
            <a
              href="#portfolio"
              className="px-8 py-4 rounded-full bg-cyan-400 text-black font-semibold hover:scale-105 transition"
            >
              View Portfolio
            </a>

            <a
              href="#contact"
              className="px-8 py-4 rounded-full border border-cyan-400 text-cyan-400 hover:bg-cyan-400 hover:text-black transition"
            >
              Contact Us
            </a>
          </div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="max-w-7xl mx-auto px-6 py-28">
        <div className="grid md:grid-cols-2 gap-16 items-center">
          <div>
            <p className="text-cyan-400 uppercase tracking-[5px] mb-4 text-sm">
              About Us
            </p>

            <h2 className="text-4xl md:text-5xl font-bold mb-6 leading-tight">
              Storytelling Through Motion & Vision
            </h2>

            <p className="text-gray-300 leading-relaxed text-lg mb-6">
              Smarts Media Solution is a premium creative production house focused
              on delivering cinematic visuals, modern storytelling, and immersive
              digital experiences for brands, creators, and businesses.
            </p>

            <p className="text-gray-400 leading-relaxed">
              From commercials and documentaries to podcasts and corporate
              productions, we blend creativity, technology, and motion design to
              craft visuals that leave impact.
            </p>
          </div>

          <div className="relative">
            <div className="absolute inset-0 bg-cyan-500/20 blur-3xl rounded-full"></div>

            <div className="relative bg-white/5 border border-white/10 backdrop-blur-2xl rounded-3xl p-10 shadow-2xl">
              <div className="grid grid-cols-2 gap-6 text-center">
                <div>
                  <h3 className="text-5xl font-black text-cyan-400">50+</h3>
                  <p className="text-gray-400 mt-2">Projects</p>
                </div>

                <div>
                  <h3 className="text-5xl font-black text-cyan-400">24/7</h3>
                  <p className="text-gray-400 mt-2">Creative Support</p>
                </div>

                <div>
                  <h3 className="text-5xl font-black text-cyan-400">4K</h3>
                  <p className="text-gray-400 mt-2">Production Quality</p>
                </div>

                <div>
                  <h3 className="text-5xl font-black text-cyan-400">100%</h3>
                  <p className="text-gray-400 mt-2">Cinematic Focus</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Services */}
      <section id="services" className="py-28 px-6 bg-white/[0.02]">
        <div className="max-w-7xl mx-auto text-center">
          <p className="text-cyan-400 uppercase tracking-[5px] mb-4 text-sm">
            Services
          </p>

          <h2 className="text-4xl md:text-5xl font-bold mb-16">
            Production Services
          </h2>

          <div className="grid md:grid-cols-3 gap-8">
            {[
              "Video Production",
              "Commercial Ads",
              "Corporate Shoots",
              "Podcast Production",
              "Motion Graphics",
              "Social Media Content",
            ].map((service, index) => (
              <div
                key={index}
                className="group bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl hover:border-cyan-400/50 transition duration-500 hover:-translate-y-2"
              >
                <div className="w-16 h-16 rounded-2xl bg-cyan-400/10 flex items-center justify-center mb-6 mx-auto group-hover:scale-110 transition">
                  <div className="w-8 h-8 rounded-full bg-cyan-400"></div>
                </div>

                <h3 className="text-2xl font-semibold mb-4">{service}</h3>

                <p className="text-gray-400 leading-relaxed">
                  Premium cinematic production tailored for modern brands and
                  visual storytelling.
                </p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Portfolio */}
      <section id="portfolio" className="max-w-7xl mx-auto px-6 py-28">
        <div className="text-center mb-16">
          <p className="text-cyan-400 uppercase tracking-[5px] mb-4 text-sm">
            Portfolio
          </p>

          <h2 className="text-4xl md:text-5xl font-bold">
            Featured Work
          </h2>
        </div>

        <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          {[
            "Commercials",
            "Corporate",
            "Documentaries",
            "Podcast",
          ].map((category, index) => (
            <div
              key={index}
              className="relative group overflow-hidden rounded-3xl border border-white/10 bg-white/5 h-[350px]"
            >
              <div className="absolute inset-0 bg-gradient-to-b from-transparent to-black"></div>

              <div className="absolute inset-0 flex items-center justify-center">
                <div className="w-24 h-24 rounded-full border border-cyan-400/30 flex items-center justify-center">
                  <div className="w-10 h-10 rounded-full bg-cyan-400"></div>
                </div>
              </div>

              <div className="absolute bottom-0 left-0 p-6 w-full">
                <h3 className="text-2xl font-bold mb-2">{category}</h3>
                <p className="text-gray-400 text-sm">
                  Upload your future projects here.
                </p>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="py-28 px-6 bg-white/[0.02]">
        <div className="max-w-5xl mx-auto text-center">
          <p className="text-cyan-400 uppercase tracking-[5px] mb-4 text-sm">
            Contact
          </p>

          <h2 className="text-4xl md:text-5xl font-bold mb-6">
            Let’s Build Something Cinematic
          </h2>

          <p className="text-gray-400 max-w-2xl mx-auto mb-14 leading-relaxed">
            Contact Smarts Media Solution for premium production, cinematic
            storytelling, motion graphics, and digital visual experiences.
          </p>

          <div className="grid md:grid-cols-2 gap-10 text-left">
            <div className="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl">
              <h3 className="text-2xl font-semibold mb-6">Contact Details</h3>

              <div className="space-y-5 text-gray-300">
                <p>
                  <span className="text-cyan-400 font-semibold">WhatsApp:</span>
                  <br />
                  0300 3925006
                </p>

                <p>
                  <span className="text-cyan-400 font-semibold">Email:</span>
                  <br />
                  smartsmediasolution@gmail.com
                </p>
              </div>

              <a
                href="https://wa.me/923003925006"
                className="inline-block mt-8 px-8 py-4 rounded-full bg-cyan-400 text-black font-semibold hover:scale-105 transition"
              >
                Chat on WhatsApp
              </a>
            </div>

            <form className="bg-white/5 border border-white/10 rounded-3xl p-8 backdrop-blur-xl space-y-6">
              <input
                type="text"
                placeholder="Your Name"
                className="w-full bg-black/30 border border-white/10 rounded-xl px-5 py-4 outline-none focus:border-cyan-400"
              />

              <input
                type="email"
                placeholder="Your Email"
                className="w-full bg-black/30 border border-white/10 rounded-xl px-5 py-4 outline-none focus:border-cyan-400"
              />

              <textarea
                rows="5"
                placeholder="Tell us about your project"
                className="w-full bg-black/30 border border-white/10 rounded-xl px-5 py-4 outline-none focus:border-cyan-400"
              ></textarea>

              <button
                type="submit"
                className="w-full py-4 rounded-xl bg-cyan-400 text-black font-bold hover:scale-[1.02] transition"
              >
                Send Message
              </button>
            </form>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-white/10 py-8 px-6 text-center text-gray-500 text-sm">
        © 2026 Smarts Media Solution — Visuals That Speak.
      </footer>
    </div>
  );
}
