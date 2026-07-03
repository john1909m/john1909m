
<style>
*{box-sizing:border-box;margin:0;padding:0}
.wrap{background:#0d1117;border-radius:16px;padding:2rem 2rem 1.5rem;font-family:'Courier New',monospace}
.hero{border-left:3px solid #3b82f6;padding-left:1.25rem;margin-bottom:1.75rem}
.typing{font-size:11px;color:#3b82f6;letter-spacing:.12em;margin-bottom:.5rem}
.name{font-size:30px;font-weight:700;color:#e6f1ff;line-height:1.15;font-family:'Courier New',monospace}
.name span{color:#3b82f6}
.role{font-size:13px;color:#7dd3fc;margin-top:.4rem;letter-spacing:.04em}
.tagline{font-size:11px;color:#475569;margin-top:.6rem;font-style:italic}
.links{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:1.75rem}
.lbadge{display:inline-flex;align-items:center;gap:5px;padding:4px 11px;border-radius:20px;font-size:11px;font-family:'Courier New',monospace;text-decoration:none;border:1px solid}
.lbadge.bl{background:#0c1a3a;border-color:#1d4ed8;color:#60a5fa}
.lbadge.bl:hover{background:#1e3a5f}
.lbadge.gr{background:#0a1f1a;border-color:#064e3b;color:#34d399}
.lbadge.pu{background:#1a0a2e;border-color:#5b21b6;color:#a78bfa}
.lbadge.gy{background:#111827;border-color:#374151;color:#9ca3af}
.sec-label{font-size:10px;color:#3b82f6;letter-spacing:.15em;margin-bottom:.75rem;font-family:'Courier New',monospace}
.sec-label::before{content:'// '}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:1.75rem}
.aitem{background:#111827;border:1px solid #1e293b;border-radius:8px;padding:.6rem .85rem;font-size:12px;color:#94a3b8;display:flex;align-items:flex-start;gap:8px;line-height:1.5}
.aitem i{font-size:14px;color:#3b82f6;flex-shrink:0;margin-top:1px}
.aitem strong{color:#e2e8f0}
.divider{height:1px;background:linear-gradient(90deg,#1d4ed8,#7c3aed,#0f172a);margin:1.5rem 0;opacity:.6}
.proj-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:1.75rem}
.pcard{background:#0f172a;border:1px solid #1e293b;border-radius:10px;padding:.85rem 1rem;transition:border-color .2s}
.pcard.star{border-color:#1d4ed8;background:#0c1a3a}
.pcard:hover{border-color:#3b82f6}
.ph{display:flex;align-items:center;gap:8px;margin-bottom:.5rem}
.picon{width:28px;height:28px;border-radius:6px;background:#0d1117;border:1px solid #1e293b;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.picon i{font-size:14px;color:#3b82f6}
.pcard.star .picon{border-color:#1d4ed8;background:#0c1a3a}
.pcard.star .picon i{color:#60a5fa}
.pname{font-size:12px;font-weight:700;color:#e2e8f0;font-family:'Courier New',monospace}
.pbadge{margin-left:auto;font-size:9px;padding:2px 7px;border-radius:10px;background:#0c1a3a;border:1px solid #1d4ed8;color:#60a5fa;font-family:'Courier New',monospace}
.pdesc{font-size:11px;color:#64748b;line-height:1.5;margin-bottom:.6rem}
.ptags{display:flex;gap:4px;flex-wrap:wrap}
.ptag{font-size:10px;padding:1px 7px;border-radius:4px;background:#111827;color:#475569;border:1px solid #1e293b;font-family:'Courier New',monospace}
.pcard.star .ptag{border-color:#172554;color:#3b82f6}
.stack-wrap{margin-bottom:1.75rem}
.sg{margin-bottom:.85rem}
.sglabel{font-size:10px;color:#475569;letter-spacing:.1em;margin-bottom:.4rem}
.spills{display:flex;gap:5px;flex-wrap:wrap}
.sp{font-size:11px;padding:3px 10px;border-radius:5px;font-family:'Courier New',monospace;border:1px solid}
.sp.be{background:#0c1a3a;border-color:#1e3a8a;color:#60a5fa}
.sp.fe{background:#0a2218;border-color:#064e3b;color:#34d399}
.sp.db{background:#1c1207;border-color:#78350f;color:#fbbf24}
.sp.to{background:#111827;border-color:#1e293b;color:#64748b}
.learning{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:1.75rem}
.lp{font-size:11px;padding:3px 11px;border-radius:20px;border:1px solid #1e293b;color:#475569;font-family:'Courier New',monospace;display:flex;align-items:center;gap:4px}
.lp i{font-size:12px;color:#3b82f6}
.footer{display:flex;align-items:center;justify-content:space-between;padding-top:.5rem;border-top:1px solid #1e293b}
.footer span{font-size:11px;color:#334155;font-family:'Courier New',monospace}
.footer .open{color:#3b82f6}
.cursor{display:inline-block;width:2px;height:14px;background:#3b82f6;margin-left:3px;vertical-align:middle;animation:blink 1s step-end infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
</style>

<div class="wrap">

  <div class="hero">
    <div class="typing">hello_world.exe</div>
    <div class="name">John Emil<span>.</span><br>Ramzy<span class="cursor"></span></div>
    <div class="role">Software Engineer &nbsp;/&nbsp; Full Stack Developer &nbsp;/&nbsp; Egypt</div>
    <div class="tagline">"Building real products that solve real problems."</div>
  </div>

  <div class="links">
    <a class="lbadge bl" href="https://john1909portfolio.netlify.app/" target="_blank"><i class="ti ti-world" aria-hidden="true"></i>portfolio</a>
    <a class="lbadge pu" href="https://www.linkedin.com/in/johnemil" target="_blank"><i class="ti ti-brand-linkedin" aria-hidden="true"></i>linkedin</a>
    <a class="lbadge gy" href="https://github.com/john1909m" target="_blank"><i class="ti ti-brand-github" aria-hidden="true"></i>github</a>
    <a class="lbadge gr" href="mailto:johnemil21@yahoo.com"><i class="ti ti-mail" aria-hidden="true"></i>email</a>
  </div>

  <div class="sec-label">about_me</div>
  <div class="about-grid">
    <div class="aitem"><i class="ti ti-school" aria-hidden="true"></i><span><strong>Computer Engineering</strong> — Modern Academy, Maadi</span></div>
    <div class="aitem"><i class="ti ti-rocket" aria-hidden="true"></i><span>Founded <strong>Storely</strong>, a multi-tenant SaaS e-commerce platform</span></div>
    <div class="aitem"><i class="ti ti-code" aria-hidden="true"></i><span>Full stack dev with a <strong>backend-focused</strong> mindset</span></div>
    <div class="aitem"><i class="ti ti-building-factory-2" aria-hidden="true"></i><span>Web Dev Intern at <strong>GUPCO</strong> — oil & gas enterprise</span></div>
  </div>

  <div class="divider"></div>

  <div class="sec-label">featured_projects</div>
  <div class="proj-grid">
    <div class="pcard star">
      <div class="ph">
        <div class="picon"><i class="ti ti-building-store" aria-hidden="true"></i></div>
        <span class="pname">Storely</span>
        <span class="pbadge">SaaS</span>
      </div>
      <div class="pdesc">Multi-tenant e-commerce platform — store builder, 3 payment gateways, OTP auth & subdomain support.</div>
      <div class="ptags"><span class="ptag">React</span><span class="ptag">Spring Boot</span><span class="ptag">OracleDB</span><span class="ptag">JWT</span></div>
    </div>
    <div class="pcard">
      <div class="ph">
        <div class="picon"><i class="ti ti-stethoscope" aria-hidden="true"></i></div>
        <span class="pname">Clinic System</span>
      </div>
      <div class="pdesc">Full-stack clinic management — patients, doctors, appointments & prescriptions with role-based access.</div>
      <div class="ptags"><span class="ptag">React</span><span class="ptag">Spring Boot</span><span class="ptag">JPA</span><span class="ptag">JWT</span></div>
    </div>
    <div class="pcard">
      <div class="ph">
        <div class="picon"><i class="ti ti-building-skyscraper" aria-hidden="true"></i></div>
        <span class="pname">Smart City</span>
      </div>
      <div class="pdesc">Real-time monitoring of CO₂, humidity, temperature & home automation with live dashboards.</div>
      <div class="ptags"><span class="ptag">React</span><span class="ptag">Spring Boot</span><span class="ptag">REST APIs</span></div>
    </div>
    <div class="pcard">
      <div class="ph">
        <div class="picon"><i class="ti ti-shopping-bag" aria-hidden="true"></i></div>
        <span class="pname">Essence</span>
      </div>
      <div class="pdesc">Responsive e-commerce frontend — clean component architecture, Context API & performance-first UX.</div>
      <div class="ptags"><span class="ptag">React</span><span class="ptag">Tailwind</span><span class="ptag">SCSS</span><span class="ptag">Netlify</span></div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="sec-label">tech_stack</div>
  <div class="stack-wrap">
    <div class="sg">
      <div class="sglabel">backend</div>
      <div class="spills">
        <span class="sp be">Java</span>
        <span class="sp be">Spring Boot</span>
        <span class="sp be">REST APIs</span>
        <span class="sp be">JWT</span>
        <span class="sp be">JPA/Hibernate</span>
      </div>
    </div>
    <div class="sg">
      <div class="sglabel">frontend</div>
      <div class="spills">
        <span class="sp fe">React.js</span>
        <span class="sp fe">JavaScript</span>
        <span class="sp fe">Tailwind CSS</span>
        <span class="sp fe">SCSS</span>
      </div>
    </div>
    <div class="sg">
      <div class="sglabel">database</div>
      <div class="spills">
        <span class="sp db">OracleDB</span>
      </div>
    </div>
    <div class="sg">
      <div class="sglabel">tools</div>
      <div class="spills">
        <span class="sp to">Git</span>
        <span class="sp to">Postman</span>
        <span class="sp to">Maven</span>
        <span class="sp to">Render</span>
      </div>
    </div>
  </div>

  <div class="sec-label">currently_learning</div>
  <div class="learning">
    <span class="lp"><i class="ti ti-arrow-right" aria-hidden="true"></i>System Design</span>
    <span class="lp"><i class="ti ti-arrow-right" aria-hidden="true"></i>Microservices</span>
    <span class="lp"><i class="ti ti-arrow-right" aria-hidden="true"></i>Spring Security</span>
    <span class="lp"><i class="ti ti-arrow-right" aria-hidden="true"></i>Flutter</span>
    <span class="lp"><i class="ti ti-arrow-right" aria-hidden="true"></i>UI/UX</span>
  </div>

  <div class="footer">
    <span><i class="ti ti-map-pin" style="font-size:12px" aria-hidden="true"></i> Giza, Egypt</span>
    <span class="open">open to work — internships & junior roles</span>
  </div>

</div>
