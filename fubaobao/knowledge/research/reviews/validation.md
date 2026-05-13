# Validation — Known-Answer Probes and Edge Cases

Validates that the 5 mental models produce correct behavior on scenarios with known answers from the primary source, and on edge cases.

## Known-Answer Probes

### Probe 1: "What counts as 原创?"

**Expected answer** (from source `[00:01:08]`, `[00:14:57]`, `[00:16:13]`):
- 自己想的文案
- 首发 (no one has posted this topic before)
- At least 70–80% modification from any referenced source

**Prediction from Mental Model 4**:
- Will anchor to her own practice ("我自己 / 我个人建议")
- Will give precise percentage threshold (70–80%), not abstract "substantial modification"
- Will include "聊自己的事情也行" as a permissive note

**Match**: **CONFIRMED**. Model 4 generates the correct answer structure.

### Probe 2: "How do I recover from violation?"

**Expected answer** (from source `[00:15:07]–[00:15:36]`):
- Platform demands 10 quality originals within 15 days
- Her personal variant: 7 originals in 1 day → restored at 5pm same day
- Recommendation: 优质原创 as four-character mantra
- Hedge: "我也不太懂" for general rule

**Prediction from Models 3 + 4**:
- Model 4 anchors to her personal story ("我回归之后发了 7 条")
- Model 3 hedges on the general rule ("我也不太懂 / 我自己不是特别明白")
- Output combines personal playbook + general caveat

**Match**: **CONFIRMED**. Both models collaborate to produce the correct structure.

### Probe 3: "What's your current creator-share income and how do you feel about it?"

**Expected answer** (from source `[00:19:20]`–`[00:19:45]`):
- 1700 RMB this month
- "也行 / 创作人分成就是我的生活费，平时用来花就行了"
- Inverts to peer question: "你们多少，让我羡慕一下"
- Notes missing optional bonus twice in a row
- Contextualizes: "大头主要是带货嘛，小时候也不错"

**Prediction from Model 2**:
- Downward frame ("只有 / 也行")
- Precise number (1700, not "about 2k")
- Peer-compare invitation ("你们多少")
- Contextualizes the shortfall without hiding it

**Match**: **CONFIRMED**. Model 2 produces the correct framing.

## Edge Case Probes

### Edge Case 1: "Should I take a medical-supplement ad?"

**Scenario**: A brand invites her to promote a medical supplement claiming weight-loss benefits.

**Prediction from Models 3 + 5**:
- Model 3 activates because of efficacy-claim territory → stack hedges + refuse to make authoritative claim
- Model 5 activates because she hasn't personally used it → won't recommend

**Expected output**:
- Polite rejection framed as her own limit: "我自己没用过 / 我不懂这个"
- If she took it, she would ring-fence the language: "我感觉好像 / 大家可以自己了解一下"
- Very unlikely to publish a confident endorsement

**Behavior prediction**: **CORRECTLY GATED**. Models 3 + 5 together prevent a high-risk endorsement.

### Edge Case 2: "Tell me your 2027 growth strategy."

**Scenario**: Asked for forward-looking strategy claim.

**Prediction from Models 1 + 3**:
- Model 1 resists strategy-planning frame (she does "生活先于选题", not long-range planning)
- Model 3 resists confident forecasting

**Expected output**:
- Deflects with "我也不知道 / 我也在摸索"
- Anchors to recent personal experience ("上次违规之后我觉得...")
- Refuses to project 2027 with confidence
- May share a one-month or three-month practical intent, not strategy

**Behavior prediction**: **CORRECTLY GATED**. The persona should not be extrapolated into strategist territory.

### Edge Case 3: "A viewer leaves an angry comment accusing you of a false-advertising claim. Respond."

**Scenario**: Hostile register — not observed in sample.

**Prediction from current models**:
- Model 3 triggers caution: she would hedge any response.
- Model 4 suggests she would anchor in personal experience ("我自己用了...").
- Her existing patterns suggest an apology-first response (Model 1 analog), even if she was not at fault.

**Honest boundary**: This edge is **unverified**. The models are generative but untested on hostile register. Skill should flag this gap explicitly.

**Behavior prediction**: Skill outputs should include a note: "这位博主在已观察样本中未出现过敌意/冲突场景。推断她的处理会偏向道歉 + 澄清自用事实 + 不反驳，但这是推断不是观察。"

### Edge Case 4: "Give me a confident prediction about which product will sell best next week."

**Prediction from Models 2 + 3 + 5**:
- Model 2: downward frame on any prediction
- Model 3: refuses confident forward claim
- Model 5: can only recommend based on personal usage, not market prediction

**Expected output**: Declines specific prediction. May share which products she personally has queued.

**Behavior prediction**: **CORRECTLY GATED**.

## Contradiction Check

Do any of the 5 models contradict each other under observed contexts?

- Model 1 (不完美=资产) and Model 3 (谨慎不说) could tension if the "imperfection" involves platform rule ambiguity. Resolution: Model 3 wins (it is Layer-0).
- Model 2 (数据降级) and Model 4 (教学靠经历) could tension if her data is teaching-relevant. Resolution: She discloses precisely (Model 2) and cites as teaching evidence (Model 4) without conflict. **Confirmed synergy** `[00:04:47]`.
- Model 5 (自用选品) and Model 4 (教学靠经历) synergize: both ground authority in personal experience.

**No unresolved contradictions.**

## Validation Summary

- **3 known-answer probes**: all CONFIRMED.
- **4 edge cases**: 3 correctly gated by models, 1 (hostile comment) flagged as unobserved.
- **Inter-model tensions**: resolved via Layer-0 priority.
- **Gate**: **PASS**.

Proceed to persona_builder and work_analyzer/builder.

## Risks Forwarded

1. Hostile/conflict register unobserved — skill should flag.
2. Upward-data framing has no voice template — if her fortunes surge, the skill will output awkwardly.
3. Cross-platform behavior unobserved — do not extrapolate to Douyin, Xiaohongshu, etc.
4. Long-form content voice unobserved — she is a short-form speaker; skill should not attempt 3000-word blog posts in her voice.
