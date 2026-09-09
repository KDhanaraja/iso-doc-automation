# ISO Document Automation System

An automated application for generating ISO design and engineering documents with dynamic field substitution.

## Features

✅ **Dynamic Field Substitution** - Enter project name once, it appears in all documents
✅ **Pre-built ISO Templates**
   - ISO 9001 (Quality Management)
   - ISO 14001 (Environmental Management)
   - ISO 27001 (Information Security)
   - Design Specification Document
   - Engineering Report

✅ **Project Management** - Save and manage multiple projects
✅ **Document Generation** - Generate documents with custom fields
✅ **PDF Export** - Download generated documents as PDF
✅ **Web Interface** - Easy-to-use modern UI

## Installation

```bash
npm install
```

## Running the Application

```bash
npm start
```

Or for development with auto-reload:

```bash
npm run dev
```

The app will be available at `http://localhost:3000`

## How to Use

1. **Create a Project**
   - Enter project name and description
   - Fill in all required fields (Project Name, Client Name, etc.)

2. **Select a Template**
   - Choose from available ISO and Engineering templates
   - The template will display required fields

3. **Generate Document**
   - All template placeholders will be replaced with your project data
   - Preview the generated document

4. **Download**
   - Download the document as PDF
   - Save projects for future use

## Project Structure

```
iso-doc-automation/
├── src/
│   ├── controllers/
│   │   └── documentController.js
│   ├── models/
│   │   ├── DocumentTemplate.js
│   │   └── Project.js
│   ├── views/
│   │   ├── index.ejs
│   │   └── documents.ejs
│   └── server.js
├── public/
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── app.js
│       └── documents.js
├── data/
│   └── projects.json (auto-generated)
├── package.json
└── README.md
```

## Available Templates

### ISO 9001 - Quality Management System
- Project Name
- Client Name
- Version
- Date
- References
- Requirements
- Compliance Notes

### ISO 14001 - Environmental Management
- Project Name
- Organization
- Version
- Date
- Environmental Policy
- Objectives
- Implementation Plan
- Monitoring

### ISO 27001 - Information Security
- Project Name
- Client Name
- Version
- Date
- Security Policy
- Asset Management
- Access Control
- Incident Management
- Compliance Requirements

### Design Specification Document
- Project Name
- Client Name
- Engineer Name
- Date
- Version
- Project Description
- Design Requirements
- Architecture Details
- Technical Specs
- Testing Plan
- Sign-off fields

### Engineering Report
- Project Name
- Client Name
- Report ID
- Date
- Summary
- Project Overview
- Technical Analysis
- Findings
- Recommendations
- Conclusion
- Prepared By

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/templates` | Get all available templates |
| POST | `/api/create-document` | Generate document from template |
| POST | `/api/generate-pdf` | Export document as PDF |
| POST | `/api/save-project` | Save project with fields |
| GET | `/api/projects` | Retrieve all saved projects |

## Technologies Used

- **Backend**: Node.js, Express.js
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Template Engine**: EJS
- **Document Generation**: PDFKit, DOCX
- **Database**: JSON (File-based)

## Features Overview

### Dynamic Field Substitution
Fields are defined with `{{FIELD_NAME}}` syntax in templates. When you enter data in the project setup, all occurrences are replaced throughout all selected documents.

### Project Persistence
All projects and their field values are saved locally, allowing you to:
- Load existing projects
- Generate documents with saved data
- Edit and update projects

### Template System
Extensible template system that allows:
- Easy addition of new ISO standards
- Custom field definitions
- Pre-formatted document structure

## Future Enhancements

- [ ] Multiple file format support (DOCX, ODT)
- [ ] Template customization
- [ ] Batch document generation
- [ ] Cloud storage integration
- [ ] Collaborative editing
- [ ] Document versioning
- [ ] Digital signatures
- [ ] Custom branding

## License

MIT License

## Support

For issues or questions, please create an issue in the repository.
