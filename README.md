# <h1 align="center" style="font-size: 36px;">🌐 Enterprise Network Infrastructure & Security Hardening Lab</h1>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Simulator-Cisco%20Packet%20Tracer-00569B?logo=cisco&logoColor=white&style=for-the-badge" alt="Simulator"></a>
  <a href="#"><img src="https://img.shields.io/badge/Security-SSH%20v2-green?style=for-the-badge" alt="Security"></a>
  <a href="#"><img src="https://img.shields.io/badge/Status-Phase%201%20Complete-orange?style=for-the-badge" alt="Status"></a>
</p>

<h3 style="font-size: 22px;">A custom, self-designed star-bus network topology built from scratch in Cisco Packet Tracer demonstrating inter-VLAN routing, subnet management, and device security hardening across core routing and switching layers.</h3>

---

## <h2 style="font-size: 26px;">📌 Project Overview</h2>

<p style="font-size: 16px;">This architecture is centered around a <strong>Core Router</strong> managing local subnets and Layer 2 access switches.</p>

<ul style="font-size: 16px;">
  <li><strong>Active Segment A:</strong> Operational on the <code>192.168.10.0/24</code> subnet. Hosts 4 endpoint devices, including a dedicated management host (<code>AdminA</code>), aggregating into <strong>Switch-A</strong>.</li>
  <li><strong>Phases 2 & 3 (In Progress):</strong> Additional distribution segments (<strong>Switch-B</strong> and <strong>Switch-C</strong>) are mapped in the topology for future expansion.</li>
</ul>

---

## <h2 style="font-size: 26px;">🛡️ Security Hardening Implemented</h2>

<p style="font-size: 16px;">To transition this network from default factory settings to a secure enterprise posture, the following controls were applied:</p>

<ol style="font-size: 16px;">
  <li><strong>Domain & Identity Management:</strong> Assigned local domain <code>mynetwork.local</code>.</li>
  <li><strong>Encrypted Management (SSH):</strong> Insecure Telnet access disabled across all virtual terminal lines (<code>line vty</code>). Remote administration is strictly restricted to encrypted <strong>SSH</strong> using globally generated <strong>1024-bit RSA keys</strong>.</li>
  <li><strong>Local Database Authentication:</strong> Enforced privilege-level local account logins (<code>privilege 15</code>).</li>
  <li><strong>Credential Protection:</strong> Activated global reversible password obfuscation (<code>service password-encryption</code>) across active infrastructure to prevent clear-text configuration harvesting.</li>
  <li><strong>Physical & Console Lines:</strong> Secured console ports and privileged execution modes with distinct physical console passwords and enable secrets.</li>
  <li><strong>Out-of-Band Management Routing:</strong> Configured a dedicated management IP (<code>192.168.10.254/24</code>) on <strong>Switch-A</strong> with explicit default gateway routing back to the Core Router interface (<code>192.168.10.1</code>).</li>
</ol>

---

## <h2 style="font-size: 26px;">🔑 Access & Lab Credentials</h2>

> <p style="font-size: 15px;"><strong>Note:</strong> These uniform credentials are set up for laboratory testing and verification purposes.</p>

<table style="width: 100%; font-size: 16px;">
  <thead>
    <tr>
      <th align="left">Parameter / Device</th>
      <th align="left">Configured Value</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><strong>Domain Name</strong></td><td><code>mynetwork.local</code></td></tr>
    <tr><td><strong>SSH / Admin Username</strong></td><td><code>admin</code></td></tr>
    <tr><td><strong>Privilege Level</strong></td><td><code>15</code> (Full Privileged Execution)</td></tr>
    <tr><td><strong>Secret / Password (SSH/VTY)</strong></td><td><code>admin123</code></td></tr>
    <tr><td><strong>Core Router Console Password</strong></td><td><code>password1234</code></td></tr>
    <tr><td><strong>Core Router Enable Secret</strong></td><td><code>secret12324</code></td></tr>
    <tr><td><strong>Core Router Gateway IP</strong></td><td><code>192.168.10.1</code></td></tr>
    <tr><td><strong>Switch-A Management IP</strong></td><td><code>192.168.10.254</code></td></tr>
    <tr><td><strong>Switch-B Status</strong></td><td>⏳ <em>Pending Phase 2 Deployment</em></td></tr>
    <tr><td><strong>Switch-C Status</strong></td><td>⏳ <em>Pending Phase 2 Deployment</em></td></tr>
  </tbody>
</table>

---

## <h2 style="font-size: 26px;">📁 Repository Structure</h2>

```text
.
├── Network_Topology.pkt                  # Cisco Packet Tracer Lab File
├── Personal_Network_Project_Showcase.docx # Project Summary Documentation
└── README.md                             # Project Overview & Credentials
