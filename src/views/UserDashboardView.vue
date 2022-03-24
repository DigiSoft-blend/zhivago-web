<template>
<DashboardSkeletonView v-if="getskeletonLoader"></DashboardSkeletonView>
  <div v-if="!getskeletonLoader" class="container-fluid page-body bg-light">

<div class="row">

  

  <div class="col-md-12  bg-secondary">
    <div class="fixed-top">


    <!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <!-- Container wrapper -->
  
    <!-- Toggle button -->
    <button class="navbar-toggler" type="button">
      <i class="fas fa-bars" onclick="toggleSideNav()"></i>
    </button>

     <img class="navbar-brand small-screen-logo" src="/assets/images/zhivago-logo.png" alt="logo"  height="40" width="130"/>

    <!-- Collapsible wrapper -->
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
     
       <img class="navbar-brand logo mx-4" src="/assets/images/zhivago-logo.png" alt="logo" />

          <form>
             <div class="search">
               <input class="nav-form-input form-control" type="text" placeholder="Search" aria-label="Search">
               <i class="mdi mdi-magnify icon"></i> 
             </div>
          </form>
      <!-- Left links -->
    </div>
    <!-- Collapsible wrapper -->

    <!-- Right elements -->
    <div class="d-flex align-items-center mx-3">
      <!-- Icon -->
      <a class="text-reset me-3" href="#">
        <i class="fas fa-message"></i>
      </a>

      <!-- Notifications -->
      <div class="dropdown">
        <a
          class="text-reset me-3 dropdown-toggle hidden-arrow"
          href="#"
          id="navbarDropdownMenuLink"
          role="button"
          data-mdb-toggle="dropdown"
          aria-expanded="false"
        >
          <i class="fas fa-bell"></i>
          <span class="badge rounded-pill badge-notification bg-danger">1</span>
        </a>
        <ul
          class="dropdown-menu dropdown-menu-end"
          aria-labelledby="navbarDropdownMenuLink"
        >
          <li>
            <a class="dropdown-item" href="#">Some news</a>
          </li>
          <li>
            <a class="dropdown-item" href="#">Another news</a>
          </li>
          <li>
            <a class="dropdown-item" href="#">Something else here</a>
          </li>
        </ul>
      </div>
      <!-- Avatar -->
      <div class="dropdown">
        <a
          class="dropdown-toggle d-flex align-items-center hidden-arrow"
          href="#"
          id="navbarDropdownMenuAvatar"
          role="button"
          data-mdb-toggle="dropdown"
          aria-expanded="false"
        >
          <img
            src="/assets/images/faces/face2.jpg"
            class="rounded-circle"
            height="40"
            alt="img"
            loading="lazy"
          />
        </a>
        <ul
          class="dropdown-menu dropdown-menu-end"
          aria-labelledby="navbarDropdownMenuAvatar"
        >
          <li>
            <a class="dropdown-item" href="#">My profile</a>
          </li>
          <li>
            <a class="dropdown-item" href="#">Settings</a>
          </li>
          <li>
            <router-link class="dropdown-item" to="/logout">Logout</router-link>
          </li>
        </ul>
      </div>
    </div>
    <!-- Right elements -->
  <!-- </div> -->
  <!-- Container wrapper -->
</nav>
<!-- Navbar -->
    

   </div>
  </div>
 </div>

    <div class="row">
               
    <nav id="mySidenav" class="col-md-3 sidebar-left py-4 px-2 p-lg-4 d-lg-block bg-light">
      <!-- <div class="position-sticky pt-5">
        <ul class="nav flex-column  nav-pills list-unstyled">
          <li class="mb-3">
            <a class="nav-link active" aria-current="page" href="/login">
             <span class="mdi mdi-home nav-icon" ></span>
              Home
            </a>
            <a class="nav-link bg-light" aria-current="page" href="#">
              <span class="mdi mdi-account nav-icon" ></span>
              Members
            </a>
          </li>

      <li class="mb-1 nav-item nav-link bg-light">
        <a class="text-muted align-items-center rounded collapsed d-flex justify-content-between" data-bs-toggle="collapse" data-bs-target="#home-collapse" aria-expanded="true">
        Marketplace
         <span class="mdi mdi-chevron-down" style="font-size:20px" ></span>
        </a>
        <div class="collapse show" id="home-collapse">
          <ul class="btn-toggle-nav list-unstyled fw-normal pb-1 small">
             <li class="nav-item">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F454;</span>
              Customers
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F524;</span>
              Reports
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="mdi mdi-git" ></span>
              Integrations
            </a>
          </li>
        
          </ul>
        </div>
      </li>
      <li class="mb-1 nav-item nav-link bg-light">
        <a class="text-muted  align-items-center collapsed d-flex justify-content-between" data-bs-toggle="collapse" data-bs-target="#dashboard-collapse" aria-expanded="false">
         Services
          <span class="mdi mdi-chevron-down" style="font-size:20px" ></span>
        </a>
        <div class="collapse" id="dashboard-collapse">
          <ul class="btn-toggle-nav list-unstyled fw-normal pb-1 small">
             <li class="nav-item">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F354;</span>
              Customers
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F624;</span>
              Reports
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="mdi mdi-web" ></span>
              Integrations
            </a>
          </li>
        
          </ul>
        </div>
      </li>


          <li class="nav-item bg-light">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F354;</span>
              Customers
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
             <span class="" >&#x1F624;</span>
              Reports
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="mdi mdi-git" ></span>
              Integrations
            </a>
          </li>
        </ul>

        <h6 class="sidebar-heading d-flex justify-content-between align-items-center px-3 mt-4 mb-1 text-muted">
          <span >Events</span>
          <a class="link-secondary" href="#" aria-label="Add a new report">
           <span class="mdi mdi-calendar" ></span>
          </a>
        </h6>
        <ul class="nav flex-column  nav-pills list-unstyled">
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
               <span class="" >&#x1F554;</span>
              Current month
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
            <span class="" >&#x1F353;</span>
              Last quarter
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="" >&#x1F324;</span>
              Social engagement
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
               <span class="" >&#x1F351;</span>
              Year-end sale
            </a>
          </li>
           <li class="nav-item">
            <a class="nav-link bg-light" href="#">
            <span class="" >&#x1F353;</span>
              Last quarter
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="" >&#x1F324;</span>
              Social engagement
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
               <span class="" >&#x1F351;</span>
              Year-end sale
            </a>
          </li>
           <li class="nav-item">
            <a class="nav-link bg-light" href="#">
            <span class="" >&#x1F353;</span>
              Last quarter
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
              <span class="" >&#x1F324;</span>
              Social engagement
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link bg-light" href="#">
               <span class="" >&#x1F351;</span>
              Year-end sale
            </a>
          </li>
        </ul>
      </div> -->

      <div class="side-menu g-col-3 g-col-md-3 position-sticky pt-5">
           <button class="btn btn-primary w-100 text-white fw-normal text-left d-flex align-items-center py-2"><span class="iconify me-2" style="color: #fff;" data-icon="bytesize:home"></span>Home</button>
           <div class="side-menu-list-parent">

             <div class="side-menu-list member">
               <p>
                 <span class="iconify text-black-50 fw-bolder me-2" data-icon="eva:arrow-right-fill" href="#collapseExample" data-mdb-toggle="collapse" role="button" aria-expanded="false" aria-controls="collapseExample"></span>
                 <a href="" class="fw-normal">Members Central</a>               
               </p>
               
               <div class="member_collapsed collapse" id="collapseExample">
                  <a href="" class="individual-member"><span >👋</span>Start here</a>
                  <a href="" class="individual-member"><span>😏</span>Introduce Yourself</a>
               </div>
             </div>

             <div class="side-menu-list vip-group">
               <p>
                 <span class="iconify text-black-50 fw-bolder me-2" data-icon="eva:arrow-right-fill" href="#collapseExample2" data-mdb-toggle="collapse" role="button" aria-expanded="false" aria-controls="collapseExample2"></span>
                 <a href="" class="fw-normal">VIP GROUPS</a>
                 <span type="button" data-bs-toggle="tooltip" data-bs-placement="top" title="Create a space">
                  <span class="iconify text-dark-50" style="font-size: 1rem;" data-icon="carbon:add-alt"></span>
                </span>
               </p>
               <div class="member_collapsed collapse" id="collapseExample2">
                  <a href="" class="individual-member"><span >🙋</span>Las Vegas Singles</a>
                  <a href="" class="individual-member"><span>💱</span>No mint Mark</a>
               </div>
             </div>

             <div class="side-menu-list vip-group">
               <p>
                 <span class="iconify text-black-50 fw-bolder me-2" data-icon="eva:arrow-right-fill" href="#collapseExample3" data-mdb-toggle="collapse" role="button" aria-expanded="false" aria-controls="collapseExample3"></span>
                 <a href="" class="fw-normal">Admins</a>
               </p>
               <div class="member_collapsed collapse" id="collapseExample3">
                  <a href="" class="individual-member"><span >😎</span>Zhivago Admins</a>
               </div>
             </div>
             
             
             
           </div>

      </div>
    </nav> 


   

 
    
  
  <nav id="sidebarMenu" class="col-md-3 sidebar-right p-4 d-lg-block bg-light collapse">
    <button class="btn btn-primary w-100 text-center text-white py-3 px-4 fw-bold">New Post</button>
      <div class="position-sticky pt-3">
       <ul class="nav flex-column mb-auto px-4 box-shadow rounded" style="background:white;">
          <li class="nav-item">
            <p class="Trend-text px-1 mt-3 text-muted p-trending-post">Trending Posts</p>
                 <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face2.jpg" alt="image" class="rounded-circle status" />
                          <div class="active"></div>
                          </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Padosky Cardiento</h6>
                            </div>
                            <p class="text-muted p-sidbar-text">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
          </li>
          <li class="nav-item">
              <div class="preview-list">
                      <div class="preview-item">
                         <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face4.jpg" alt="image" class="rounded-circle status" />
                          <div class="active"></div>
                          </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Marcelo frichxzany</h6>
                            </div>
                            <p class="text-muted p-sidbar-text">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                </div>
          </li>
         
          
          <li class="nav-item">
              <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face8.jpg" alt="image" class="rounded-circle status" />
                          <div class="active"></div>
                          </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Sexy Tilda</h6>
                            </div>
                            <p class="text-muted p-sidbar-text">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                </div>
          </li>

          <li class="nav-item px-2">
            <p class="text-muted text-muted p-see-all">See all</p>
          </li>
        </ul>

        <div class="text-center">
          <em>-advertisement-</em>
          <ul class="ad-space nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
          <li class="nav-item p-0 m-0">
                
                <div class="_ad_inner_space d-flex justify-content-center py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <h3>250 x 250</h3>
             </div>
          </li>
        </ul>

        </div>
          
        
      </div>
    </nav> 

 
  <div class="main-view col-lg-6  container bg-light">
    <div class="row content gy-2">

      <div class="card card1 bg-light p-0 m-0  px-3 mt-3">
        <div class="card-body bg-light p-0 m-0">
          <div class="d-flex flex-row justify-content-between mt-3">
            <h4 class="card-title">Home</h4>
           
            <div class="dropdown">
              <a
                class="dropdown-toggle text-muted"
                href="#"
                role="button"
                id="dropdownMenuLink"
                data-mdb-toggle="dropdown"
                aria-expanded="false"
              >
              Latest
              </a>

              <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink">
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else here</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>


      <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>

      <div class="card text-dark mb-2 box-shadow p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between p-0 m-0 px-3">
                  <div class="preview-list">
                      <div class="preview-item">
                        <div class="preview-thumbnail">
                          <div class="img-div">
                          <img src="/assets/images/faces/face15.jpg" alt="image" class="rounded-circle status" />
                          <div class="active"></div>
                          </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Jack Thummar</h6>
                            </div>
                             <span class="badge rounded-pill bg-primary">Admin</span>
                             <span class="mx-1 badge rounded-pill bg-primary">now</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
               <p class="p-card-body">hello there sexy</p>
            </div>
             <div class="d-flex justify-content-center py-1">
                <img src="/img/IMG-20220322-WA0006.jpg" class="img-fluid" alt="...">
             </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                 <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col1" role="button" aria-expanded="false" aria-controls="col1"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

               <!-- comment section -->
          <div class="collapse comment-section" id="col1">
            <div class="comment-text text-center py-3 border-bottom border-gray">
              <div class="individual-comment-parent">
                <div class="individual-comment d-flex justify-content-between align-items-start">
                  <div class="profileImg overflow-hidden rounded-circle me-4">
                    <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                  </div>
                  <div class="flex-grow-1">
                    <div class="d-flex justify-content-between">
                      <span class="fw-normal">Junior Sam</span>
                      <span class="text-muted flex-grow-1 ms-3 text-left" style="font-size: 0.8rem;">a month ago</span>
                      <span class="iconify text-muted hover me-2" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                    </div>
                    <p class="my-2 text-start">Thanks alot, this was very helpful</p>
                    <div class="my-1 text-start">
                       <span class="commentbtn ms-2">Reply</span>
                       <span class="commentbtn ms-2">Like</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="show-comment justify-content-around m-auto">
                <button type="button" class="btn btn-outline-dark">Show more comment</button>
              </div>
            </div>
            <div class="newcomment d-flex justify-content-between align-items-start py-3 pe-3">
               <div class="profileImg overflow-hidden rounded-circle me-4">
                  <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                </div>
                <div class="flex-grow-1 border-gray border rounded p-3">
                  <input type="text" id="#col1-input" placeholder="What are your thoughts?" class="new-comment-input text-break w-100 p-2">
                  <div class="d-flex justify-content-between mt-2">
                    <span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="akar-icons:video"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="bi:image"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:gif-20-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:emoji-28-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="teenyicons:attach-solid"></span>
                    </span>
                    <button class="btn btn-primary px-4 py-2 fw-normal">Post</button>
                  </div>
                </div>
            </div>
          </div>

              <!-- advertisement -->
          <div class="card text-center p-0 mt-2 mb-4">
          <em>-advertisement-</em>
          <div class="card-body m-0 p-0">
              <div class="d-flex justify-content-center bg-dark py-5">
                  <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                  <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                    <li class="nav-item p-0 m-0">
                          <div class=" d-flex justify-content-center text-muted">
                          <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                            <h1> 730 x 100</h1>
                        </div>
                    </li>
                  </ul>
                  
              </div>
            </div>
        </div>
       </div>


       <div class="card text-dark mt-3 box-shadow p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between p-0 m-0 px-3">
                  <div class="preview-list">
                      <div class="preview-item">
                         <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face2.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Padosky Cardiento</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">5 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
             <div class="mx-3">
               <p class="p-card-body">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus tenetur ab odio adipisci nihil recusandae. Nobis fuga minus excepturi quae tenetur rem aperiam accusamus amet ex possimus? Consectetur, debitis corporis.</p>
             </div>
              <div class="d-flex justify-content-center py-1">
                 <img src="/img/IMG-20220322-WA0007.jpg" class="img-fluid" alt="...">
              </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col2" role="button" aria-expanded="false" aria-controls="col2"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

          <!-- comment section -->
          <div class="collapse comment-section" id="col2">
            <div class="comment-text text-center py-3 border-bottom border-gray">
              <div class="individual-comment-parent">
                <div class="individual-comment d-flex justify-content-between align-items-start">
                  <div class="profileImg overflow-hidden rounded-circle me-4">
                    <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                  </div>
                  <div class="flex-grow-1">
                    <div class="d-flex justify-content-between">
                      <span class="fw-normal">Junior Sam</span>
                      <span class="text-muted flex-grow-1 ms-3 text-left" style="font-size: 0.8rem;">a month ago</span>
                      <span class="iconify text-muted hover me-2" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                    </div>
                    <p class="my-2 text-start">Thanks alot, this was very helpful</p>
                    <div class="my-1 text-start">
                       <span class="commentbtn ms-2">Reply</span>
                       <span class="commentbtn ms-2">Like</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="show-comment justify-content-around m-auto">
                <button type="button" class="btn btn-outline-dark">Show more comment</button>
              </div>
            </div>
            <div class="newcomment d-flex justify-content-between align-items-start py-3 pe-3">
               <div class="profileImg overflow-hidden rounded-circle me-4">
                  <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                </div>
                <div class="flex-grow-1 border-gray border rounded p-3">
                  <input type="text" id="#col1-input" placeholder="What are your thoughts?" class="new-comment-input text-break w-100 p-2">
                  <div class="d-flex justify-content-between mt-2">
                    <span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="akar-icons:video"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="bi:image"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:gif-20-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:emoji-28-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="teenyicons:attach-solid"></span>
                    </span>
                    <button class="btn btn-primary px-4 py-2 fw-normal">Post</button>
                  </div>
                </div>
            </div>
          </div>

                  <!-- advertisement -->
              <div class="card text-center p-0 mt-2 mb-4">
            <em>-advertisement-</em>
            <div class="card-body m-0 p-0">
                <div class="d-flex justify-content-center bg-dark py-5">
                    <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                    <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                      <li class="nav-item p-0 m-0">
                            <div class=" d-flex justify-content-center text-muted">
                            <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                              <h1> 730 x 100</h1>
                          </div>
                      </li>
                    </ul>
                    
                </div>
              </div>
          </div>
       </div>


<div class="card text-dark mt-4 box-shadow p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between p-0 m-0 px-3">
                  <div class="preview-list">
                      <div class="preview-item">
                         <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face4.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Marcelo frichxzany</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">3 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
               <p class="p-card-body">Come bang me babe</p>
            </div>
             <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0008.jpg" class="img-fluid" alt="...">
             </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col3" role="button" aria-expanded="false" aria-controls="col3"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

          <!-- comment section -->
          <div class="collapse comment-section" id="col3">
            <div class="comment-text text-center py-3 border-bottom border-gray">
              <div class="individual-comment-parent">
                <div class="individual-comment d-flex justify-content-between align-items-start">
                  <div class="profileImg overflow-hidden rounded-circle me-4">
                    <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                  </div>
                  <div class="flex-grow-1">
                    <div class="d-flex justify-content-between">
                      <span class="fw-normal">Junior Sam</span>
                      <span class="text-muted flex-grow-1 ms-3 text-left" style="font-size: 0.8rem;">a month ago</span>
                      <span class="iconify text-muted hover me-2" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                    </div>
                    <p class="my-2 text-start">Thanks alot, this was very helpful</p>
                    <div class="my-1 text-start">
                       <span class="commentbtn ms-2">Reply</span>
                       <span class="commentbtn ms-2">Like</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="show-comment justify-content-around m-auto">
                <button type="button" class="btn btn-outline-dark">Show more comment</button>
              </div>
            </div>
            <div class="newcomment d-flex justify-content-between align-items-start py-3 pe-3">
               <div class="profileImg overflow-hidden rounded-circle me-4">
                  <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                </div>
                <div class="flex-grow-1 border-gray border rounded p-3">
                  <input type="text" id="#col1-input" placeholder="What are your thoughts?" class="new-comment-input text-break w-100 p-2">
                  <div class="d-flex justify-content-between mt-2">
                    <span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="akar-icons:video"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="bi:image"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:gif-20-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:emoji-28-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="teenyicons:attach-solid"></span>
                    </span>
                    <button class="btn btn-primary px-4 py-2 fw-normal">Post</button>
                  </div>
                </div>
            </div>
          </div>

              <!-- advertisement -->
          <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div>
      
 <div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face7.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Tom Cruise</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Horny sexy girls damn!!!</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0009.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col4" role="button" aria-expanded="false" aria-controls="col4"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

          <!-- comment section -->
          <div class="collapse comment-section" id="col4">
            <div class="comment-text text-center py-3 border-bottom border-gray">
              <div class="individual-comment-parent">
                <div class="individual-comment d-flex justify-content-between align-items-start">
                  <div class="profileImg overflow-hidden rounded-circle me-4">
                    <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                  </div>
                  <div class="flex-grow-1">
                    <div class="d-flex justify-content-between">
                      <span class="fw-normal">Junior Sam</span>
                      <span class="text-muted flex-grow-1 ms-3 text-left" style="font-size: 0.8rem;">a month ago</span>
                      <span class="iconify text-muted hover me-2" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                    </div>
                    <p class="my-2 text-start">Thanks alot, this was very helpful</p>
                    <div class="my-1 text-start">
                       <span class="commentbtn ms-2">Reply</span>
                       <span class="commentbtn ms-2">Like</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="show-comment justify-content-around m-auto">
                <button type="button" class="btn btn-outline-dark">Show more comment</button>
              </div>
            </div>
            <div class="newcomment d-flex justify-content-between align-items-start py-3 pe-3">
               <div class="profileImg overflow-hidden rounded-circle me-4">
                  <img src="/assets/images/faces/face4.jpg" alt="" class="w-100">
                </div>
                <div class="flex-grow-1 border-gray border rounded p-3">
                  <input type="text" id="#col1-input" placeholder="What are your thoughts?" class="new-comment-input text-break w-100 p-2">
                  <div class="d-flex justify-content-between mt-2">
                    <span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="akar-icons:video"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="bi:image"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:gif-20-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="fluent:emoji-28-regular"></span>
                      <span class="iconify me-2 text-muted" style="font-size: 1.3rem;" data-icon="teenyicons:attach-solid"></span>
                    </span>
                    <button class="btn btn-primary px-4 py-2 fw-normal">Post</button>
                  </div>
                </div>
            </div>
          </div>

           
              <!-- adveertisement -->

            <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 



       <div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face8.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Sexy Tilda</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Call me babe, need you now !!!</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0010.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col5" role="button" aria-expanded="false" aria-controls="col5"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

          <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 



<div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                         <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face10.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Micky Ashanti</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Just me and you all night</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0003.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col6" role="button" aria-expanded="false" aria-controls="col6"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

            <!-- advertisement -->
          <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 



<div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                         <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face11.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Alan Walker</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Need you  in the middle now babe !</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0011.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col7" role="button" aria-expanded="false" aria-controls="col7"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

            <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 


<div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face12.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Jerry Dick</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                  <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Badass girlfrind killing it !</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0004.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col8" role="button" aria-expanded="false" aria-controls="col8"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>
          
          <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 


<div class="card text-dark mt-4 p-0 m-0">
            <div class="card-header  d-flex  d-xl-flex justify-content-between">
                  <div class="preview-list">
                      <div class="preview-item">
                        <div class="img-div">
                        <div class="preview-thumbnail">
                          <img src="/assets/images/faces/face13.jpg" alt="image" class="rounded-circle status" />
                         <div class="active"></div>
                         </div>
                        </div>
                        <div class="preview-item-content d-flex flex-grow">
                          <div class="flex-grow">
                            <div class="d-flex d-md-block d-xl-flex justify-content-between">
                              <h6 class="preview-subject p-user-name">Thanos Hacky</h6>
                            </div>
                            <span class="badge rounded-pill bg-primary">2 days ago</span>
                            <p class="text-muted p-card-header mt-2">Well, it seems to be working now.</p>
                          </div>
                        </div>
                      </div>
                 </div>
                 <p class="text-muted mt-2 small p-share p-1 position-relative">
                     <a href="" class="sharebtn hover mx-3">Share</a>
                     <span class="iconify text-muted hover" style="font-size: 1.7rem;" data-icon="mi:options-horizontal"></span>
                  </p>
                  <div v-if="false" class="share-post d-flex justify-content-between position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <div>
                    <a href=""><p>Share to web</p></a>
                    <small class="text-muted">This post is Public.</small>
                  </div>
                  <button class="btn btn-outline-gray ">Copy link</button>
                </div>
                <div v-if="false" class="post-option position-absolute border border-gray border-1 rounded-1 shadow-sm">
                  <a href="#"><div>
                    <p>Edit post</p>
                    <small class="text-muted">Make changes to this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Unfollow post</p>
                    <small class="text-muted">Turn off notifications for this post</small>
                  </div></a>
                   <a href="#"><div>
                    <p>Delete post</p>
                    <small class="text-muted">Permanently delete this post</small>
                  </div></a>
                </div>
          </div>
          <div class="card-body m-0 p-0">
            <div class="mx-3">
              <p class="p-card-body">Sexy latina, fricky hot !</p>
            </div>
            <div class="d-flex justify-content-center py-1">
               <img src="/img/IMG-20220322-WA0005.jpg" class="img-fluid" alt="...">
            </div>
          </div>
          <div class="card-footer mt-4 py-3 border-top" style="background-color:white; border:none">
               <div class="row row-footer">
                  <div class="col-4">
                    <div class="col-12 footer-div">
                      <a href="" class="likebtn d-flex align-items-center"><span class="iconify" data-icon="fa-regular:thumbs-up"></span>Like</a>
                    </div>
                 </div>
                 <div class="col-4">
                     <div class="col-12 footer-div">
                      <a class="flex-grow-1 ps-3 commentbtn d-flex align-items-center" data-mdb-toggle="collapse" href="#col9" role="button" aria-expanded="false" aria-controls="col9"><span class="iconify me-2" data-icon="bx:message"></span>Comment</a>
                     </div>
                 </div>
                 <div class="col-4">
                    <div class="col-12 footer-div">
                        <i class="mdi mdi-share-outline"></i>
                        <p class="">4</p>
                    </div>
                 </div>
               </div>
          </div>

          <div class="card text-center p-0 mt-2 mb-4">
        <em>-advertisement-</em>
        <div class="card-body m-0 p-0">
             <div class="d-flex justify-content-center bg-dark py-5">
                <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                 <ul class="nav flex-column mb-auto px-4 mt-3 box-shadow bg-dark">
                  <li class="nav-item p-0 m-0">
                        <div class=" d-flex justify-content-center text-muted">
                        <!-- <img src="/cars/11231.jpg" class="img-fluid" alt="..."> -->
                          <h1> 730 x 100</h1>
                      </div>
                  </li>
                </ul>
                
             </div>
          </div>
      </div>
       </div> 


     
      </div>
     </div>
    </div>

    <div class="container">
   <div class="offcanvas offcanvas-start  w-50 h-50 bg-light" tabindex="-4" id="offcanvas" data-bs-keyboard="false" data-bs-backdrop="false">
    <div class="offcanvas-header">
        <h6 class="offcanvas-title d-none d-sm-block" id="offcanvas"><strong>Menu</strong></h6>
        <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
    </div>
    <div class="offcanvas-body  p-0 m-0">
        <ul class="nav nav-pills flex-column mb-sm-auto mb-0 align-items-start" id="menu">
           
           
            <li>
                <a href="#" class="nav-link text-truncate">
                 <span class="ms-1 d-none d-sm-inline">Products</span>
                 </a>
            </li>
            <li>
                <a href="#" class="nav-link text-truncate">
                 <span class="ms-1 d-none d-sm-inline">Customers</span> 
                 </a>
            </li>
        </ul>
    </div>
 </div>

 </div>
  </div>
</template>

<script>

import DashboardSkeletonView from './DashboardSkeletonView.vue'

export default {

   created(){
     
   },


   computed: {
      getskeletonLoader(){
        return this.$store.getters.getskeletonLoader
      },
      getUser(){
         return  this.$store.getters.getUser
       },
       getLoader() {
       return this.$store.getters.getLoader
       }, 
   },

   methods:{
     
   },

    components: { DashboardSkeletonView }
    
};

</script>

<style scoped>
*{
  /* font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"; */
  color: hsl(0, 0%, 23.1%);
}

.hover{
  color: hsl(0, 0%, 23.1%);
  cursor: pointer;
}
.hover:hover{
  color: #0d6efd;
}

form{
  margin-left:38px;
}

/* .page-body{
  max-width: 1440px!important;
} */
/* .logo{
  width: 15% !important;
} */

/* .profile{
  width: 23%;
}
.user-profile{
  width: 16%;
  display: flex;
  justify-content: space-around;
} */
/* 
main{
  display: grid;
  grid-template-columns: 20% 55% 20%;
  gap: 2em;
  background: #fff;
  margin-inline: auto;
} */

/* .search{
  background: #EFFFFD  !important;
} */

.tp_img{
  width: 18%

}

.tp_details h5{
  font-size: 0.9rem;
  margin-bottom: 0.3em;
  margin-top: 0.5em;
}

.username_tp{
  font-size: 0.8rem;
  opacity: 0.9;
}

.sharebtn, .likebtn, .commentbtn{
  color: hsl(219, 14%, 50%);
  text-decoration: none;
  cursor: pointer;
}

.likebtn p{
  margin: 0;
}
.sharebtn:hover, .likebtn:hover, .commentbtn{
  color: #000;
}

/* .main-posts{
  height: 100vh;
  max-height: 100vh;
  position: relative;
} */

.post-ad-inner-space{
  height: 90px!important;
  width: 100%!important;
  max-width: 730px;
}

._ad_inner_space{
  /* background: #eee; */
  height: 250px;
  width: 250px;
  margin-inline: auto;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.side-menu-list{
  margin: 2em 0.5em;
}

.side-menu-list p{
  display: flex;
  align-items: center;
  margin-bottom: 0;
}
.side-menu-list a{
  text-decoration: none;
  color: #000;
  font-weight: 500;
  font-size: 1.1rem;
  width: 100%;
  margin: 0;
  display: flex;
  align-items: center;
}

.member_collapsed{
  margin: 0 1em;

}

.member_collapsed a{
  text-decoration: none;
  color: hsl(219, 14%, 50%);
  margin: 0.5em 0;
  display: flex;
  font-size: 0.9rem;
}

.member_collapsed a span{
  margin-right: 0.5em;
}

.main-post-img{
  display: flex;
  justify-content: space-between;
}

.main-post-img img{
  width: 48%;
}

.comment-text{
  width: 100%;
}

/* .profile-details{

 } */

.authentication ul li{
  list-style-type: none;

}

.profileImg{
  width: 8%;
}

.new-comment-input{
  border: none;
  outline: none;
}

.post-likes-img{
  width: 35%;
}

.share-post{
  width: 65%;
  top: 6%;
  right: 2em;
  background: #fff;
  padding: 1em;
}

.share-post p, .post-option a p{
  margin: 0;
  font-weight: 600;
  font-size: 1rem;
}

.post-option{
  background: #fff;
  top: 6%;
  right: 1em;
  width: 55%;
  padding: 1em;
}

.post-option a{
  text-decoration: none;
}

.post-option a div{
  margin-block: 0.5em;
}


 
@media screen and (max-width: 1200px){
  main{
    grid-template-columns: 24% 50% 23%;
  }

  form{
    margin-left: 0;
  }

  .main-post-img{
  height: 100%;
  }

  .login-signup{
  width: 21%;
  }

  .pos_absolute{
    width: 45%;
    left: 28%;
  }

  .post-ad-inner-space{
  width: 100%!important;
}

}

@media screen and (max-width: 800px){
  main{
    display: block;
  }

  .profile{
    width: 35%;
  }


}

@media screen and (max-width: 450px){
  .share-post{
    width: 98%;
    right: 0em;
  }
  .post-option{
    right: 0em;
    width: 98%;
  }
}

</style>


