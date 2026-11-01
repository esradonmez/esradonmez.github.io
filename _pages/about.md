---
layout: about
title: About
permalink: /
subtitle: <a href='https://www.ims.uni-stuttgart.de/en/'>IMS, University of Stuttgart</a>

profile:
  align: right
  image: prof_pic2.jpeg
  image_circular: true # crops the image to make it circular
  more_info: >
    <p style="display:block; text-align:center;">they/them &middot; she/her</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # rendered from the page body below (so the heading can read "current news")
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 3 # leave blank to include all the news in the `_news` folder


# latest_posts:
#   enabled: true
#   scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
#   limit: 3 # leave blank to include all the blog posts
---

<style>
  @media (min-width: 576px) {
    .profile {
      width: 29%;
      margin-top: -1.5rem;
    }
  }
  .job-market {
    margin: 1.5rem 0;
    padding: 0.9rem 1.1rem;
    border-left: 4px solid var(--global-theme-color);
    border-radius: 4px;
    background-color: color-mix(in srgb, var(--global-theme-color) 8%, var(--global-bg-color));
  }
  .job-market p {
    margin: 0;
  }
</style>

I am a final-year PhD Candidate at the IMS, University of Stuttgart, advised by [Agnieszka Faleńska](https://www.ims.uni-stuttgart.de/en/institute/team/Falenska/). My research focuses on socially embedded AI systems, spanning responsible/ethical AI and sociotechnical approaches to model design, alignment operationalization and objective trade-offs, sociotechnical evaluation and benchmarking, and the societal implications of AI.

Over the past year, I've been a visiting researcher at [MilaNLP](https://milanlproc.github.io/#about), advised by [Dirk Hovy](https://www.dirkhovy.com/), and at the [University of Edinburgh](https://informatics.ed.ac.uk/ilcc) and [Heriot-Watt University](https://www.hw.ac.uk/about/our-schools/mathematical-and-computer-sciences/research/computer-science/interaction-lab), working with [Björn Ross](https://sweb.inf.ed.ac.uk/bross3/) and [Gavin Abercrombie](https://gavinabercrombie.github.io/). During these stays, I've been investigating `pluralistic AI alignment`, with the goal of developing language technologies that represent diverse human perspectives and can dynamically adapt to new and/or minority perspectives.

<div class="job-market">
  <p><strong>I am on the academic job market</strong>, looking for postdoc and junior faculty positions. If you think I could be a good fit for your group or department, please get in touch!</p>
</div>

## your contribution is appreciated

<div class="news">
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
      <tr>
        <th scope="row" style="width: 20%"><a href="https://knittogether.github.io/kt25/">KnitTogether</a></th>
        <td>
          We are raising funds for the second edition of <a href="https://knittogether.github.io/kt25/">KnitTogether</a>, the European CL Research Summit for Junior Researchers (<a href="https://hub.hslu.ch/informatik/young-voices-for-fair-ai-research-that-connects/">write-up of the first edition</a>). If you or your institution would like to support it, please get in touch.
        </td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%"><a href="https://acpaths.ims.uni-stuttgart.de/">Survey</a></th>
        <td>
          We are running a <a href="https://acpaths.ims.uni-stuttgart.de/">community survey on careers in NLP</a> — how working in the field shapes our lives and the trade-offs we navigate. Please share your experiences and perspectives, whatever your career stage.
        </td>
      </tr>
      <tr>
        <th scope="row" style="width: 20%">Responsible NLP</th>
        <td>
          We are investigating responsible NLP practices in our community. If your work has been flagged for ethical issues, or you have served as an ethics reviewer or in any ethics review pipeline, we would love to hear about your experience — please get in touch.
        </td>
      </tr>
    </table>
  </div>
</div>

<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">current news</a></h2>

{% include news.liquid limit=true %}
