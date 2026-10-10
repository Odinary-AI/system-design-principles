# 案例与原始来源

用途：在需要解释原则或比较设计机制时读取相应条目。无需每次任务重新浏览全部来源。历史机制用于类比；当前产品状态、版本参数和性能需重新核实。官方自述也不等于独立验证。

## 理论来源

- **NASA 系统工程**：目标、边界、技术与生命周期取舍，支持 P01、P14。[Fundamentals of Systems Engineering](https://www.nasa.gov/reference/2-0-fundamentals-of-systems-engineering/)
- **NASA 设计过程**：要求一致、必要、可行和可验证，并区分符合规格与满足任务，支持 P02、P07、P13。[System Design Processes](https://www.nasa.gov/reference/4-0-system-design-processes/)
- **Simon，1962**：近可分解系统允许在合适条件下分层理解和分析，支持 P04、P06；不是所有系统都具有这一性质。[The Architecture of Complexity](https://www.andrew.cmu.edu/course/15-440/assets/READINGS/simon-architecture-of-complexity-1962.pdf)
- **Parnas，1972**：通过信息隐藏隔离设计决策，支持 P04、P05、P11；不是仅按执行步骤划分模块。[On the Criteria To Be Used in Decomposing Systems into Modules](https://www.cs.lafayette.edu/~gexia/cs301/resources/parnas.html)
- **Suh 公理化设计**：功能要求独立；在满足独立性的方案中比较满足要求的成功概率，支持 P04、P09。其“信息量”与成功概率有关，不能误解成代码行数或文档字数。[MIT 原始教材](https://web.mit.edu/2.882/www/chapter1/chapter1.htm)
- **Saltzer 与 Schroeder，1975**：机制经济性、最小权限、默认拒绝等保护原则，支持 P03、P10。[Basic Principles of Information Protection](https://web.mit.edu/Saltzer/www/publications/protection/Basic.html)

## 通用原则与方法的补充来源

2026-10-10 对照补充。以下注明实际查阅范围；条目是本项目的综合适配，不将作者主张升级为普适定理，不复制整套教材或专业认证流程。既有同类 skill 调研保留其历史范围，本轮基于跨领域原始资料补充 P16 和方法参考。方法名称见 [设计分析方法](design-methods.md)。

- **INCOSE，2022，Systems Engineering Principles**：读取原则正文和解释；第5、6、9项支持模型局限、逐步理解与不确定性决策，第2项支持整体及环境交互。对应 P07、P16 和方案取舍方法；其编号与本项目 P01–P16 不同，该原则集自身允许继续演进。[原文，第2、5、6、9项及解释](https://www.incose.org/wp-content/uploads/2026/01/systems_engineering_principles_book_v12_watson.pdf)
- **NASA，Systems Engineering Handbook，第二版**：读取第2、4、6章相关网页正文。第2章支持系统包括人员、流程与设施及整体相互作用（P01、P16）；第4章支持需要—功能—实现的递归推导；第6章的6.2、6.5、6.8节分别支持需求追踪与余量、配置与证据对象、按决策影响选择分析强度（P07、P12、P15及相应方法）。提炼工程机制，不迁移 NASA 的审批、文档或项目阶段要求。[第2章](https://www.nasa.gov/reference/2-0-fundamentals-of-systems-engineering/)、[第4章](https://www.nasa.gov/reference/4-0-system-design-processes/)、[第6章](https://www.nasa.gov/reference/6-0-crosscutting-technical-management/)
- **Donella Meadows，Leverage Points: Places to Intervene in a System，1999**：读取作者原文，重点为缓冲、存量与流量、延迟、调节与放大反馈；支持 P16 和状态、流与反馈分析。采用解释动态行为的机制，不把干预点排序当作所有工程系统的固定优先级。[作者原文](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/)
- **ISO 6385:2016，Ergonomics principles in the design of work systems**：读取官方摘要，支持将人员、设备、环境与工作组织共同考虑（P06、P08、P13）。未读取标准全文，不声称本项目覆盖其条款或符合标准。[官方摘要](https://www.iso.org/standard/63785.html)
- **Nancy Leveson，Engineering a Safer World，2012**：读取出版社书籍说明及2012-02-23作者访谈，未通读全书；作者说明正常部件之间的不安全交互也可能导致事故，支持 P09、P10、P16。只迁移这一判断边界，不据出版社或作者自述宣称方法效果优于所有其他方法。[书籍说明](https://mitpress.mit.edu/9780262016629/engineering-a-safer-world/)、[作者访谈](https://news.mit.edu/2012/qa-with-nancy-leveson)
- **Nancy Leveson 与 John Thomas，STPA Handbook，2018，第1–2章相关部分**：读取介绍和不安全控制动作分类；用于故障与危险分析的方法选择，检查动作提供/缺失、时机/顺序及持续时间与危险的关系。方法参考只给局部分析入口，不等同于完成正式 STPA，不替代领域安全证据。[作者手册](https://psas.scripts.mit.edu/home/get_file.php?name=STPA_handbook.pdf)
- **Kossiakoff、Seymour、Flanigan 与 Biemer，Systems Engineering Principles and Practice，第3版，2020，第6章**：读取出版社的需求分析章摘要，强调将客户需要转换为可供方案响应的性能要求；辅助需求—功能—实现映射。未读取章节全文，不据摘要扩展具体方法或效果结论。[章节摘要](https://onlinelibrary.wiley.com/doi/10.1002/9781119516699.ch6)
- **Saltzer、Reed 与 Clark，End-to-End Arguments in System Design，1984**：读取作者存档原文，支持按完整承诺所需信息配置责任（P05、需求与证据追踪）。仅在承诺需要端点掌握的信息时应用，不推出所有功能都应移到端点。[作者存档](https://web.mit.edu/Saltzer/www/publications/endtoend/endtoend.pdf)
- **W. Ross Ashby，An Introduction to Cybernetics，1956，第11章11/5–11/9节**：读取必要多样性定律的定义、条件和扩展，启发 P08 对干预能力的检查。形式结论依赖其扰动、调节与结果模型；不据此要求所有控制器增加复杂度。[作者家族档案中的书籍](https://ashby.info/Ashby-Introduction-to-Cybernetics.pdf)

已有 Parnas 原文支持按设计决策与变化划分模块；已有 Suh 教材支持区分功能要求、设计参数和物理零件，沿用上方来源。需要用其特定设计理论作判断时注明适用条件，不把功能独立性当作一切系统必须完全解耦的要求。

## 猛禽发动机：在整机边界内理解集成化

来源：SpaceX 关于 Raptor 3 的更新说明将传感器、控制器内部集成并配合热防护，与取消单独发动机防护罩联系起来。[SpaceX Updates](https://new.spacex.com/updates)

可迁移的机制：集成可能同时减少外部连接、防护和装配负担。评价 P03、P04、P13、P14 时，需要把外围结构纳入成本边界。

不可直接推导：外观更简洁意味着更易维修、更低全寿命成本或更高长期可靠性。还需要制造、检查、更换和使用数据；不能凭厂商性能目标证明已经达成。

## Linux：稳定外部承诺，允许内部演进

来源：官方文档区分稳定的内核到用户空间接口与允许改变的内核内部接口，并说明协调修改内部消费者的做法。[The Linux Kernel Driver Interface](https://cdn.kernel.org/doc/html/latest/process/stable-api-nonsense.html)

可迁移的机制：把兼容成本放在有真实消费者依赖的边界，支持 P05、P11、P13。

适用条件：能够协调内部消费者。对无法同步升级的第三方接口、独立部署服务或已售硬件，不能照搬内部接口自由变化的做法。

## 互联网：共同接口与端到端责任

来源：IP 提供跨异构网络的共同层；某些功能只有端点掌握足够信息才能完整实现。[RFC 1958](https://www.rfc-editor.org/rfc/rfc1958.html)

可迁移的机制：少量共同规则容纳不同实现，职责放在有足够信息的地方，支持 P04、P05、P12。

边界：不要推导出所有功能都必须移到边缘。历史上的宽容接收原则也不能机械套用；长期接受错误和歧义可能损害互操作性，应主动维护协议。[RFC 9413](https://datatracker.ietf.org/doc/html/rfc9413)

## SQLite：明确能力上限，验证异常路径

来源：官方适用范围说明单个数据库文件同一时刻的写入限制；测试包含内存不足、I/O 错误、崩溃模拟及复合失败。[适用场景](https://www.sqlite.org/whentouse.html)、[测试方法](https://www.sqlite.org/testing.html)

可迁移的机制：P01、P07、P09、P12。优秀系统可有明确边界；关键承诺需要失败条件下的证据。

边界：不能由“嵌入式”推断容量不足，也不能由测试数量推断绝对正确。判断需结合目标负载、访问模式与具体版本。

## 航天飞机飞控：按故障模型设计冗余

来源：多台主计算机之外，备用飞控软件采用独立开发，以降低共同软件缺陷的风险。[NASA：计算机与备用飞控](https://www.nasa.gov/history/sts1/pages/computer.html)

可迁移的机制：P03、P09。检查副本间共享的软件、供电、环境与切换机制；相同副本主要解决一部分失败方式。

边界：独立开发不能保证统计独立，也不能据飞控子系统推断整机安全。冗余数量应由具体任务和失效分析决定。

## 丰田生产系统：异常可见、可以停线、按需求生产

来源：自働化允许发现异常后停机或停线；准时化根据下游需求协调生产，仍保留必要的最小库存。[Toyota Production System](https://global.toyota/en/company/vision-and-philosophy/production-system/)

可迁移的机制：P08、P14、P15。局部停止能防止缺陷扩散，局部忙碌不代表整体有效产出。

边界：不要把精益解释成零库存、零余量或任何异常都停掉整个系统。缓冲与停止范围由波动、损失和恢复成本决定。

## 同类 skill 的机制参考

以下来源提供检查方法的启发，不是理论原始文献，也不证明本 skill 的实际效果；仅按相应问题借鉴，未引入其完整流程。

- **关键状态与依赖契约**：参考 pinchen147 对状态权威、派生数据恢复和依赖边界的检查，具体化 P02、P05、P09；保留多个主体通过协调保证约束的可能性。[固定版本](https://github.com/pinchen147/system-design-skill/blob/a1769c5e49f586c21ca6bef7435eaa5b70352534/skills/system-design/SKILL.md)
- **设计偏差处理**：参考 magnus919 对缺陷、例外、需求变化和过时规则的区分，具体化 P15。[固定版本](https://github.com/magnus919/agent-skills/blob/9a5adbcbe7877bcf3137664a5abb76dd4c6692fc/software-architecture/references/evolution-fitness-functions-and-drift.md)
- **迁移中间状态**：参考 magnus919 对共存假设、切换条件和不可逆步骤的要求，具体化 P11。[固定版本](https://github.com/magnus919/agent-skills/blob/9a5adbcbe7877bcf3137664a5abb76dd4c6692fc/software-architecture/references/migration-and-coexistence.md)
- **关键假设敏感性**：K-Dense-AI 的系统工程 agent 配置强调取舍分析中的权重敏感性；本项目将这一思路用于检查负载、成本等关键假设变化是否改变推荐，属于本项目的适配，不引入固定评分或扰动幅度。[固定版本](https://github.com/K-Dense-AI/scientific-agents/blob/acbd93db7ed551f703225c38ed90a30bd95d23be/scientific-agents/systems-engineer/AGENTS.md)

## 校准用例

用于自查应用方式，不要求每次运行，也不是已完成的行为测试记录。

- **小型离线工具**：用户担忧未来扩容，当前没有规模变化证据。先检查实际目标与容量，不为了“可扩展”引入分布式架构。
- **只读设计评审**：有设计图但没有实现和运行数据。可以发现图中的职责或接口矛盾；不能声称测出延迟、证明可靠性或修改代码。
- **重复订单改进**：已授权修复订单写入成功但响应丢失后，重试又创建订单的问题。检查业务请求身份、约束的保证机制和成功确认边界，实施最小修正并验证重复提交；网络超时本身不能证明首次写入失败。
- **多个写入者**：多个客户端离线添加集合元素，集合并集满足已声明的“保留全部新增项”要求，不能仅凭多写入者判错。若两个售票端各自确认售出同一座位，事后合并记录仍不能满足“不重复售出”；需检查销售确认前的约束保证机制。
- **慢依赖与重试**：下游处理变慢，上游与中间层均有重试且共享工作池积压。追踪总尝试量、时限与处理能力，检查既有责任和积压边界，再提出最小修正；不能仅以没有报错或各层都有重试认定可靠。
- **设计偏差**：旧图规定同步生成报表，但有效的新决定允许延迟且实现符合要求，应指出旧图过时并建议更新，不能据此报告实现缺陷。若新运行证据显示延迟已违反仍有效的交付要求，应重新评估相关决定，不能以“已记录”为由排除问题。
- **新旧版本共存**：新版将金额字段从 `amount` 改为只写 `total`，旧客户端仍仅读取 `amount`。新版单独通过检查不能证明滚动升级可行；应检查共存期间的读写兼容与切换条件，回退程序也不自动恢复已改写的数据。
- **推荐依赖成本假设**：两个方案均满足硬约束，建设与维护成本的取舍相反，已有报价支持的维护成本区间使总成本排序可能反转。应给出各自成立的条件和优先核实的成本项，不能只取区间中点作确定推荐；若范围内排序不变，不应仅因存在不确定性追加调查。缺少可靠范围时不虚设扰动幅度。
- **生产线有限缓冲**：下游设备短暂停顿，上游继续送料，缓冲容量有限。检查停顿期间的积压、满载动作及恢复后的处理能力，再评价是否需改变节拍或缓冲；使用物料与时间约束，不要求引入软件幂等键或一律停掉全线。
- **备用设备去重**：用户认为主备设备重复。查明故障模型及共享依赖后评价保留或删除，不能仅凭 P03 得出删除结论。
- **未知性能要求**：用户要求“更快”，没有负载和基线。先明确可观测场景与低成本测量；不承诺任意百分比提升。
- **局部模块已合理**：证据未显示实质问题。允许交付“在本次范围内未发现需要修改的问题”，说明未覆盖内容，不强行建议重构。

### 整体行为与方法选择的校准用例

以下为构造场景及判断标准，不是真实事故、实测数据或已完成的独立代理测试。数字只用于表达场景约束。

- **延迟反馈**：温控器每5秒根据测温提高加热功率，但测温反映约20秒前的状态，观察到温度反复过冲。检查 P16 的延迟、反馈与热积累，同时核对传感器误差、执行器及控制规则；可提出区分根因的小检查，不能仅凭延迟指定新周期或增益，也不能用“加强复盘”代替运行分析。
- **组合预算与互斥状态**：供电可持续提供60 W，两个负载各需40 W。若要求同时持续工作且无其他能源支持，整体需求80 W超出限制；若有已验证的互斥控制、切换瞬态也符合限制，不能仅凭两者相加判错。按实际运行状态检查 P05、P12，不擅自规定统一余量。
- **人工接管时限**：系统要求告警后2秒完成动作，现有观察显示操作员仅辨认告警就需6秒，且没有自动保护。接管安排不能满足既定时限；检查信息、工作负荷、控制权限及可行保护，培训或“有人值守”不能单独证明问题已解决。
- **稳态模型与启动声明**：只有额定运行的稳态模型通过校核，却声称证明启动阶段不会过热。限定现有证据范围，核对启动热量积累、初始条件及保护响应，选择最小瞬态分析或试验；证据不足不直接证明一定过热。
- **正常动作的不安全组合**：设计要求人员进入检修区时设备不得启动，但门控制与设备启动分别按各自合法指令执行，两者间没有状态协调；假定无其他保护。指出设计不能保证整体安全约束，追踪控制与反馈并验证相应保护；增加相同设备副本不解决这个交互问题，也不能声称事故已经发生。
- **简单任务的范围控制**：用户只要求评审离线计算工具的一处单位转换，有明确规格与示例，未发现动态、资源或安全问题。针对单位、转换和示例完成判断，保持只读；不启动七种方法、不要求仿真或完整需求矩阵，也不把局部通过写成整套工具已验证。
- **环境与能力的联合边界**：某构造设备规格在20 ℃可持续输出10 kW，在40 ℃仅支持6 kW；任务要求在40 ℃持续输出8 kW。即使温度未超工作范围、功率未超单独标示的最大值，联合条件仍不满足规格。若任务改为5 kW且其他条件满足，不因接近高温端点自动判错；不能由设备未损坏证明输出达标。
- **峰值、持续与未知边界**：某构造设备可持续输出10 kW，峰值15 kW最多10秒且两次峰值间需恢复60秒。不能用峰值支持持续15 kW的任务；符合上述间隔的5秒脉冲在其他条件满足时可成立。若只有20 ℃下的实测记录、其他温度范围未知，只能限定该次证据，不能补造工作温度上下限；局部说明文字修改不因此要求测量全部环境参数。
