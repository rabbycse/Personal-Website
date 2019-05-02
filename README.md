Simple-Personal-Website
========================
[![SMS Created](https://img.shields.io/badge/Created-March%202019-blue.svg)](#)
[![SMS version](https://img.shields.io/badge/Personal%20Website-orange.svg)](#)
[![SMS Licence](https://img.shields.io/badge/Language-CSharp-green.svg)](#)

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/37344605/57102470-623f5700-6d45-11e9-8576-5e45069aad87.gif)

Website url: http://rabby.net

<h1>About This Site</h1>
<h3>
    ASP.NET Core 2.2 MVC
</h3>
<h3>
    Angular JS
</h3>
<p>
    The image galleries and  slide shows in the <a href="@Url.Action("index", "trips")">trips</a> portion
    of the site use <a href="http://www.angularjs.org/" target="_blank">Angular JS</a>. The images are
    all deployed to a separate domain. Each collection of images also contains an index file with titles,
    the date the picture was taken, and a few descriptions. An <a href="http://www.angularjs.org/" target="_blank">Angular JS</a>
    controller loads the index file using $http and builds the list of images, or the slide show view client side.
</p>
<h3>
    Bootstrap
</h3>
<p>
    Using <a href="http://getbootstrap.com" target="_blank">Bootstrap</a> made the styling of this site super easy.
    I used some of the responsive features of the framework in the <a href="@Url.Action("index", "trips")">trips</a> portion
    of the site to hide the left nav on smaller devices. Since I'm not a graphic designer (and I'm colorblind), I used
    the Flatly theme from <a href="http://bootswatch.com" target="_blank">Bootswatch</a> for the look and feel.
</p>
<h3>
    Automated Testing
</h3>
<p>
    Unit tests for the image collection index editing app are implemented in <a href="http://www.nunit.org/" target="_blank">NUnit</a>.
    Acceptance tests are implemented in <a href="http://www.specflow.org/" target="_blank">SpecFlow</a>.
    <a href="http://www.jetbrains.com/teamcity/" target="_blank">TeamCity</a> runs these with every commit. There are no
    tests for the server side portion of the website because all the dynamic behavior is implemented with
    <a href="http://www.angularjs.org/" target="_blank">Angular JS</a> on the client side. The <a href="http://www.angularjs.org/" target="_blank">Angular JS</a>
    code is tested with <a href="http://karma-runner.github.io" target="_blank">Karma</a>.
</p>
<h3>
    Infrastructure
</h3>
<p>
    This site is hosted on an Amazon Linux <a href="http://aws.amazon.com/ec2/" target="_blank">EC2</a> instance in Amazon Web Services.
    Versions of the site created with other technologies also run on the instance with <a href="http://nginx.org/" target="_blank">Nginx</a>
    proxying port 80 traffic to the appropriate port for each version based on host header.
</p>
<p>
    All the AWS infrastructure is created by <a href="https://www.terraform.io/" target="_blank">Terraform</a>. The Terraform files are
    kept under source control so that infrastructure changes are versioned.
</p>

