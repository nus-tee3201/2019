<frontmatter>
title: "Full Schedule of Module Activities"
footer: footer.md
head: scheduleHead.md
</frontmatter>

{% import "common/outcomes.njk" as outcomes with context %}

{% set weeks = [
    {num: "1", day:"Jan 14"},
    {num: "2", day:"Jan 21"},
    {num: "3", day:"Jan 28"},
    {num: "4", day:"Feb 4"},
    {num: "5", day: "Feb 11" },
    {num: "6", day: "Feb 18" },
    {num: "7", day: "Mar 4" },
    {num: "8", day: "Mar 11" },
    {num: "9", day: "Mar 18" },
    {num: "10", day: "Mar 25" },
    {num: "11", day: "Apr 1" },
    {num: "12", day: "Apr 8" },
    {num: "13", day: "Apr 12" }
] %}


{% set current_weeks = ["1"] %}


{% set all_outcomes = [
{week: "1"},
  {name: "SE Intro"},
    {heading: "SE: Intro"},
      {location: ["softwareEngineering", "introduction", "prosAndCons"]},
{week: "2"},
  {name: "Activity Diagrams"},
    {heading: "Activity Diagrams"},
      {location: ["modeling", "modelingBehaviors", "activityDiagrams"]},
      {location: ["modeling", "modelingBehaviors", "activityDiagramsIntermediate"], omit_evidence: true},
  {name: "Requirements"},
    {heading: "Requirements: Intro"},
      {location: ["requirements", "introduction"], omit_evidence: true},
      {location: ["requirements", "nonFunctionalRequirements"], omit_evidence: true},
      {location: ["requirements", "prioritizing"], omit_evidence: true},
      {location: ["requirements", "quality"], omit_evidence: true},
    {heading: "Gathering Requirements"},
      {location: ["gatheringRequirements", "brainstorming"], omit_evidence: true},
      {location: ["gatheringRequirements", "productSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "observation"], omit_evidence: true},
      {location: ["gatheringRequirements", "userSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "interviews"], omit_evidence: true},
      {location: ["gatheringRequirements", "focusGroups"], omit_evidence: true},
      {location: ["gatheringRequirements", "prototyping"], omit_evidence: true},
{week: "3"},
  {name: "Requirements"},
    {heading: "Specifying Requirements"},
      {subheading: "Prose"},
        {location: ["specifyingRequirements", "prose", "what"], omit_evidence: true},
      {subheading: "Feature Lists"},
        {location: ["specifyingRequirements", "featureList", "what"], omit_evidence: true},
      {subheading: "User Stories"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"], omit_evidence: true},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Use Cases"},
        {location: ["specifyingRequirements", "useCases", "introduction"], omit_evidence: true},
        {location: ["specifyingRequirements", "useCases", "identifying"], omit_evidence: true},
        {location: ["specifyingRequirements", "useCases", "details"]},
        {location: ["specifyingRequirements", "useCases", "usage"], omit_evidence: true},
      {subheading: "Glossary"},
        {location: ["specifyingRequirements", "glossary", "what"], omit_evidence: true},
      {subheading: "Supplementary Requirements"},
        {location: ["specifyingRequirements", "supplementaryRequirements", "what"], omit_evidence: true},
{week: "4"},
  {name: "Design"},
    {heading: "Design Principles: Basics"},
      {subheading: "Abstraction"},
        {location: ["designFundamentals", "abstraction", "what"], omit_evidence: true},
  {name: "OOP"},
    {heading: "OOP: Classes & Objects"},
      {location: ["oop", "introduction", "what"], omit_evidence: true},
      {location: ["oop", "objects", "what"], omit_evidence: true},
      {location: ["oop", "objects", "abstraction"], omit_evidence: true},
      {location: ["oop", "objects", "encapsulation"], omit_evidence: true},
{week: "5"},
  {name: "Implementation"},
    {heading: "Exception Handling"},
      {location: ["errorHandling", "introduction", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "how"]},
      {location: ["errorHandling", "exceptions", "when"], omit_evidence: true},
{week: "6"},
  {name: "Project Management"},
    {heading: "Project Mgt: Scheduling and Tracking"},
      {location: ["projectPlanning", "milestones"]},
      {location: ["projectPlanning", "buffers"]},
      {location: ["projectPlanning", "issueTrackers"]},
      {location: ["projectPlanning", "workBreakdownStructure"]},
      {location: ["projectPlanning", "ganttCharts"], omit_evidence: true},
      {location: ["projectPlanning", "pertCharts"], omit_evidence: true},
      {location: ["teamwork", "teamStructures"]},
{week: "7"},
  {name: "Implementation"},
    {heading: "IDEs: Basic Features"},
      {location: ["ides", "introduction", "what"]},
      {location: ["ides", "debugging", "what"], omit_evidence: true},
    {heading: "Integration Approaches"},
      {location: ["integration", "introduction", "what"], omit_evidence: true},
      {location: ["integration", "approaches", "lateVsEarly"], omit_evidence: true},
      {location: ["integration", "approaches", "bigBangVsIncremental"], omit_evidence: true},
      {location: ["integration", "approaches", "topDownVsBottomUp"], omit_evidence: true},
  {name: "Project Management"},
    {heading: "SDLC Process Models"},
      {location: ["processModels", "introduction", "what"], omit_evidence: true},
      {location: ["processModels", "introduction", "sequentialModels"]},
      {location: ["processModels", "introduction", "iterativeModels"]},
      {location: ["processModels", "introduction", "agileModels"]},
      {location: ["processModels", "exampleProcessModels", "scrum"], evidence: "project.md#relate_process"},
      {location: ["processModels", "exampleProcessModels", "xp"], evidence: "project.md#relate_process"},
      {location: ["processModels", "exampleProcessModels", "unifiedProcess"], evidence: "project.md#relate_process"},
      {location: ["processModels", "more", "cmmi"], omit_evidence: true},
      {location: ["processModels", "summary", "recap"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"], omit_evidence: true},
{week: "8"},
  {name: "Testing"},
    {heading: "Automated Testing of Text UIs"},
      {location: ["testing", "introduction", "what"]},
      {location: ["testing", "testingTypes", "regressionTesting", "what"]},
      {location: ["testing", "testAutomation", "what"], omit_evidence: true},
      {location: ["testing", "testAutomation", "testingTextUis"]},
{week: "9"},
  {name: "OOP"},
    {heading: "OOP: classes"},
      {location: ["oop", "classes", "what"], omit_evidence: true},
      {location: ["oop", "classes", "classLevelMembers"], omit_evidence: true},
  {name: "Design"},
    {heading: "Design: Models"},
      {location: ["modeling", "introduction", "what"], omit_evidence: true},
      {location: ["modeling", "introduction", "how"]},
    {heading: "Class/Ojbect Diagrams: Basics"},
      {location: ["modeling", "modelingStructures", "ooStructures"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
      {location: ["modeling", "modelingStructures", "objectDiagrams"]},
      {location: ["uml", "miscellaneous", "objectVsClassDiagrams"], omit_evidence: true},
      {location: ["uml", "notes", "notes"], omit_evidence: true},
      {location: ["uml", "notes", "constraints"], omit_evidence: true},
      {location: ["uml", "classDiagrams", "associationsAsAttributes", "what"], omit_evidence: true},
{week: "10"},
  {name: "OOP"},
    {heading: "OOP: Inheritance"},
      {location: ["oop", "inheritance", "what"], omit_evidence: true},
      {location: ["oop", "inheritance", "overloading"], omit_evidence: true},
      {location: ["oop", "inheritance", "overriding"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Coding Standards"},
      {location: ["codeQuality", "introduction", "basic"], omit_evidence: true},
      {location: ["codeQuality", "followStandard", "introduction"]},
      {location: ["codeQuality", "followStandard", "basic"]},
      {location: ["codeQuality", "followStandard", "intermediate"]},
    {heading: "CodeQuality: Readability"},
      {location: ["codeQuality", "maximiseReadability", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidLongMethods"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidDeepNesting"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidComplicatedExpressions"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidMagicNumbers"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "basic", "makeCodeObvious"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "structureCodeLogically"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "dontTripReader"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "practiceKISSing"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "avoidPrematureOptimizations"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "slapHard"], omit_evidence: true},
      {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"], omit_evidence: true},
    {heading: "CodeQuality: Naming"},
      {location: ["codeQuality", "nameWell", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "useStandardWords"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"], omit_evidence: true},
    {heading: "CodeQuality: Unsafe Practices"},
      {location: ["codeQuality", "avoidShortcuts", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "useDefaultBranch"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "dontRecycleVarsOrParams"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "avoidEmptyCatchBlocks"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "deleteDeadCode"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseVariableScope"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseCodeDuplication"], omit_evidence: true},
    {heading: "CodeQuality: Code Comments"},
      {location: ["codeQuality", "commentMinimally", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Refactoring: Basics"},
      {location: ["refactoring", "what"]},
      {location: ["intellij", "refactoring"]},
      {location: ["refactoring", "how"]},
      {location: ["refactoring", "when"]},
{week: "11"},
  {name: "Quality Assurance"},
    {heading: "Developer Testing: Basics"},
      {location: ["testing", "testingTypes", "developerTesting", "what"], omit_evidence: true},
      {location: ["testing", "testingTypes", "developerTesting", "why"]},
      {location: ["testing", "testAutomation", "usingTestDrivers"], omit_evidence: true},
      {location: ["testing", "testAutomation", "tools"], omit_evidence: true},
    {heading: "Types of Testing"},
      {subheading: "Unit Testing"},
        {location: ["testing", "testingTypes", "unitTesting", "what"]},
        {location: ["testing", "testingTypes", "unitTesting", "stubs"]},
        {location: ["testing", "dependencyInjection", "what"], omit_evidence: true},
        {location: ["testing", "dependencyInjection", "how"], omit_evidence: true},
      {subheading: "Integration Testing"},
        {location: ["testing", "testingTypes", "integrationTesting", "what"]},
        {location: ["testing", "testingTypes", "integrationTesting", "how"]},
      {subheading: "System Testing"},
        {location: ["testing", "testingTypes", "systemTesting", "what"]},
        {location: ["testing", "testAutomation", "testingGuis"]},
      {subheading: "Acceptance Testing"},
        {location: ["testing", "testingTypes", "acceptanceTesting", "what"]},
        {location: ["testing", "testingTypes", "acceptanceTesting", "acceptanceVsSystemTesting"]},
      {subheading: "Alpha/Beta Testing"},
        {location: ["testing", "testingTypes", "alphaBetaTesting", "what"]},
    {heading: "Test Case Design"},
      {location: ["testCaseDesign", "introduction", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "when"], omit_evidence: true},
      {location: ["testCaseDesign", "introduction", "positiveVsNegative"]},
      {location: ["testCaseDesign", "introduction", "blackVsGlass"]},
      {location: ["testCaseDesign", "more", "testingUseCases"]},
    {heading: "Equivalence Partitioning"},
      {location: ["testCaseDesign", "equivalencePartitions", "what"], omit_evidence: true},
      {location: ["testCaseDesign", "equivalencePartitions", "basic"], omit_evidence: true},
      {location: ["testCaseDesign", "equivalencePartitions", "intermediate"]},
    {heading: "Boundary Value Analysis"},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "what"], omit_evidence: true},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "how"], omit_evidence: true},
    {heading: "Other QA Techniques"},
      {location: ["qualityAssurance", "introduction", "what"], omit_evidence: true},
      {location: ["qualityAssurance", "introduction", "validationVsVerification"]},
      {location: ["qualityAssurance", "codeReviews", "what"]},
      {location: ["qualityAssurance", "staticAnalysis", "what"]},
      {location: ["qualityAssurance", "formalVerification", "what"], omit_evidence: true},
{week: "12"},
  {name: "Implementation"},
    {heading: "Reuse: APIs, Frameworks, Libraries, Platforms"},
      {subheading: "Reuse"},
        {location: ["reuse", "introduction", "what"], omit_evidence: true},
        {location: ["reuse", "introduction", "when"]},
      {subheading: "APIs"},
        {location: ["reuse", "apis", "what"]},
      {subheading: "Libraries"},
        {location: ["reuse", "libraries", "what"]},
        {location: ["reuse", "libraries", "how"]},
      {subheading: "Frameworks"},
        {location: ["reuse", "frameworks", "what"]},
        {location: ["reuse", "frameworks", "frameworksVsLibraries"]},
      {subheading: "Platforms"},
        {location: ["reuse", "platforms", "what"]},
    {heading: "Cloud Computing"},
      {location: ["reuse", "cloudComputing", "what"], omit_evidence: true},
      {location: ["reuse", "cloudComputing", "services"], omit_evidence: true},
  {name: "Design"},
    {heading: "Other UML Models"},
      {location: ["modeling", "modelingStructures", "deploymentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "componentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "packageDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "compositeStructureDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "timingDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "interactionOverviewDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "communicationDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "stateMachineDiagrams"], omit_evidence: true},
  {name: "Revision Control"},
    {heading: "RCS: Revision History"},
      {location: ["revisionControl", "what"]},
      {location: ["revisionControl", "repositories"]},
  {name: "Documentation"},
    {heading: "Writing Developer Documents"},
      {subheading: "Type of Developer Docs"},
        {location: ["documentation", "introduction", "what"]},
      {subheading: "Guideline: Aim for Comprehensibility"},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "how"]},
      {subheading: "Guideline: Describe Top-Down"},
        {location: ["documentation", "guidelines", "goTopDown", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "goTopDown", "why"]},
        {location: ["documentation", "guidelines", "goTopDown", "how"]},
      {subheading: "Guideline: Minimal but Sufficient"},
        {location: ["documentation", "guidelines", "documentMinimally", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "documentMinimally", "how"], omit_evidence: true},

{week: "13"}
]%}


{% macro show_week_outcomes(week_num, path="") %}
<panel type="seamless" popup-url="{{baseUrl}}/schedule/week{{ week_num }}/outcomes.html" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_outcome }} Outcomes</span>
  <div class="indented">
  {{ outcomes.show_week_schedule_main(week_num, all_outcomes, path) }}
  </div>
</panel>
{% endmacro %}


{% macro show_week_todos(week_num, path="") %}
<panel type="seamless" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_todo }} Todo</span>
  <div class="indented">
  <include src="{{ path }}todo.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_tutorial(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_tutorial }} Tutorial {{ week_num }}</span>
   <div class="indented">
   <include src="{{ path }}tutorial.md" />
   </div>
</panel>
{% endmacro %}


{% macro show_week_lecture(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_lecture }} Lecture {{ week_num }}</span>
  <div class="indented">
  <include src="{{ path }}lecture.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_schedule(week_num_string, path="") %}

{% set week_num_int = week_num_string | int %}
{% set week = weeks[week_num_int - 1] %}

<include src="../../common/header.md" />

<div class="website-content" id="main">

{{ show_nav_buttons(week.num) }}

{{ show_week_schedule_body(week, path) }}

</div>

{% endmacro %}


{% macro show_nav_buttons(week_num) %}
{% set week_num = week_num | int %}
{% if week_num != 1 %}<span style="float:left"><md>[{{ glyphicon_chevron_left }} Previous Week]({{ baseUrl }}/schedule/week{{ (week_num - 1) }}/)</md></span>{% endif %}{% if week_num != 13 %}<span style="float:right"><md>[Next Week {{ glyphicon_chevron_right }}]({{ baseUrl }}/schedule/week{{ (week_num + 1) }}/)</md></span>{% endif %}<br>

{% endmacro %}


{% macro show_week_schedule_body(week, path="") %}

# Week {{ week.num }} <small><small>%%[{{ week.day }}]%%</small></small>

<include src="{{ path }}notices-{{ module | lower }}.md" optional />

<tabs>
  <tab header="{{ fas_graduation_cap }} SE Topics">
    <include src="{{ path }}topics.md" />
  </tab>
  <tab header="{{ fas_laptop_code }} Programming Topics">
    <include src="{{ path }}../python-topics.md#week{{ week.num }}" />
  </tab>
</tabs>

{% endmacro %}




<!-- ============================= page content ============================================ -->

<include src="../common/header.md" />

<div class="website-content" id="main">

{{ show_nav_buttons(current_weeks[0]) }}

{% for week in weeks %}
{% set week_num = week.num | int %}
{% if week.num in current_weeks %}
  {{ show_week_schedule_body(week, "week" + week_num + "/") }}
<br>
<br>
{% endif %}
{% endfor %}

</div>