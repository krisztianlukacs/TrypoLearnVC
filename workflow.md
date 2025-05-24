# This is the current workflow of the TrypoLearn MVP

1. University teacher streams a course on Google Meet.
2. The video downloads to the VPS.
3. Separating the voice channel from the video.
4. AI writes the transcript (minutes:seconds of the video + Text)
5. Optional: AI can translate the transcript text. Write the dictionary with the new words.
6. AI generates a fully detailed text from the transcript.
7. AI generates a summary from the full text.
8. AI generates learning materials from the full text.
9. The platform publishes the learning materials and the summary, transcript to the GCP vector database and the Git-based text knowledgebase.
10. Teachers can upload other documents (PDF, PPT, DOC) as well.
11. A document-to-text converter converts all documents to text.
12. The platform uploads this text to the vector datastore and the Text knowledgebase also.
13. GCP Gemini AI learns from the vector database.
14. Students can register on the Platform.
15. Students can chat with AI on the Web application or Telegram.
16. Students can read all text knowledgebase on their smartphone (The application displays the Markdown file on the phone).

![Mindmap of the workflow](/pics/trypolearn_mindmap_highres.png)

[Highly detailed mindmap of the workflow](/pics/trypolearn_mindmap_highres.png)

## Planned Features for the Future

- Exam practice generator
- Group learning
- Role management. Every student can define their own roles for AI.

## Details of every step in the workflow

### 1. University teacher streams a course on Google Meet

During this initial stage of the TrypoLearn MVP, university teachers utilize the video conferencing platform Google Meet to broadcast their courses. This real-time instruction provides an interactive and engaging learning environment for students. Teachers can share a wide range of educational content, from lecture slides to demonstrations, fostering comprehensive understanding among learners.

### 2. The video downloads to the Virtual Private Server (VPS) for further processing

During this step, the video streamed by the university teacher in Google Meet is automatically downloaded onto a Virtual Private Server (VPS). This process ensures that the video can be efficiently processed and utilized for generating learning materials without any interruptions or delays. The VPS serves as a central hub for all operations related to data handling, making it easier to manage and scale the system as required.

### 3. Extracting Audio from the Video and Separating the Voice Channel

During this process, we extract the audio track from the video streamed by the university teacher on Google Meet. This is an essential step because separating the voice channel from the video enables more accurate transcription by our AI and allows for a smoother processing workflow. By isolating the voice channel, we ensure that only speech is transcribed, improving the quality of the generated learning materials.

### 4. AI writes an accurate and synchronized transcript for each second of the video along with corresponding time stamps and transcribed text

During this crucial step, our sophisticated AI technology transcribes every word spoken by the university teacher in real-time during their Google Meet session. The AI precisely matches each utterance to its respective time stamp on the video, ensuring an accurate and synchronized transcript is generated for seamless reference and further processing.

### 5. Optional: AI can translate the transcript text into multiple languages for better accessibility to students worldwide

In an effort to cater to a diverse student population, this feature allows the advanced AI to convert the transcribed text from the university teacher's Google Meet session into several languages. By enabling multilingual support, the platform ensures that students from various linguistic backgrounds can benefit from high-quality educational resources regardless of their native language. The translated transcript is then seamlessly integrated with the learning materials for a comprehensive and inclusive learning experience.

### 6. AI processes and structures the transcribed text into a coherent and comprehensive written form, creating a detailed text for each second of the video

The sophisticated AI employed in this phase takes the transcript generated in step 4 and organizes it into a well-structured and readable text format. The AI system meticulously examines the transcribed speech and arranges it into paragraphs, sentences, and phrases, ensuring that every word spoken by the university teacher during their Google Meet session is accounted for in a clear, coherent manner. This detailed text serves as the foundation for generating summaries, learning materials, and other value-added content, offering students a concise yet comprehensive understanding of each course.

### 7. AI generates a concise and insightful summary from the full text

During this stage, the advanced AI technology within TrypoLearn processes the entire transcribed text generated in step 6 to create an accurate and informative summary for each course. The AI system distills the key points, main ideas, and essential concepts presented by the university teacher during their Google Meet session, offering students a condensed yet comprehensive overview of each course without needing to read through the full text. This summary is instrumental in helping students quickly grasp the core principles and identify the areas that require further study or exploration.

### 8. AI generates learning materials from the full text

In this step, our advanced AI technology uses the comprehensive and coherent text generated in Step 6 to create valuable learning materials for students. The AI system meticulously examines the transcribed content, identifies key concepts and educational principles, and tailors the learning materials accordingly. This may include study guides, quizzes, interactive simulations, and supplementary resources that help learners better understand and apply the knowledge gained from the course.

Moreover, these learning materials are designed to cater to various learning styles and preferences. Some students might prefer visual content like diagrams or illustrations, while others might find written explanations more helpful. By offering a diverse range of learning materials, we ensure that each student can access the content in the most effective manner for them.

### The platform publishes the learning materials and the summary, transcript to the GCP vector database and the Git-based text knowledgebase

The platform, upon completion of generating the learning materials and summary from the transcript, stores this valuable data in two distinct knowledge repositories for efficient retrieval and future use. The Google Cloud Platform (GCP) vector database is employed to handle large-scale data processing tasks related to machine learning algorithms, such as Gemini AI. Meanwhile, a Git-based text knowledgebase is utilized to store all the transcribed texts, summaries, and learning materials in a structured format that can be easily accessed, edited, and version-controlled by teachers or administrators if necessary. This dual-repository approach ensures optimal data management and scalability for TrypoLearn's MVP.

The vector database, specifically, serves as the primary knowledge repository for GCP Gemini AI. It houses an extensive collection of learning materials, summaries, and transcribed text from multiple courses. This allows the AI to continuously learn from the vast array of data it encounters, refining its abilities to generate accurate, comprehensive, and contextually relevant learning materials for students in a variety of subjects. By employing machine learning algorithms that leverage this rich database, the platform can adapt to new teaching styles, content formats, and student needs over time, fostering a more effective and engaging educational experience.

The text knowledgebase, on the other hand, functions as a centralized location for all transcribed texts, summaries, and learning materials in a human-readable format. This repository enables teachers to easily access, edit, or expand upon existing course content. Additionally, it allows students to explore related topics or delve deeper into specific areas of interest by offering a vast library of educational resources at their fingertips. By consolidating this information in a structured and accessible manner, the text knowledgebase contributes significantly to enriching the learning experience on TrypoLearn's MVP platform.

### 10. Teachers can upload other documents (PDF, PPT, DOC) as well

By providing teachers with the ability to upload additional resources beyond just video lectures, they can enrich their courses and cater to diverse learning styles. Various document types, such as PDFs, PowerPoint presentations, or Microsoft Word files, can be added to the platform for students' perusal. These supplementary materials may contain visual aids like charts or diagrams, detailed explanations in written form, or complex data sets that complement and reinforce the knowledge imparted through the video lectures. By incorporating multiple types of content, teachers ensure that students can grasp the subject matter effectively, regardless of their preferred learning style.

Additionally, these uploaded documents undergo the same processing as the video lecture transcripts. The document-to-text converter scans and transcribes the contents into editable text, which is then integrated with the vector datastore and the text knowledgebase for easy retrieval by students. This unified approach to managing all learning materials ensures a consistent and seamless educational experience for learners as they navigate through the platform's various resources.

### 11. A highly advanced and intelligent document-to-text converter system transforms all uploaded documents into easily searchable and editable text format

During this crucial process, the platform's document-to-text converter automatically scans each uploaded file (PDF, PPT, DOC) from teachers or administrators. The system then utilizes sophisticated OCR (Optical Character Recognition) technology to convert the visual content into digital text, preserving the document's original layout and formatting as much as possible. This digitized text is then automatically added to the vector datastore and the text knowledgebase for easy retrieval by students or teachers in need of supplementary learning materials.

By employing a document-to-text converter, TrypoLearn's MVP platform ensures that all resources available on the system can be easily indexed, searched, and edited to keep the educational content fresh and up-to-date. Moreover, by converting uploaded documents into text format, learners with visual impairments can benefit from accessible learning materials, fostering an inclusive environment for all students.

The document-to-text converter is yet another example of TrypoLearn's commitment to providing a comprehensive and adaptable educational platform that caters to diverse learning styles, needs, and preferences.

### 12. The platform uploads the transcribed text, summaries, and learning materials to both the Google Cloud Platform (GCP) vector database and the Git-based text knowledgebase

In this step, all valuable data generated by our advanced AI technology - the transcribed text from each second of the video along with their corresponding summaries, learning materials, and any additional uploaded documents processed by the document-to-text converter - are stored in two distinct knowledge repositories: the GCP vector database and the Git-based text knowledgebase.

The GCP vector database is a crucial resource for machine learning algorithms like Gemini AI. By storing extensive collections of learning materials, summaries, and transcribed texts from numerous courses within this repository, the platform enables the AI to continue learning, adapting, and refining its abilities to generate contextually relevant and high-quality educational content.

The text knowledgebase, on the other hand, serves as a centralized location for all transcribed texts, summaries, and learning materials in an editable and human-readable format. This repository allows teachers to easily access, edit, or expand upon existing course content, while offering students a vast library of educational resources at their fingertips. By consolidating these valuable learning materials in a structured and accessible manner, the platform significantly enhances the overall learning experience on TrypoLearn's MVP.

### 13. GCP Gemini AI learns from the vector database

During this critical step, our advanced machine learning model called GCP Gemini AI harnesses the power of the vast knowledge contained within the vector database. The AI system continually learns and improves its abilities by analyzing the rich and diverse array of data stored in the vector repository. This ongoing learning process enables GCP Gemini AI to refine its understanding of different subjects, teaching styles, content formats, and student needs.

By adapting to these varied aspects, the AI model becomes more effective at generating accurate, coherent, and contextually relevant learning materials for students across various disciplines. Moreover, as new data is added to the vector database regularly, GCP Gemini AI remains up-to-date with the latest teaching methodologies and educational content trends, ensuring an engaging and enriching learning experience for users of TrypoLearn's MVP platform.

The machine learning algorithms employed by GCP Gemini AI rely on this extensive collection of data from multiple courses to continually refine their abilities to generate accurate, comprehensive, and contextually relevant learning materials for students worldwide. This self-learning approach enables the platform to adapt and evolve with the needs of both teachers and learners, fostering a more effective and engaging educational experience over time.

### 14. Students can register on the Platform

During this stage, prospective students are welcomed to join the TrypoLearn MVP platform by completing a registration process. The user-friendly interface provides a simple and straightforward experience, requiring essential information such as name, email address, and password for account creation. By granting access to students worldwide, the platform caters to diverse learners with varying backgrounds, interests, and educational needs.

Moreover, students have the flexibility to choose between registering via the web application or using popular messaging platforms like Telegram for a more seamless integration into their daily digital routines. This versatile approach ensures that TrypoLearn MVP can be accessed easily by students regardless of their preferred communication channel or device preference.

The registration process is crucial in granting students access to the wealth of educational resources available on the platform, including video lectures, transcribed text, summaries, learning materials, and supplementary documents. Once registered, students can immerse themselves in a wide range of courses taught by university professors, engaging in interactive learning environments designed to foster comprehensive understanding and knowledge retention.

### 15. Students can interact with AI chatbots on both the Web application and Telegram

This innovative feature allows students to engage in real-time discussions with our advanced AI chatbots either through the web platform or popular messaging app, Telegram. By providing multiple communication channels for interaction, the platform ensures that students can easily access support, clarify doubts, ask questions, and receive personalized guidance regardless of their preferred medium. This flexibility empowers students to learn at their own pace, fostering a more engaging and efficient educational experience on TrypoLearn's MVP.

### 16. Students can access and explore the entire text knowledgebase on their smartphones using TrypoLearn's mobile application, which displays the Markdown files directly on the device screen

With the increasing reliance on portable devices as an integral part of daily life, TrypoLearn MVP understands the importance of making educational resources readily accessible to students on-the-go. The platform offers a dedicated mobile application for smartphones that enables learners to access the text knowledgebase without limitation.

The application is designed with an intuitive user interface, ensuring easy navigation and seamless access to the vast library of learning materials available on the platform. Upon logging in, students can effortlessly explore course topics, search for specific keywords or phrases, and access a wealth of information at their fingertips. Moreover, the smartphone application displays Markdown files directly on the screen, making it easy for learners to read and engage with the educational content regardless of their location or time constraints.

This feature not only caters to students' diverse preferences for learning but also fosters a more flexible and adaptable educational experience by empowering them to learn anytime, anywhere. By providing mobile access to the text knowledgebase, TrypoLearn MVP underscores its commitment to making quality education accessible to all learners worldwide.

## New features in the future

In an effort to continually enhance the learning experience for students on TrypoLearn's MVP, the platform plans to introduce several new features that cater to various learning styles and preferences. Here is a brief overview of these exciting developments:

### Exam practice generator

To help students better prepare for examinations, the platform will offer an automated exam practice generator feature. This tool uses the knowledge gleaned from transcribed lectures, text summaries, and other educational resources to create realistic, multiple-choice questions tailored to each student's learning progress. By providing adaptive quizzes based on their understanding, students can identify areas requiring further study and track their progress effectively, ultimately improving exam performance.

### Group learning

Collaborative learning is an essential component of the educational process. To facilitate group interactions among students, TrypoLearn MVP will soon introduce a feature that allows students to form study groups. These groups can share resources, engage in discussions, and collaborate on projects related to their courses, fostering a more engaging and effective learning environment. This feature enables learners to benefit from the diverse perspectives and expertise of their peers, enhancing overall understanding and knowledge retention.

### Role management. Every student can define their own roles for AI

The platform also recognizes the importance of personalization in the educational experience. To that end, it will offer a unique role management feature allowing students to define custom roles for the AI chatbots. By setting preferences such as preferred communication style, level of interaction, or learning pace, students can tailor their educational journey to suit their individual needs and preferences. This level of personalization ensures an engaging, adaptable, and efficient learning experience that caters to each student's unique requirements.
