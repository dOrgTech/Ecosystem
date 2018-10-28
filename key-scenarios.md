<head>
    <meta charset='UTF-8'>
    <title>Progress Bars</title>
    <link rel='stylesheet' href='./style.css'>
    <script>
        var ProgressBarProto = Object.create(HTMLElement.prototype);
        ProgressBarProto.createdCallback = function() {
            var shadow = this.createShadowRoot();
            var div = document.createElement("div");
            div.className = "meter red";
            var span = document.createElement("span");
            span.style = "width: 80%";
            div.appendChild(span);
            shadow.appendChild(div);
            // TODO: figure out why this doesn't work
            // - add property to make it easier
            // - desired result <progress-bar completed:"50%"></progress-bar>
        };
        var ProgressBar = document.registerElement("progress-bar", {
            prototype: ProgressBarProto
        });
    </script>
</head>

# Key Scenarios  
This is a high level, technology independent look at the scenarios we're interested in enabling.  

### Feature Groups  
[Legal]  
[Finance]  
[Community]  
[Development]  
[Project Management]  
[*] == all groups above  

|  # | Scenario | Feature Group(s) | % Realized |  
| -- | -------- | ---------------- | ---------- |  
|  0 | [Scenario Spec Template](./scenario-specs/0-spec-template.md) | | 0%<div class="meter red"><span style="width: 1%"></span></div> |  
|  1 | [dOrg Setup and Configuration](./scenario-specs/1-setup-and-configure.md) | [*] | <progress-bar completed="50%"> </progress-bar> |  
|  2 | [Optional dOrg Visibility](./scenario-specs/2-optional-dorg-visibility.md) | [*] | |  
|  3 | [Open dOrg Participation](./scenario-specs/3-open-dorg-participation.md) | [*] | |  
|  4 | [Closed dOrg Participation](./scenario-specs/4-closed-dorg-participation.md) | [*] | |  
|  5 | [Browse a dOrg](./scenario-specs/5-browse-a-dorg.md) | [Community] | |  
|  6 | [dOrgs Are Discoverable](./scenario-specs/6-dorgs-are-discoverable.md) | [Community] | |  
|  7 | [User Profiles](./scenario-specs/7-user-profiles.md) | [Community] | |  
|  8 | [Support Attested Users](./scenario-specs/8-support-attested-users.md) | [Legal]<br>[Community] | |  
|  9 | [Support Anon Users](./scenario-specs/9-support-anon-users.md) | [Legal]<br>[Community] | |  
| 10 | [Instant Communication](./scenario-specs/10-instant-communication.md) | [Community]<br>[Project Management] | |  
| 11 | [Structured Communication](./scenario-specs/11-structured-communication.md) | [Community]<br>[Project Management] | |  
| 12 | [Add Contributors to dOrg](./scenario-specs/12-add-contributors-to-dorg.md) | [Community]<br>[Project Management] | |  
| 13 | [Task Creation](./scenario-specs/13-task-creation.md) | [Project Management] | |  
| 14 | [Task Rewards](./scenario-specs/14-task-rewards.md) | [Project Management] | |  
| 15 | [Consensus Functionality and Applicability](./scenario-specs/15-consensus-functionality-and-applicability.md) | [Project Management] | |  
| 16 | [Task Prioritization, Grouping, and Dependencies](./scenario-specs/16-task-prioritization-grouping-and-dependencies.md) | [Project Management] | |  
| 17 | [Repository Connections](./scenario-specs/17-repository-connections.md) | [Development]<br>[Project Management] | |  
| 18 | [Automated Deployments](./scenario-specs/18-automated-deployments.md) | [*] | |  
| 19 | [Funding / Investing](./scenario-specs/19-funding-investing.md) | [Finance] | |  
| 20 | [Enable Verifiable Revenue Streams](./scenario-specs/20-enable-verifiable-revenue-streams.md) | [Legal]<br>[Finance] | |  
| 21 | [Legal Agreements](./scenario-specs/21-legal-agreements.md) | [Legal] | |  
