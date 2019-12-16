# The Digital Gal 12 Days Trivia Contest

Facebook Messenger is a great new way of building a subscriber base, and Facebook ads promoting competitions
fit well with the kinds of things Facebook users are doing and engaging in.

ManyChat is a Facebook Messenger Flow builder that allows for automated messenger responses to 
selection from a "pick a path" style set of buttons. Unlike a regular chatbot from the past where
the software needed to interpret text, Facebook Messenger Marketing allows for buttons to simply
be pressed to go down a multi-choice path leading to more specific information and options.

## Introducing Trivia Contests within Messenger

Available for purchase, this set of ManyChat templates are designed to engage your audience with
a competition that lasts up to 12 days. Prizes are drawn at the end, and users are required
to answer the trivia questions as they come out each day to be awarded points.

Spot prizes and an overall prize are also helpful in keeping the audience engaged.

The template is designed and tested to be very visual and appealing, resulting in users that are
asking after and waiting for each day to come out, it is quite fun and visual.

The purpose of this document is to describe how to install the templates and guide you through
options for configuration.

## Features

* Unlocks a new trivia question each day
* Broadcast template provided for notifying audience each day
* Score tracking each day
* Prize templates for each day
* Notification manager to pause notifications and unsubscribe
* Visual display of prizes, questions and answers
* Storing and retreiving data from Google Docs spreadsheets
* Mailchimp support for notifying email addresses about the final result
* All works within Facebook Messenger

## Template installation

### Prerequisites to installation 

You will need to have a ManyChat Pro account connected to a Facebook page. For information on how
to set this up, visit [ManyChat].

[ManyChat]: http://www.manychat.com

### Installation

You will be given a one time use URL to download the template. Upon clicking the link you will
be taken to ManyChat where you will need to select the page you wish to install into.

The template will be contained within its own folder, so will not conflict with any existing flows.

## Duplicating from the templates

Create a folder under "Flows" called "Trivia Contest" or similar. This is where you will copy
your templates to and modify them to suit your competition.

### Duplicating flows

Duplicate the [START] template in the "Templates" folder by clicking the three dots icon to the
right and selecting "Duplicate". You will see an identical flow with " copy" at the end of the name.

Now drag this into the "Trivia Contest" folder to the left.

On the left hand navigation menu, you will be able to click the "Trivia Contest" folder and see the
template now in there. Click on the template to open it. At the top, click on the title to rename
it to "START". Press "Edit" in the middle of the large flow chart area at the top.

You will see green windows to the right named "See My Score", "Play More Trivia", "Prize List" and
"Question 1". You will need to systematically go and find each of these templates, copy them into
your "Trivia Contest" folder, or a sub folder that matches the template folder as you have done
for the first template. Then you will need to go back into "START", click "Edit" and click on each 
green flow to open it in the left pane. 
 
The easiest way to find each, is click "Open Flow", navigate to it, on the top right beside "Edit Flow"
 is the 3 dot button, where you can duplicate it, now click "Flows > " which will show the menu where
 you can find the copy to move it to "Trivia Contest" folder. You will need to click the ">" icon
  to expand folders to find the "Templates" folder. Once you see the folder, click it. Now you will see
the copied template. You can rename it with the 3 dots icon to the right, move it by dragging it
to the "Trivia Contest" folder again, removing [Template] from the name and tidying up the name to 
remove " copy". 

Now you need to go back to the "START" flow, and click on the green heading again in edit mode. This time
click X beside the template name and then the button "Click to Select a Flow". Find the copy of the 
template, selecting that instead and click "Select This Flow"

### Swapping out flow links

Once you get the hang of duplicating, it may pay to duplicate all flows in a folder, then drag them in all at once
and rename them all at once, then link them all at once. Just be careful not to select the wrong flow when
you swap it out!

Note that you will need to click "Publish" once you have swapped out each on a flow.

#### Folder Structure

Note also that "Prizes List" is in the "3) Prizes [Templates]" folder, so you will want to make a new
"3) Prizes" folder under "Trivia Contest" folder before duplicating and copying this template.
Always try to keep the folder structure the same so you can reference back to the templates folder and
see where everything is.

For "Day 1 Trivia Question", you should copy this into a new folder named "2) Trivia Questions". Also make
"1) Trivia Questions Locked" folder for later.

#### Google Drive 

When copying the "2) Trivia Questions", you will need to select the spreadsheet in Google Drive first in two actions called
"Google Sheets Actions". For this, in edit mode, click the yellow action window to have it appear in the left pane.
Select the spreadsheet supplied which you should have a copy of in your Google Drive account. If you do not
have Google Drive, you can get an account from following this [Google Drive] link, but it the Google Drive sheet template
should have been shared with you when you bought the template.

* Select the spreadsheet,
* Select "Sheet 1"
* Select Lookup Column as "User Player Number Custom Field"
* Select "Player Number"

Note, you can type instead of scroll, to filter and the select.

Then scroll down to the "Question_X" where X is the current question you are editing. To the left select "score_X"
where X is again, the current question you are editing. Click Save.

You will need to do the above in two places before these flows will duplicate successfully. If they don't duplicate
 successfully you may see residue copies with single text blocks in them - you can remove these. Click "Publish" and it
will show you where the error lies.

Alternatively you can remove the "Google Sheets Action", but make sure you put it back in and map the spreadsheet again 
once making the copy and putting
it in the right place. Also make sure you put it back into the template! To add it back again, select the "+Action" button
on the second action, after "Played Day X Trivia" (in two places, one with a green tick and one with a red cross beside "Actions")
select "Google Sheets Actions", then click "Select action" and select "Update Row", then follow the bullet points
above. Note, you only need to select "score_X" for the trivia question you are updating, nothing else.

[Google Drive]: https://drive.google.com

#### Advanced Trivia Question Template

You will notice in the template folder named "1) Trivia Questions" there is a special version of template 12 called "ADVANCED".
This template has the conditional logic to pull the questions and answers from a spreadsheet. Standard templates will need
to have questions and answers entered directly in each template, but with this you can edit the "Decisions" Google Spreadsheet
and have the questions and answers flow through automatically. This helps to have a centralised place to manage questions
and answers, however the images will still need dragging in, and the Google Drive connection for answers will still need doing.

To use it, after duplicating it and moving it into the "Trivia Contest > 1) Trivia Questions" folder, in edit mode, go to
the "Starting Step" Action and change the "12DTC_current_day_number" to the day for this trivia question, then in the next
"Google Sheets Action", select "Get Row By Value". 

* Select the "Decisions" spreadsheet
* Select "Questions & Answers" Worksheet
* Select # as the Lookup Column
* Select "12DTC_current_day_number" as the "Lookup Value"

Then against the "Google Column Titles", select each corresponding Custom Field:

* Question > "12DTC_current_question"
* Answer 1 > "12DTC_current_answer_1"
* Answer 2 > "12DTC_current_answer_2"
* Answer 3 > "12DTC_current_answer_3"
* Correct # > "12DTC_current_correct_answer"
* Correct Description > "12DTC_current_correct_description"

Click "Save". Now change the "Trivia Day X" to the current day for each place you see 12. This includes swapping out tags
and custom fields all the way through.

For the second yellow action with a green tick, select "Update Row" and use the following for the spreadsheet setup:

* Select the "Trivia Scores" spreadsheet,
* Select "Sheet 1"
* Select Lookup Column as "User Player Number Custom Field"
* Select "Player Number"

Then scroll down to the "question_X" row, where "X" is the number of the flow you are editing, and put "score_X" beside it,
where "X" is again the number of the flow you are editing.

#### Prize X Template

In the last part of the "Trivia Question X" is a "Jump to Flow" to "Prize X [Template]". You will need to copy this flow and
swap it out with the template version. 

In this flow, on the starting action, the only thing you have to do is ensure the "12DTC_current_day_number" is set to the
correct day, and click the "Get Row By Value" Google Sheets Action to edit it.

Similar to with the advanced trivia question template, select the following:

* Select the "Decisions" spreadsheet
* Select "Questions & Answers" Worksheet
* Select # as the Lookup Column
* Select "12DTC_current_day_number" as the "Lookup Value"

and then for the "Google Column Titles", just do the one named:

* Prize Name > 12DTC_current_prize_name

#### See My Score Template

In the Starting Step "Calculate Total Score" action, click "Get Row By Value" and:

* Select the "Trivia Scores" spreadsheet,
* Select "Sheet 1"
* Select Lookup Column as "User Player Number Custom Field"
* Select "Player Number"

and then for the "Google Column Titles", just set the ones named:

* total points > score_total
* question_X > score_X (where X is the number from 1 to 12).

#### Start Template

In the Starting Step, select "Get Row By Value" select the following:

* Select the "Decisions" spreadsheet
* Select "Overall Settings" Worksheet
* Select # as the Lookup Column
* Select "12DTC_current_contest" as the "Lookup Value"

and then for the "Google Column Titles", just set the ones named:

* Price Announce Date > 12DTC_announce_date
* Contest Description > 12DTC_current_contest_description
* Contest Start Date > 12DTC_current_contest_date_start

Click "Save".

In the "Add Email to Mailchimp" action, ensure a Mailchimp account is selected and an new empty list is selected in the
 "Add Subscriber to a List" action. If you don't have MailChimp you can get it from the [MailChimp] link.

[MailChimp]: https://www.mailchimp.com

Click the "Google Sheets Actions" "Update row" link and:

* Select the "Trivia Scores" spreadsheet,
* Select "Sheet 1"
* Select Lookup Column as "User Player Number Custom Field"
* Select "Player Number"

and then map the following:

* Player Number > User Player Number Custom Field
* First Name > First Name
* Last Name > Last Name
* User Id > User ID
* Last Interaction > Last Interaction
* Email > Email
* Player Count > player count
* score_total > total points
* score_X > question_X (where X is the number 1 to 12)

Click "Save".

Swap out all the "Jump To Flow" green boxes.

#### Play More Trivia 1-6 and 7-12

Swap out all the "Jump To Flow" green boxes ensure none say [Template].

#### Prize 1 to 12

Swap out all the "Jump To Flow" green boxes ensure none say [Template].

#### Day X Trivia Questions

Swap out all the "Jump To Flow" green boxes ensure none say [Template] and the prize at the bottom maps correctly.

## Creating Engagement

## Hooking it to an ad

## Broadcasts

## The Prize Draw
