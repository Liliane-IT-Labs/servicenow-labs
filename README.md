# ServiceNow IT Support: Incident, Problem, Knowledge, and Service Request Management

**Hands-on portfolio project | ServiceNow training simulator | IT Support / Help Desk**

## 1. Real-World Scenario (Context)

Imagine you are an **IT Support Technician** helping employees at a company. Employees report computer issues, request equipment and software, and need instructions for common tasks such as resetting passwords. Your team also investigates a network server that keeps going offline. You use **ServiceNow** to track the work, organize urgent incidents, document a recurring problem, monitor workloads, and guide employees to self-service resources.

**Simple analogy:** ServiceNow is a help-desk notebook, a request counter, a team task board, and a reporting dashboard in one place.

### What this project demonstrates

- Navigating ServiceNow as a **Platform User** in a training simulator.
- Pinning the **All** menu and favoriting the **Knowledge** module.
- Filtering, sorting, mass-editing, and personalizing **incident** lists.
- Creating a **Problem** record for a repeating network outage.
- Organizing work on a **Visual Task Board**.
- Building a **pie chart** and a dashboard for open incidents.
- Requesting a new **Knowledge Base** through Employee Center.
- Requesting office equipment and software from the **Service Catalog**.
- Finding a password-reset article using the **Virtual Agent**.

---

## Lab 1 — Personalize the ServiceNow Workspace

### Real-life context

You start a new help-desk shift. You want your navigation menu to stay visible and your most-used knowledge articles to be one click away.

### Goal

Impersonate **Platform User**, pin **All**, and add **Self-Service > Knowledge** to Favorites.

### Step-by-step in the simulator

1. Launch the ServiceNow training simulator. It logs you in as **System Administrator** for this lab.
2. Look at the **top-right corner** and click the **System Administrator avatar/user menu**.
3. Choose **Impersonate user**.
4. In the search or selection field, find **Platform User** (user ID: `platform.user`).
5. Select **Platform User** from the results.
6. Click the **Impersonate user** button to confirm.
7. Verify that you are now operating as **Platform User**.
8. Open the **All** navigation menu.
9. Click its **pin icon** so the All menu stays displayed while navigating.
10. If the menu disappears when your browser window is narrow, **maximize or widen** the window.
11. In **All**, navigate to **Self-Service > Knowledge**.
12. Explore the Knowledge home page and available knowledge categories.
13. Find the **favorite/star control** for the Knowledge module, and select it to add **Knowledge** to Favorites.
14. Open **Favorites** and confirm **Knowledge** is listed.
15. Review what applications/modules are available to the **Platform User** role.

**Expected result:** The All menu is pinned, and Knowledge appears under Favorites.

**Evidence to capture after doing it:** `screenshots/01-all-pinned-knowledge-favorite.png`.

---

## Lab 2 — Filter, Update, and Personalize Incident Records

### Real-life context

You have many incident tickets. You need to focus on assigned, active work, find the most urgent incidents, and update several tickets efficiently.

### Goal

Display active, assigned incidents; prioritize **1 - Critical** incidents; change their states to **In Progress**; and personalize the incident list.

### Step-by-step in the simulator

1. Open **All > Incident > All**.
2. You should now see the **incident list**.
3. At the top of the list, click **Show/Hide filter** (the **funnel** icon).
4. Create the first filter condition:
   - **Field:** `State`
   - **Operator:** `is not`
   - **Value:** `Closed`
5. Add another condition connected by **AND**:
   - **Field:** `Assignment group`
   - **Operator:** `is not empty`
6. Add a third condition connected by **AND**:
   - **Field:** `Assigned to`
   - **Operator:** `is not empty`
7. Check that **all three conditions use AND**, not OR.
8. Click **Run** to apply the filter.

<img width="865" height="820" alt="image" src="https://github.com/user-attachments/assets/7d993116-50e3-40f5-843a-7aadaf5fab98" />

10. Find the **Priority** column header and click it to sort. If the order is reversed, click again, until **1 - Critical** appears at the top.
11. Look only at the **1 - Critical** rows.
12. To change a single incident, double-click its **State** cell, choose **In Progress**, and save the inline edit (the lab depicts a **green checkmark**).
13. To update multiple critical incidents with the **List Editor**, hold **Shift** and **click/drag** down the **State** cells to select a range, as described in the lab.
14. Set the selected states to **In Progress**, then click the **green checkmark** to save. The lab expects **at least 10 incident rows** to be updated. Verify your selected rows are all **1 - Critical** before editing.
<img width="1167" height="537" alt="image" src="https://github.com/user-attachments/assets/558d82ef-7dc0-4550-a4be-6475166b6224" />

16. Find **Personalize List** (the **gear** icon above the incident list).
17. In the list personalization window, remove **Opened** and **Updated by** from the selected/displayed columns.
18. Apply or confirm the column changes, depending on the simulator's controls.
<img width="1043" height="651" alt="image" src="https://github.com/user-attachments/assets/10ba4a9a-0db0-46da-ab4f-57c57e05ede6" />

20. Locate incident **`INC0000055`**. Use the list search or incident number if needed.
21. Open that incident or use inline editing on its **Category** field.
22. Set **Category** to **Software**.
23. **Save/Update** the record, and confirm it now shows **Software**.
<img width="900" height="655" alt="image" src="https://github.com/user-attachments/assets/e02da779-938b-44f2-bba0-a0de3bb440c5" />

**Expected result:** Filtered list shows non-closed, assigned incidents; the critical incidents have state **In Progress**; unwanted columns are hidden; and `INC0000055` has category **Software**.

**Why AND matters:** With **AND**, a ticket must satisfy **every** condition. With **OR**, a ticket can meet just one, which may show unrelated incidents.

---

## Lab 3 — Create and Favorite a Network Problem Record

### Real-life context

Employees keep losing access to a network server several times per week. Restarting it every time is only a short-term fix. Your team needs a **Problem record** to investigate the root cause and find a lasting solution.

**Incident vs. Problem:** An **incident** restores service after something goes wrong. A **problem** investigates why similar incidents keep happening.

### Goal

Create a **Network** problem, save it, and customize its Favorite.

### Step-by-step in the simulator

1. Navigate to **All > Problem > Create New**.
2. On the new Problem form, find **Category** and choose **Network**.
3. Find **Service** and choose **IT Services**.
4. Set **Impact** to **2 - Medium**.
5. Set **Urgency** to **2 - Medium**.
6. Observe that the lab says **Priority** automatically changes to **3 - Moderate** for these choices.
7. Find **Assignment group** and select **Network**.
8. Enter the following **Problem statement** exactly:

   `Unable to connect to network server.`

9. Enter the following **Description** exactly:

   `The department network server seems to be going down multiple times a week and I currently can't connect to it. We would like a more permanent solution.`

10. Review the six main form fields and the two text fields.
11. Open the **Form Context Menu** on the Problem form.
12. Choose **Save**. Do not confuse **Save** with deleting or closing the record.
<img width="1424" height="592" alt="image" src="https://github.com/user-attachments/assets/41f849b5-c6b7-4808-b6f6-5bb6b2d2aa81" />

14. Write down the **Problem number** generated by your instance; it can vary from the training example.
15. Open the **Form Context Menu** again.
16. Choose **Create Favorite**.
17. In the pop-up for the newly added Favorite, select **More**.
<img width="1311" height="587" alt="image" src="https://github.com/user-attachments/assets/d8053e8d-f951-4008-a51e-44b2c7efcb24" />

19. Choose any icon and color you like.
20. Click **Save edits**.
21. Open **Favorites** and confirm the saved Problem record appears.
<img width="1321" height="549" alt="image" src="https://github.com/user-attachments/assets/7c7fa72b-1137-4709-92ee-fc3908397561" />

**Expected result:** A saved Network Problem record about a recurring outage appears in Favorites.

---

## Lab 4 — Organize Tickets With a Visual Task Board

### Real-life context

Your help-desk team needs a simple board that groups different types of work: network problems, employee incidents, and change requests.

### Goal

Create a **Freeform Board** named **My Requests** and add your network Problem to its **Problem** lane.

### Step-by-step in the simulator

1. Navigate to **All > Self-Service > Visual Task Boards**.
2. Click **New**.
3. Choose **Freeform Board**.
4. Double-click the board's current title and rename it **My Requests**.
5. Double-click the existing lane name **To Do** and rename it **Problem**.
6. Double-click **Doing** and rename it **Incident**.
7. Double-click **Done** and rename it **Change**.
8. Confirm the board now contains **Problem**, **Incident**, and **Change** lanes.
9. The training instructions say changes to the Visual Task Board are **automatically saved**.
<img width="1232" height="520" alt="image" src="https://github.com/user-attachments/assets/43e9fcc9-3134-4992-82f4-c2ff6e4f0520" />

11. Open **Favorites**.
12. Select the **Problem Favorite** you created in **Lab 3** (number and icon vary).
13. Once the Problem record opens, use its **Form Context Menu**.
14. Select **Add to Visual Task Board**.
<img width="1414" height="558" alt="image" src="https://github.com/user-attachments/assets/986a2167-f664-4541-9fbd-d1e1e62e097f" />

16. Choose **My Requests**.
17. The lab expects a confirmation banner similar to: **“Unable to connect to network server. Has been added to My Requests.”**
18. Click **View Board**.
19. Confirm the Problem is displayed in the **Problem** lane.
<img width="1204" height="458" alt="image" src="https://github.com/user-attachments/assets/e50b75d7-39dd-41f7-a8a9-433f7fd3ad90" />

**Expected result:** A three-lane board named **My Requests** contains the network Problem card under **Problem**.



---

## Lab 5 — Build an Incident Priority Chart and Dashboard

### Real-life context

A help-desk lead asks: “Among incidents that are not closed, how many are Critical, High, Moderate, Low, or Planning?” A chart makes the answer easier to see than reading tickets one by one.

### Goal

Create a pie chart named **Open Incidents by Priority**, then add it to a dashboard named **Incident Overview**.

### Step-by-step in the simulator

1. Navigate to **All > Incident > All**.
2. Open the **funnel/filter** if it is not already open.
3. Filter the incidents with:
   - **Field:** `State`
   - **Operator:** `is not`
   - **Value:** `Closed`
4. Click **Run**.
<img width="1160" height="879" alt="image" src="https://github.com/user-attachments/assets/d2cf1ec1-d501-4f9f-bff0-ee65c0ac84f2" />

6. Right-click the **Priority** column heading.
7. From the menu, select **Pie Chart**.
8. Review the resulting pie chart.
9. Hover your mouse over each **pie slice** to view the corresponding priority and percentage.
10. Open or select the **Details** panel for the chart.
11. Change the chart name to **Open Incidents by Priority**.
12. Click **Save**.
<img width="1442" height="743" alt="image" src="https://github.com/user-attachments/assets/17834cb8-0b60-4c22-a547-e8f0bea1c208" />

14. Select **Add to Dashboard > Add to new dashboard**.
15. Find the **Dashboard Title** and choose **Edit dashboard name**.
16. Rename it **Incident Overview**.
17. Click **Save**.
18. Open the dashboard and verify the **Open Incidents by Priority** chart is present.
<img width="1088" height="497" alt="image" src="https://github.com/user-attachments/assets/5770078e-fe2c-4037-9c92-82b77d33e116" />

**Expected result:** The **Incident Overview** dashboard contains the new priority pie chart, based on incidents whose state is not Closed.

---

## Lab 6 — Request a New Knowledge Base

### Real-life context

New employees need a single place to find their first-week instructions. Instead of answering the same questions repeatedly, you request a dedicated knowledge base for onboarding resources.

### Goal

Submit a Knowledge Base request named **New Employee Resources** through **Employee Center**.

### Step-by-step in the simulator

1. Navigate to **All > Self-Service > Employee Center**.
2. **Optional shortcut from the instructions:** Open your own ServiceNow instance's Employee Center path (`/esc`) instead of the main platform page. Use **your instance hostname**, not the illustrative hostname from the lab screenshot.
3. In the Employee Center header, open the **Technology services** drop-down.
4. Select **IT for IT**.
5. Click **Request Knowledge Base**.
6. In the request form, find the field asking why the knowledge base should be created.
7. Enter exactly:

   `New employees need resources to help with Week 1 tasks on the job.`

8. In the **Knowledge Base name** field, enter:

   `New Employee Resources`
<img width="1642" height="758" alt="image" src="https://github.com/user-attachments/assets/f44d8d5e-a075-4ba1-a1be-615a07e7aab0" />

9. Review the form and select **Submit**.
11. Record your newly generated request number (the lab indicates that the **REQ** number may vary).
12. Verify that the submission or request detail page appears.
13. To return to the platform view, remove the **Employee Center ticket-page suffix** from your browser's URL and use the main instance URL, or return using your platform navigation. The screenshot calls out a suffix beginning with `esc?id=ticket`.
<img width="1077" height="778" alt="image" src="https://github.com/user-attachments/assets/f966be3d-3f26-4e5d-b812-783578eb9b67" />

**Expected result:** A submitted request for the **New Employee Resources** knowledge base, with a request number.

---

## Lab 7 — Request Equipment and Software Through the Service Catalog

### Real-life context

An employee needs a desk phone to take work calls and Adobe Acrobat Pro for documents. The Service Catalog collects both requests and records the submission.

### Goal

Add a **Telephone Extension (IP 560 Phone)** and **Adobe Acrobat Pro** to the cart, then check out.

### Step-by-step in the simulator

1. Navigate to **All > Self-Service > Service Catalog**.
2. If your browser is still in the Service Portal, remove its `/sp` path suffix and return to the **platform** before using the All menu, as directed by the lab.
3. In the Service Catalog, choose the **Office** category.
4. Scroll through the Office items until you find **Telephone Extension (IP 560 Phone)**.
5. Open **Telephone Extension (IP 560 Phone)**.
6. Click **Add to Cart**.
7. Click **Continue Shopping**.
8. Go back to the Service Catalog home page.
9. Select the **Software** category.
10. Choose **Adobe Acrobat Pro**.
11. Click **Add to Cart**.
12. Check the shopping cart: it should show **2 items**.
13. Click **Proceed to Checkout**.
14. Finish the checkout flow, if your simulator presents an additional confirmation.
15. Confirm the message **“Thank you, your request has been submitted.”**
<img width="945" height="547" alt="image" src="https://github.com/user-attachments/assets/f4348167-39ad-4675-b0c1-7ec6e2fbc218" />

**Expected result:** A Service Catalog request is submitted for two items: a desk phone and Adobe Acrobat Pro.


---

## Lab 8 — Find Password Reset Help With Virtual Agent

### Real-life context

An employee asks how to change a password. Rather than immediately opening a support ticket, you use ServiceNow's Virtual Agent to find a self-service knowledge article.

### Goal

Find knowledge article **`KB0010003`**, give feedback that it was helpful, rate it **5 stars**, and submit a comment.

### Step-by-step in the simulator

1. Open the **Service Portal** for your own instance, using its `/sp` path. The lab image uses an **example URL**, not a universal link.
2. Locate the **Open Chat Window** control at the **bottom-right corner**.
3. Click it to open **Virtual Agent**.
4. In the box labeled something like **“Please type your request”**, type:

   `change password`

5. Submit your message.
6. The lab expects the Virtual Agent to show two choices: **Password Reset Instructions** and **I want something else**.
7. Click **Password Reset Instructions**.
<img width="1874" height="795" alt="image" src="https://github.com/user-attachments/assets/968d41fd-2cfa-41fb-bfcc-da2cd1d0c85c" />

9. The Virtual Agent should suggest Knowledge article **`KB0010003`**.
10. Click **KB0010003** to open the article.
<img width="473" height="757" alt="image" src="https://github.com/user-attachments/assets/b58150b5-fbdb-4612-81c5-49d7b1550c29" />

12. Find the **Helpful?** area of the article.
13. Click **Yes**.
14. Rate the article **5 stars**.
<img width="1121" height="720" alt="image" src="https://github.com/user-attachments/assets/03032a2d-6e41-488a-afba-6344e74fc489" />

16. Type a brief, genuine comment reflecting your experience (for example, **“The instructions were easy to follow.”** if that is true for you).
17. Click **Submit** to save your comment.
<img width="1121" height="720" alt="image" src="https://github.com/user-attachments/assets/13165b5e-a969-4ed4-80a5-d31a8379adb5" />

<img width="1075" height="413" alt="image" src="https://github.com/user-attachments/assets/0c746236-bf63-4fda-a167-7125c5c151c7" />


**Expected result:** The password-reset knowledge article was opened through Virtual Agent, and feedback was submitted.


---

## Skills Practiced

| Skill | How this project demonstrates it |
|---|---|
| Help Desk and ITSM | Navigate incidents, problems, and user requests in ServiceNow. |
| Incident Management | Filter active tickets and update critical incident states. |
| Problem Management | Report a repeating server outage for root-cause investigation. |
| Ticket Documentation | Record problem statement, description, assignment group, and service. |
| Workflow Organization | Add a problem to a Visual Task Board. |
| Reporting and Dashboards | Create and save a pie chart grouped by incident priority. |
| Knowledge Management | Favorite Knowledge and request a new onboarding Knowledge Base. |
| Service Request Management | Request approved office and software items through a catalog. |
| Self-Service Support | Find password-reset instructions using Virtual Agent. |

## Results and Verification Checklist

Only mark an item after **you have performed and verified it** in your own training instance:

- [ ] **Lab 1:** All pinned; Knowledge in Favorites.
- [ ] **Lab 2:** Filter created; 1-Critical rows updated to In Progress (at least 10); columns personalized; `INC0000055` categorized as Software.
- [ ] **Lab 3:** Network Problem saved and favorited. **My Problem #:** `__________`
- [ ] **Lab 4:** My Requests board created; Problem card appears under Problem.
- [ ] **Lab 5:** Open Incidents by Priority chart saved to Incident Overview dashboard.
- [ ] **Lab 6:** New Employee Resources Knowledge Base request submitted. **My REQ #:** `__________`
- [ ] **Lab 7:** Two catalog items submitted; confirmation displayed.
- [ ] **Lab 8:** `KB0010003` opened; Yes / 5 stars / comment submitted.

## Evidence / Screenshots

Screenshots taken **while completing the task** are much stronger portfolio evidence than screenshots of the task instructions. Add your own PNG screenshots to the `screenshots/` folder. Use descriptive filenames listed in each lab section.

To embed a screenshot in this README after uploading it to GitHub, add a line like:

```markdown
![Critical incident filter in ServiceNow](screenshots/02a-incident-three-filters.png)
```

**Recommended minimum evidence set:** one screenshot of the pinned menu, the incident filter, the updated incident state, the new Problem, the task board, the pie chart/dashboard, the KB request, catalog confirmation, and Virtual Agent/KB article.

> **Safety:** Blur names, emails, internal server addresses, personal data, request details belonging to real people, and any credentials before making screenshots public.

## Troubleshooting Quick Notes

- **All menu disappears:** Maximize/widen your browser; the pinned panel may hide on narrow windows.
- **A module is missing:** Verify the simulator still shows **Platform User**, and use the lab's exact menu path.
- **Incident filter shows unexpected results:** Make sure **all three conditions use AND** and run the filter again.
- **Bulk edit does not save:** Select only the intended cells, use the **green checkmark**, and verify the values after editing.
- **Priority changed after Impact and Urgency:** This can be expected; the lab specifically points out **3 - Moderate**.
- **Problem Favorite not found:** Open the saved **Problem record**, not just the Problem menu item, and use its Form Context Menu.
- **Service Portal or Employee Center does not look like the platform:** Check your instance URL path (`/sp` for Service Portal; `/esc` for Employee Center) and return to the main instance for platform navigation.
- **Different record/request number:** Use the number created in **your** simulator; training samples do not always match.
- **Your organization's ServiceNow looks different:** Roles, plugins, instance version, and configured modules can change the interface. These instructions describe the provided **training simulator**.

## Portfolio Summary (Complete After Verifying the Labs)

I practiced key IT Service Management workflows in the ServiceNow training simulator, including incident filtering and updates, recurring-problem documentation, task-board organization, priority dashboards, employee knowledge requests, service catalog checkout, and Virtual Agent self-service support. This project demonstrates the processes used by IT Support and Help Desk teams to organize, prioritize, and document employee support work.

**Tools:** ServiceNow training simulator, Incident Management, Problem Management, Visual Task Boards, Dashboards, Employee Center, Service Catalog, Virtual Agent, Knowledge.

---

*Training portfolio. These are simulated exercises, not production changes or employer support records.*
