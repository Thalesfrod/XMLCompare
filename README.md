# XML Structure Comparator 🚀

A simple, powerful, and client-side web tool to visually compare the structure of two XML documents. This tool helps developers and data analysts quickly identify differences in tags, attributes, and node hierarchy without worrying about the actual content.

## 📜 Overview
Ever had two XML files that were supposed to be similar but weren't? Manually checking for a missing tag or attribute in a large XML file can be a nightmare. This tool solves that problem by providing a clear, side-by-side comparison that highlights structural discrepancies. It's built with vanilla JavaScript and Tailwind CSS, running entirely in your browser—no data ever leaves your computer.

## ✨ Features

Side-by-Side View
Paste or drop your XML files into two distinct text areas for a clear comparison.



Drag & Drop
Easily drag and drop your .xml files directly from your desktop into the input boxes.

Base Structure View
Automatically generates a clean, unique-node view of your XML's skeleton, ignoring repetitive tags.

Structural Diffing
Compares tag names, attribute counts, and child node counts recursively.

Instant Feedback
Results are displayed instantly, pointing out the exact paths where differences were found.

Error Handling
Detects and reports parsing errors if the provided XML is invalid.

Client-Side Only
All processing is done in your browser. Your data is 100% private and secure.

Responsive Design
The interface is fully responsive and works great on both desktop and mobile devices.

## 🛠️ How to Use
Using the tool is straightforward.

Open the xml_comparator.html file in your favorite web browser.

Provide the XML inputs. You have two options:

Copy & Paste: Paste the content of your first XML into the "XML 1" box and the second into the "XML 2" box.

Drag & Drop: Drag your first .xml file and drop it onto the "XML 1" box. Do the same for the second file and the "XML 2" box.

Review the Base Structure (Optional): As you input the XML, a simplified structure view will appear below each input box. This helps you get a quick overview of the XML's hierarchy.

Click the "Compare Structures" button.

Analyze the Results:

If the structures are identical, a green success message will appear. ✅

If differences are found, a yellow results box will list each discrepancy, including the path where it occurred. ⚠️

## 🔬 How It Works
The comparison logic is handled entirely by JavaScript using the browser's native DOMParser.

Parsing: When you click "Compare", each XML string is parsed into a DOM tree.

Recursive Traversal: A recursive function starts from the root element of each DOM tree (documentElement).

Comparison at Each Node: At each level, the function compares:

The node name (tag name).

The number of attributes.

The presence of each attribute (by name, not value).

The number of child elements.

Report Generation: If any of these checks fail, a descriptive string is added to a differences array, which is then beautifully rendered in the results area.

The "Base Structure" view is generated similarly, but it traverses the tree and only keeps a record of the first occurrence of each tag at any given level, effectively de-duplicating the structure for readability.

## 📸 Screenshots
**

**

## 💻 Tech Stack
HTML5: For the basic structure of the page.

Tailwind CSS: For modern, responsive, and utility-first styling.

JavaScript (ES6+): For all the logic, including DOM parsing, comparison algorithms, and event handling. No frameworks, just pure JS!

## 🤝 Contributing
Contributions are welcome! If you have ideas for new features or improvements, feel free to fork the repository and submit a pull request.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

## 📄 License
This project is licensed under the MIT License - see the LICENSE.md file for details.
