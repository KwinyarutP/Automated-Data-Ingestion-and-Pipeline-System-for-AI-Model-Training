**Project Title**		Automated Data Ingestion and Pipeline System for AI Model Training   
**Member(s)**		Ms. Kwinyarut Poungsangthanakul, MR. Parit Leelasetawong  
**Project Advisor**	Dr. Aye Hninn Khine  
**Program**		Bachelor of Engineering  
**Field of Study**		Computer Engineering  
**Department** 		Computer Engineering  
**Faculty** 		Engineering  
**Academic Year** 	2025

## **ABSTRACT** {#abstract}

The growing demand for AI at Siam.AI Cloud requires large, high-quality datasets that can be processed reliably across many different formats. However, current data preparation workflows are fragmented, largely manual and error-prone especially for Thai-language data. This project addresses these challenges by building an end-to-end, open-source, on-premise pipeline that takes raw data in various formats and converts it into clean, standardized outputs ready for training large language models.

The system uses a Data Lakehouse design with MinIO for scalable object storage, PostgreSQL for metadata and processing logs and Apache Airflow for automating the entire workflow. The pipeline handles ingestion, cleaning, normalization, deduplication and quality validation across various data types, with a primary focus on the NECTEC corpus, covering formats such as JSONL, Parquet, CSV, TXT, PDF documents and audio recordings. For PDFs, the pipeline employs an OCR model deployed  in order to extract text from scanned and digitally-encoded Thai documents through a dual-pass strategy, while attempting fast text extraction first and falling back to OCR when encoding issues are detected. Moreover, the audio pipeline leverages an ASR-Whisper model to transcribe Thai speech, incorporating a multi-level quality checking system capable of validating output even in the absence of ground truth labels. Pipeline health, storage usage and data quality are monitored in real time through Prometheus and Grafana dashboards.

The resulting system reduces manual effort, ensures consistent data quality across all processing stages, and produces standardized JSONL outputs ready for AI model training. It establishes a reusable foundation for Thai LLM development and future data engineering work at Siam.AI Cloud.