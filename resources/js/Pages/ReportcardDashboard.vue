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
                                        aria-controls="v-pills-orgprofile" aria-selected="true">School
                                        Profile</a>
                                    <a class="nav-link" id="v-pills-upload-tab" data-toggle="pill"
                                        href="#v-pills-upload" role="tab" aria-controls="v-pills-upload"
                                        aria-selected="false">Generate Cards</a>
                                </div>
                            </div>
                            <div class="col-md-12 col-lg-9">
                                <div class="tab-content" id="my-account-tabsContent">
                                    <div class="tab-pane fade show active" id="v-pills-profile"
                                        role="tabpanel" aria-labelledby="v-pills-profile-tab">
                                        <h4 class="card-heading p-b-20">Profile</h4>
                                        <form>
                                            <div class="form-group">
                                                <!-- <img src="../assets/img/avatars/1.jpg"
                                                    class="w-50 rounded-circle" alt="Albert Einstein"> -->
                                                <div class="file-upload">
                                                    <label for="upload" class="btn btn-primary m-b-0 m-l-5 m-r-5">Upload
                                                        a new picture</label>
                                                    <input id="upload" class="file-upload__input" type="file"
                                                        name="file-upload">
                                                </div>
                                                <button class="btn btn-secondary">Delete</button>
                                            </div>
                                            <div class="form-group">
                                                <label for="inputName">Your name</label>
                                                <input type="text" class="form-control" id="inputName"
                                                    autocomplete="name" placeholder="Enter your name">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleInputEmail1">Email address</label>
                                                <input type="email" class="form-control" autocomplete="email"
                                                    id="exampleInputEmail1" placeholder="Enter email">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleInputPassword1">Password</label>
                                                <input type="password" class="form-control"
                                                    id="exampleInputPassword1" autocomplete="password"
                                                    aria-describedby="passwordHelp" placeholder="Password">
                                                <small id="passwordHelp" class="form-text text-muted">We
                                                    recommend at least 8 characters long, avoiding patterns and
                                                    common words/phrases.</small>
                                            </div>
                                            <div class="form-group">
                                                <label for="inputLocation">Location</label>
                                                <input type="text" class="form-control" id="inputLocation"
                                                    placeholder="Enter location">
                                            </div>
                                            <div class="form-group">
                                                <label for="exampleFormControlTextarea1">Bio</label>
                                                <textarea class="form-control" id="exampleFormControlTextarea1"
                                                    rows="3"></textarea>
                                            </div>
                                            <button type="submit" class="btn btn-primary">Update Profile</button>
                                        </form>
                                    </div>
                                    <div class="tab-pane fade" id="v-pills-orgprofile" role="tabpanel"
                                        aria-labelledby="v-pills-orgprofile-tab">
                                        <h4>School profile</h4>
                                    </div>
                                    <div class="tab-pane fade" id="v-pills-upload" role="tabpanel"
                                        aria-labelledby="v-pills-upload-tab">
                                        <h4 class="card-heading p-b-20">Payment Info</h4>
                                        <form>
                                            <div class="form-group ">
                                                <div class="custom-control custom-radio m-b-20">
                                                    <input type="radio" id="customRadioInline1"
                                                        name="customRadioInline1" class="custom-control-input" checked>
                                                    <!-- <label class="custom-control-label" for="customRadioInline1">
                                                        <img class="max-w-50 m-r-15"
                                                            src="../assets/img/payment-icons/Visa%402x.png" alt>
                                                        <img class="max-w-50 m-r-15"
                                                            src="../assets/img/payment-icons/MasterCard%402x.png" alt>
                                                        <img class="max-w-50 m-r-15"
                                                            src="../assets/img/payment-icons/Discover%402x.png" alt>
                                                        <img class="max-w-50 m-r-15"
                                                            src="../assets/img/payment-icons/AmericanExpress%402x.png"
                                                            alt></label> -->
                                                </div>
                                                <div class="custom-control custom-radio m-b-20">
                                                    <input type="radio" id="customRadioInline2"
                                                        name="customRadioInline1" class="custom-control-input">
                                                    <!-- <label class="custom-control-label" for="customRadioInline2"><img
                                                            class="max-w-50 m-r-15"
                                                            src="../assets/img/payment-icons/Paypal%402x.png" alt></label> -->
                                                </div>
                                            </div>
                                            <div class="form-group">
                                                <label for="inputCard">Card Number</label>
                                                <input type="text" class="form-control" id="inputCard"
                                                    placeholder="•••• •••• •••• 1234">
                                            </div>
                                            <div class="form-row">
                                                <div class="form-group col-md-6">
                                                    <label for="inputExpiration">Expiration</label>
                                                    <input type="text" class="form-control" id="inputExpiration"
                                                        placeholder="MM / YY">
                                                </div>
                                                <div class="form-group col-md-6">
                                                    <label for="inputCvv">CVV</label>
                                                    <input type="text" class="form-control" id="inputCvv"
                                                        placeholder="123">
                                                </div>
                                            </div>
                                            <button type="submit" class="btn btn-primary">Update Profile</button>
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

<script>
export default {

}
</script>

<style>

</style>