# Frontend-day1
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Learning Frontend - Day 1</title>
  <style>
    :root{
      --page-width: 980px;
      --muted:#666;
      --accent:#2b6cb0;
      --border:#8a8a8a;
      --table-bg:#fff;
      font-family: "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }

    body{
      margin:24px;
      color:#111;
      line-height:1.4;
      display:flex;
      justify-content:center;
    }

    .container{
      width:100%;
      max-width:var(--page-width);
    }

    header h1{
      margin:0 0 6px 0;
      font-size:36px;
      letter-spacing: -0.5px;
    }

    header p.subtitle{
      margin:0 0 18px 0;
      color:var(--muted);
      font-size:14px;
    }

    /* Small student table */
    .student-table{
      border-collapse:collapse;
      margin-bottom:18px;
      width:420px;
      box-shadow: 0 0 0 1px rgba(0,0,0,0.06);
      background:var(--table-bg);
    }
    .student-table th,
    .student-table td{
      border:1px solid var(--border);
      padding:6px 8px;
      text-align:left;
      font-size:13px;
    }
    .student-table th{
      background:#f4f4f4;
      font-weight:600;
    }
    .student-table tfoot td{
      font-weight:700;
      background:#fafafa;
    }

    /* List section */
    .content{
      margin:18px 0;
      font-size:15px;
    }
    .content ol{ margin:8px 0 8px 24px; }
    .content ul{ margin:8px 0 0 24px; list-style:disc; }

    a{
      color:var(--accent);
      text-decoration:underline;
    }

    .definitions{
      margin:12px 0 18px 0;
      font-size:14px;
      color:var(--muted);
    }

    /* Big projects table */
    .projects-wrapper{
      margin-top:18px;
      overflow-x:auto;
    }
    .projects{
      border-collapse:collapse;
      width:100%;
      min-width:900px; /* allow horizontal scroll on smaller screens */
    }
    .projects caption{
      caption-side:top;
      font-weight:700;
      text-align:center;
      padding:6px 0;
      border:1px solid var(--border);
      background:#f8f8f8;
      font-size:16px;
    }
    .projects th,
    .projects td{
      border:1px solid var(--border);
      padding:10px 12px;
      vertical-align:top;
      font-size:13px;
    }
    .projects th{
      background:#fafafa;
      text-align:left;
      font-weight:700;
    }

    .col-sr{ width:44px; text-align:center; }
    .col-category{ width:110px; text-align:left; }
    .col-name{ width:180px; }
    .col-desc{ width:320px; }
    .col-skills{ width:160px; }
    .col-links{ width:80px; text-align:center; }

    /* skills as bullet list inside table cell */
    .skills-list{
      margin:0;
      padding-left:18px;
    }

    /* right column links */
    .view-link{
      display:inline-block;
      font-size:13px;
      text-decoration:underline;
      color:var(--accent);
    }

    /* small responsive tweaks */
    @media (max-width:720px){
      header h1{ font-size:28px; }
      .student-table{ width:100%; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Learning Frontend</h1>
      <p class="subtitle">Welcome to Day 1</p>
    </header>

    <!-- small student table -->
    <table class="student-table" aria-describedby="students-desc">
      <thead>
        <tr>
          <th>Sr.NO</th>
          <th>Name</th>
          <th>Age</th>
          <th>City</th>
          <th>Marks</th>
          <th>Category</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td>John</td>
          <td>25</td>
          <td>New York</td>
          <td>90</td>
          <td>Frontend</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Jane</td>
          <td>30</td>
          <td>Los Angeles</td>
          <td>80</td>
          <td>Frontend</td>
        </tr>
        <tr>
          <td>3</td>
          <td>Mike</td>
          <td>28</td>
          <td>Chicago</td>
          <td>50</td>
          <td>Backend</td>
        </tr>
        <tr>
          <td>4</td>
          <td>Sara</td>
          <td>22</td>
          <td>Miami</td>
          <td>70</td>
          <td>Backend</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td colspan="4">Total Marks</td>
          <td>290</td>
          <td></td>
        </tr>
      </tfoot>
    </table>

    <!-- outline + bullets + links -->
    <div class="content" id="students-desc">
      <ol>
        <li>Introduction to HTML</li>
        <li>Understanding CSS</li>
        <li>Basics of JavaScript</li>
        <li>Building a simple webpage</li>
      </ol>

      <ul>
        <li>HTML Elements</li>
        <li>CSS Selectors</li>
        <li>JavaScript Functions</li>
        <li>Webpage Layout</li>
      </ul>

      <p style="margin-top:12px;">
        <a href="#" title="HTML overview">HTML</a><br>
        <span class="definitions">HyperText Markup Language</span>
      </p>

      <p>
        <a href="#" title="CSS overview">CSS</a><br>
        <span class="definitions">Cascading Style Sheets</span>
      </p>

      <p>
        JavaScript<br>
        <span class="definitions">A programming language for the web</span>
      </p>
    </div>

    <!-- Projects table -->
    <div class="projects-wrapper" role="region" aria-label="My Projects">
      <table class="projects" summary="List of projects with categories, descriptions, skills and links">
        <caption>My Projects</caption>
        <thead>
          <tr>
            <th class="col-sr">Sr.<br>No</th>
            <th class="col-category">Category</th>
            <th class="col-name">Name</th>
            <th class="col-desc">Description</th>
            <th class="col-skills">Skills</th>
            <th class="col-links">Links</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="col-sr">1</td>
            <td class="col-category">Frontend</td>
            <td class="col-name">Portfolio Website</td>
            <td class="col-desc">A personal portfolio to showcase my work</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>

          <tr>
            <td class="col-sr">2</td>
            <td class="col-category">Frontend</td>
            <td class="col-name">API Development</td>
            <td class="col-desc">Developed RESTful APIs for a web application</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>Node.js</li>
                <li>Express.js</li>
                <li>MongoDB</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>

          <tr>
            <td class="col-sr">3</td>
            <td class="col-category">Backend</td>
            <td class="col-name">Database Management</td>
            <td class="col-desc">Managed databases for a large-scale application</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>MySQL</li>
                <li>PostgreSQL</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>

          <tr>
            <td class="col-sr">4</td>
            <td class="col-category">Frontend</td>
            <td class="col-name">Web Application</td>
            <td class="col-desc">Built a full-stack web application with user authentication</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>React.js</li>
                <li>Node.js</li>
                <li>Express.js</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>

          <tr>
            <td class="col-sr">5</td>
            <td class="col-category">Backend</td>
            <td class="col-name">Data Analysis</td>
            <td class="col-desc">Analyzed large datasets using Python and Pandas</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>Python</li>
                <li>Pandas</li>
                <li>NumPy</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>

          <tr>
            <td class="col-sr">6</td>
            <td class="col-category">Backend</td>
            <td class="col-name">Machine Learning</td>
            <td class="col-desc">Developed machine learning models for predictive analytics</td>
            <td class="col-skills">
              <ul class="skills-list">
                <li>Scikit-learn</li>
                <li>TensorFlow</li>
                <li>Keras</li>
              </ul>
            </td>
            <td class="col-links"><a class="view-link" href="#">View Project</a></td>
          </tr>
        </tbody>
      </table>
    </div>

  </div>
</body>
</html>
