import React from 'react';
import './globals.css';

const projects = [
  {
    name: 'Cleaning Management System',
    description: 'A full-featured system for managing client properties, cleaners, schedules, and service records. Built with C#, .NET Core, Entity Framework, and SQL Server.',
    github: 'https://github.com/yourusername/cleaning-management-system', // Replace with your actual repo URL
  },
];

const skills = {
  languages: ['C#', 'JavaScript', 'TypeScript', 'Python'],
  frameworks: ['.NET Core', 'AngularJS', 'React', 'ASP.NET MVC', 'WPF', 'Knockout.js', 'VB.NET'],
  databases: ['MySQL', 'Oracle', 'SQL Server', 'Firebase'],
  cloud: ['Azure', 'Docker', 'GitHub Actions'],
  tools: ['Git', 'Visual Studio', 'Postman', 'Jupyter', 'NUnit', 'xUnit', 'Selenium', 'JMeter', 'Azure DevOps'],
  methodologies: ['Agile', 'Scrum', 'SDLC', 'Pair Programming', 'Code Reviews'],
};

const ContactLink = ({ href, children }) => (
  <a href={href} target="_blank" rel="noopener noreferrer" style={{color: '#007acc', textDecoration: 'none'}}>
    {children}
  </a>
);

export default function Portfolio() {
  return (
    <div style={{
      fontFamily: "'Segoe UI', Tahoma, Geneva, Verdana, sans-serif",
      maxWidth: 900,
      margin: 'auto',
      padding: 20,
      color: '#222',
      lineHeight: 1.6,
    }}>
      <header style={{marginBottom: 40}}>
        <h1 style={{fontSize: '2.5rem', marginBottom: 5}}>Hi there, I'm <strong>Nuwanga</strong> 👋</h1>
        <p style={{fontSize: '1.2rem', color: '#555'}}>
          FullStack Engineer | C# / .NET Core / SQL / Azure<br />
          Focused on clean architecture, scalable systems, and real-world business solutions.
        </p>
      </header>

      <section style={{marginBottom: 40}}>
        <h2>🚀 About Me</h2>
        <ul>
          <li>🧠 3+ years building production-ready backend systems</li>
          <li>💼 Specializing in C#, .NET Core, Entity Framework, and SQL</li>
          <li>🌍 Strong interest in system design, performance tuning, and backend scalability</li>
          <li>🛠️ Committed to writing clean, testable, and maintainable code</li>
        </ul>
      </section>

      <section style={{marginBottom: 40}}>
        <h2>🔨 Featured Project</h2>
        {projects.map(({name, description, github}) => (
          <div key={name} style={{marginBottom: 20}}>
            <h3>{name}</h3>
            <p>{description}</p>
            <p>
              🔗{' '}
              <ContactLink href={github}>GitHub Repo</ContactLink>
            </p>
          </div>
        ))}
      </section>

      <section style={{marginBottom: 40}}>
        <h2>🧰 Tech Stack</h2>
        <div style={{display: 'grid', gridTemplateColumns: 'repeat(auto-fit, minmax(200px, 1fr))', gap: 20}}>
          <div>
            <h3>💻 Languages</h3>
            <ul>{skills.languages.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
          <div>
            <h3>🧱 Frameworks & Libraries</h3>
            <ul>{skills.frameworks.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
          <div>
            <h3>🗄️ Databases</h3>
            <ul>{skills.databases.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
          <div>
            <h3>☁️ Cloud & DevOps</h3>
            <ul>{skills.cloud.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
          <div>
            <h3>🧪 Testing & Tools</h3>
            <ul>{skills.tools.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
          <div>
            <h3>📋 Methodologies</h3>
            <ul>{skills.methodologies.map(skill => <li key={skill}>{skill}</li>)}</ul>
          </div>
        </div>
      </section>

      <section style={{marginBottom: 40}}>
        <h2>📫 Reach Me</h2>
        <ul>
          <li>📧 Email: <a href="mailto:nuwanga.rodrigo@email.com" style={{color:'#007acc'}}>nuwanga.rodrigo@email.com</a></li>
          <li>💼 LinkedIn: <ContactLink href="https://linkedin.com/in/yourprofile">linkedin.com/in/yourprofile</ContactLink></li>
          <li>🤝 GitHub: <ContactLink href="https://github.com/yourusername">github.com/yourusername</ContactLink></li>
        </ul>
      </section>

      <section>
        <h2>🤝 Let's Connect</h2>
        <p>
          I'm currently open to:<br />
          - Back-end engineering roles (.NET, C#)<br />
          - Backend-heavy SaaS projects<br />
          - Long-term opportunities with product-driven teams<br />
          Let’s talk if you’re hiring or want to collaborate!
        </p>
      </section>
    </div>
  );
}
