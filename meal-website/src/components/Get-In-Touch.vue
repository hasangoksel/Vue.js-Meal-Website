<template>
    <div class="get-in-touch">
        <div class="get-in-touch-title">
            <h2>Get In Touch</h2>
        </div>
        <form class="get-in-touch-form">
            <div class="form-group">
                <label for="get-name">Name</label>
                <div class="form-input-group">
                    <input type="text" id="get-name">
                    <i class="fa-solid fa-user"></i>
                </div>
            </div>
            <div class="form-group">
                <label for="get-email">E-mail</label>
                <div class="form-input-group">
                    <input type="email" id="get-email">
                    <i class="fa-solid fa-envelope"></i>
                </div>
            </div>
            <div class="form-group">
                <label for="get-phone">Phone</label>
                <div class="form-input-group">
                    <input type="tel" id="get-phone">
                    <i class="fa-solid fa-phone"></i>
                </div>
            </div>
            <div class="form-group-textarea">
                <label for="message" class="label-textarea">Message</label>
                <div class="form-input-group">
                    <textarea id="message"
                    cols="83" rows="12"></textarea>
                </div>
            </div>
            <div class="form-group">
                <button>Send Message</button>
            </div>
        </form>
    </div>
</template>