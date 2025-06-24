# steelmet-website
steelmet-website
import React, { useState } from "react";

export default function App() {
  const [lang, setLang] = useState("en");
  const [selected, setSelected] = useState(null);

  const content = {
    en: {
      title: "Steelmet International",
      subtitle: "Global Steel Trading & Risk Management",
      heroTitle: "Connecting the Global Steel Market",
      heroText:
        "Steelmet International connects global producers and consumers, providing physical steel trading and financial hedging solutions.",
      aboutTitle: "About Us",
      aboutText:
        "Based in London, Steelmet International is a subsidiary of Levmet (Monaco). We specialize in the trading of flat and long steel products such as coils, billets, rebar, wire rod, and scrap metal. We also assist clients in managing price volatility through steel derivatives and risk strategies.",
      productsTitle: "Our Products",
      servicesTitle: "Our Services",
      services: [
        {
          title: "Physical trading of steel and scrap",
          desc:
            "Buying and selling actual steel and scrap products worldwide, managing logistics, storage and delivery."
        },
        {
          title: "Risk management through derivatives",
          desc:
            "Using financial instruments like futures and options to hedge against steel price volatility and protect margins."
        },
        {
          title: "Global logistics and shipping coordination",
          desc:
            "Coordinating and managing the international transportation of steel goods across sea, road and rail safely and efficiently."
        },
        {
          title: "Tailored financial solutions",
          desc:
            "Structured trade finance and financial planning to optimize working capital and secure funding for steel transactions."
        },
        {
          title: "Market research and price forecasts",
          desc:
            "Analyzing global steel supply-demand trends, market data and price forecasts to inform smarter trading decisions."
        }
      ],
      teamTitle: "Our Team",
      contactTitle: "Contact Us",
      location: "Location",
      phone: "Phone",
      email: "Email",
      inquiry: "Send Inquiry",
      close: "Close",
      footer: "All rights reserved.",
      products: [
        { key: "Hot-Rolled Coil", title: "Hot-Rolled Coil" },
        { key: "Cold-Rolled Coil", title: "Cold-Rolled Coil" },
        { key: "Galvanized Steel", title: "Galvanized Steel" },
        { key: "Billet", title: "Billet" },
        { key: "Rebar", title: "Rebar" },
        { key: "Wire Rod", title: "Wire Rod" },
        { key: "Scrap Metal", title: "Scrap Metal" }
      ]
    },
    es: {
      title: "Steelmet Internacional",
      subtitle: "Trading Global de Acero y Gestión de Riesgos",
      heroTitle: "Conectando el Mercado Global del Acero",
      heroText:
        "Steelmet conecta productores y consumidores de todo el mundo, ofreciendo trading físico y soluciones de cobertura financiera.",
      aboutTitle: "Quiénes Somos",
      aboutText:
        "Con sede en Londres, Steelmet es una subsidiaria de Levmet (Mónaco). Estamos especializados en el comercio de productos siderúrgicos planos y largos como bobinas, billets, rebar, alambres y chatarra. También ayudamos a gestionar la volatilidad de precios con derivados del acero y estrategias de cobertura.",
      productsTitle: "Nuestros Productos",
      servicesTitle: "Nuestros Servicios",
      services: [
        {
          title: "Trading físico de acero y chatarra",
          desc:
            "Compra y venta de acero y chatarra reales a nivel mundial, gestionando logística, almacenamiento y entrega."
        },
        {
          title: "Gestión de riesgos con derivados",
          desc:
            "Uso de instrumentos financieros como futuros y opciones para cubrir la volatilidad de precios del acero y proteger los márgenes."
        },
        {
          title: "Coordinación logística y transporte global",
          desc:
            "Coordinación y gestión del transporte internacional de acero por mar, carretera y ferrocarril de forma segura y eficiente."
        },
        {
          title: "Soluciones financieras personalizadas",
          desc:
            "Financiación estructurada y planificación financiera para optimizar capital de trabajo y asegurar fondos en transacciones de acero."
        },
        {
          title: "Investigación de mercado y previsión de precios",
          desc:
            "Análisis de tendencias globales de oferta-demanda, datos del mercado y previsiones de precios para informar decisiones de trading."
        }
      ],
      teamTitle: "Nuestro Equipo",
      contactTitle: "Contacto",
      location: "Ubicación",
      phone: "Teléfono",
      email: "Correo electrónico",
      inquiry: "Enviar Consulta",
      close: "Cerrar",
      footer: "Todos los derechos reservados.",
      products: [
        { key: "Hot-Rolled Coil", title: "Bobina Laminada en Caliente" },
        { key: "Cold-Rolled Coil", title: "Bobina Laminada en Frío" },
        { key: "Galvanized Steel", title: "Acero Galvanizado" },
        { key: "Billet", title: "Billet" },
        { key: "Rebar", title: "Barras de Refuerzo" },
        { key: "Wire Rod", title: "Alambre Laminado" },
        { key: "Scrap Metal", title: "Chatarra" }
      ]
    }
  };

  const descriptions = {
    "Hot-Rolled Coil": {
      en: "Hot-rolled coils are produced by rolling steel at high temperatures. They are cost-effective, strong, and used in construction and manufacturing.",
      es: "Las bobinas laminadas en caliente se producen a altas temperaturas. Son económicas, resistentes y usadas en construcción e industria."
    },
    "Cold-Rolled Coil": {
      en: "Cold-rolled coils are processed at room temperature. They offer a smooth finish and are used in appliances, automotive, and precision components.",
      es: "Las bobinas laminadas en frío se procesan a temperatura ambiente. Tienen acabado liso y se usan en electrodomésticos, automoción y piezas de precisión."
    },
    "Galvanized Steel": {
      en: "Galvanized steel is coated with zinc for corrosion protection. It's widely used in outdoor construction and automotive parts.",
      es: "El acero galvanizado tiene un recubrimiento de zinc para proteger contra la corrosión. Se usa ampliamente en construcción y automoción."
    },
    "Billet": {
      en: "Billet is a semi-finished steel product used as raw material for rolling mills and forging operations.",
      es: "El billet es un producto de acero semielaborado usado como materia prima para laminado o forjado."
    },
    "Rebar": {
      en: "Rebar (reinforcing bar) is a steel rod used to strengthen concrete structures in construction.",
      es: "La barra de refuerzo (rebar) es una varilla de acero usada para fortalecer estructuras de hormigón."
    },
    "Wire Rod": {
      en: "Wire rod is rolled steel in coil form, used to produce wire, nails, and steel mesh.",
      es: "El alambre laminado es acero enrollado, usado para producir alambre, clavos y mallas de acero."
    },
    "Scrap Metal": {
      en: "Scrap metal is recycled steel used as raw material in steelmaking, helping reduce costs and environmental impact.",
      es: "La chatarra es acero reciclado que se usa como materia prima en la siderurgia, reduciendo costes e impacto ambiental."
    }
  };

  const t = content[lang];

  const team = [
    { name: "Giulio Thuburn", role: lang === "en" ? "Commercial Director" : "Director Comercial" },
    { name: "Anna Petrova", role: lang === "en" ? "Operations Manager" : "Responsable de Operaciones" },
    { name: "James Liu", role: lang === "en" ? "Risk Analyst" : "Analista de Riesgos" },
    { name: "Lina González", role: lang === "en" ? "Trade Coordinator" : "Coordinadora de Comercio" }
  ];

  const cardStyle = {
    border: "1px solid #ccc",
    borderRadius: "8px",
    padding: "1rem",
    backgroundColor: "#f9f9f9",
    boxShadow: "0 2px 5px rgba(0,0,0,0.05)",
    textAlign: "center",
    cursor: "pointer"
  };

  const navLink = {
    color: "#e2e8f0",
    marginRight: "1rem",
    textDecoration: "none",
    fontSize: "0.95rem"
  };

  const sectionTitle = {
    fontSize: "1.6rem",
    marginBottom: "1.2rem"
  };

  const sectionStyle = {
    padding: "3rem 2rem",
    maxWidth: "1000px",
    margin: "0 auto"
  };

  const gridStyle = {
    display: "grid",
    gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))",
    gap: "1rem"
  };

  const buttonStyle = {
    marginTop: "1rem",
    padding: "0.6rem 1.2rem",
    backgroundColor: "#2563eb",
    color: "white",
    border: "none",
    borderRadius: "4px",
    cursor: "pointer",
    fontSize: "1rem"
  };

  return (
    <div style={{ fontFamily: "Segoe UI, sans-serif" }}>
      {/* Header */}
      <header
        style={{
          background: "#1e293b",
          color: "#fff",
          padding: "1rem 2rem",
          position: "sticky",
          top: 0,
          zIndex: 1000
        }}
      >
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
          <div>
            <h1 style={{ margin: 0, fontSize: "1.8rem" }}>{t.title}</h1>
            <p style={{ margin: 0 }}>{t.subtitle}</p>
          </div>
          <select value={lang} onChange={(e) => setLang(e.target.value)} style={{ padding: "0.3rem", borderRadius: "4px" }}>
            <option value="en">English</option>
            <option value="es">Español</option>
          </select>
        </div>
        <nav style={{ marginTop: "0.5rem" }}>
          <a href="#about" style={navLink}>
            {t.aboutTitle}
          </a>
          <a href="#products" style={navLink}>
            {t.productsTitle}
          </a>
          <a href="#services" style={navLink}>
            {t.servicesTitle}
          </a>
          <a href="#team" style={navLink}>
            {t.teamTitle}
          </a>
          <a href="#contact" style={navLink}>
            {t.contactTitle}
          </a>
        </nav>
      </header>

      {/* Hero */}
      <section style={{ padding: "4rem 2rem", background: "#f3f4f6", textAlign: "center" }}>
        <h2 style={{ fontSize: "2rem", marginBottom: "1rem" }}>{t.heroTitle}</h2>
        <p style={{ fontSize: "1.1rem", maxWidth: "600px", margin: "0 auto" }}>{t.heroText}</p>
      </section>

      {/* About */}
      <section id="about" style={sectionStyle}>
        <h3 style={sectionTitle}>{t.aboutTitle}</h3>
        <p>{t.aboutText}</p>
      </section>

      {/* Products */}
      <section id="products" style={{ ...sectionStyle, background: "#f9fafb" }}>
        <h3 style={sectionTitle}>{t.productsTitle}</h3>
        <div style={gridStyle}>
          {t.products.map((product) => (
            <div key={product.key} style={cardStyle} onClick={() => setSelected(product.key)}>
              <h4>{product.title}</h4>
            </div>
          ))}
        </div>
      </section>

      {/* Modal for product description */}
      {selected && (
        <div
          style={{
            position: "fixed",
            top: 0,
            left: 0,
            width: "100%",
            height: "100%",
            backgroundColor: "rgba(0,0,0,0.5)",
            display: "flex",
            justifyContent: "center",
            alignItems: "center"
          }}
          onClick={() => setSelected(null)}
        >
          <div
            style={{ background: "#fff", padding: "2rem", borderRadius: "8px", maxWidth: "500px" }}
            onClick={(e) => e.stopPropagation()}
          >
            <h4>{t.products.find((p) => p.key === selected).title}</h4>
            <p>{descriptions[selected][lang]}</p>
            <button style={buttonStyle} onClick={() => setSelected(null)}>
              {t.close}
            </button>
          </div>
        </div>
      )}

      {/* Services */}
      <section id="services" style={sectionStyle}>
        <h3 style={sectionTitle}>{t.servicesTitle}</h3>
        <div style={gridStyle}>
          {t.services.map(({ title, desc }) => (
            <div
              key={title}
              style={{
                background: "#fff",
                padding: "1rem",
                borderRadius: "8px",
                boxShadow: "0 3px 10px rgba(0,0,0,0.1)",
                borderLeft: "4px solid #2563eb"
              }}
            >
              <h4 style={{ color: "#2563eb", marginBottom: "0.5rem" }}>{title}</h4>
              <p style={{ fontSize: "0.95rem", color: "#444", lineHeight: "1.4" }}>{desc}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Team */}
      <section id="team" style={{ ...sectionStyle, background: "#f9fafb" }}>
        <h3 style={sectionTitle}>{t.teamTitle}</h3>
        <div style={gridStyle}>
          {team.map((member) => (
            <div key={member.name} style={cardStyle}>
              <h4>{member.name}</h4>
              <p style={{ fontSize: "0.9rem", color: "#555" }}>{member.role}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section id="contact" style={sectionStyle}>
        <h3 style={sectionTitle}>{t.contactTitle}</h3>
        <p>
          <strong>{t.location}:</strong> London, UK
        </p>
        <p>
          <strong>{t.phone}:</strong> +44 20 1234 5678
        </p>
        <p>
          <strong>{t.email}:</strong> info@steelmet.com
        </p>
        <button style={buttonStyle}>{t.inquiry}</button>
      </section>

      {/* Footer */}
      <footer style={{ background: "#1e293b", color: "#fff", textAlign: "center", padding: "1rem", fontSize: "0.8rem" }}>
        © {new Date().getFullYear()} Steelmet International. {t.footer}
      </footer>
    </div>
  );
}
