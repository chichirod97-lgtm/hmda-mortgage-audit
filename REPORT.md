# Mortgage Underwriting Audit / 住房贷款模型审计

## English

This coursework adapts the first two experiments of Bowen, Price, Stein and Yang, *Generative AI and the Evolution of Mortgage Underwriting: Measuring and Mitigating Racial Disparities*. The audit uses 50 synthetic mortgage applications and DeepSeek Flash. The three assigned credit scores are 640, 715 and 790. The regressions control for credit score and loan fixed effects, with standard errors clustered by loan. Offered rates include rates returned alongside a recommendation to deny the loan.

### Experiment 1

The Black–White comparison uses 300 observations from the original pilot. Black variants were approved in 93.33% of cases and White variants in 92.67%. The estimated difference was +0.67 percentage points (p = 0.604). The estimated difference in offered interest rates was −2 basis points (p = 0.713). The exploratory interactions between the Black indicator and credit score, LTV and DTI were individually nonsignificant for both outcomes. Twenty-nine parsed results were recovered from previously displayed logs.

### Experiment 2

All five demographic conditions were evaluated with thinking disabled. The 750 observations use the same underlying applications. With race omitted, approval was 80.67% and the mean offered rate was 5.063%. The eight contrasts below compare each disclosed category with that condition. P-values are adjusted together by Holm.

| Category | Approval difference (pp) | Adjusted p | Offered rate difference (bp) | Adjusted p |
|---|---:|---:|---:|---:|
| Asian | +11.33 | 0.0220 | −41 | 0.0001 |
| Black | +4.67 | 0.3224 | −23 | 0.1161 |
| Hispanic | +6.67 | 0.1161 | −12 | 0.3224 |
| White | +8.67 | 0.1118 | −23 | 0.1032 |

The supplementary Black–White contrast was −4.00 percentage points for approval (95% CI [−9.84, +1.84], Holm-adjusted p = 0.3499) and 0 basis points for the offered rate (95% CI [−17.49, +17.49], adjusted p = 1.0000). Holm adjustment for this contrast covered two outcomes. One initially refused request later had a valid response. The saved numeric result agrees with that response.

### AI assistance and scope

AI assisted with drafting Python and Colab code, diagnosing API failures, organizing the results and drafting this bilingual report. The workflow saved outputs to Drive and distinguished model refusals from loan denials. The different API settings across the two experiments limit comparisons between them. The sample is synthetic and the results apply to the tested prompts and model settings. Experiments 3–6 and the repayment analysis are outside the results reported here.

## 中文

本作业改编了 Bowen、Price、Stein 和 Yang 关于生成式 AI 与住房贷款审批的论文中的前两项实验。审计使用50笔合成住房贷款申请及 DeepSeek Flash。实验设置三个信用评分：640、715 和 790。回归控制信用评分，纳入贷款固定效应，并按贷款聚类计算标准误。利率分析包括模型建议拒绝贷款时仍给出的报价。

### 实验1

初步实验包含300条观测。黑人条件的建议批准率为93.33%，白人条件为92.67%。批准率估计差异为 +0.67 个百分点（p = 0.604），报价利率差异为 −2 个基点（p = 0.713）。黑人条件与信用评分、贷款价值比和债务收入比的探索性交互项在两个结果中均未达到统计显著性。29条解析结果从此前显示的日志中恢复。

### 实验2

五种人口条件均在关闭推理模式后进行测试，同一批基础申请共生成750条观测。未披露种族时，建议批准率为80.67%，平均报价利率为5.063%。下表以未披露种族为参照，对八项检验统一进行 Holm 校正。

| 类别 | 批准率差异（百分点） | 校正后 p | 报价利率差异（基点） | 校正后 p |
|---|---:|---:|---:|---:|
| 亚裔 | +11.33 | 0.0220 | −41 | 0.0001 |
| 黑人 | +4.67 | 0.3224 | −23 | 0.1161 |
| 西班牙裔 | +6.67 | 0.1161 | −12 | 0.3224 |
| 白人 | +8.67 | 0.1118 | −23 | 0.1032 |

黑人与白人条件的补充比较显示，批准率差异为 −4.00 个百分点（95%置信区间 [−9.84, +1.84]，Holm 校正后 p = 0.3499），报价利率差异为0个基点（95%置信区间 [−17.49, +17.49]，校正后 p = 1.0000）。此处 Holm 校正涵盖两个结果。一条最初被模型拒答的请求后来获得了有效响应，保存的数值与该响应一致。

### AI 辅助与研究范围

AI 用于辅助编写 Python 和 Colab 代码、诊断 API 故障、整理结果及起草双语报告。流程将结果保存至 Drive，并区分模型拒答与贷款拒批。两项实验的 API 设置不同，限制了跨实验比较。样本为合成数据，结论适用于所测试的提示词和模型设置。本文未报告实验3至6或还款分析。

