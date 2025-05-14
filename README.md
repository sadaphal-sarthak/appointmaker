Index.html 
import React from "react"; import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button";﻿

function Home() { return ( <Card className="m-6"> <CardContent className="p-6"> <h2 className="text-xl font-semibold mb-2">Welcome to Bliss</h2> <p>We offer relaxing treatments for hair, skin, and nails in a calm, luxurious setting.</p> </CardContent> </Card> ); }﻿

function About() { return ( <Card className="m-6"> <CardContent className="p-6"> <h2 className="text-xl font-semibold mb-2">Our Story</h2> <p>Founded in 2015, Bliss Salon & Spa is dedicated to making you feel beautiful inside and out.</p> </CardContent> </Card> ); }﻿

function Services() { return ( <Card className="m-6"> <CardContent className="p-6 space-y-4"> <div> <h3 className="font-medium">Hair Styling</h3> <p>Modern cuts, color, and treatments</p> </div> <div> <h3 className="font-medium">Facials & Skincare</h3> <p>Glow with our rejuvenating facials</p> </div> <div> <h3 className="font-medium">Manicure & Pedicure</h3> <p>Clean, polish, and shine</p> </div> </CardContent> </Card> ); }﻿

function Gallery() { return ( <Card className="m-6"> <CardContent className="p-6 grid grid-cols-2 gap-4"> <div className="bg-gray-100 aspect-square rounded-xl"></div> <div className="bg-gray-100 aspect-square rounded-xl"></div> <div className="bg-gray-100 aspect-square rounded-xl"></div> <div className="bg-gray-100 aspect-square rounded-xl"></div> </CardContent> </Card> ); }﻿

function Contact() { return ( <Card className="m-6"> <CardContent className="p-6 space-y-4"> <p><strong>Address:</strong> 123 Beauty Lane, Wellness City</p> <p><strong>Phone:</strong> (123) 456-7890</p> <p><strong>Email:</strong> contact@blisssalon.com</p> <Button className="mt-4">Book Appointment</Button> </CardContent> </Card> ); }﻿

export default function App() { return ( <Router> <div className="min-h-screen bg-white text-gray-800"> <header className="p-6 bg-[#f8f9fa] shadow-md flex justify-between items-center"> <div> <h1 className="text-3xl font-bold">Bliss Salon & Spa</h1> <p className="text-sm text-gray-600">Pamper yourself with our premium services</p> </div> <nav className="space-x-4"> <Link to="/" className="hover:underline">Home</Link> <Link to="/about" className="hover:underline">About</Link> <Link to="/services" className="hover:underline">Services</Link> <Link to="/gallery" className="hover:underline">Gallery</Link> <Link to="/contact" className="hover:underline">Contact</Link> </nav> </header>﻿

<main>﻿
      <Routes>﻿
        <Route path="/" element={<Home />} />﻿
        <Route path="/about" element={<About />} />﻿
        <Route path="/services" element={<Services />} />﻿
        <Route path="/gallery" element={<Gallery />} />﻿
        <Route path="/contact" element={<Contact />} />﻿
      </Routes>﻿
    </main>﻿

    <footer className="text-center p-4 text-sm text-gray-500">﻿
      © 2025 Bliss Salon & Spa. All rights reserved.﻿
    </footer>﻿
  </div>﻿
</Router>﻿

); }
