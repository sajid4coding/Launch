<script setup>
    import { Icon } from '@iconify/vue';
    const margin = 'margin-bottom: 120px'
</script>

<template>
    <div class="container" :style="margin">
        <section class="mb-4">

            <h2 class="h1-responsive font-weight-bold text-center my-4">Get In Touch</h2>
            <p class="text-center w-responsive mx-auto mb-5">Do you have any questions? Please do not hesitate to contact us directly. Our team will come back to you within
                a matter of hours to help you.</p>

            <div class="row">

                <!--Grid column-->
                <div class="col-md-8 mb-md-0 mb-5">
                    <form>

                        <!--Grid row-->
                        <div class="row">

                            <!--Grid column-->
                            <div class="col-md-6">
                                <div class="md-form mb-3">
                                    <label for="name" class="">Your name</label>
                                    <input type="text" id="name" name="name" class="form-control">
                                </div>
                            </div>
                            <!--Grid column-->

                            <!--Grid column-->
                            <div class="col-md-6">
                                <div class="md-form mb-3">
                                    <label for="email" class="">Your email</label>
                                    <input type="text" id="email" name="email" class="form-control">
                                </div>
                            </div>
                            <!--Grid column-->

                        </div>
                        <!--Grid row-->

                        <!--Grid row-->
                        <div class="row">
                            <div class="col-md-12">
                                <div class="md-form mb-3">
                                    <label for="subject" class="">Subject</label>
                                    <input type="text" id="subject" name="subject" class="form-control">
                                </div>
                            </div>
                        </div>
                        <!--Grid row-->

                        <!--Grid row-->
                        <div class="row">

                            <!--Grid column-->
                            <div class="col-md-12">

                                <div class="md-form">
                                    <label for="message">Your message</label>
                                    <textarea type="text" id="message" name="message" rows="10" class="form-control md-textarea"></textarea>
                                </div>

                            </div>
                        </div>
                        <!--Grid row-->

                    </form>

                    <div class="text-center d-grid gap-2 col-6 mx-auto my-4">
                        <button class="btn btn-primary" type="button">Send</button>
                    </div>

                    <div class="status"></div>
                </div>
                <!--Grid column-->

                <!--Grid column-->
                <div class="col-md-4">
                    <h4 class="mb-4">Contact Us</h4>
                    <ul class="list-unstyled mb-0">
                        <li>
                            <p><Icon icon="ion:location-sharp" /> San Francisco, CA 94126, USA</p>
                        </li>

                        <li>
                            <p><Icon icon="ic:round-phone" /> + 01 234 567 89</p>
                        </li>

                        <li>
                            <p><Icon icon="ic:round-phone" /> + 01 234 567 90</p>
                        </li>

                        <li>
                            <p><Icon icon="ic:baseline-email" /> contact@example.com</p>
                        </li>

                        <li>
                            <p><Icon icon="icon-park:world" /> www.example.com</p>
                        </li>
                    </ul>
                </div>
                <!--Grid column-->

            </div>

        </section>
    </div>
</template>