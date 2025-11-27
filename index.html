import React, { useState, useEffect, useRef } from 'react';
import { 
  Activity, Server, Cpu, Eye, Box, Terminal, Settings, 
  BarChart2, Zap, Layers, Code, ShieldAlert, Smartphone, 
  CheckCircle, Menu, X, Brain, Network, Workflow,
  Wrench, Battery, AlertTriangle, TrendingDown, Wifi,
  Database, Gauge, ArrowRight, ChevronDown, ChevronUp,
  Mic2, Radio, Anchor, Lock, File, MousePointer
} from 'lucide-react';

// --- CSS ANIMATIONS ---
const GLOBAL_STYLES = `
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .animate-fade-in-up {
    animation: fadeInUp 0.8s cubic-bezier(0.22, 1, 0.36, 1) forwards;
  }
  .custom-scrollbar::-webkit-scrollbar {
    height: 6px; width: 6px;
  }
  .custom-scrollbar::-webkit-scrollbar-track {
    background: #111; 
  }
  .custom-scrollbar::-webkit-scrollbar-thumb {
    background: #333; border-radius: 3px;
  }
  html { scroll-behavior: smooth; }
`;

// --- THEME CONFIG ---
const THEME = {
  dark: {
    bg: 'bg-[#050505]', text: 'text-white', subtext: 'text-gray-400',
    border: 'border-gray-800', accent: 'text-[#dca54c]', 
    cardBg: 'bg-[#111]', cardHover: 'hover:bg-[#161616]',
    codeBlock: 'bg-[#0a0a0a] border-gray-800 text-gray-300',
    button: 'border-[#dca54c] text-[#dca54c] hover:bg-[#dca54c] hover:text-black'
  },
  light: {
    bg: 'bg-[#f4f4f0]', text: 'text-[#1a1a1a]', subtext: 'text-gray-600',
    border: 'border-[#d0d0d0]', accent: 'text-[#c2410c]', 
    cardBg: 'bg-[#ffffff]', cardHover: 'hover:bg-[#fbfbfb]',
    codeBlock: 'bg-[#e5e5e5] border-[#d0d0d0] text-[#1a1a1a]',
    button: 'border-[#c2410c] text-[#c2410c] hover:bg-[#c2410c] hover:text-white'
  }
};

// --- MOCK DATA ---
const QC_DEFECTS = [
  { id: 'CAM-01', type: 'Oil Stain', conf: 0.98, status: 'CRITICAL' },
  { id: 'CAM-03', type: 'Stitch err', conf: 0.87, status: 'MAJOR' },
  { id: 'CAM-02', type: 'No Defect', conf: 0.99, status: 'PASS' },
];

// --- UTILITIES ---
const useOnScreen = (options) => {
  const ref = useRef(null);
  const [visible, setVisible] = useState(false);
  useEffect(() => {
    const observer = new IntersectionObserver(([entry]) => {
      if (entry.isIntersecting) { setVisible(true); observer.unobserve(entry.target); }
    }, options);
    if (ref.current) observer.observe(ref.current);
    return () => { if (ref.current) observer.unobserve(ref.current); };
  }, [ref, options]);
  return [ref, visible];
};

// --- COMPONENTS ---

const Reveal = ({ children, delay = 0, className = "" }) => {
  const [ref, visible] = useOnScreen({ threshold: 0.1 });
  return (
    <div ref={ref} className={`transition-all duration-1000 ease-[0.22,1,0.36,1] transform ${visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} ${className}`} style={{ transitionDelay: `${delay}ms` }}>
      {children}
    </div>
  );
};

const FadeIn = ({ children, delay = 0 }) => {
  const [mounted, setMounted] = useState(false);
  useEffect(() => {
    const timer = setTimeout(() => setMounted(true), 100);
    return () => clearTimeout(timer);
  }, []);
  return (
    <div className={`transition-all duration-1000 ease-out transform ${mounted ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'}`} style={{ transitionDelay: `${delay}ms` }}>
      {children}
    </div>
  );
};

const SectionHeader = ({ number, title, subtitle, theme = 'dark' }) => {
  const t = THEME[theme];
  return (
    <div className="mb-24">
      <Reveal>
        <div className={`flex items-baseline space-x-4 border-b ${t.border} pb-6`}>
          <span className={`text-xs font-mono ${t.accent} tracking-widest`}>0{number}</span>
          <h2 className={`text-4xl md:text-7xl font-light tracking-tighter ${t.text} uppercase`}>{title}</h2>
        </div>
        {subtitle && <p className={`mt-8 ${t.subtext} max-w-2xl text-xl font-light leading-relaxed`}>{subtitle}</p>}
      </Reveal>
    </div>
  );
};

const Accordion = ({ title, children, theme = 'dark' }) => {
  const [isOpen, setIsOpen] = useState(false);
  const t = THEME[theme];
  return (
    <div className={`border ${t.border} rounded-sm overflow-hidden mb-4 transition-all duration-500`}>
      <button onClick={() => setIsOpen(!isOpen)} className={`w-full flex justify-between items-center p-6 ${t.cardBg} hover:opacity-90 transition-opacity`}>
        <div className="flex items-center space-x-3">
          <Code className={`w-5 h-5 ${t.accent}`} />
          <span className={`font-mono text-sm uppercase tracking-wider ${t.text}`}>{title}</span>
        </div>
        {isOpen ? <ChevronUp className={t.text} /> : <ChevronDown className={t.text} />}
      </button>
      <div className={`transition-all duration-500 ease-in-out overflow-hidden ${isOpen ? 'max-h-[800px] opacity-100' : 'max-h-0 opacity-0'}`}>
        <div className={`p-6 ${t.codeBlock}`}>{children}</div>
      </div>
    </div>
  );
};

const CodeSnippet = ({ code }) => (
  <pre className="font-mono text-xs md:text-sm leading-relaxed overflow-x-auto custom-scrollbar text-gray-400 p-2">{code}</pre>
);

const StatBox = ({ value, label, sub, icon: Icon, theme = 'dark' }) => {
  const t = THEME[theme];
  return (
    <div className={`border ${t.border} p-6 flex flex-col justify-between h-32 ${t.cardBg} group`}>
      <div className="flex justify-between items-start">
        <span className={`text-4xl font-light ${t.text}`}>{value}</span>
        {Icon && <Icon className={`w-5 h-5 ${t.accent} opacity-50 group-hover:opacity-100 transition-opacity`} />}
      </div>
      <div>
        <span className={`text-xs font-mono uppercase tracking-widest ${t.subtext}`}>{label}</span>
        {sub && <span className={`block text-[10px] ${t.subtext} opacity-60`}>{sub}</span>}
      </div>
    </div>
  );
};

const FeatureRow = ({ title, description, tags, theme = 'dark' }) => {
  const t = THEME[theme];
  return (
    <div className={`group border-t ${t.border} py-12 md:py-16 ${t.cardHover} transition-colors cursor-default`}>
      <div className="grid grid-cols-1 md:grid-cols-12 gap-8 items-start">
        <div className="md:col-span-4">
          <h3 className={`text-2xl md:text-3xl font-light ${t.text} group-hover:translate-x-4 transition-transform duration-500`}>
            {title}
          </h3>
        </div>
        <div className="md:col-span-5">
          <p className={`${t.subtext} text-lg font-light leading-relaxed`}>
            {description}
          </p>
        </div>
        <div className="md:col-span-3 flex flex-wrap gap-2 justify-start md:justify-end">
          {tags.map((tag, i) => (
            <span key={i} className={`px-3 py-1 border ${t.border} text-xs ${t.subtext} uppercase tracking-widest rounded-full`}>
              {tag}
            </span>
          ))}
        </div>
      </div>
    </div>
  );
};

// --- VISUALIZATIONS ---

const DashboardMockup = () => (
  <div className="w-full bg-[#111] border border-gray-800 p-6 relative overflow-hidden group">
    <div className="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-[#dca54c] to-transparent opacity-50" />
    <div className="flex justify-between items-center mb-8">
      <div>
        <h3 className="text-xs font-mono text-[#dca54c] mb-1">LIVE FEED</h3>
        <h2 className="text-2xl font-light text-white">Line-A / Inspection Station 04</h2>
      </div>
      <div className="flex gap-4">
        <div className="text-right">
          <div className="text-xl font-light text-white">99.8%</div>
          <div className="text-[10px] font-mono text-gray-500">YIELD</div>
        </div>
      </div>
    </div>
    <div className="space-y-3">
      {QC_DEFECTS.map((defect, i) => (
        <div key={i} className="grid grid-cols-12 items-center py-3 border-b border-gray-800/50 hover:bg-white/5 transition-colors">
          <div className="col-span-2 font-mono text-xs text-gray-400">{defect.id}</div>
          <div className="col-span-4 text-sm text-white">{defect.type}</div>
          <div className="col-span-3">
            <div className="h-1 w-16 bg-gray-800 rounded-full overflow-hidden">
              <div className="h-full bg-[#dca54c]" style={{ width: `${defect.conf * 100}%` }} />
            </div>
          </div>
          <div className="col-span-3 text-right">
            <span className={`text-[10px] font-bold px-2 py-1 rounded ${
              defect.status === 'CRITICAL' ? 'bg-red-900/40 text-red-400' :
              defect.status === 'PASS' ? 'bg-green-900/40 text-green-400' : 'bg-orange-900/40 text-orange-400'
            }`}>
              {defect.status}
            </span>
          </div>
        </div>
      ))}
    </div>
  </div>
);

const SpectralHeatmap = () => (
  <div className="w-full h-64 relative bg-[#111] border border-gray-800 overflow-hidden">
    <div className="absolute top-2 left-2 text-xs font-mono text-[#dca54c]">SPECTRUM ANALYSIS</div>
    <div className="flex h-full items-end space-x-px opacity-80">
      {[...Array(40)].map((_, i) => {
        const height = 20 + Math.random() * 60;
        const color = i > 30 ? '#ef4444' : '#dca54c';
        return (
          <div key={i} className="flex-1 transition-all duration-500" style={{ height: `${height}%`, backgroundColor: color, opacity: 0.6 + Math.random() * 0.4 }} />
        );
      })}
    </div>
  </div>
);

const LoadShiftDiagram = () => (
  <div className="w-full h-64 relative bg-white border border-[#d0d0d0] overflow-hidden p-4">
    <div className="absolute top-2 left-4 text-xs font-mono text-[#c2410c]">LOAD OPTIMIZATION</div>
    <div className="relative h-full w-full flex items-end space-x-1">
      {[...Array(24)].map((_, i) => {
        const h = 30 + Math.random() * 50;
        const isPeak = i > 16 && i < 20;
        return (
          <div key={i} className={`flex-1 ${isPeak ? 'bg-gray-300' : 'bg-[#c2410c]'}`} style={{ height: `${isPeak ? h * 0.6 : h}%` }} />
        )
      })}
    </div>
    <div className="absolute bottom-2 right-4 text-[10px] text-gray-500">24H CYCLE</div>
  </div>
);

// --- PAGE COMPONENTS ---

const QCVisionPage = ({ onNavigate }) => (
  <div className="w-full">
    {/* Hero */}
    <header className="relative min-h-[90vh] flex flex-col justify-center px-6 md:px-12 lg:px-24 bg-[#050505] text-white">
      <FadeIn delay={100}>
        <div className="flex items-center space-x-3 mb-8">
          <div className="w-2 h-2 bg-[#dca54c] rounded-full animate-pulse" />
          <span className="text-xs font-mono text-[#dca54c] uppercase tracking-widest">The Platform</span>
        </div>
      </FadeIn>
      <FadeIn delay={300}>
        <h1 className="text-6xl md:text-8xl lg:text-9xl font-light leading-[0.9] tracking-tighter uppercase mb-12">
          Total <br />
          Factory <br />
          <span className="text-[#dca54c]">Autonomy</span>
        </h1>
      </FadeIn>
      <FadeIn delay={500}>
        <p className="text-xl text-gray-400 font-light max-w-2xl leading-relaxed mb-12">
          A unified neural infrastructure for the modern factory. Three interconnected modules operating at the edge.
        </p>
      </FadeIn>
    </header>

    {/* NEW: Module Nexus / Menu Section (Light) */}
    <section className="py-24 px-6 md:px-12 lg:px-24 bg-white text-[#1a1a1a]">
      <SectionHeader number="0" title="The Triad" subtitle="Select a module to explore the architecture." theme="light" />
      <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div 
          onClick={() => onNavigate('qc-vision')}
          className="p-8 border border-gray-200 hover:border-[#dca54c] cursor-pointer group transition-all duration-300 hover:shadow-xl"
        >
          <div className="flex justify-between items-start mb-8">
            <Eye className="w-10 h-10 text-[#dca54c]" />
            <span className="text-xs font-mono text-gray-400 uppercase group-hover:text-[#dca54c]">Module 01</span>
          </div>
          <h3 className="text-3xl font-light mb-4 group-hover:translate-x-2 transition-transform">QC Vision</h3>
          <p className="text-gray-600 font-light leading-relaxed mb-6">
            The Eyes. 100% visual defect detection at 300ft/min using MicroViT.
          </p>
          <div className="flex items-center space-x-2 text-xs font-bold uppercase tracking-widest text-[#dca54c]">
            <span>Deep Dive</span> <ArrowRight className="w-4 h-4" />
          </div>
        </div>

        <div 
          onClick={() => onNavigate('failpredict')}
          className="p-8 border border-gray-200 hover:border-[#dca54c] cursor-pointer group transition-all duration-300 hover:shadow-xl"
        >
          <div className="flex justify-between items-start mb-8">
            <Activity className="w-10 h-10 text-[#dca54c]" />
            <span className="text-xs font-mono text-gray-400 uppercase group-hover:text-[#dca54c]">Module 02</span>
          </div>
          <h3 className="text-3xl font-light mb-4 group-hover:translate-x-2 transition-transform">FailPredict</h3>
          <p className="text-gray-600 font-light leading-relaxed mb-6">
            The Pulse. Vibration analysis that predicts machine failure weeks in advance.
          </p>
          <div className="flex items-center space-x-2 text-xs font-bold uppercase tracking-widest text-[#dca54c]">
            <span>Deep Dive</span> <ArrowRight className="w-4 h-4" />
          </div>
        </div>

        <div 
          onClick={() => onNavigate('powerguard')}
          className="p-8 border border-gray-200 hover:border-[#dca54c] cursor-pointer group transition-all duration-300 hover:shadow-xl"
        >
          <div className="flex justify-between items-start mb-8">
            <Zap className="w-10 h-10 text-[#dca54c]" />
            <span className="text-xs font-mono text-gray-400 uppercase group-hover:text-[#dca54c]">Module 03</span>
          </div>
          <h3 className="text-3xl font-light mb-4 group-hover:translate-x-2 transition-transform">PowerGuard</h3>
          <p className="text-gray-600 font-light leading-relaxed mb-6">
            The Metabolism. Real-time energy optimization and anomaly detection.
          </p>
          <div className="flex items-center space-x-2 text-xs font-bold uppercase tracking-widest text-[#dca54c]">
            <span>Deep Dive</span> <ArrowRight className="w-4 h-4" />
          </div>
        </div>
      </div>
    </section>

    {/* QC Vision Deep Dive (Dark) - Restored Full Detail */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#050505] text-white border-t border-gray-900">
      <div className="mb-12">
        <span className="text-xs font-mono text-[#dca54c] uppercase tracking-widest mb-2 block">Module 01 Focus</span>
        <SectionHeader number="1" title="The Neural Core" theme="dark" />
      </div>
      
      <Reveal>
        <div className="space-y-0 mb-16">
          <FeatureRow 
            title="Data Engine" 
            description="Automated ingestion with version control. Includes class balancing via WeightedRandomSampler and synthetic defect generation using MixUp/CutMix strategies."
            tags={['Albumentations', 'OpenCV', 'JSON Annotations']}
            theme="dark"
          />
          <FeatureRow 
            title="MicroViT Architecture" 
            description="Custom lightweight Vision Transformer optimized for edge latency. Features efficient patch embedding and linear attention mechanisms for O(N) complexity."
            tags={['PyTorch', 'Transformer', 'Attention']}
            theme="dark"
          />
          <FeatureRow 
            title="Advanced Training" 
            description="Mixed precision (FP16/BF16) training loop with Gradient Accumulation, dynamic loss scaling, and distributed training support (DDP)."
            tags={['AMP', 'Gradient Clipping', 'DDP']}
            theme="dark"
          />
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-2 gap-12">
          <div className="space-y-4">
            <h3 className="text-xl font-light text-white">Trainer Implementation</h3>
            <p className="text-gray-500 font-light mb-4">Core training loop supporting accumulation & mixed precision.</p>
            <Accordion title="FabricDefectTrainer.py">
              <CodeSnippet code={`class FabricDefectTrainer:
    def _train_epoch(self) -> Dict[str, float]:
        self.model.train()
        
        for batch_idx, (images, labels) in enumerate(pbar):
            # MixUp/CutMix Augmentation
            images, labels_a, labels_b, lam = self._mixup_cutmix(images, labels)
            
            # Mixed Precision Forward
            with self.mp_trainer.autocast_context():
                outputs = self.model(images)
                loss = lam * self.criterion(outputs, labels_a) + \\
                       (1 - lam) * self.criterion(outputs, labels_b)
            
            # Gradient Accumulation
            if self.mp_trainer.accumulator.backward(loss):
                self.mp_trainer.accumulator.step()
                self.scheduler.step()`} />
            </Accordion>
          </div>
          
          <div className="bg-[#111] p-8 border border-gray-800 flex flex-col justify-center items-center text-center">
            <Layers className="w-16 h-16 text-[#dca54c] mb-6" />
            <h3 className="text-2xl text-white font-light mb-2">MicroViT Tiny</h3>
            <p className="text-4xl font-mono text-white mb-2">99.2%</p>
            <p className="text-sm text-gray-500 uppercase tracking-widest">Validation Accuracy</p>
            <div className="w-full h-px bg-gray-800 my-8" />
            <div className="flex space-x-8">
              <div>
                <p className="text-2xl text-white">3.2M</p>
                <p className="text-xs text-gray-500">Params</p>
              </div>
              <div>
                <p className="text-2xl text-white">12ms</p>
                <p className="text-xs text-gray-500">Latency</p>
              </div>
            </div>
          </div>
        </div>
      </Reveal>
    </section>

    {/* Edge Deployment (Light) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#f4f4f0] text-[#1a1a1a]">
      <SectionHeader number="2" title="Edge Deployment" theme="light" />
      <Reveal>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
          <StatBox label="Quantization" value="INT8" sub="Dynamic / Static" icon={Box} theme="light" />
          <StatBox label="Export Format" value="ONNX" sub="Opset 17" icon={File} theme="light" />
          <StatBox label="Runtime" value="ORT" sub="Optimized" icon={Cpu} theme="light" />
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center border border-gray-200 bg-[#ffffff] p-8 md:p-12">
          <div className="lg:col-span-5 space-y-8">
            <div>
              <h3 className="text-3xl font-light text-[#1a1a1a] mb-4">Hardware Agnostic</h3>
              <p className="text-gray-600 leading-relaxed font-light">
                Our <code>EdgeInferenceEngine</code> abstracts hardware specifics, automatically selecting the optimal execution provider (CUDA, TensorRT, OpenVINO, or NNAPI) based on the available accelerator.
              </p>
            </div>
            <ul className="space-y-4">
              <li className="flex items-center space-x-4">
                 <div className="p-2 bg-white border border-gray-200 rounded"><Cpu className="w-5 h-5 text-[#c2410c]" /></div>
                 <div><h4 className="text-[#1a1a1a] text-sm">Raspberry Pi 4/5</h4><p className="text-xs text-gray-500">ARM NEON + GPIO Triggers</p></div>
              </li>
              <li className="flex items-center space-x-4">
                 <div className="p-2 bg-white border border-gray-200 rounded"><Smartphone className="w-5 h-5 text-[#c2410c]" /></div>
                 <div><h4 className="text-[#1a1a1a] text-sm">Android Mobile</h4><p className="text-xs text-gray-500">ONNX Runtime Mobile + Kotlin</p></div>
              </li>
            </ul>
          </div>
          
          <div className="lg:col-span-7">
             <Accordion title="Edge Inference (Python)" theme="light">
               <CodeSnippet code={`class EdgeInferenceEngine:
    def _create_session(self) -> ort.InferenceSession:
        providers = self._get_providers()
        
        # Hardware specific optimizations
        sess_options = ort.SessionOptions()
        sess_options.graph_optimization_level = \\
            ort.GraphOptimizationLevel.ORT_ENABLE_ALL
        sess_options.enable_mem_pattern = True
        
        return ort.InferenceSession(
            str(self.model_path),
            sess_options,
            providers=providers
        )

    def predict(self, image):
        # Sub-millisecond inference
        start = time.perf_counter()
        outputs = self.session.run(...)
        latency = (time.perf_counter() - start) * 1000
        return self._post_process(outputs, latency)`} />
             </Accordion>
          </div>
        </div>
      </Reveal>
    </section>

    {/* Monitoring (Dark) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#050505] text-white border-t border-gray-900">
      <SectionHeader number="3" title="Production Intelligence" theme="dark" />
      <Reveal>
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-24">
          <div className="lg:col-span-4 space-y-12">
            <div className="space-y-4">
              <BarChart2 className="w-8 h-8 text-[#dca54c]" />
              <h3 className="text-2xl text-white font-light">Metric Collection</h3>
              <p className="text-gray-400 font-light">Automatic tracking of inference latency, defect distribution, and confidence scores.</p>
            </div>
            <div className="space-y-4">
              <ShieldAlert className="w-8 h-8 text-[#dca54c]" />
              <h3 className="text-2xl text-white font-light">Alert System</h3>
              <p className="text-gray-400 font-light">Multi-channel notification dispatch (Webhook, Email, SMS) for critical defects.</p>
            </div>
          </div>

          <div className="lg:col-span-8">
            <DashboardMockup />
          </div>
        </div>
      </Reveal>
    </section>
  </div>
);

const FailPredictPage = () => (
  <div className="w-full">
    {/* Hero */}
    <header className="relative min-h-[90vh] flex flex-col justify-center px-6 md:px-12 lg:px-24 bg-[#050505] text-white">
      <FadeIn delay={100}>
        <div className="flex items-center space-x-3 mb-8">
          <div className="w-2 h-2 bg-[#dca54c] rounded-full animate-pulse" />
          <span className="text-xs font-mono text-[#dca54c] uppercase tracking-widest">Module 02</span>
        </div>
      </FadeIn>
      <FadeIn delay={300}>
        <h1 className="text-5xl md:text-8xl lg:text-9xl font-light leading-[0.9] tracking-tighter uppercase mb-12">
          Silence <br /> Before <br /> <span className="text-[#dca54c]">Failure</span>
        </h1>
      </FadeIn>
      <FadeIn delay={500}>
        <p className="text-xl text-gray-400 font-light max-w-2xl leading-relaxed">
          Machines speak a language of vibration. FailPredict listens to these whispers at 100Hz, 
          predicting the end of life with 89% accuracy.
        </p>
      </FadeIn>
    </header>

    {/* Primer (Light) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#f4f4f0] text-[#1a1a1a]">
      <Reveal>
        <h2 className="text-3xl md:text-5xl font-light mb-8">The Pulse of the Machine</h2>
        <div className="grid grid-cols-1 lg:grid-cols-2 gap-16">
          <div>
            <p className="text-lg text-gray-600 font-light leading-relaxed mb-6">
              Reactive maintenance ("fixing it when it breaks") is the most expensive strategy in manufacturing. 
              Scheduled maintenance ("fixing it whether it needs it or not") is wasteful.
            </p>
            <p className="text-lg text-gray-600 font-light leading-relaxed">
              We utilize <strong>Condition-Based Maintenance (CBM)</strong>. By fusing 3-axis acceleration data 
              with temperature readings, we construct a multidimensional health index.
            </p>
          </div>
          <div className="grid grid-cols-2 gap-4">
            <StatBox value="100Hz" label="Sampling" theme="light" />
            <StatBox value="120h" label="Warning" theme="light" />
            <StatBox value="<$90" label="Hardware Cost" theme="light" />
            <StatBox value="MPU" label="Sensor Core" theme="light" />
          </div>
        </div>
      </Reveal>
    </section>

    {/* Prediction Engine (Dark) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#050505] text-white border-t border-gray-900">
      <SectionHeader number="1" title="Prediction Engine" theme="dark" />
      <Reveal>
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-16">
          <div className="lg:col-span-5 space-y-8">
            <h3 className="text-2xl font-light text-[#dca54c]">Stacked GRU Network</h3>
            <p className="text-gray-400 font-light">
              Vibration data is temporal. We employ a Gated Recurrent Unit (GRU) 
              network trained on the NASA CMAPSS dataset to model temporal degradation.
            </p>
            <div className="p-6 border border-gray-800 bg-[#111] rounded-sm">
              <h4 className="text-sm font-bold text-white uppercase mb-4 flex items-center gap-2">
                <Activity className="w-4 h-4 text-[#dca54c]" /> Signal Path
              </h4>
              <ul className="space-y-3 text-xs font-mono text-gray-400">
                <li className="flex justify-between"><span>1. Acquisition</span> <span className="text-white">MPU-6050 @ 100Hz</span></li>
                <li className="flex justify-between"><span>2. Transformation</span> <span className="text-white">Fast Fourier Transform</span></li>
                <li className="flex justify-between"><span>3. Feature Eng</span> <span className="text-white">Spectral Entropy</span></li>
                <li className="flex justify-between"><span>4. Inference</span> <span className="text-[#dca54c]">RUL Regression</span></li>
              </ul>
            </div>
          </div>
          <div className="lg:col-span-7">
            <Accordion title="Model Architecture (PyTorch)">
              <CodeSnippet code={`class RULPredictor(nn.Module):
    def __init__(self, input_size=24, hidden_sizes=[64, 32]):
        super().__init__()
        # Stacked GRU layers for temporal patterns
        self.gru1 = nn.GRU(input_size, hidden_sizes[0], batch_first=True, dropout=0.2)
        self.gru2 = nn.GRU(hidden_sizes[0], hidden_sizes[1], batch_first=True, dropout=0.2)
        
        # Temporal Attention to weigh critical moments
        self.attention = TemporalAttention(hidden_sizes[1])
        
        # Regression head for Remaining Useful Life
        self.head = nn.Sequential(
            nn.Linear(hidden_sizes[1], 32),
            nn.ReLU(),
            nn.Linear(32, 1) # Output: Hours remaining
        )

    def forward(self, x):
        x, _ = self.gru1(x)
        x, _ = self.gru2(x)
        x = self.attention(x)
        return self.head(x)`} />
            </Accordion>
          </div>
        </div>
      </Reveal>
    </section>

    {/* Health Monitor (Dark) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#050505] text-white border-t border-gray-900">
      <SectionHeader number="2" title="Health Monitor" theme="dark" />
      <Reveal>
        <div className="border border-gray-800 bg-[#111] p-8">
          <div className="flex justify-between items-end mb-8">
            <div>
              <h3 className="text-xs font-mono text-[#dca54c] mb-2">ASSET: SEW-A-001</h3>
              <h2 className="text-3xl font-light">Main Drive Bearing</h2>
            </div>
            <div className="text-right">
              <div className="text-4xl font-light text-white">342h</div>
              <div className="text-xs font-mono text-gray-500">REMAINING LIFE</div>
            </div>
          </div>
          <SpectralHeatmap />
        </div>
      </Reveal>
    </section>
  </div>
);

const PowerGuardPage = () => (
  <div className="w-full bg-[#f4f4f0]">
    {/* Hero */}
    <header className="relative min-h-[90vh] flex flex-col justify-center px-6 md:px-12 lg:px-24 bg-[#f4f4f0]">
      <FadeIn delay={100}>
        <div className="flex items-center space-x-3 mb-8">
          <div className="w-2 h-2 bg-[#c2410c] rounded-full animate-pulse" />
          <span className="text-xs font-mono text-[#c2410c] uppercase tracking-widest">Module 03</span>
        </div>
      </FadeIn>
      <FadeIn delay={300}>
        <h1 className="text-5xl md:text-8xl lg:text-9xl font-light leading-[0.9] tracking-tighter text-[#1a1a1a] uppercase mb-12">
          Invisible <br /> <span className="text-[#c2410c]">Waste</span> <br /> Visible
        </h1>
      </FadeIn>
      <FadeIn delay={500}>
        <p className="text-xl text-gray-600 font-light max-w-2xl leading-relaxed">
          PowerGuard creates a digital twin of your factory's electrical consumption, 
          detecting anomalies and optimizing for industrial tariff structures in real-time.
        </p>
      </FadeIn>
    </header>

    {/* Narrative (Dark) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#050505] text-white">
      <Reveal>
        <h2 className="text-3xl md:text-5xl font-light mb-8">Factory Metabolism</h2>
        <div className="grid grid-cols-1 lg:grid-cols-2 gap-16">
          <div>
            <p className="text-lg text-gray-400 font-light leading-relaxed mb-6">
              Hidden within the noise of motors and compressors are phantom loads and efficiency losses. 
              PowerGuard uses Unsupervised Learning to learn the "normal" electrical signature of your facility.
            </p>
          </div>
          <div className="grid grid-cols-2 gap-4">
            <StatBox value="18%" label="Savings" theme="dark" />
            <StatBox value="<200ms" label="Anomaly Detect" theme="dark" />
            <StatBox value="PZEM" label="Sensor Core" theme="dark" />
            <StatBox value="TS2Vec" label="Model Arch" theme="dark" />
          </div>
        </div>
      </Reveal>
    </section>

    {/* Anomaly Detection (Light) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#f4f4f0] text-[#1a1a1a] border-t border-gray-200">
      <SectionHeader number="1" title="Anomaly Detection" theme="light" />
      <Reveal>
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-16">
          <div className="lg:col-span-5 space-y-8">
            <h3 className="text-2xl font-light text-[#c2410c]">TS2Vec + Ruptures</h3>
            <p className="text-gray-600 font-light">
              We use TS2Vec to convert time-series power data into dense vector representations, 
              allowing us to compare the "shape" of power usage, not just the amplitude.
            </p>
            <ul className="space-y-3 text-xs font-mono text-gray-500 border-t border-gray-200 pt-4">
              <li className="flex justify-between"><span>Algorithm</span> <span className="text-[#1a1a1a]">Unsupervised Contrastive</span></li>
              <li className="flex justify-between"><span>Sensitivity</span> <span className="text-[#1a1a1a]">Adaptive Threshold</span></li>
            </ul>
          </div>
          <div className="lg:col-span-7">
            <Accordion title="Anomaly Logic (Python)" theme="light">
              <CodeSnippet code={`class PowerDetector:
    def detect(self, series):
        # 1. Encode
        repr = self.ts2vec.encode(series)
        # 2. Deviation
        z_score = abs((repr - self.mean) / self.std)
        # 3. Segmentation
        algo = rpt.Pelt(model="rbf").fit(series)
        return z_score.max() > 2.5`} />
            </Accordion>
          </div>
        </div>
      </Reveal>
    </section>

    {/* Load Intelligence (Light) */}
    <section className="py-32 px-6 md:px-12 lg:px-24 bg-[#f4f4f0] text-[#1a1a1a]">
      <SectionHeader number="2" title="Load Intelligence" theme="light" />
      <Reveal>
        <div className="border border-[#d0d0d0] bg-white p-8 shadow-lg">
          <div className="flex justify-between items-end mb-8">
            <div>
              <h3 className="text-xs font-mono text-[#c2410c] mb-2">FACTORY MAIN FEED</h3>
              <h2 className="text-3xl font-light">Peak Shaving Optimization</h2>
            </div>
            <div className="text-right">
              <div className="text-4xl font-light">-18%</div>
              <div className="text-xs font-mono text-gray-500">SAVINGS</div>
            </div>
          </div>
          <LoadShiftDiagram />
        </div>
      </Reveal>
    </section>
  </div>
);

// --- MAIN APP ---

const App = () => {
  const [activePage, setActivePage] = useState('qc-vision');
  const [isMenuOpen, setIsMenuOpen] = useState(false);

  const handleNav = (page) => {
    setActivePage(page);
    setIsMenuOpen(false);
    window.scrollTo(0, 0);
  };

  return (
    <div className="bg-[#050505] min-h-screen text-gray-200 font-sans overflow-x-hidden scroll-smooth selection:bg-[#dca54c] selection:text-black">
      <style>{GLOBAL_STYLES}</style>
      
      {/* GLOBAL NAVIGATION */}
      <nav className="fixed top-0 w-full z-[100] px-6 py-6 md:px-12 md:py-8 flex justify-between items-center mix-blend-difference text-white bg-[#050505]/80 backdrop-blur-sm border-b border-gray-800/50">
        <div className="text-xl md:text-2xl font-bold tracking-tighter cursor-pointer select-none" onClick={() => handleNav('qc-vision')}>
          INDUSTRIAL<span className="text-[#dca54c]">AI</span>.ONE
        </div>
        
        <div className="hidden md:flex space-x-8 font-mono text-xs uppercase tracking-widest text-gray-300">
          {['qc-vision', 'failpredict', 'powerguard'].map((page) => (
            <button 
              key={page}
              onClick={() => handleNav(page)} 
              className={`hover:text-[#dca54c] transition-colors duration-300 ${activePage === page ? 'text-[#dca54c]' : ''}`}
            >
              {page.replace('-', ' ')}
            </button>
          ))}
        </div>

        <button className="md:hidden z-50" onClick={() => setIsMenuOpen(!isMenuOpen)}>
          {isMenuOpen ? <X /> : <Menu />}
        </button>

        {isMenuOpen && (
          <div className="fixed inset-0 bg-white flex flex-col justify-center items-center space-y-8 text-xl z-40 text-black">
            {['qc-vision', 'failpredict', 'powerguard'].map((page) => (
              <button key={page} onClick={() => handleNav(page)} className="hover:text-[#dca54c] capitalize">
                {page.replace('-', ' ')}
              </button>
            ))}
          </div>
        )}
      </nav>

      {/* DYNAMIC CONTENT */}
      <main>
        {activePage === 'qc-vision' && <QCVisionPage onNavigate={handleNav} />}
        {activePage === 'failpredict' && <FailPredictPage />}
        {activePage === 'powerguard' && <PowerGuardPage />}
      </main>

      {/* FOOTER */}
      <footer className="py-24 px-6 md:px-12 lg:px-24 bg-[#050505] border-t border-gray-900 text-gray-500">
        <div className="flex flex-col md:flex-row justify-between items-start md:items-center mb-12">
          <div className="mb-8 md:mb-0">
            <h2 className="text-2xl font-bold tracking-tighter text-white mb-2">
              INDUSTRIAL<span className="text-[#dca54c]">AI</span>.ONE
            </h2>
            <p className="font-light text-sm">Blueprints for the autonomous future.</p>
          </div>
          <div className="flex space-x-8 text-xs font-mono uppercase tracking-widest">
            <button className="hover:text-white transition-colors">Documentation</button>
            <button className="hover:text-white transition-colors">GitHub</button>
            <button className="hover:text-white transition-colors">Contact</button>
          </div>
        </div>
        <div className="border-t border-gray-900 pt-8 text-xs font-mono uppercase">
          © 2025 Industrial-AI.One Engineering.
        </div>
      </footer>
    </div>
  );
};

export default App;


