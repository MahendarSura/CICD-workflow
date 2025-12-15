## 5️⃣ Testing & QA Automation – Simple Telugu-Medium Style

---

### 5.1 Unit / Integration / End-to-End Tests

**Emti (What):**  
Code lo chinna parts (functions), combined modules, and full application flow correct ga work chesthunaya ani test cheyadam.

**Enduku Use Cheyali (Why):**  
- Bugs early ga dorakadaniki  
- CI/CD pipeline lo fail ayite immediate alert ravadaniki  
- Production lo issues raakunda quality maintain cheyadaniki

**Ela Use Chestharu (How):**  
- **Unit Tests:** Single function/module test  
- **Integration Tests:** Modules madhya interaction test  
- **End-to-End Tests:** User start nunchi end varaku app flow test

**Epudu Use Cheyali (When):**  
- Code push / Pull Request taruvatha

**Ekkada Use Cheyali (Where):**  
- Local machine, CI/CD pipeline

---

### 5.2 Regression Testing

**Emti (What):**  
New code changes valla old features break avvaledu ani check cheyadam.

**Enduku Use Cheyali (Why):**  
- Already working features safe ga undadaniki  
- Customer issues avoid cheyadaniki

**Ela Use Chestharu (How):**  
- Existing test cases automatic ga run chestharu  
- Nightly / weekly scheduled pipelines use chestharu

**Epudu Use Cheyali (When):**  
- New feature add chesina taruvatha  
- Bug fix taruvatha

**Ekkada Use Cheyali (Where):**  
- CI/CD pipeline, Staging environment

---

### 5.3 Code Quality / Coverage

**Emti (What):**  
Code quality, standards, and test coverage measure cheyadam.

**Tools:**  
SonarQube, ESLint, Pylint, Coveralls

**Enduku Use Cheyali (Why):**  
- Clean & maintainable code undadaniki  
- Coverage taggite pipeline fail cheyadaniki

**Ela Use Chestharu (How):**  
- Code scan → report generate → pipeline decision

**Epudu Use Cheyali (When):**  
- PR create chesinappudu  
- Merge mundu

**Ekkada Use Cheyali (Where):**  
- CI/CD pipeline, Code repository

---

## Real-Time Daily CI/CD Workflow: Testing & QA Automation

---

### What: Evaru em chestharu?

- **Developers:**  
  Code write → push / PR create → tests trigger

- **QA/Testers:**  
  Automated test reports analyze → manual testing if needed

- **CI/CD Pipeline:**  
  Unit → Integration → End-to-End tests run → pass/fail decide

- **DevOps:**  
  Test pass ayite next stage (deploy) approve cheyadam

---

### Why: Enduku ila chestharu?

- Bugs early ga dorakadaniki  
- Production lo failures avoid cheyadaniki  
- Fast feedback developers ki ivvadaniki  
- App quality improve cheyadaniki

---

### When: Epudu chestharu?

- Code push / PR create ayyaka  
- Nightly regression testing  
- Release mundu full test cycle

---

### Where: Ekkada chestharu?

- Local dev environment → unit tests  
- CI/CD pipeline → automated tests  
- Staging environment → QA validation

---

### How: Ela chestharu?

1. Developer code push chesthadu  
2. CI/CD pipeline trigger avuthundi  
3. Unit tests → Integration tests → E2E tests run avuthai  
4. Test fail ayite pipeline stop → alert send  
5. Test pass ayite → next stage (container/deploy) ki move avuthundi  
6. QA reports verify chestharu → sign-off

---

### Practical Points

- Automated tests mandatory cheyandi  
- Regression tests schedule cheyandi  
- Test failures ni ignore cheyakandi  
- Reports ni daily review cheyandi
