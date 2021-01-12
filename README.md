

# LiveProjectSummary
  This was a two week Scrum Sprint project utilizing Azure Devops linked to Visual Studio 2019 through Git. 
The project was develoing a CMS Web Application for a theatre group. There were daily Scrum meetings,
where each team member reported their work from the previous and current days. If the member was in need, 
the Scrum Master would give help on how to proceed. 

  The mechanism of work was to choose a problem that needed accomplished on the "Boards" section of Azure Devops. 
I then created a branch through Git inside of Visual Studio 2019. I was able to ask questions to a Scrum Master
through Slack. When I was able to achieve the desired web page, I sent it through a Pull Request from Visual
Studio 2019 to Azure.

The first job that I was assigned was to fix the back button on the "Delete" page of the Sponsors. The back button
was confirming deleting the sponsor. The fix was a change in the button code.

<button class="iconBtn" onclick="window.location.href ='@Url.Action("Index", "Sponsors")'">

  Another of the jobs that I was charged with was working on editing the Details page of the DisplayLinks. 
I reformatted the text and added buttons to the Back and Edit links. I performed most of the editing within the form here:

<dl class="Display-container-title-details">
    <dd>
        <p style="font-size:25px;" "text-align:center;">
            @Html.DisplayFor(model => model.Name)
        </p>

    </dd>
    <hr />
    <dt>
        <p class="bold" style="text-align:left"><i>@Html.DisplayNameFor(model => model.Text)</i></p>
    </dt>

    <dd>
        <p style="text-align:left; margin-left:5%">@Html.DisplayFor(model => model.Text)</p>
    </dd>

    <dt>
        <p class="bold" style="text-align:left"><i>@Html.DisplayNameFor(model => model.Link)</i></p>
    </dt>

    <dd>
        <p style="text-align:left; margin-left:5%">@Html.DisplayFor(model => model.Link)</p>
    </dd>
   
In addition. I supplied buttons to the Edit and Back To List links, as shown here:
   
   **<p>
    <a class="btn btn-main" href="@Url.Action("Edit", "DisplayLinks", new { id = Model.LinkId})"><i class="fa fa-edit fa-fw"></i>Edit</a>
    <a class="btn btn-main" href="@Url.Action("Index", "DisplayLinks")"><i class="fa fa-hand-point-left fa-fw"></i>Back To List</a>

**</p>

Another task that I was assigned with was enhancing the sponsors' icons on the index page.
Part of this task was to make the sponsor's icon zoom in slightly when hovering over it.
I was unable to find a proper class in the bootstrap.css, so I resorted to creating my own class in Site.css, as shown here:


CSS:
.zoom {
    padding: 10px;
    transition: transform .2s; /* w3schools */
    width: auto;
    height: auto;
}

    .zoom:hover {
        transform: scale(1.075); 
        cursor: model.link;
        }

HTML (class zoom)
<img src="@Url.Action("DisplayPhoto", "Photo", new { id = item.PhotoId})" class="thumbnail_size zoom" alt="Sponsor Logo Image" onclick="@Url.Action(model => model.Link)"/>


  

Conclusion:

  This was a great first experience in web development, and I gained a great deal of understanding about what
  to expect working on a company team. I expanded my skillset, and received a lot of valuable knowledge in
  front-end web development.
