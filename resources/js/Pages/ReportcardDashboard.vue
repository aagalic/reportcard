
<script setup>
import { router } from '@inertiajs/vue3'
import { useForm } from '@inertiajs/vue3'

const form = useForm({
    forceFormData: true,
    name: null,
    email: null,
    password: null,
    bio: null,
    profilepic: null
})

function handleProfileForm(){
    form.post(
    "/",
    form,
    {
        forceFormData: true,
    }
)
}

function handleSchoolForm(){
    alert('hello from school')
}
    

</script>
<template>
  <nav class="top-toolbar navbar navbar-mobile navbar-tablet">
				<ul class="navbar-nav nav-left">
					<li class="nav-item">
						<a href="javascript:void(0)" data-toggle-state="aside-left-open">
							<i class="icon dripicons-align-left"></i>
						</a>
					</li>
				</ul>
				<ul class="navbar-nav nav-center site-logo">
					<li>
						<a href="index-2.html">
							<div class="logo_mobile">
							</div>
							<h1 class="brand-text">Report Card</h1>
						</a>
					</li>
				</ul>
			</nav>
			<nav class="top-toolbar navbar navbar-desktop flex-nowrap">
				<ul class="site-logo">
					<li>
						<!-- START LOGO -->
						<a href="index-2.html">
							<div class="logo">

							</div>
							<h1 class="brand-text">Report Card</h1>
						</a>
						<!-- END LOGO -->
					</li>
					<li class="nav-item dropdown dropdown-menu-lg">
						<a role="button" aria-haspopup="true" aria-expanded="false">
							Home
						</a>
					</li>
					<li class="nav-item dropdown dropdown-notifications dropdown-menu-lg">
						<a role="button" aria-haspopup="true" aria-expanded="false">
							About
						</a>

					</li>

					<li class="nav-item">
						<a data-toggle-state="aside-right-open">
							Contact
						</a>
					</li>
				</ul>

			</nav>
			<!-- END TOP TOOLBAR WRAPPER -->

            <div class="content-wrapper">

<div class="container">
    <header class="page-header">
        <div class="d-flex align-items-center">
            <div class="mr-auto">
                <h1 class="separator">My Account</h1>

            </div>
        </div>
    </header>
    <section class="page-content container-fluid">
        <div class="row">
            <div class="col">
                <div class="card">
                    <div class="card-body">
                        <div class="row">
                            <div class="col-md-12 col-lg-3">
                                <div class="nav flex-column nav-pills" id="my-account-tabs"
                                    role="tablist" aria-orientation="vertical">
                                    <a class="nav-link active" id="v-pills-profile-tab"
                                        data-toggle="pill" href="#v-pills-profile" role="tab"
                                        aria-controls="v-pills-profile" aria-selected="true">Personal
                                        Profile</a>
                                    <a class="nav-link" id="v-pills-orgprofile-tab" data-toggle="pill"
                                        href="#v-pills-orgprofile" role="tab"
                                        aria-controls="v-pills-orgprofile" aria-selected="true">Generate Report Cards</a>
                                   
                                </div>
                            </div>
                            <div class="col-md-12 col-lg-9">
                                <div class="tab-content" id="my-account-tabsContent">
                                    <div class="tab-pane fade show active" id="v-pills-profile"
                                        role="tabpanel" aria-labelledby="v-pills-profile-tab">
                                        <h4 class="card-heading p-b-20">Profile</h4>
                                        <form @submit.prevent="form.post('/')">
                                            <div class="form-group">
                                                <!-- <img src="../assets/img/avatars/1.jpg"
                                                    class="w-50 rounded-circle" alt="Albert Einstein"> -->
                                                <div class="file-upload">
                                                    <label for="upload" class="btn btn-primary m-b-0 m-l-5 m-r-5">Upload a new picture</label>
                                                    <input id="upload" @input="form.profilepic = $event.target.files[0]" class="file-upload__input" type="file"/>
                                                    <!-- <progress v-if="form.progress" :value="form.progress.percentage" max="100">
                                                    {{ form.progress.percentage }}%
                                                    </progress> -->
                                                </div>
                                                <button class="btn btn-secondary">Delete</button>
                                            </div>
                                            <div class="form-group">
                                                <label for="inputName">Your name</label>
                                                <input v-model="form.name" type="text" class="form-control" id="inputName"
                                                    autocomplete="name" placeholder="Enter your name">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleInputEmail1">Email address</label>
                                                <input v-model="form.email" type="email" class="form-control" autocomplete="email"
                                                    id="exampleInputEmail1" placeholder="Enter email">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleInputPassword1">Password</label>
                                                <input v-model="form.password" type="password" class="form-control"
                                                    id="exampleInputPassword1" autocomplete="password"
                                                    aria-describedby="passwordHelp" placeholder="Password">
                                                <small id="passwordHelp" class="form-text text-muted">We
                                                    recommend at least 8 characters long, avoiding patterns and
                                                    common words/phrases.</small>
                                            </div>
                                            <div class="form-group">
                                                <label for="inputLocation">Location</label>
                                                <input v-model="location" type="text" class="form-control" id="inputLocation"
                                                    placeholder="Enter location">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleFormControlTextarea1">Bio</label>
                                                <textarea v-model="form.bio" class="form-control" id="exampleFormControlTextarea1"
                                                    rows="3"></textarea>
                                            </div>
                                            <button type="submit" @click="handleProfileForm()" class="btn btn-primary">Update Profile</button>
                                        </form>
                                    </div>
                                    <div class="tab-pane fade" id="v-pills-orgprofile" role="tabpanel"
                                        aria-labelledby="v-pills-orgprofile-tab">
                                        <h4  class="card-heading">Generate Report Cards</h4>
                                        <form>
                                           
                                            <div class="form-group">
                                                <div class="form-row">

                                                    <label for="inputCard">School Name</label>
                                                    <input type="text" class="form-control" id="inputCard"
                                                        placeholder="School Name">
                                                </div>
                                                <div class="form-row">
    
                                                    <label for="inputCard">Report Title</label>
                                                    <input type="text" class="form-control" id="inputCard"
                                                        placeholder="Report Title">
                                                </div>

                                                <div class="form-row">
                                                    <div class="form-group col-md-6">
                                                        <label for="level">Level</label>
                                                        <input type="text" class="form-control" id="level"
                                                            placeholder="Level">
                                                    </div>
                                                    <div class="form-group col-md-6">
                                                        <label for="level">Contact Number</label>
                                                        <input type="text" class="form-control" id="level"
                                                            placeholder="Contact Number">
                                                    </div>
                                                </div>

                                                <div class="form-row">
                                                    <label for="upload" class="btn btn-primary m-b-10 m-l-5 m-r-5">Upload School Logo </label>
                                                    <input id="upload" @input="form.schoollogo = $event.target.files[0]" class="file-upload__input" type="file"/>
                                                </div>
                                            </div>
                                            <div class="form-row">
                                                <div class="form-group col-md-6">
                                                    <label for="academicyear">Academic Year</label>
                                                    <input type="text" class="form-control" id="academicyear"
                                                        placeholder="YYYY">
                                                </div>
                                                <div class="form-group col-md-6">
                                                    <label for="term">Term</label>
                                                    <input type="text" class="form-control" id="term"
                                                        placeholder="Term">
                                                </div>
                                            </div>
                                            <div class="form-row">
                                                <div class="form-group col-md-6">
                                                    <label for="nexttermbegins">Next Term Begins</label>
                                                    <input type="text" class="form-control" id="nexttermbegins"
                                                        placeholder="YYYY">
                                                </div>
                                                <div class="form-group col-md-6">
                                                    <label for="term">Term</label>
                                                    <input type="text" class="form-control" id="term"
                                                        placeholder="Term">
                                                </div>
                                                <label for="upload" class="btn btn-primary m-b-0 m-l-5 m-r-5">Upload grades</label>
                                                <input id="upload" @input="form.grades = $event.target.files[0]" class="file-upload__input" type="file"/>
                                            </div>
                                            <button type="submit" @click="handleGradesForm()" class="btn btn-primary mt-5">Generate Grades</button>
                                        </form>
                                    </div>
                                    
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</div>
</div>
</template>
