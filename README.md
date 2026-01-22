<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E.T.R. Workshop Bulandshahr - Structural & Financial Analysis</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f5f5f5;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
        }
        
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }
        
        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        header p {
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        .project-info {
            background: #f8f9fa;
            padding: 30px;
            border-left: 5px solid #2a5298;
            margin: 20px 0;
        }
        
        .project-info h2 {
            color: #1e3c72;
            margin-bottom: 15px;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }
        
        .info-item {
            background: white;
            padding: 15px;
            border-radius: 5px;
            border-left: 3px solid #2a5298;
        }
        
        .info-label {
            font-weight: bold;
            color: #555;
            font-size: 0.9em;
        }
        
        .info-value {
            font-size: 1.1em;
            color: #1e3c72;
            margin-top: 5px;
        }
        
        nav {
            background: #2a5298;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            border-radius: 5px;
            transition: background 0.3s;
        }
        
        nav a:hover {
            background: rgba(255,255,255,0.2);
        }
        
        .content {
            padding: 40px;
        }
        
        section {
            margin-bottom: 50px;
        }
        
        h2 {
            color: #1e3c72;
            font-size: 2em;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #2a5298;
        }
        
        h3 {
            color: #2a5298;
            font-size: 1.5em;
            margin: 25px 0 15px 0;
        }
        
        h4 {
            color: #444;
            font-size: 1.2em;
            margin: 20px 0 10px 0;
        }
        
        p {
            margin-bottom: 15px;
            text-align: justify;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        th {
            background: #2a5298;
            color: white;
            padding: 12px;
            text-align: left;
            font-weight: 600;
        }
        
        td {
            padding: 10px 12px;
            border-bottom: 1px solid #ddd;
        }
        
        tr:hover {
            background: #f8f9fa;
        }
        
        .highlight {
            background: #fff3cd;
            padding: 20px;
            border-left: 5px solid #ffc107;
            margin: 20px 0;
        }
        
        .warning {
            background: #f8d7da;
            padding: 20px;
            border-left: 5px solid #dc3545;
            margin: 20px 0;
        }
        
        .success {
            background: #d4edda;
            padding: 20px;
            border-left: 5px solid #28a745;
            margin: 20px 0;
        }
        
        .metric-box {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            margin: 10px 0;
        }
        
        .metric-value {
            font-size: 2.5em;
            font-weight: bold;
        }
        
        .metric-label {
            font-size: 1.1em;
            opacity: 0.9;
        }
        
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .card {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .status-badge {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: bold;
        }
        
        .status-critical {
            background: #dc3545;
            color: white;
        }
        
        .status-warning {
            background: #ffc107;
            color: #333;
        }
        
        .status-good {
            background: #28a745;
            color: white;
        }
        
        footer {
            background: #1e3c72;
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        @media print {
            nav {
                display: none;
            }
            
            .no-print {
                display: none;
            }
            
            section {
                page-break-inside: avoid;
            }
        }
        
        .edit-controls {
            background: #f8f9fa;
            padding: 15px;
            margin: 20px 0;
            border-radius: 5px;
            border: 1px solid #dee2e6;
        }
        
        .edit-controls h4 {
            margin: 0 0 10px 0;
            color: #495057;
            font-size: 1em;
        }
        
        .edit-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        .edit-btn {
            padding: 8px 16px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9em;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        
        .edit-btn-primary {
            background: #2a5298;
            color: white;
        }
        
        .edit-btn-primary:hover {
            background: #1e3c72;
        }
        
        .edit-btn-secondary {
            background: #6c757d;
            color: white;
        }
        
        .edit-btn-secondary:hover {
            background: #545b62;
        }
        
        .edit-btn-success {
            background: #28a745;
            color: white;
        }
        
        .edit-btn-success:hover {
            background: #218838;
        }
        
        .edit-btn-warning {
            background: #ffc107;
            color: #333;
        }
        
        .edit-btn-warning:hover {
            background: #e0a800;
        }
        
        .editable-section {
            position: relative;
            padding: 20px;
            border: 2px dashed transparent;
            transition: all 0.3s;
        }
        
        .editable-section:hover {
            border-color: #2a5298;
            background: #f8f9fa;
        }
        
        .section-actions {
            position: absolute;
            top: 10px;
            right: 10px;
            display: none;
        }
        
        .editable-section:hover .section-actions {
            display: flex;
            gap: 5px;
        }
        
        .action-icon {
            width: 30px;
            height: 30px;
            background: white;
            border: 1px solid #dee2e6;
            border-radius: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .action-icon:hover {
            background: #2a5298;
            color: white;
        }
        
        .editable-field {
            border: 1px solid #ced4da;
            padding: 8px;
            border-radius: 4px;
            width: 100%;
            font-family: inherit;
            font-size: inherit;
        }
        
        .editable-field:focus {
            outline: none;
            border-color: #2a5298;
            box-shadow: 0 0 0 3px rgba(42, 82, 152, 0.1);
        }
        
        textarea.editable-field {
            min-height: 100px;
            resize: vertical;
        }
        
        .edit-mode {
            background: #fff9e6;
            border: 2px solid #ffc107;
        }
        
        .save-indicator {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #28a745;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            display: none;
            z-index: 1000;
            animation: slideIn 0.3s;
        }
        
        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }
        
        .comment-section {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px;
            margin: 15px 0;
            display: none;
        }
        
        .comment-section.active {
            display: block;
        }
        
        .comment-input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ced4da;
            border-radius: 4px;
            margin-bottom: 10px;
        }
        
        .version-history {
            background: #e7f3ff;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
            display: none;
        }
        
        .version-item {
            padding: 8px;
            margin: 5px 0;
            background: white;
            border-radius: 3px;
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .content {
                padding: 20px;
            }
            
            header h1 {
                font-size: 1.8em;
            }
            
            table {
                font-size: 0.9em;
            }
            
            th, td {
                padding: 8px;
            }
            
            .edit-buttons {
                flex-direction: column;
            }
            
            .edit-btn {
                width: 100%;
            }
        }
        
        @media print {
            .edit-controls,
            .section-actions,
            .save-indicator,
            .comment-section,
            .version-history {
                display: none !important;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Save Indicator -->
        <div class="save-indicator" id="saveIndicator">✓ Changes Saved</div>
        
        <header>
            <h1>E.T.R. WORKSHOP BULANDSHAHR</h1>
            <p>Comprehensive Structural & Financial Analysis</p>
            <p style="font-size: 0.9em; margin-top: 10px;">Civil Engineering Report | January 2026</p>
        </header>
        
        <!-- Global Edit Controls -->
        <div class="edit-controls no-print">
            <h4>📝 Document Controls</h4>
            <div class="edit-buttons">
                <button class="edit-btn edit-btn-primary" onclick="enableGlobalEdit()">✏️ Enable Editing Mode</button>
                <button class="edit-btn edit-btn-success" onclick="saveAllChanges()">💾 Save All Changes</button>
                <button class="edit-btn edit-btn-secondary" onclick="exportToPDF()">📄 Export to PDF</button>
                <button class="edit-btn edit-btn-secondary" onclick="downloadHTML()">⬇️ Download HTML</button>
                <button class="edit-btn edit-btn-warning" onclick="toggleVersionHistory()">📜 Version History</button>
                <button class="edit-btn edit-btn-secondary" onclick="printDocument()">🖨️ Print</button>
            </div>
        </div>
        
        <!-- Version History -->
        <div class="version-history" id="versionHistory">
            <h4>Version History</h4>
            <div id="versionList">
                <div class="version-item">
                    <strong>Version 1.0</strong> - January 22, 2026 - Initial document creation
                </div>
            </div>
        </div>
        
        <div class="project-info">
            <h2>Project Information</h2>
            <div class="info-grid">
                <div class="info-item">
                    <div class="info-label">Project Name</div>
                    <div class="info-value">E.T.R. Workshop Bulandshahr</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Client</div>
                    <div class="info-value">PVVNL - Uttar Pradesh</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Contractor</div>
                    <div class="info-value">S R INFRACONSTRUCTION PVT LTD</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Contract Value</div>
                    <div class="info-value">₹1,31,15,816</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Discount Offered</div>
                    <div class="info-value">9.70%</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Project Duration</div>
                    <div class="info-value">24 Weeks</div>
                </div>
            </div>
        </div>
        
        <nav>
            <ul>
                <li><a href="#drawings">Drawing Analysis</a></li>
                <li><a href="#rcc">RCC Column Height</a></li>
                <li><a href="#composite">Composite Column</a></li>
                <li><a href="#rate-analysis">Rate Analysis</a></li>
                <li><a href="#materials">Material Consumption</a></li>
                <li><a href="#cashflow">Capital Flow</a></li>
                <li><a href="#recommendations">Recommendations</a></li>
            </ul>
        </nav>
        
        <div class="content">
            <!-- SECTION 1: INITIAL DRAWING ANALYSIS -->
            <section id="drawings" class="editable-section">
                <div class="section-actions no-print">
                    <div class="action-icon" onclick="editSection(this)" title="Edit Section">✏️</div>
                    <div class="action-icon" onclick="addComment(this)" title="Add Comment">💬</div>
                    <div class="action-icon" onclick="addNote(this)" title="Add Note">📝</div>
                </div>
                
                <h2>1. STRUCTURAL DRAWING ANALYSIS</h2>
                
                <div class="edit-controls no-print">
                    <h4>Section Controls</h4>
                    <div class="edit-buttons">
                        <button class="edit-btn edit-btn-primary" onclick="editText(this.closest('section'))">✏️ Edit Content</button>
                        <button class="edit-btn edit-btn-success" onclick="saveSection(this.closest('section'))">💾 Save Section</button>
                        <button class="edit-btn edit-btn-secondary" onclick="addTable(this.closest('section'))">➕ Add Table</button>
                        <button class="edit-btn edit-btn-warning" onclick="highlightSection(this.closest('section'))">🖍️ Highlight</button>
                    </div>
                </div>
                
                <div class="comment-section" id="comments-drawings">
                    <strong>Comments & Notes:</strong>
                    <textarea class="comment-input" placeholder="Add your comments here..."></textarea>
                    <button class="edit-btn edit-btn-success" onclick="saveComment('drawings')">Save Comment</button>
                </div>
                
                <h3>1.1 Building Configuration Overview</h3>
                <p>The E.T.R. Workshop in Bulandshahr represents a single-story industrial facility with a rectangular footprint measuring 10,500 millimeters by 8,600 millimeters. The structural system employs a systematic column grid arrangement with spacing of 4,300 millimeters between column lines in both directions, creating an efficient and economical framework for construction. This regularity is particularly advantageous for construction efficiency and cost control, as it allows for maximum reuse of formwork systems and standardization of structural elements.</p>
                
                <h3>1.2 Foundation System</h3>
                <p>The foundation design utilizes isolated square footings supporting the column grid at sixteen locations. According to the foundation schedule, Footing Type F1 has dimensions of 2,000 millimeters by 2,000 millimeters with a thickness of 600 millimeters and placement depth of 200 millimeters below the finished ground level. The foundations employ M20 grade concrete with reinforcement bars of 12 millimeter diameter arranged at 100 millimeter centers in both directions, providing adequate capacity for the anticipated soil bearing conditions typical of this region.</p>
                
                <div class="grid-2">
                    <div class="card">
                        <h4>Foundation Specifications</h4>
                        <table>
                            <tr><td>Type</td><td>F1 - Isolated Square Footing</td></tr>
                            <tr><td>Size</td><td>2000mm × 2000mm</td></tr>
                            <tr><td>Thickness</td><td>600mm</td></tr>
                            <tr><td>Depth Below GL</td><td>200mm</td></tr>
                            <tr><td>Concrete Grade</td><td>M20</td></tr>
                            <tr><td>Reinforcement</td><td>12mm ⌀ @ 100mm c/c</td></tr>
                        </table>
                    </div>
                    
                    <div class="card">
                        <h4>Column Grid System</h4>
                        <table>
                            <tr><td>Building Length</td><td>10,500mm</td></tr>
                            <tr><td>Building Width</td><td>8,600mm</td></tr>
                            <tr><td>Grid Spacing</td><td>4,300mm c/c</td></tr>
                            <tr><td>Total Columns</td><td>16 Numbers</td></tr>
                            <tr><td>Grid Pattern</td><td>2 × 8 Configuration</td></tr>
                        </table>
                    </div>
                </div>
                
                <h3>1.3 Column System Analysis</h3>
                <p>The column schedule reveals a two-stage construction approach with columns extending from the foundation level to the plinth level, then continuing above to support the roof structure. The columns maintain a consistent rectangular cross-section of 250 millimeters by 400 millimeters throughout their height. The longitudinal reinforcement consists of ten bars of 16 millimeter diameter, providing substantial capacity for both axial loads and bending moments that may arise from lateral forces or eccentric loading conditions.</p>
                
                <p>The reinforcement arrangement includes corner bars and intermediate bars along the longer faces of the rectangular section to maximize structural efficiency. Lateral ties prevent buckling of the longitudinal bars and provide confinement to the concrete core, which is particularly important for seismic resistance. The structure has been designed for seismic load conditions as indicated in the general notes, incorporating ductile detailing provisions required by current Indian Standards.</p>
                
                <h3>1.4 Beam and Plinth System</h3>
                <p>The plinth beam system ties all columns together at ground level, serving multiple critical structural functions. These beams resist differential settlement between footings, provide lateral restraint to column bases, support the floor slab system, and contribute to overall lateral load resistance. The beam dimensions of 300 millimeters width by 450 millimeters depth provide adequate stiffness and strength for the span lengths involved.</p>
                
                <p>Reinforcement detailing shows proper consideration of moment and shear demands with additional top reinforcement at support zones where negative moments occur, and bottom reinforcement at mid-span where positive moments dominate. The vertical stirrups are spaced more closely near supports where shear forces reach their maximum values, transitioning to wider spacing in the central span regions where shear demands are lower.</p>
                
                <h3>1.5 Roof Structural System</h3>
                <p>The roof framing employs steel trusses fabricated from Indian Standard Angle sections spanning between the column supports. The members schedule indicates the use of ISA 75×75×8 millimeter angles for primary truss members and ISA 60×60×8 millimeter angles for secondary elements. Secondary framing consists of ISMC 100 purlins spanning transversely between trusses at regular intervals determined by the spanning capability of the chosen roofing material.</p>
                
                <p>The truss configuration appears to be a simple pitched roof design with integrated provisions for material handling equipment, as evidenced by references to crane girder systems. The connection between the steel roof structure and concrete columns requires careful detailing with anchor bolts embedded in the column tops and proper base plates to distribute concentrated forces over adequate bearing areas.</p>
                
                <h3>1.6 Material Specifications</h3>
                <p>Throughout all structural elements, consistent material specifications ensure quality and performance. The concrete grade is M20 with characteristic compressive strength of 20 Newtons per square millimeter at twenty-eight days, which is appropriate for this type of light industrial structure. The reinforcement uses Fe500 grade thermo-mechanically treated steel with minimum yield strength of 500 Newtons per square millimeter, which is the current standard for seismic-resistant design in India.</p>
                
                <p>Concrete cover specifications are carefully designated based on exposure conditions: 75 millimeters for foundations in contact with soil to protect against moisture and chemical attack, 50 millimeters for columns, 40 millimeters for walls, and 30 millimeters for beams and slabs. These cover dimensions provide adequate protection against corrosion in normal exposure conditions while facilitating proper concrete placement and compaction around the reinforcement.</p>
            </section>
            
            <!-- SECTION 2: RCC COLUMN HEIGHT -->
            <section id="rcc">
                <h2>2. RCC COLUMN HEIGHT DETERMINATION</h2>
                
                <div class="warning">
                    <h4>⚠️ Critical Information Gap</h4>
                    <p>After thorough examination of all four structural drawings provided, the exact height of the RCC columns is not explicitly dimensioned on these sheets. However, based on professional analysis of available details and standard construction practices, reasonable estimates can be provided with critical dimensions requiring verification before construction proceeds.</p>
                </div>
                
                <h3>2.1 Column Height Components</h3>
                <p>The RCC columns are divided into two distinct vertical segments. The first segment extends from the foundation level to the plinth level, while the second segment continues from the plinth level upward to the roof truss bearing level. The total column height represents the sum of these two segments plus any projection required above the roof bearing for anchor bolt installation.</p>
                
                <h4>Foundation to Plinth Level Segment</h4>
                <p>The foundation plan shows footings positioned at 200 millimeters below the finished ground level with a total footing thickness of 600 millimeters. In standard Indian construction practice for industrial buildings, the plinth level typically ranges from 450 millimeters to 600 millimeters above the natural ground level to protect the building interior from surface water drainage and provide adequate clearance for utilities.</p>
                
                <p>Given that the footing schedule indicates footings at 200 millimeters depth below finished ground level, and assuming the plinth beam sits at a standard plinth height, the column height from foundation level to plinth level would be approximately 600 millimeters to 800 millimeters. This represents the column length within the foundation zone before reaching the plinth beam level where the floor system begins.</p>
                
                <h4>Plinth Level to Roof Bearing Level Segment</h4>
                <p>The more substantial portion of the column height extends from the plinth level upward to the point where the steel roof trusses bear on the column tops. For an industrial workshop building with a steel truss roof system spanning 10,500 millimeters, typical design practice would establish the eaves height in the range of 4,000 millimeters to 6,000 millimeters. This range provides adequate clearance for workshop operations, equipment, and potential overhead crane systems while maintaining reasonable proportions for the structural design.</p>
                
                <p>The drawings show reference to a crane girder in the roof detail, which suggests the building is designed to accommodate material handling equipment. Workshop buildings with overhead crane provisions typically require minimum clear heights of 4,500 millimeters to 5,500 millimeters below the crane rail level to allow adequate headroom for crane hook travel and the loads being lifted. This consideration supports an estimate of approximately 5,000 millimeters to 5,500 millimeters from plinth level to the truss bearing elevation.</p>
                
                <h3>2.2 Estimated Total Column Height</h3>
                <div class="metric-box">
                    <div class="metric-value">5.7m - 6.2m</div>
                    <div class="metric-label">Estimated Total RCC Column Height</div>
                    <div style="margin-top: 10px; font-size: 0.9em;">From top of footing to roof bearing level</div>
                </div>
                
                <p>Combining the foundation to plinth segment of approximately 700 millimeters with the plinth to roof bearing segment of approximately 5,000 millimeters to 5,500 millimeters yields a total RCC column height of approximately 5,700 millimeters to 6,200 millimeters from the top of footing to the roof bearing level. This represents a reasonable estimate for preliminary material procurement and construction planning purposes, though exact confirmation is essential before proceeding.</p>
                
                <h3>2.3 Verification Requirements</h3>
                <div class="highlight">
                    <h4>Critical Dimensions Requiring Confirmation</h4>
                    <p><strong>Before proceeding with construction, the following vertical dimensions must be obtained from the complete drawing set or confirmed with the structural engineer:</strong></p>
                    <p>The finished floor level relative to the natural ground level must be established, as this determines excavation depths and the elevation reference for all subsequent work. The plinth level elevation above the finished floor level or above the top of footing needs precise specification to ensure plinth beams are constructed at the correct height.</p>
                    <p>Most critically, the column height from plinth level to the underside of roof truss bearing requires exact dimensioning. This affects the total length of column reinforcement bars to be fabricated, the height of column formwork panels needed, the volume of concrete to be procured, the positioning of construction joints if the column is cast in multiple lifts, and the elevation at which anchor bolts for truss connections must be installed.</p>
                </div>
                
                <h3>2.4 Impact on Construction Planning</h3>
                <p>The column height significantly impacts construction methodology and equipment selection. Columns in the 5,500 millimeter to 6,000 millimeter height range can typically be cast in a single continuous pour using conventional concrete pumping equipment or bucket and crane placement methods. The formwork system must be designed for the lateral concrete pressure at this height, which requires adequate tie spacing and waling support to prevent bulging or failure during concrete placement.</p>
                
                <p>The column reinforcement consists of ten bars of 16 millimeter diameter as the main longitudinal steel. If the total column height is approximately 6,000 millimeters as estimated, the reinforcement bars would need to be procured in lengths of at least 6,500 millimeters to 7,000 millimeters to account for the lap length at the base with dowel bars from the footing, any required projection at the top for anchor bolt installation, and cutting tolerances during fabrication.</p>
                
                <p>Standard steel mills supply reinforcement bars in lengths of twelve meters, which would accommodate the full column height in single pieces without requiring intermediate splices. This is preferable from both structural and construction efficiency perspectives, as eliminating mid-height lap splices reduces reinforcement congestion and simplifies the cage assembly and installation process.</p>
            </section>
            
            <!-- SECTION 3: COMPOSITE COLUMN CLARIFICATION -->
            <section id="composite">
                <h2>3. COMPOSITE COLUMN ASSESSMENT</h2>
                
                <div class="success">
                    <h4>✓ Clarification on Column Design</h4>
                    <p>After careful re-examination of all four structural drawings for the E.T.R. Workshop Bulandshahr project, it must be clarified that <strong>these are NOT composite columns</strong>. The structural system uses conventional reinforced concrete columns throughout the entire building.</p>
                </div>
                
                <h3>3.1 Actual Column System Confirmed</h3>
                <p>The column layout plan and detailed column schedules clearly indicate that all columns are constructed using M20 grade concrete with Fe500 grade reinforcement steel. The typical column section detail shows a rectangular concrete section measuring 250 millimeters by 400 millimeters with ten bars of 16 millimeter diameter as longitudinal reinforcement, confined by lateral ties. This configuration represents standard reinforced concrete column design without any structural steel sections embedded within the concrete.</p>
                
                <h3>3.2 Distinction from Composite Construction</h3>
                <p>Composite columns, by definition, combine structural steel sections such as I-beams, H-sections, or hollow steel tubes encased in concrete or filled with concrete to create a hybrid structural element that capitalizes on the strengths of both materials. The steel section carries a significant portion of the axial and bending loads while the concrete provides additional compression capacity, fire resistance, and lateral support to prevent local buckling of steel elements.</p>
                
                <p>In contrast, this project employs traditional reinforced concrete columns where the steel reinforcement bars serve primarily to resist tensile stresses and provide ductility, while the concrete carries most of the compression. The reinforcement bars are relatively small in cross-sectional area compared to the total concrete section, typically comprising one to four percent of the gross column area.</p>
                
                <table>
                    <thead>
                        <tr>
                            <th>Aspect</th>
                            <th>This Project (RCC)</th>
                            <th>Composite Column</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Column Type</td>
                            <td>Reinforced Concrete</td>
                            <td>Steel + Concrete Composite</td>
                        </tr>
                        <tr>
                            <td>Steel Component</td>
                            <td>10-16mm ⌀ bars (2% area)</td>
                            <td>Structural section (10-20% area)</td>
                        </tr>
                        <tr>
                            <td>Load Distribution</td>
                            <td>Concrete carries compression</td>
                            <td>Steel shares major load</td>
                        </tr>
                        <tr>
                            <td>Construction</td>
                            <td>Standard formwork & casting</td>
                            <td>Steel erection + encasement</td>
                        </tr>
                        <tr>
                            <td>Connection to Footing</td>
                            <td>Dowel bar lap splice</td>
                            <td>Base plate with anchor bolts</td>
                        </tr>
                    </tbody>
                </table>
                
                <h3>3.3 Mixed Construction Approach</h3>
                <p>While the building does incorporate both concrete and steel structural elements, these function as separate systems rather than composite action. The lower portion of the structure including foundations, columns, and plinth beams consists entirely of reinforced concrete construction. The roof framing system transitions to structural steel, utilizing angle section trusses and channel section purlins.</p>
                
                <p>This represents a mixed construction approach rather than composite member design. The interface between the concrete columns and steel roof trusses occurs at the column tops where anchor bolts embedded in the concrete receive the steel base plates welded to the truss bottom chords. This connection transfers loads from the steel roof system down into the concrete columns, but the columns themselves remain purely reinforced concrete members without embedded steel sections.</p>
                
                <h3>3.4 Construction Implications</h3>
                <p>The absence of composite column design simplifies the construction process considerably compared to what composite construction would require. For composite columns, contractors must accurately position and support heavy steel sections during concrete placement, ensure proper concrete flow around the steel shape including into any re-entrant corners of the section profile, and coordinate the steel fabrication tolerances with concrete formwork dimensions.</p>
                
                <p>Construction of the reinforced concrete columns follows standard procedures with reinforcement cages fabricated from individual bars, assembled using binding wire at bar intersections, and positioned within conventional column formwork. The concrete placement requires only standard internal vibration techniques to achieve proper consolidation around the reinforcement bars. Quality control focuses on verifying bar sizes, quantities, spacing, cover dimensions, and lap lengths according to the reinforcement schedule, along with ensuring concrete strength through cube testing protocols.</p>
            </section>
            
            <!-- SECTION 4: RATE ANALYSIS -->
            <section id="rate-analysis">
                <h2>4. COMPREHENSIVE RATE ANALYSIS</h2>
                
                <h3>4.1 Project Financial Overview</h3>
                <div class="grid-2">
                    <div class="metric-box" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">
                        <div class="metric-value">₹1,45,24,713</div>
                        <div class="metric-label">Original BOQ Value</div>
                    </div>
                    <div class="metric-box" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);">
                        <div class="metric-value">₹1,31,15,816</div>
                        <div class="metric-label">Contract Value (After 9.70% Discount)</div>
                    </div>
                </div>
                
                <h3>4.2 Work Category Breakdown</h3>
                
                <h4>Earthwork & Site Preparation</h4>
                <table>
                    <thead>
                        <tr>
                            <th>Description</th>
                            <th>Quantity</th>
                            <th>Unit</th>
                            <th>Rate (₹)</th>
                            <th>Amount (₹)</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Excavation (mechanical/manual)</td>
                            <td>151</td>
                            <td>cum</td>
                            <td>196.79</td>
                            <td>29,715</td>
                        </tr>
                        <tr>
                            <td>Earth filling in layers</td>
                            <td>265</td>
                            <td>cum</td>
                            <td>148.18</td>
                            <td>39,268</td>
                        </tr>
                        <tr>
                            <td>Local earth supply & filling</td>
                            <td>100</td>
                            <td>cum</td>
                            <td>529.58</td>
                            <td>52,958</td>
                        </tr>
                        <tr>
                            <td>Sand filling in plinth</td>
                            <td>110</td>
                            <td>cum</td>
                            <td>1,605.56</td>
                            <td>1,76,612</td>
                        </tr>
                        <tr style="font-weight: bold; background: #f0f0f0;">
                            <td colspan="4">TOTAL EARTHWORK</td>
                            <td>₹2,99,077</td>
                        </tr>
                    </tbody>
                </table>
                
                <h4>Concrete Works Analysis</h4>
                <p>The concrete works constitute a major portion of the structural cost, with carefully graded rates reflecting the increasing complexity of work at higher levels. Plain cement concrete for foundations and leveling uses economical 1:5:10 mix at ₹4,928 per cubic meter. The reinforced cement concrete employs richer 1:1.5:3 mix with rates varying from ₹6,839 per cubic meter for work up to plinth level to ₹8,698 per cubic meter for beams and suspended slabs, representing a 27% premium for overhead work requiring more elaborate formwork and staging.</p>
                
                <table>
                    <thead>
                        <tr>
                            <th>Concrete Type</th>
                            <th>Location</th>
                            <th>Quantity (cum)</th>
                            <th>Rate (₹/cum)</th>
                            <th>Amount (₹)</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>PCC 1:5:10</td>
                            <td>Lean concrete/blinding</td>
                            <td>40</td>
                            <td>4,928</td>
                            <td>1,97,122</td>
                        </tr>
                        <tr>
                            <td>RCC 1:1.5:3</td>
