1. Project Overview: 
The Deadlock Prevention and Recovery Toolkit is a web-based 
simulation and visualization platform designed to educate and assist users 
in understanding and managing deadlocks in operating systems. This 
interactive toolkit allows users to simulate resource allocation among 
processes, detect potential deadlocks, apply the Banker's Algorithm for 
prevention, and simulate recovery from deadlocks using process 
termination. 
Key Features 
1. Dynamic Simulation Setup 
• Users can configure the number of processes (up to 6) and 
resources (up to 4). 
• Supports setting maximum demand, allocation, and resource 
requests interactively. 
2. Real-Time Visualization 
• Utilizes D3.js to render a Resource Allocation Graph (RAG). 
• Distinct color-coded links: 
o Solid for allocations 
o Dashed for requests 
o Highlighted red for deadlock cycles 
• Nodes represent Processes and Resources with hoverable tooltips 
showing detailed info. 
3. Deadlock Detection 
• Implements cycle detection using Depth-First Search (DFS) to find 
circular waits in the RAG. 
• Visual indication of deadlock cycles in the graph. 
4. Deadlock Prevention 
• Integrates Banker's Algorithm to evaluate the system's safety state 
before allocation. 
• Outputs a safe sequence if one exists; otherwise, it flags an unsafe 
state. 
5. Deadlock Recovery 
• Simulates deadlock recovery by terminating one process from the 
detected cycle. 
• Frees its allocated resources and updates the system state 
accordingly. 
6. User Interaction & Status Updates 
• Real-time logging of actions and system status. 
• Input fields for setting demands, allocations, and requests in a user
friendly format. 
1. Module-Wise Breakdown: 
1. Input Module: 
Handles all user inputs including the number of processes and resources, 
as well as custom configurations like maximum demand, current 
allocation, and resource requests. This module ensures that the inputs are 
valid and interprets them into the internal data structures used by the 
system. 
2. Visualization Module: 
Utilizes D3.js to create and update the Resource Allocation Graph (RAG). It 
visually represents processes and resources as nodes, and uses color
coded edges to show allocations, requests, and deadlock cycles, providing 
a clear graphical understanding of the system state. 
3. Simulation Core Module: 
Manages the main data structures such as allocation matrices, need 
matrices, and available resources. It updates the system state based on 
user interactions and coordinates with other modules to reflect changes in 
the visualization and logic. 
4. Banker’s Algorithm Module: 
Implements the Banker's Algorithm to evaluate the safety of the system 
state. It checks whether the system can avoid a deadlock by finding a safe 
execution sequence for the processes, and reports either a safe sequence 
or an unsafe condition. 
5. Deadlock Detection Module: 
Detects deadlocks by applying Depth-First Search (DFS) on the Resource 
Allocation Graph to find cycles. If a cycle is found, it identifies the involved 
processes and resources, flags the deadlock, and marks the cycle in the 
graph. 
6. Deadlock Recovery Module: 
Handles deadlock resolution by selecting and terminating one of the 
processes involved in the deadlock. It releases the process's resources, 
updates the system state, and rechecks for deadlocks. 
7. Status and Logging Module: 
Maintains a live log of all operations, system changes, and errors. It 
provides timestamped updates to keep users informed of the current 
system status, making the simulation informative and traceable. 
3. Functionalities: 
1. Initialize Simulation: 
Allows users to set the number of processes and resources (within limits) 
and initializes all required data structures like allocation matrices, 
available resources, and demand vectors for a fresh simulation. 
2. Set Maximum Demand: 
Enables users to input the maximum demand of each process for different 
resources. This data is essential for calculating the need matrix and for 
running the Banker's Algorithm accurately. 
3. Allocate and Request Resources: 
Supports the allocation of resources to processes and the simulation of 
resource requests. Allocation updates the system’s state immediately, 
while requests help simulate potential deadlock conditions. 
4. Run Banker's Algorithm: 
Executes the Banker's Algorithm to determine if the current state of 
resource allocation is safe. If safe, a valid sequence of process execution 
is displayed; if not, an unsafe state is flagged. 
5. Check for Deadlock: 
Analyzes the Resource Allocation Graph using DFS to detect circular waits 
that indicate deadlocks. If detected, the deadlock cycle is visually 
highlighted in red on the graph. 
6. Deadlock Recovery: 
Simulates deadlock resolution by terminating a process involved in the 
deadlock cycle, thereby releasing its resources and restoring system 
functionality. 
7. Real-Time Visualization: 
Displays the Resource Allocation Graph dynamically using D3.js, with 
interactive and draggable nodes, and visual differentiation between 
allocation, request, and deadlock edges. 
8. System State Display: 
Shows real-time system parameters including available resources, current 
allocations, and resource needs for each process. Updates are logged for 
each action taken. 
9. Clear All Functionality: 
Provides a reset option to clear all configurations, inputs, and simulation 
data, allowing users to restart with a fresh setup. 
4. Technologies used:  
• Programming Languages: 
The project is built using HTML, CSS, and JavaScript. HTML provides the 
structure of the webpage, CSS (with Tailwind CSS) is used for styling and 
layout, while JavaScript handles the simulation logic, algorithm 
implementation, and dynamic interactivity. 
• Libraries and Tools: 
• D3.js: Used for creating and managing the Resource Allocation 
Graph (RAG) visualization, including nodes, edges, and interactive 
elements. 
• Tailwind CSS: A utility-first CSS framework used for designing a 
responsive and modern user interface. 
• Web APIs (DOM manipulation, event handling): Utilized within 
JavaScript to interact with input fields, buttons, and display elements 
dynamically. 
5. Flow diagram: 
6. Revision Tracking on GitHub: 
Repository Name:  Deadlock Prevention and Recovery Toolkit
Repository Link: https://github.com/ravi-raj2327/Deadlock-Prevention-and-Recovery-Toolkit-
Deployed Link:- https://aditya1787.github.io/Deadlock-prevention-and-recovery-/
7. Conclusion and Future Scope: 
The Deadlock Prevention and Recovery Toolkit successfully demonstrates 
key operating system concepts by providing an interactive environment to 
simulate, detect, prevent, and recover from deadlocks. By integrating 
visualization, Banker's Algorithm, and graph-based detection methods, it 
makes complex concepts more intuitive and accessible for students, 
educators, and developers. The modular design ensures that each 
component can function independently while contributing to the overall 
simulation experience. 
In the future, this toolkit can be extended with advanced features such as 
support for file-based input/output, integration of additional algorithms 
like Wait-Die and Wound-Wait, and visual analytics to track historical 
system states. Incorporating real-time collaboration and cloud-based 
deployment can also make it a powerful educational tool for classroom 
and remote learning environments. Moreover, support for saving and 
loading simulation states would allow for deeper analysis and 
experimentation. 
8. References Appendix: 
A: AI-Generated Project Elaboration/Breakdown Report 
1. Introduction 
Overview: A brief description of the project, its purpose, and its 
scope. 
Objectives: What the AI-generated solution aims to achieve. 
Challenges Addressed: Identify the key problems the project seeks 
to solve. 
2. Project Breakdown 
Phase 1: Research & Planning 
Literature review on similar AI solutions. 
Analysis of potential AI models to be used. 
Feasibility study. 
Phase 2: Data Collection & Preprocessing 
Sources of data for training the AI model. 
Steps involved in data cleaning and preprocessing. 
Tools and technologies used (e.g., Python libraries, data sources). 
Phase 3: Model Selection & Training 
Explanation of the AI models chosen (e.g., neural networks, decision 
trees, etc.). 
Model training details: architecture, data used, hyperparameters. 
Performance metrics and evaluation. 
Phase 4: Deployment & Integration 
Integrating the AI model into the final product or system. 
Deployment considerations (e.g., cloud services, hardware 
requirements). 
Phase 5: Testing & Optimization 
Test cases for validating AI functionality. 
Methods for optimizing model performance and reducing errors. 
3. Technologies & Tools Used 
AI Models: List of algorithms (e.g., CNN, RNN, etc.). 
Programming Languages: Python, Dart, etc. 
Libraries/Frameworks: TensorFlow, PyTorch, Scikit-learn, etc. 
Deployment Tools: Docker, Kubernetes, etc.6. Conclusion 
Summary of the AI-generated project. 
Future work and improvements. 
Potential for real-world impact and scalability. 
B. Problem Statement: 
Deadlock Prevention and Recovery Toolkit Description: Create a toolkit 
that detects, prevents, and recovers from deadlocks in real time. The 
system should implement algorithms like Banker's Algorithm and display 
resource allocation graphs for clarity. Include a feature for simulating 
deadlock scenarios with custom user inputs. 
C. Solution/Code: 
<!DOCTYPE html> 
<html lang="en"> 
<head> 
<meta charset="UTF-8"> 
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
<title>Deadlock Toolkit</title> 
<script src="https://d3js.org/d3.v7.min.js"></script> 
<script src="https://cdn.tailwindcss.com"></script> 
<style> 
body { font-family: 'Inter', sans-serif; } 
.node.process circle { fill: #4b5563; } 
.node.resource circle { fill: #6b7280; } 
.node text { fill: white; font-size: 12px; } 
.link.allocation { stroke: #374151; stroke-width: 2px; } 
.link.request { stroke: #6b7280; stroke-width: 2px; stroke-dasharray: 5,5; } 
.link.deadlock { stroke: #dc2626; stroke-width: 3px; } 
.link-label { font-size: 10px; fill: #374151; } 
.arrow { fill: #374151; } 
.arrow.request { fill: #6b7280; } 
.arrow.deadlock { fill: #dc2626; } 
</style> 
</head> 
<body class="bg-gray-100 min-h-screen p-6"> 
<div class="container max-w-7xl mx-auto bg-white rounded-xl shadow-md p-6 ring-1 
ring-gray-200 hover:ring-gray-300 transition-all duration-300"> 
<h1 class="text-3xl font-extrabold text-gray-800 mb-8 text-center tracking
tight">Deadlock Toolkit</h1> 
<div class="grid grid-cols-1 lg:grid-cols-3 gap-6"> 
<div class="col-span-1"> 
<div class="bg-gray-50 p-6 rounded-lg border border-gray-200 hover:shadow
md transition-shadow duration-200"> 
<h2 class="text-xl font-semibold text-gray-700 mb-4">Controls</h2> 
<div class="space-y-4"> 
<div class="flex gap-4"> 
<input type="number" id="numProcesses" min="1" max="6" value="4" 
placeholder="Processes" class="w-full p-3 border border-gray-300 rounded-md 
focus:ring-2 focus:ring-gray-400 focus:border-gray-400 transition-colors duration-200 
placeholder-gray-500"> 
<input type="number" id="numResources" min="1" max="4" value="3" 
placeholder="Resources" class="w-full p-3 border border-gray-300 rounded-md 
focus:ring-2 focus:ring-gray-400 focus:border-gray-400 transition-colors duration-200 
placeholder-gray-500"> 
</div> 
<div class="grid grid-cols-2 gap-4"> 
<button onclick="initializeSimulation()" class="bg-gray-600 text-white p-3 
rounded-md hover:bg-gray-700 active:scale-95 transition-all duration
200">Initialize</button> 
<button onclick="clearAll()" class="bg-gray-600 text-white p-3 rounded
md hover:bg-gray-700 active:scale-95 transition-all duration-200">Clear All</button> 
</div> 
<input type="text" id="maxDemand" placeholder="Max Demand (e.g., 
P1:R1=3,R2=2)" class="w-full p-3 border border-gray-300 rounded-md focus:ring-2 
focus:ring-gray-400 focus:border-gray-400 transition-colors duration-200 placeholder
gray-500"> 
<input type="text" id="allocation" placeholder="Allocation (e.g., P1->R1:1)" 
class="w-full p-3 border border-gray-300 rounded-md focus:ring-2 focus:ring-gray-400 
focus:border-gray-400 transition-colors duration-200 placeholder-gray-500"> 
<input type="text" id="request" placeholder="Request (e.g., P1->R1:1)" 
class="w-full p-3 border border-gray-300 rounded-md focus:ring-2 focus:ring-gray-400 
focus:border-gray-400 transition-colors duration-200 placeholder-gray-500"> 
<div class="grid grid-cols-3 gap-4"> 
<button onclick="setMaxDemand()" class="bg-gray-600 text-white p-3 
rounded-md hover:bg-gray-700 active:scale-95 transition-all duration-200">Set 
Demand</button> 
<button onclick="manageEdge('allocation')" class="bg-gray-600 text
white p-3 rounded-md hover:bg-gray-700 active:scale-95 transition-all duration
200">Allocate</button> 
<button onclick="manageEdge('request')" class="bg-gray-600 text-white 
p-3 rounded-md hover:bg-gray-700 active:scale-95 transition-all duration
200">Request</button> 
</div> 
<div class="grid grid-cols-2 gap-4"> 
<button onclick="runBankersAlgorithm()" class="bg-gray-600 text-white p
3 rounded-md hover:bg-gray-700 active:scale-95 transition-all duration
200">Banker's</button> 
<button onclick="checkDeadlock()" class="bg-gray-600 text-white p-3 
rounded-md hover:bg-gray-700 active:scale-95 transition-all duration-200">Check 
Deadlock</button> 
</div> 
<button onclick="recoverDeadlock()" class="bg-gray-600 text-white p-3 
rounded-md hover:bg-gray-700 active:scale-95 transition-all duration-200">Recover 
Deadlock</button> 
</div> 
</div> 
</div> 
<div class="col-span-2 space-y-6"> 
<div class="bg-gray-50 p-6 rounded-lg border border-gray-200 hover:shadow
md transition-shadow duration-200"> 
<h2 class="text-xl font-semibold text-gray-700 mb-4">Resource Allocation 
Graph</h2> 
<svg id="rag" class="w-full h-[400px] rounded-md border border-gray-200 bg
gray-50"></svg> 
</div> 
<div class="bg-gray-50 p-6 rounded-lg border border-gray-200 hover:shadow
md transition-shadow duration-200"> 
<h2 class="text-xl font-semibold text-gray-700 mb-4">System Status</h2> 
<div id="status" class="text-sm text-gray-600 h-[200px] overflow-y-auto 
scroll-py-2"></div> 
</div> 
</div> 
</div> 
</div> 
<script> 
let processes = [], resources = [], edges = [], available = [], maxDemand = {}, 
allocation = {}, need = {}; 
let deadlockDetected = false, deadlockCycle = []; 
function initializeSimulation() { 
try { 
const numProcesses = 
parseInt(document.getElementById('numProcesses').value); 
const numResources = 
parseInt(document.getElementById('numResources').value); 
if (!numProcesses || !numResources || numProcesses > 6 || numResources > 4) { 
updateStatus('Error: Processes (1-6), Resources (1-4) required.'); 
return; 
} 
processes = Array.from({ length: numProcesses }, (_, i) => ({ id: `P${i + 1}`, type: 
'process' })); 
resources = Array.from({ length: numResources }, (_, i) => ({ id: `R${i + 1}`, type: 
'resource' })); 
edges = []; 
available = Array(numResources).fill(10); 
maxDemand = {}; 
allocation = {}; 
need = {}; 
deadlockDetected = false; 
deadlockCycle = []; 
processes.forEach(p => { 
maxDemand[p.id] = Array(numResources).fill(0); 
allocation[p.id] = Array(numResources).fill(0); 
need[p.id] = Array(numResources).fill(0); 
}); 
updateStatus(`Initialized: ${numProcesses} processes, ${numResources} 
resources.`); 
updateGraph(); 
clearInputs(); 
} catch (e) { 
updateStatus('Error: Initialization failed.'); 
} 
} 
function clearAll() { 
processes = []; 
resources = []; 
edges = []; 
available = []; 
maxDemand = {}; 
allocation = {}; 
need = {}; 
deadlockDetected = false; 
deadlockCycle = []; 
clearInputs(); 
updateStatus('Simulation cleared.'); 
updateGraph(); 
} 
function clearInputs() { 
document.getElementById('maxDemand').value = ''; 
document.getElementById('allocation').value = ''; 
document.getElementById('request').value = ''; 
} 
function setMaxDemand() { 
try { 
const input = document.getElementById('maxDemand').value.trim(); 
const regex = /(P\d+):((?:R\d+=\d+,?)+)/g; 
let valid = true; 
for (const match of input.matchAll(regex)) { 
const process = match[1]; 
const demands = match[2].split(',').filter(d => d); 
if (!processes.find(p => p.id === process)) { 
updateStatus(`Error: Invalid process ${process}.`); 
valid = false; 
continue; 
} 
demands.forEach(d => { 
const [resource, units] = d.split('='); 
const resourceIdx = resources.findIndex(r => r.id === resource); 
if (resourceIdx === -1 || parseInt(units) > 10 || parseInt(units) < 0) { 
updateStatus(`Error: Invalid demand ${resource}=${units}.`); 
valid = false; 
} else { 
maxDemand[process][resourceIdx] = parseInt(units); 
need[process][resourceIdx] = maxDemand[process][resourceIdx] - 
allocation[process][resourceIdx]; 
updateStatus(`Set demand: ${process} -> ${resource}=${units}`); 
} 
}); 
} 
if (valid) { 
updateGraph(); 
showSystemState(); 
} 
} catch (e) { 
updateStatus('Error: Failed to set demand.'); 
} 
} 
function manageEdge(type) { 
try { 
const input = document.getElementById(type).value.trim(); 
const regex = /(P\d+)->(R\d+):(\d+)/g; 
let valid = true; 
for (const match of input.matchAll(regex)) { 
const process = match[1], resource = match[2], units = parseInt(match[3]); 
const resourceIdx = resources.findIndex(r => r.id === resource); 
const processIdx = processes.findIndex(p => p.id === process); 
if (processIdx === -1 || resourceIdx === -1 || units <= 0) { 
updateStatus(`Error: Invalid ${type} ${process}->${resource}:${units}.`); 
valid = false; 
continue; 
} 
if (units + allocation[process][resourceIdx] > 
maxDemand[process][resourceIdx]) { 
updateStatus(`Error: ${type} exceeds max demand for ${process} on 
${resource}.`); 
valid = false; 
continue; 
} 
if (type === 'allocation' && units > available[resourceIdx]) { 
updateStatus(`Error: Only ${available[resourceIdx]} units available for 
${resource}.`); 
valid = false; 
continue; 
} 
edges.push({ 
source: type === 'allocation' ? process : resource, 
target: type === 'allocation' ? resource : process, 
units, 
type 
}); 
if (type === 'allocation') { 
allocation[process][resourceIdx] += units; 
need[process][resourceIdx] = maxDemand[process][resourceIdx] - 
allocation[process][resourceIdx]; 
available[resourceIdx] -= units; 
} 
updateStatus(`${type === 'allocation' ? 'Allocated' : 'Requested'}: ${process} 
> ${resource} (${units} units)`); 
} 
if (valid) { 
updateGraph(); 
showSystemState(); 
} 
} catch (e) { 
updateStatus(`Error: Failed to add ${type}.`); 
} 
} 
function runBankersAlgorithm() { 
try { 
if (!Object.keys(maxDemand).length) { 
updateStatus('Error: Set max demand first.'); 
return; 
} 
const work = [...available]; 
const finish = Array(processes.length).fill(false); 
const safeSequence = []; 
while (safeSequence.length < processes.length) { 
let found = false; 
for (let i = 0; i < processes.length; i++) { 
if (!finish[i] && need[processes[i].id].every((n, j) => n <= work[j])) { 
work.forEach((w, j) => work[j] += allocation[processes[i].id][j]); 
finish[i] = true; 
safeSequence.push(processes[i].id); 
found = true; 
} 
} 
if (!found) { 
updateStatus('Unsafe state detected!'); 
return; 
} 
} 
updateStatus(`Safe state! Sequence: ${safeSequence.join(' -> ')}`); 
} catch (e) { 
updateStatus('Error: Failed to run Banker’s algorithm.'); 
} 
} 
function checkDeadlock() { 
try { 
const graph = {}; 
processes.forEach(p => graph[p.id] = new Set()); 
resources.forEach(r => graph[r.id] = new Set()); 
edges.forEach(e => graph[e.source].add(e.target)); 
const visited = new Set(), recStack = new Set(); 
deadlockDetected = false; 
deadlockCycle = []; 
function dfs(node, parent, path) { 
visited.add(node); 
recStack.add(node); 
path.push(node); 
for (const neighbor of graph[node]) { 
if (neighbor !== parent && !visited.has(neighbor)) { 
if (dfs(neighbor, node, [...path])) return true; 
} else if (neighbor !== parent && recStack.has(neighbor)) { 
const cycleStart = path.indexOf(neighbor); 
if (cycleStart !== -1) { 
deadlockCycle = path.slice(cycleStart); 
deadlockCycle.push(neighbor); 
return true; 
} 
} 
} 
recStack.delete(node); 
path.pop(); 
return false; 
} 
for (const node of processes.map(p => p.id)) { 
if (!visited.has(node) && dfs(node, null, [])) { 
deadlockDetected = true; 
break; 
} 
} 
updateStatus(deadlockDetected ? `Deadlock detected! Cycle: 
${deadlockCycle.join(' -> ')}` : 'No deadlock detected.'); 
updateGraph(); 
} catch (e) { 
updateStatus('Error: Failed to check deadlock.'); 
} 
} 
function recoverDeadlock() { 
try { 
if (!deadlockDetected) { 
updateStatus('No deadlock to recover.'); 
return; 
} 
const processToTerminate = processes.find(p => allocation[p.id].some(a => a > 
0) && deadlockCycle.includes(p.id))?.id; 
if (!processToTerminate) { 
updateStatus('No process to terminate.'); 
return; 
} 
edges = edges.filter(e => e.source !== processToTerminate && e.target !== 
processToTerminate); 
const resourceIdxs = allocation[processToTerminate].map((a, i) => a > 0 ? i : 
1).filter(i => i !== -1); 
resourceIdxs.forEach(i => { 
available[i] += allocation[processToTerminate][i]; 
allocation[processToTerminate][i] = 0; 
need[processToTerminate][i] = maxDemand[processToTerminate][i]; 
}); 
updateStatus(`Recovered by terminating ${processToTerminate}.`); 
deadlockDetected = false; 
deadlockCycle = []; 
updateGraph(); 
checkDeadlock(); 
} catch (e) { 
updateStatus('Error: Failed to recover deadlock.'); 
} 
} 
function showSystemState() { 
let state = `System State:\nAvailable: ${available.map((a, i) => `R${i + 
1}=${a}`).join(', ')}\n`; 
processes.forEach(p => { 
state += `${p.id}: Alloc=[${allocation[p.id].join(',')}], 
Need=[${need[p.id].join(',')}]\n`; 
}); 
updateStatus(state); 
} 
function updateStatus(message) { 
const statusDiv = document.getElementById('status'); 
const p = document.createElement('p'); 
p.textContent = `[${new Date().toLocaleTimeString()}] ${message}`; 
statusDiv.appendChild(p); 
statusDiv.scrollTop = statusDiv.scrollHeight; 
} 
function updateGraph() { 
try { 
const svg = d3.select('#rag'); 
svg.selectAll('*').remove(); 
const width = svg.node().getBoundingClientRect().width, height = 400; 
svg.append('defs').selectAll('marker') 
.data(['allocation', 'request', 'deadlock']) 
.enter().append('marker') 
.attr('id', d => `arrow-${d}`) 
.attr('viewBox', '0 -5 10 10') 
.attr('refX', 25) 
.attr('refY', 0) 
.attr('markerWidth', 8) 
.attr('markerHeight', 8) 
.attr('orient', 'auto') 
.append('path') 
.attr('d', 'M0,-5L10,0L0,5') 
.attr('class', d => `arrow ${d}`); 
const nodes = [...processes, ...resources]; 
const links = edges.map(e => ({ 
source: e.source, 
target: e.target, 
units: e.units, 
type: deadlockCycle.length > 0 && isEdgeInCycle(e) ? 'deadlock' : e.type 
})); 
nodes.forEach((node, i) => { 
node.x = width * 0.2 + (i % 3) * width * 0.3; 
node.y = height * 0.2 + Math.floor(i / 3) * height * 0.3; 
}); 
const simulation = d3.forceSimulation(nodes) 
.force('link', d3.forceLink(links).id(d => d.id).distance(100)) 
.force('charge', d3.forceManyBody().strength(-600)) 
.force('center', d3.forceCenter(width / 2, height / 2)) 
.force('collision', d3.forceCollide().radius(40)); 
const link = svg.append('g') 
.selectAll('line') 
.data(links) 
.enter().append('line') 
.attr('class', d => `link ${d.type}`) 
.attr('marker-end', d => `url(#arrow-${d.type})`); 
const linkLabel = svg.append('g') 
.selectAll('text') 
.data(links) 
.enter().append('text') 
.attr('class', 'link-label') 
.text(d => d.units) 
.attr('dy', -5); 
const node = svg.append('g') 
.selectAll('.node') 
.data(nodes) 
.enter().append('g') 
.attr('class', 'node') 
.call(d3.drag() 
.on('start', d => { if (!d.active) simulation.alphaTarget(0.3).restart(); 
d.subject.fx = d.subject.x; d.subject.fy = d.subject.y; }) 
.on('drag', d => { d.subject.fx = d.x; d.subject.fy = d.y; }) 
.on('end', d => { if (!d.active) simulation.alphaTarget(0); d.subject.fx = null; 
d.subject.fy = null; })); 
node.append('circle').attr('r', 20).attr('class', d => d.type); 
node.append('text').attr('dy', '.35em').attr('text-anchor', 'middle').text(d => d.id); 
node.append('title').text(d => d.type === 'process' 
? `Process ${d.id}\nAlloc: ${allocation[d.id]?.join(',') || 'None'}\nNeed: 
${need[d.id]?.join(',') || 'None'}` 
: `Resource ${d.id}\nAvailable: ${available[resources.findIndex(r => r.id === 
d.id)] || 0}`); 
link.append('title').text(d => `${d.source.id} ${d.type === 'allocation' ? '->' : '<-'} 
${d.target.id}: ${d.units} units (${d.type})`); 
simulation.on('tick', () => { 
link 
.attr('x1', d => Math.max(20, Math.min(width - 20, d.source.x))) 
.attr('y1', d => Math.max(20, Math.min(height - 20, d.source.y))) 
.attr('x2', d => Math.max(20, Math.min(width - 20, d.target.x))) 
.attr('y2', d => Math.max(20, Math.min(height - 20, d.target.y))); 
linkLabel 
.attr('x', d => Math.max(20, Math.min(width - 20, (d.source.x + d.target.x) / 
2))) 
.attr('y', d => Math.max(20, Math.min(height - 20, (d.source.y + d.target.y) / 
2))); 
1]) || 
node 
.attr('transform', d => { 
d.x = Math.max(20, Math.min(width - 20, d.x)); 
d.y = Math.max(20, Math.min(height - 20, d.y)); 
return `translate(${d.x},${d.y})`; 
}); 
}); 
function isEdgeInCycle(edge) { 
for (let i = 0; i < deadlockCycle.length - 1; i++) { 
if ((edge.source === deadlockCycle[i] && edge.target === deadlockCycle[i + 
(edge.source === deadlockCycle[i + 1] && edge.target === 
deadlockCycle[i])) { 
return true; 
} 
} 
return false; 
} 
} catch (e) { 
updateStatus('Error: Failed to update graph.'); 
} 
} 
if (typeof d3 === 'undefined') { 
updateStatus('Error: D3.js not loaded.'); 
} else { 
initializeSimulation(); 
} 
</script> 
</body> 
</html> 
