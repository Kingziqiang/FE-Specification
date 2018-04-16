### 重构指导
#### 1、预估风险
重构涉及面广，风险自然高。这就需要一些自动化测试工具帮助回归验证，然而自动化之类的在很多公司都没有，这就需要QA的协助了。当然如果连QA也没有，那就需要斟酌了。

#### 2、明确目的与范围
明确重构的目的与范围，不能因为不想维护之前别人的代码或者看不懂之前的逻辑，为了重构而重构（特别是在业务繁忙的时候，重构如果没有收益是很难做下去的）。前端的重构主要是提高代码的可维护性，可读性和性能。

#### 3、先易后难
先易后难，循序渐进。这样风险低，也更容易去理解项目现有架构。

#### 4、持续测试
重构过程中，一但到了某个节点，一定要不断的反复测试现有的重构情况，用来检验自己的理解与业务结合情况。以便在逐步迭代的过程中保证将风险降到最低。

#### 5、性能
在保证了原有业务的逻辑完整性后，需要不断完善与提升现有产品中的性能问题。