{% from "schedule/index.md" import weeks, current_weeks with context %}
<navbar placement="top" type="inverse">
  <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">{{ module_pair }} <small>{{ period }}</small></a>
  <dropdown text="Schedule" class="nav-link">
{% for week in weeks %}
<li><a href="{{ baseUrl }}/schedule/week{{ week.num }}/index.html" class="dropdown-item"> <md>**Week {{ week.num }}** [{{ week.day }}] {% if current_weeks[0] == week.num %} {{ fas_arrow_circle_left }}{% endif %}</md></a></li>
{% endfor %}
  </dropdown>
  <dropdown text="Textbook" class="nav-link">
    <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="dropdown-item">SE Textbook</a></li>
    <li><a href="{{baseUrl}}/programming/index.html" class="dropdown-item">Programming Textbook</a></li>
  </dropdown>
  <li><a href="{{baseUrl}}/admin/te3201-admin.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown text="Links" class="nav-link">
    <li><a href="{{forum_link}}" target="_blank" class="dropdown-item">{{ fas_comment }} Forum</a></li>
    <li><a href="https://www.comp.nus.edu.sg/~damithch/" target="_blank" class="dropdown-item">{{ fas_user_tie }} Instructor</a></li>
    <li><a href="{{ivle_announcements}}" target="_blank" class="dropdown-item">{{ fas_bullhorn }} Announcements</a></li>
    <li><a href="{{ivle_slides}}" target="_blank" class="dropdown-item">{{ icon_slides }} Lecture Notes</a></li>
    <li><a href="{{ivle_files}}" target="_blank" class="dropdown-item">{{ fas_file_upload }} File Submissions</a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>
    </form>
  </li>
</navbar>
