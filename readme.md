# 1. Object-Oriented General-Purpose Prompt Terminology Definition: The Potential of Object-Oriented Prompt Programming

[日本語(Japanese)](readme-ja.md) [英語(English)](readme.md)

## 1. Introduction

This paper discusses a novel approach with the potential to revolutionize AI communication: "Object-Oriented Prompt Programming." This method distinguishes itself from conventional prompt engineering by **applying Object-Oriented Programming (OOP) concepts to prompt design.**

Programmers, what if you could instruct AI models not only with natural language but also with familiar concepts like "classes, objects, methods, and events"? The "Object-Oriented Terminology for Prompt Design (OOPD)" introduced in this paper makes that a reality.

By using OOPD, you can describe prompts for instructing AI to perform complex tasks and generate advanced responses in a manner that is **more structured, efficient, and intuitive.** This allows you to transcend the limitations of traditional prompt engineering and maximize the potential of AI.

**Positioning of this paper:**

- This is a **presentation of the idea** of OOPD and a demonstration of one example of its practical application at this stage.
- The current implementation faces several challenges, including prompt text bloat, increased memory consumption, and reduced processing speed.
- We believe that future AI advancements may eliminate the need for such prompt design efforts. However, at present, we propose OOPD as an effective means to achieve more advanced communication with AI.
- The OOPD presented in this paper is designed based on Japanese. Currently, only Japanese and English versions of the definitions are available, but we believe that expansion to other languages is relatively easy.

## 2. What is Object-Oriented Terminology for Prompt Design (OOPD)?

OOPD is a common language for AI to interpret prompts and generate responses. It redefines key OOP concepts (classes, objects, properties, methods, etc.) for structuring and interpreting prompts. This allows AI to understand prompts not merely as a sequence of text but as structured information, enabling it to generate more consistent responses.

## 3. How OOPD Works

OOPD consists of the following elements:

- **Class:** A blueprint for objects. It defines the type of object and allows for the creation of multiple objects.
- **Object:** An instance created from a class. It has state (properties) and behavior (methods).
- **Instance:** An individual entity created based on a class (almost synonymous with object).
- **Property:** An attribute of an object. It represents the object's state.
- **Method:** An action performed by an object. It defines the object's behavior.
- **Type:** The kind of data. It specifies the type of properties or arguments, enhancing consistency.
- **Interface:** A contract that a class must implement. It defines behavior and achieves loose coupling.
- **Event:** An occurrence within an object. It represents a state change or stimulus and executes an event handler.
- **Composition:** A relationship where a class has another class (strong association, has-a). The lifecycles are shared.
- **Aggregation:** A relationship where a class has another class (weak association, has-a). The lifecycles are independent.
- **OOPD Format:** A structured prompt description format for users to give instructions to AI. It is based on Markdown format and combines natural language with OOP concepts.

## 4. Natural Language Programming with OOPD

By using OOPD, users can instruct AI with natural language and define program behavior. For example, you can instruct as follows:

**Example:**

```text
Create a Dog class.
The Dog class should have properties for name (string type) and age (numeric type).
The Dog class should have a bark() method.
The bark() method should output "Woof!".

Create a dog object named Pochi.
Pochi's age is 3 years old.

Instruct Pochi to bark.
```

**AI Response (Normal Response):**

```text
Woof!
```

The AI interprets this instruction as follows:

1. Create a blueprint called `Dog class`.
2. Give the `Dog class` attributes (properties) called `name` and `age`.
3. Give the `Dog class` an action (method) called `bark`.
4. The `bark` method outputs "Woof!".
5. Create an object (instance) named `Pochi` from the `Dog class`.
6. Set the `age` property of `Pochi` to `3`.
7. Execute the `bark` method of `Pochi`.

Then, the AI responds with "Woof!".

**Generating Dog Class Definition (OOPD Format):**

Furthermore, by the following instruction, the AI structures and outputs the above instructions and responses (here, the normal response and the result of method execution) in OOPD format.

**Instruction to AI:**

```text
Output the above instructions and responses in OOPD format.
```

**AI Response (OOPD Format):**

```Markdown
## Dog Class (DogClass)

**Properties:**
  - `Name (String)`: Dog's name
  - `Age (Numeric)`: Dog's age

**Methods:**
  - `Bark(): String`: Dog barks. Returns "Woof!".

## Object Creation

- `Pochi`: DogClass
  - `Name`: "Pochi"
  - `Age`: 3

## Method Execution

Pochi.Bark() -> "Woof!"
```

## 5. OOPD Format Class Definition and Usage Example

The following shows a class definition written in OOPD format and an example of its use.

```Markdown
## Number List Processor Class (NumberListProcessorClass)

**Properties:**
  - `Number List (List<Numeric>)`: A list of numbers

**Methods:**
  - `Calculate Total Detailed(): Numeric`: Calculates the sum of the number list using detailed steps.
    ---
    Total = 0
    Repeat for each element in the number list:
        Total = Total + Element
    Return Total
    ---

  - `Calculate Total Concise(): Numeric`: Calculates the sum of the number list.
```

**Usage Example:**

```text
Create a number list processing object with the number list set to [1, 2, 3, 4, 5].
Execute the Calculate Total Detailed method with the number list processing object.
Execute the Calculate Total Concise method with the number list processing object.
```

**AI Response (Example):**

```text
Result of Calculate Total Detailed: 15
Result of Calculate Total Concise: 15
```

**Explanation:**

In the example above, a `Number List Processor Class` is defined. This class has a `Number List` property and two methods: `Calculate Total Detailed` and `Calculate Total Concise`.

- The `Calculate Total Detailed` method calculates the sum of the number list according to the detailed steps described in pseudo-code.
- The `Calculate Total Concise` method has only a simple definition: "Calculates the sum of the number list." However, the AI understands that this method calculates the sum of the number list from the class context and the method name and operates appropriately.

In this way, by using the OOPD format, you can use detailed instructions (pseudo-code) and concise instructions that leave the autonomous judgment to the AI within the same class.

## 6. Introduction of Practical Class: Human Class

As an application example of OOPD, we introduce a simple `Human Class`. This class has basic attributes for representing humans and can be used to generate more human-like responses in interactions with AI.

```Markdown
## Human Class (HumanClass)

**Properties:**
  - `Name (String)`: Human's name (display name).
  - `Age (Numeric)`: Age.
  - `Gender (String)`: Gender ("Male", "Female", "Other", etc.).
  - `Height (Numeric)`: Height (cm).
  - `Weight (Numeric)`: Weight (kg).
  - `Emotion (String)`: Current emotion ("Joy", "Sadness", "Anger", etc.).
  - `First Person Pronoun (String)`: First-person pronoun ("I", "Me", etc.).
  - `Second Person Pronoun (String)`: Second-person pronoun ("You", etc.).
  - `Tone (String)`: Tone ("Polite", "Normal", "Rude", etc.).
  - `Sentence Ending (String)`: Characteristic sentence ending ("です", "ます", "だ", "である", "～ね", "～よ", etc. - Japanese examples).
```

**Usage Example of Human Class:**

The following shows a prompt written in OOPD format that creates three humans using the `Human Class` and makes them converse.

Human Class Instance Generation (YAML Format):

```YAML
Taro:
  Class: HumanClass
  Properties:
    Name: Taro
    Age: 25
    Gender: Male
    Height: 175
    Weight: 70
    Emotion: Normal
    First Person Pronoun: I (More like "Boku," a casual male pronoun)
    Second Person Pronoun: You (More like "Kimi," a friendly pronoun)
    Tone: Normal
    Sentence Ending: [None/Plain] (Speaks plainly/informally)
Jiro:
  Class: HumanClass
  Properties:
    Name: Jiro
    Age: 30
    Gender: Male
    Height: 180
    Weight: 80
    Emotion: Anger
    First Person Pronoun: I (More like "Ore," a rough male pronoun)
    Second Person Pronoun: You (Rude)
    Tone: Rude
    Sentence Ending: [None/Plain] (Speaks bluntly/aggressively)
Hanako:
  Class: HumanClass
  Properties:
    Name: Hanako
    Age: 22
    Gender: Female
    Height: 160
    Weight: 55
    Emotion: Joy
    First Person Pronoun: I (More like "Watashi," a polite pronoun)
    Second Person Pronoun: You (Polite)
    Tone: Polite
    Sentence Ending: "Desu/Masu" (Speaks politely/formally)
```

Conversation Instruction (Markdown Format):

```Markdown
## Conversation Instruction

Theme: How to spend this weekend

Roles:
  - Taro: Proposer (actively proposes)
  - Hanako: Cautious (considers risks)
  - Jiro: Moody (reacts emotionally)

Have Taro, Hanako, and Jiro converse based on the above theme and roles.
```

**AI Response (Example):**

```text
Taro: "Hey everyone, how about going camping this weekend? The weather looks perfect!"
Hanako: "Camping... That sounds fun, but I saw a news report recently about bears appearing. Are you sure it's safe?"
Jiro: "Bears!? That's a pain... I'd rather just laze around at home."
Taro: "It'll be fine! I'll prepare bear spray and everything. Besides, isn't it great to sit around a campfire and talk with everyone?"
Hanako: "Well... If we prepare properly, it might be fun. What do you think, Jiro?"
Jiro: "...Well, if there's good meat to eat, I might consider it."
```

**Explanation:**

In this example, we use the `Human Class` to create three instances (objects): `Taro`, `Hanako`, and `Jiro`. Each instance has different properties (name, age, gender, emotion, tone, etc.). The YAML format is used to generate the instances.

The conversation instruction sets the theme of "How to spend this weekend" and the role of each character (proposer, cautious, moody). The AI refers to this information and the properties of each instance (especially `First Person Pronoun`, `Second Person Pronoun`, `Tone`, and `Sentence Ending`) to generate appropriate wording and role-based statements for each character.

## 7. Application Examples of Inheritance, Events, and Interfaces: Monitoring System

Here, we create a `Monitored Human Class` inherited from the `Human Class` and show an example of a monitoring system that utilizes events and interfaces.

```Markdown
## Log Recording Interface (ILogger)

**Methods:**
  - `Log(Message: String)`: Records a log message.

## Monitored Human Class (MonitoredHumanClass)

**Base Class:** Human Class (HumanClass)

**Properties:**
  - `Previous Emotion (String)`: Records the previous emotion.

**Events:**
  - `Emotion Change Event(Before Change: String, After Change: String)`: An event that occurs when the emotion changes.

**Methods:**
  - `Set Emotion(New Emotion: String)`: Sets the emotion and issues an emotion change event if there is a change.

## Log Recording Class (LoggerClass)
**Interface Implementation:** Log Recording Interface (ILogger)

**Methods:**
  - `Log(Message: String)`: Outputs a message to the log.
```

**Usage Example:**

```Markdown
## Instance Generation Instructions

- Taro: Instance of Human Class
- Jiro: Instance of Monitored Human Class
- Hanako: Instance of Human Class (does not participate directly in the conversation)

## Initial Value Settings for Each Instance

- `Taro`:
  Name: Taro
  Age: 25
  Gender: Male
  Height: 175
  Weight: 70
  Emotion: Normal
  First Person Pronoun: I (More like "Boku," a casual male pronoun)
  Second Person Pronoun: You (More like "Kimi," a friendly pronoun)
  Tone: Normal
  Sentence Ending: [None/Plain] (Speaks plainly/informally)

- `Jiro`:
  Name: Jiro
  Age: 30
  Gender: Male
  Height: 180
  Weight: 80
  Emotion: Normal
  First Person Pronoun: I (More like "Ore," a rough male pronoun)
  Second Person Pronoun: You (Rude)
  Tone: Rude
  Sentence Ending: [None/Plain] (Speaks bluntly/aggressively)
  Previous Emotion: Normal (Property of MonitoredHumanClass)

- `Hanako`:
  Name: Hanako
  Age: 22
  Gender: Female
  Height: 160
  Weight: 55
  Emotion: Joy
  First Person Pronoun: I (More like "Watashi," a polite pronoun)
  Second Person Pronoun: You (Polite)
  Tone: Polite
  Sentence Ending: "Desu/Masu" (Speaks politely/formally)

## Log Recording Settings

Create a log recording object.

Subscribe to Jiro's emotion change event, and register an event handler that uses the log method of the log recording object to output the emotions before and after the change to the log.

## Conversation Instruction

Theme: Planning Hanako's surprise birthday party

Roles:
  - Taro: Planner (actively promotes the plan)
  - Jiro: Collaborator (helps Taro's plan)
  - Hanako: (Because she is the target of the surprise, she does not participate directly in the conversation. However, Taro and Jiro talk while guessing Hanako's feelings)

Have Taro and Jiro talk about planning Hanako's surprise birthday party based on the above theme and roles.
```

**AI Response (Conversation Example):**

```text
Taro: "Hey Jiro, Hanako's birthday is coming up, right? Let's throw her a surprise party!"
Jiro: "Oh, good idea! Hanako hasn't been feeling so great lately, so I hope she'll be happy." (Emotion: Anticipation)
Taro: "Yeah! So, what should we do... Hanako said she wanted to go camping recently, right?"
Jiro: "Yeah, she did. But isn't she afraid of bugs?" (Emotion: Concern)
Taro: "Oh... That's right. Then, instead of camping, how about getting tickets to Hanako's favorite artist's concert?"
Jiro: "Oh, that's a great idea! She'll definitely be happy!" (Emotion: Joy)
Taro: "Okay, I'll go ahead and get the tickets... What?! Sold out!? Seriously..." (Emotion: Disappointment)
Jiro: "Oh no, really... We have to think of another plan..." (Emotion: Disappointment)
Taro: "Hmm... How about making a reservation at a restaurant that Hanako likes and having a party there?"
Jiro: "Oh, that's definitely a safe bet. Okay, let's go with that!" (Emotion: Relief)
```

**Log Output (Example):**

```text
[Log] Jiro's emotion change: Normal -> Anticipation
[Log] Jiro's emotion change: Anticipation -> Concern
[Log] Jiro's emotion change: Concern -> Joy
[Log] Jiro's emotion change: Joy -> Disappointment
[Log] Jiro's emotion change: Disappointment -> Relief
```

**Explanation:**

- **Instance Generation Instructions:** Taro, Jiro and Hanako are explicitly instructed as to which class to use respectively.
- **Initial Value Settings:** The properties of each instance are set in a form similar to YAML format.
- **Log Recording Settings:** A `Log Recording Object` is created, and an event handler is registered to subscribe to `Jiro`'s `Emotion Change Event`.
- **Conversation Instruction:** Clearly instructs the theme, roles, and participants of the conversation.
- **AI Response (Conversation Example):** A conversation between Taro and Jiro is generated. Jiro's emotions change according to the development of the conversation, and each time the `Set Emotion` method is called and the `Emotion Change Event` is generated.
- **Log Output (Example):** According to the `Emotion Change Event`, the `Log` method of the `Log Recording Object` is called, and the emotion change is output to the log.

In this example, we build a flexible and scalable monitoring system by combining inheritance, events, and interfaces. The `MonitoredHumanClass` has the functions of the `HumanClass` and adds a new function of emotion monitoring.

## 8. Precautions When Leaving Processing to AI: Fluctuations and Countermeasures

In OOPD, you can simplify the definition of methods and entrust the specific processing details to AI (e.g., the `Calculate Total Concise` method of the `Number List Processor Class`). This approach offers benefits such as flexibility and descriptive efficiency, but also comes with the caveat that "fluctuations" in the processing content may occur due to AI interpretation.

### 8.1. Merits

- **Flexibility:** AI can autonomously determine and execute the optimal processing according to the context and situation of the prompt. This eliminates the need to define all processing patterns in detail in advance and may allow for handling unforeseen situations.
- **Descriptive Efficiency:** Instead of describing detailed algorithms, programmers can simply instruct the desired result in natural language. This reduces the amount of prompt text and improves development efficiency.
- **AI Knowledge Utilization:** AI can utilize its own knowledge and learning data to perform instructed tasks at a more advanced level. For example, it may automatically perform not only simple numerical summation but also statistical analysis and outlier detection.

### 8.2. Demerits

- **Uncertainty of Processing Content:** Because AI performs processing based on prompt interpretation and its own knowledge, the results are not always what the programmer intended. In particular, if the instructions are ambiguous or AI's knowledge is insufficient, unexpected results may occur.
- **Difficulty of Debugging:** Because the processing content is left to the AI, it can be difficult to identify and correct the cause of an error. In order to understand what kind of judgment the AI made in processing, it may be necessary to analyze detailed logs or interact with the AI.
- **Reproducibility Issues:** Even if the same prompt is given to the same AI, different results may be obtained due to changes in the AI's internal state or learning data. This can be a problem in fields that require strict reproducibility, such as scientific and technical calculations and financial transactions.

### 8.3. Countermeasures Against Fluctuations

In order to minimize fluctuations when leaving processing to AI and obtain more reliable results, the following measures can be considered:

- **Clear and Specific Instructions:** Prompts should be written as specifically and clearly as possible, eliminating ambiguity. Instead of "Calculate the sum of the number list," it is important to clearly convey the expected processing content, such as "Simply add each element of the number list to find the sum."
- **Adding Constraints:** It is also effective to set constraints to limit the scope of AI's actions. By instructing specific conditions, such as "Exclude elements that exceed a specific value when calculating the sum," you can narrow the range of AI interpretation and prevent unintended processing.
- **Testing and Feedback:** For methods using concise instructions, it is important to test using various input data and confirm that the expected results are obtained. If unintended results are obtained, you can gradually improve the AI's behavior by modifying the prompt or giving feedback to the AI.
- **Detailed Log Output:** It is recommended to design the system to output detailed logs in order to understand what kind of judgment the AI made in processing. This makes debugging easier and helps identify the cause when problems occur.
- **Combined Use with Detailed Version:** For important processing, it is also effective to prepare both a method that describes detailed steps (e.g., the `Calculate Total Detailed` method of the `Number List Processor Class`) and a method based on concise instructions, and use them selectively depending on the situation.
- **AI Model Selection:** It is also important to understand the characteristics of the AI model used and select a model that is suitable for the task. By selecting a model specialized for a specific task or a model with higher accuracy, it is possible to reduce fluctuations.

### 8.4. 5.4 Summary

Entrusting tasks to AI is not always a bad thing.
Entrusting tasks to AI is a powerful approach in prompt engineering, and by taking appropriate measures as described above, it is possible to maximize its merits while minimizing its demerits.

## 9. Conclusion

In this paper, we proposed a new concept of "Object-Oriented Prompt Programming" using natural language, and introduced OOPD (Object-Oriented Terminology for Prompt Design) as its specific framework.

OOPD brings the following benefits by incorporating object-oriented thinking into conventional prompt engineering:

- **Prompt Structuring:** Prompts can be described in a more organized and easy-to-understand form using concepts such as classes, objects, and methods.
- **Improved Reusability:** Defined classes and methods can be reused in different prompts, improving development efficiency.
- **Improved Maintainability:** By structuring prompts, modifications and changes become easier.
- **More Advanced Communication with AI:** Through object-oriented concepts, it becomes possible to give more complex and sophisticated instructions to AI.

However, at present, OOPD is still a developing technology, and the following challenges remain:

- **Prompt Text Bloat:** Especially when giving detailed instructions, the prompt text tends to become long.
- **Processing Speed Reduction:** Processing speed may be reduced because AI interprets and executes complex prompts.
- **AI Model Support:** In order to maximize the benefits of OOPD, support on the AI model side is also required.

Further research and development is necessary in the future to overcome these challenges and make OOPD a more practical technology.

In the future, AI model evolution may lead to a future where prompt engineering itself becomes unnecessary. However, until then, OOPD can be an effective means of achieving smoother and more efficient communication between humans and AI. We hope that this paper will help deepen the discussion on object-oriented prompt programming and new ways of interacting with AI.
