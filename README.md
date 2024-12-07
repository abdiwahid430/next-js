import Head from 'next/head';
import styles from '../styles/Home.module.css';
import Image from 'next/image';
import profilePic from '../public/profile.jpg';
import Navbar from '../components/Navbar';

function HomePage() {
  return (
    <div className={styles.container}>
      <Head>
        <title>My Portfolio</title>
        <meta name="description" content="My Portfolio Website" />
      </Head>

      <Navbar />
      
      <div className={styles.hero}>
        <h1>Welcome to My Portfolio</h1>
        <Image src={profilePic} alt="Profile Picture" width={150} height={150} />
      </div>

      <p>I'm a web developer passionate about building amazing projects.</p>
    </div>
  );
}

export default HomePage;

import Navbar from '../components/Navbar';

function AboutPage() {
  return (
    <div>
      <Navbar />
      <h1>About Me</h1>
      <p>I am a web developer with a strong passion for creating responsive and dynamic websites.</p>
    </div>
  );
}

export default AboutPage;

import Navbar from '../components/Navbar';

function ProjectsPage() {
  return (
    <div>
      <Navbar />
      <h1>My Projects</h1>
      <div>
        <h2>Project 1: Portfolio Website</h2>
        <p>This is the website you are currently viewing, built with Next.js.</p>
      </div>
      <div>
        <h2>Project 2: E-commerce App</h2>
        <p>Built with React and integrated with Stripe for payment processing.</p>
      </div>
    </div>
  );
}

export default ProjectsPage;

import Navbar from '../components/Navbar';

function ContactPage() {
  return (
    <div>
      <Navbar />
      <h1>Contact Me</h1>
      <p>Email: myemail@example.com</p>
      <p>Phone: (123) 456-7890</p>
    </div>
  );
}

export default ContactPage;

import Link from 'next/link';

function Navbar() {
  return (
    <nav style={{ backgroundColor: '#333', padding: '10px' }}>
      <ul style={{ listStyleType: 'none', display: 'flex', gap: '20px' }}>
        <li>
          <Link href="/">Home</Link>
        </li>
        <li>
          <Link href="/about">About</Link>
        </li>
        <li>
          <Link href="/projects">Projects</Link>
        </li>
        <li>
          <Link href="/contact">Contact</Link>
        </li>
      </ul>
    </nav>
  );
}

export default Navbar;

.container {
    text-align: center;
    padding: 20px;
  }
  
  .hero {
    margin-top: 50px;
    margin-bottom: 30px;
  }
  
  h1 {
    color: #333;
  }
  
  p {
    font-size: 1.2em;
  }
