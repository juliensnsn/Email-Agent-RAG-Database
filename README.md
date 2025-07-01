<h2>📧 Email Agent – RAG Database</h2>

<img align="center" alt="Agency-Socials-Website-Management" src="https://imgur.com/b1ytWR0.png"/>

<h3>📝 Context</h3>
<p>
  The client owns a sports equipment store and needed an agent capable of replying to customer emails. The agent had to provide precise answers to product-related questions.
</p>

<h3>🛠️ Build</h3>
<ol>
  <li>
    <strong>Add data to the vector database (<code>Watch Trigger (Drive) – Files Created</code>)</strong>
    <ul>
      <li>First step is to add data to your database! You can simply do this by uploading any file into your GDrive folder named <code>Documents</code>.</li>
      <li>The file will then be decomposed into vectors and can be retrieved in your Supabase vector database named <code>documents</code>.</li>
    </ul>
  </li>
  <li>
    <strong>Update data in the vector database (<code>Watch Trigger (Drive) – Files Updated</code>)</strong>
    <ul>
      <li>If you update a Google Doc directly in the GDrive folder, it will be instantly updated in the vector database.</li>
    </ul>
  </li>
  <li>
    <strong>When an email asking about equipment & characteristics is received (<code>Main Flow</code>)</strong>
    <ul>
      <li>The workflow first checks if the email comes from a Gmail thread and retrieves its history.</li>
      <li>If there is no Gmail thread, the workflow checks for other sender’s emails in the inbox.</li>
      <li>The workflow decides if the email needs an answer (if it concerns equipment and characteristics). If yes, the process continues.</li>
      <li>The email is written by the email agent, and data is retrieved from the vector database.</li>
      <li>Email conversation history is updated and kept for next time!</li>
    </ul>
  </li>
</ol>

<p>
  Project access 👉🏻 <a href="https://www.notion.so/julien-sanson/Email-Agent-Vector-Database-1b09a792e6bf80c8a5a2ffc21f6350da?source=copy_link">here</a>
</p>
