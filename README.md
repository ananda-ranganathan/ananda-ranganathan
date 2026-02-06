  ## Hi there 👋
  
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github, Linkedin, Mail, Sparkles } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-950 via-slate-900 to-black text-slate-100 px-6 py-12">
      {/* HERO SECTION */}
      <motion.section
        initial={{ opacity: 0, y: 40 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
        className="max-w-5xl mx-auto text-center"
      >
        <motion.h1
          initial={{ scale: 0.9 }}
          animate={{ scale: 1 }}
          transition={{ duration: 0.6 }}
          className="text-4xl md:text-6xl font-bold tracking-tight"
        >
          Ananda Ranganathan Harikrishnan
        </motion.h1>

        <motion.p
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.4 }}
          className="mt-4 text-lg md:text-xl text-slate-300"
        >
          Data Analyst • Data Scientist • Machine Learning • GenAI
        </motion.p>

        <div className="mt-6 flex justify-center gap-4">
          <Button variant="secondary" className="rounded-2xl gap-2">
            <Github size={18} /> GitHub
          </Button>
          <Button variant="secondary" className="rounded-2xl gap-2">
            <Linkedin size={18} /> LinkedIn
          </Button>
          <Button variant="secondary" className="rounded-2xl gap-2">
            <Mail size={18} /> Email
          </Button>
        </div>
      </motion.section>

      {/* ABOUT */}
      <motion.section
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 0.8 }}
        viewport={{ once: true }}
        className="max-w-4xl mx-auto mt-20"
      >
        <Card className="bg-slate-900/70 backdrop-blur border-slate-800 rounded-2xl shadow-xl">
          <CardContent className="p-6 text-center">
            <h2 className="text-2xl font-semibold mb-3">About Me</h2>
            <p className="text-slate-300 leading-relaxed">
              I transform raw data into meaningful insights and intelligent
              systems. Passionate about analytics, machine learning, and
              Generative AI, I focus on building practical, business-ready
              solutions using real-world data.
            </p>
          </CardContent>
        </Card>
      </motion.section>

      {/* SKILLS */}
      <motion.section
        initial={{ opacity: 0, y: 30 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.6 }}
        viewport={{ once: true }}
        className="max-w-5xl mx-auto mt-20"
      >
        <h2 className="text-2xl font-semibold text-center mb-8">Core Skills</h2>
        <div className="grid md:grid-cols-4 gap-6">
          {["Python & SQL", "Data Analysis", "Machine Learning", "GenAI & LLMs"].map(
            (skill, i) => (
              <motion.div
                key={skill}
                whileHover={{ scale: 1.05 }}
                transition={{ type: "spring", stiffness: 200 }}
              >
                <Card className="bg-slate-900 border-slate-800 rounded-2xl">
                  <CardContent className="p-6 flex items-center justify-center gap-2">
                    <Sparkles size={18} />
                    <span className="font-medium">{skill}</span>
                  </CardContent>
                </Card>
              </motion.div>
            )
          )}
        </div>
      </motion.section>

      {/* PROJECTS */}
      <motion.section
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 0.8 }}
        viewport={{ once: true }}
        className="max-w-5xl mx-auto mt-24"
      >
        <h2 className="text-2xl font-semibold text-center mb-10">Featured Projects</h2>
        <div className="grid md:grid-cols-2 gap-8">
          <motion.div whileHover={{ y: -6 }}>
            <Card className="bg-gradient-to-br from-slate-900 to-slate-800 border-slate-700 rounded-2xl">
              <CardContent className="p-6">
                <h3 className="text-xl font-semibold mb-2">
                  Customer Segmentation (K-Means)
                </h3>
                <p className="text-slate-300 mb-4">
                  Identified customer groups using clustering and visualized
                  actionable business insights.
                </p>
                <Button variant="outline" className="rounded-xl">
                  View on GitHub
                </Button>
              </CardContent>
            </Card>
          </motion.div>

          <motion.div whileHover={{ y: -6 }}>
            <Card className="bg-gradient-to-br from-slate-900 to-slate-800 border-slate-700 rounded-2xl">
              <CardContent className="p-6">
                <h3 className="text-xl font-semibold mb-2">
                  Exploratory Data Analysis
                </h3>
                <p className="text-slate-300 mb-4">
                  Cleaned, analyzed, and visualized datasets to uncover hidden
                  trends and patterns.
                </p>
                <Button variant="outline" className="rounded-xl">
                  View on GitHub
                </Button>
              </CardContent>
            </Card>
          </motion.div>
        </div>
      </motion.section>

      {/* FOOTER */}
      <motion.footer
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 1 }}
        viewport={{ once: true }}
        className="mt-28 text-center text-slate-400"
      >
        © {new Date().getFullYear()} Ananda Ranganathan Harikrishnan · Built with Data & ❤️
      </motion.footer>
    </div>
  );
}

