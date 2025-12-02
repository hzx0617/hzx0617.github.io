---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

# 欢迎来到我的学术主页 👋

我目前是中南大学计算机学院数据科学与大数据技术专业2022级本科生，研究方向包括群智感知、强化学习、偏好推理等，目前对大模型感兴趣。

---

## 🎓 教育经历
- **北京大学**，计算机科学与技术（研究生），2026.9入学
- **中南大学**，数据科学与大数据技术（本科），2022.9–2026.6  
  GPA: 93.29/100（前6学期） 专业排名：1/114（前1%）

---

## 🔬 研究经历
### **SPDTM: A Shapley-value Based Preference Discovery and Task Matching to Maximize Satisfaction in Mobile Crowd Sensing**  
*2024.4 – 2025.3*
- 本人为 **第一作者**，论文发表于 *Computer Networks*（CCF-B类期刊，JCR一区），正式见刊于2025年8月  
  DOI: [10.1016/j.comnet.2025.111602](https://doi.org/10.1016/j.comnet.2025.111602)
- 针对群智感知（MCS）中任务与工人偏好不可知、虚假偏好上报等问题，提出 **SPDTM** 算法框架；
- 方案结合 **Shapley值** 与 **多智能体强化学习（MADDPG）**，通过 **多臂赌博机（MAB）** 平衡探索与利用；
- 设计了三阶段算法：  
  1. Shapley值驱动的任务-工人真实偏好发现；  
  2. 基于 MADDPG + MAB 的强化学习优化策略；  
  3. 满意度驱动的任务-工人匹配机制；
- 实验结果表明，SPDTM在真实数据集上的表现显著优于现有算法：  
  1. 工人真实偏好识别率：**94.79%**  
  2. 任务完成率：**91.77%**  
  3. 证明了其在偏好失真与噪声环境下的鲁棒性与实用性。

---

## 💻 项目经历

### **基于本地 LLM 的知识问答系统（RAG 框架）**  
*大模型后端开发项目，2025.4 – 2025.8*  

- 开发轻量级 **GraphRAG 框架**，实现基于关系图检索的本地文档问答系统；
- 支持 **OpenAI、DeepSeek、Ollama** 等多API并发请求；
- 兼容 **text2vec、HuggingFace、sentence-transformers** 等多种 Embedding；
- 优化检索与准确率：结合 **jieba 分词 + rank_BM25 + reranker 模块**；
- 支持多格式文档（PDF/DOCX/Markdown/TXT）与中英文混合文本；
- 基于 **Gradio** 实现流式对话界面，增强交互体验与可扩展性。

---

### **基于计算机视觉的交通路口智能监控系统**  
*国家级大学生创新创业项目，2023.5 – 2024.3*  

- 利用 **YOLO 算法** 实现行人闯红灯、交通拥堵等异常检测与实时预警；
- 构建系统架构：SRS流媒体服务器 + GPU云端服务器 + 本地客户端；
- 本地端基于 **Socket + selectors I/O复用** 实现并发通信；
- 可实时获取车流量、人流量及拥堵指标，支持视频流动态切换与可视化分析。

---

### **城市路口交通态势多维数据可视分析系统**  
*ChinaVis 数据可视化竞赛二等奖，2023.3 – 2023.6*  

- 设计交通态势可视分析系统，融合拥堵识别与事件检测；
- 使用 **Python** 进行数据清洗与聚合；
- 前端基于 **ECharts + JavaScript** 实现交互式可视化；
- 支持 2D 地图展示、时间序列分析、违规事件统计与道路健康度评估。

---

## 🧠 专业技能

- **编程语言与框架：** Python、C/C++、TensorFlow、PyTorch、Flask、Vue、Spark  
- **机器学习与强化学习：** 熟悉 DQN、DDPG、MADDPG 等算法框架  
- **数据挖掘与可视化：** 掌握特征工程、聚类、关联分析、推荐系统、情感分析、图计算；熟悉 Pandas、Scikit-learn、ECharts、Plotly  
- **科研工具：** Git、LaTeX、Origin、Jupyter Notebook、SQL  

---

## 🏆 荣誉与奖项

- 国家奖学金  
- 国家励志奖学金  
- 学年特等奖学金、学年一等奖学金
- 优秀学生干部、优秀学生标兵  

---

*最后更新于 2025 年 11 月*  
