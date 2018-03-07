# Transactor

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
[![Gitter](https://badges.gitter.im/metacurrency/holochain.svg)](https://gitter.im/metacurrency/holochain?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=body_badge)

**Asset backed mutual-credit currency built on holochain**
Prototype of mutual-credit currency with reserve accounts and pre-authorization.
## Sequence Diagram

<svg id="mermaidChart382" width="100%" xmlns="http://www.w3.org/2000/svg" height="100%" style="max-width:758.703125px;" viewBox="-91.546875 -10 758.703125 836"><style>
  .mermaid .label{color:#333}.node circle,.node ellipse,.node polygon,.node rect{fill:#ececff;stroke:#ccf;stroke-width:1px}.node.clickable{cursor:pointer}.arrowheadPath{fill:#333}.edgePath .path{stroke:#333}.edgeLabel{background-color:#e8e8e8}.cluster rect{fill:#ffffde!important;rx:4!important;stroke:#aa3!important;stroke-width:1px!important}.cluster text{fill:#333}.actor{stroke:#ccf;fill:#ececff}text.actor{fill:#000;stroke:none}.actor-line{stroke:grey}.messageLine0{marker-end:"url(#arrowhead)"}.messageLine0,.messageLine1{stroke-width:1.5;stroke-dasharray:"2 2";stroke:#333}#arrowhead{fill:#333}#crosshead path{fill:#333!important;stroke:#333!important}.messageText{fill:#333;stroke:none}.labelBox{stroke:#ccf;fill:#ececff}.labelText,.loopText{fill:#000;stroke:none}.loopLine{stroke-width:2;stroke-dasharray:"2 2";marker-end:"url(#arrowhead)";stroke:#ccf}.note{stroke:#aa3;fill:#fff5ad}.noteText{fill:#000;stroke:none;font-family:trebuchet ms,verdana,arial;font-size:14px}.section{stroke:none;opacity:.2}.section0{fill:rgba(102,102,255,.49)}.section2{fill:#fff400}.section1,.section3{fill:#fff;opacity:.2}.sectionTitle0,.sectionTitle1,.sectionTitle2,.sectionTitle3{fill:#333}.sectionTitle{text-anchor:start;font-size:11px;text-height:14px}.grid .tick{stroke:#d3d3d3;opacity:.3;shape-rendering:crispEdges}.grid path{stroke-width:0}.today{fill:none;stroke:red;stroke-width:2px}.task{stroke-width:2}.taskText{text-anchor:middle;font-size:11px}.taskTextOutsideRight{fill:#000;text-anchor:start;font-size:11px}.taskTextOutsideLeft{fill:#000;text-anchor:end;font-size:11px}.taskText0,.taskText1,.taskText2,.taskText3{fill:#fff}.task0,.task1,.task2,.task3{fill:#8a90dd;stroke:#534fbc}.taskTextOutside0,.taskTextOutside1,.taskTextOutside2,.taskTextOutside3{fill:#000}.active0,.active1,.active2,.active3{fill:#bfc7ff;stroke:#534fbc}.activeText0,.activeText1,.activeText2,.activeText3{fill:#000!important}.done0,.done1,.done2,.done3{stroke:grey;fill:#d3d3d3;stroke-width:2}.doneText0,.doneText1,.doneText2,.doneText3{fill:#000!important}.crit0,.crit1,.crit2,.crit3{stroke:#f88;fill:red;stroke-width:2}.activeCrit0,.activeCrit1,.activeCrit2,.activeCrit3{stroke:#f88;fill:#bfc7ff;stroke-width:2}.doneCrit0,.doneCrit1,.doneCrit2,.doneCrit3{stroke:#f88;fill:#d3d3d3;stroke-width:2;cursor:pointer;shape-rendering:crispEdges}.activeCritText0,.activeCritText1,.activeCritText2,.activeCritText3,.doneCritText0,.doneCritText1,.doneCritText2,.doneCritText3{fill:#000!important}.titleText{text-anchor:middle;font-size:18px;fill:#000}g.classGroup text{fill:#9370db;stroke:none;font-family:trebuchet ms,verdana,arial;font-size:10px}g.classGroup rect{fill:#ececff;stroke:#9370db}g.classGroup line{stroke:#9370db;stroke-width:1}svg .classLabel .box{stroke:none;stroke-width:0;fill:#ececff;opacity:.5}svg .classLabel .label{fill:#9370db;font-size:10px}.relation{stroke:#9370db;stroke-width:1;fill:none}#compositionEnd,#compositionStart,.composition{fill:#9370db;stroke:#9370db;stroke-width:1}#aggregationEnd,#aggregationStart,.aggregation{fill:#ececff;stroke:#9370db;stroke-width:1}#dependencyEnd,#dependencyStart,#extensionEnd,#extensionStart{fill:#9370db;stroke:#9370db;stroke-width:1}.node text{font-size:14px}.node text,div.mermaidTooltip{font-family:trebuchet ms,verdana,arial}div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-size:12px;background:#ffffde;border:1px solid #aa3;border-radius:2px;pointer-events:none;z-index:100}
svg {
  color: rgb(51, 51, 51);
  font: normal normal 400 normal 13.6px / 19.72px Menlo, Monaco, Consolas, "Courier New", monospace;
}
  </style><g></g><g><line id="actor1125" x1="75" y1="5" x2="75" y2="825" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="0" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="75" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="75" dy="0">Spender</tspan></text></g><g><line id="actor1126" x1="275" y1="5" x2="275" y2="825" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="200" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="275" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="275" dy="0">DHT</tspan></text></g><g><line id="actor1127" x1="475" y1="5" x2="475" y2="825" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="400" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="475" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="475" dy="0">Receiver</tspan></text></g><defs><marker id="arrowhead" refX="5" refY="2" markerWidth="6" markerHeight="4" orient="auto"><path d="M 0,0 V 4 L6,2 Z"></path></marker></defs><defs><marker id="crosshead" markerWidth="15" markerHeight="8" orient="auto" refX="16" refY="4"><path fill="black" stroke="#000000" stroke-width="1px" d="M 9,2 V 6 L16,4 Z" style="stroke-dasharray: 0, 0;"></path><path fill="none" stroke="#000000" stroke-width="1px" d="M 0,1 L 6,7 M 6,1 L 0,7" style="stroke-dasharray: 0, 0;"></path></marker></defs><g><text x="475" y="93" class="messageText" style="text-anchor: middle;">commit('preauthInvoice', params)</text><path d="M 475,100 C 535,90 535,130 475,120" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></path></g><g><text x="375" y="158" class="messageText" style="text-anchor: middle;">commit(link on Spender to invoice)</text><line x1="475" y1="165" x2="275" y2="165" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></line></g><g><text x="375" y="193" class="messageText" style="text-anchor: middle;">hash of committed link</text><line x1="275" y1="200" x2="475" y2="200" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></line></g><g><text x="175" y="228" class="messageText" style="text-anchor: middle;">getLinks(me, 'invoice')</text><line x1="75" y1="235" x2="275" y2="235" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="175" y="263" class="messageText" style="text-anchor: middle;">invoices</text><line x1="275" y1="270" x2="75" y2="270" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="75" y="323" class="messageText" style="text-anchor: middle;">createTransaction(params)</text><path d="M 75,330 C 135,320 135,360 75,350" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></path></g><g><text x="275" y="388" class="messageText" style="text-anchor: middle;">Send(PotentialTX)</text><line x1="75" y1="395" x2="475" y2="395" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="475" y="423" class="messageText" style="text-anchor: middle;">CompleteTX by adding HeaderHash</text><path d="M 475,430 C 535,420 535,460 475,450" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></path></g><g><text x="275" y="488" class="messageText" style="text-anchor: middle;">Complete-TX-Approval-Response</text><line x1="475" y1="495" x2="75" y2="495" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="75" y="523" class="messageText" style="text-anchor: middle;">commit(tx)</text><path d="M 75,530 C 135,520 135,560 75,550" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></path></g><g><text x="275" y="588" class="messageText" style="text-anchor: middle;">signed header</text><line x1="75" y1="595" x2="475" y2="595" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="475" y="623" class="messageText" style="text-anchor: middle;">commit(tx)</text><path d="M 475,630 C 535,620 535,660 475,650" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></path></g><g><text x="175" y="688" class="messageText" style="text-anchor: middle;">TX &amp; headers</text><line x1="75" y1="695" x2="275" y2="695" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></line></g><g><text x="375" y="723" class="messageText" style="text-anchor: middle;">TX &amp; headers</text><line x1="475" y1="730" x2="275" y2="730" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></line></g><g><line x1="-41.546875" y1="280" x2="617.15625" y2="280" class="loopLine"></line><line x1="617.15625" y1="280" x2="617.15625" y2="740" class="loopLine"></line><line x1="-41.546875" y1="740" x2="617.15625" y2="740" class="loopLine"></line><line x1="-41.546875" y1="280" x2="-41.546875" y2="740" class="loopLine"></line><polygon points="-41.546875,280 8.453125,280 8.453125,293 0.053124999999999645,300 -41.546875,300" class="labelBox"></polygon><text x="-34.046875" y="295" fill="black" class="labelText"><tspan x="-34.046875" fill="black">loop</tspan></text><text x="287.8046875" y="295" fill="black" class="loopText" style="text-anchor: middle;"><tspan x="287.8046875" fill="black">[ Pay Invoices ]</tspan></text></g><g><rect x="0" y="760" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="75" y="792.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="75" dy="0">Spender</tspan></text></g><g><rect x="200" y="760" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="275" y="792.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="275" dy="0">DHT</tspan></text></g><g><rect x="400" y="760" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="475" y="792.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="475" dy="0">Receiver</tspan></text></g></svg>
  
## Installation

Prerequisite: [Install holochain](https://github.com/metacurrency/holochain/#installation) on your machine.
You can install transactor very simply with this:

``` shell
hcdev init -cloneExample=transactor

```

## Usage

To do a test run of transactor simply type

``` shell
cd transactor
hcdev web
```
you should see something like:

``` shell
Copying chain to: /home/bootstrap/.holochaindev
...
Serving holochain with DNA hash:QmZYxoxcqgCp6Xf6xVe8ptzPkmH8QMzxqp4r49QYpS2fEF on port:4141
```
Then simply point your browser to http://localhost:4141 access the UI.

### Tests
To run all the stand alone tests:

``` shell
hcdev test
```

## Contribute
We welcome pull requests and issue tickets.  Find us on [gitter](https://gitter.im/metacurrency/holochain) to chat.

Contributors to this project are expected to follow our [development protocols & practices](https://github.com/metacurrency/holochain/wiki/Development-Protocols).


## License
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)

Copyright (C) 2017, The MetaCurrency Project (Eric Harris-Braun, Arthur Brock, et. al.)

This program is free software: you can redistribute it and/or modify it under the terms of the license provided in the LICENSE file (GPLv3).  This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

**Note:** We are considering other 'looser' licensing options (like MIT license) but at this stage are using GPL while we're getting the matter sorted out.
