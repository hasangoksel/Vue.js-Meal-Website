<template>
    <div id="reserve" class="reservation">
        <div class="reservation-title">
            <h2>Reservation</h2>
            <p>Free Website Template For Restaurants Made by Göksel</p>
        </div>
        <form class="reservation-form">
            <div class="form-group">
                <label for="name">Name</label>
                <div class="form-input-group">
                    <input type="text" id="name">
                    <i class="fa-solid fa-user"></i>
                </div>
            </div>
            <div class="form-group">
                <label for="email">E-mail</label>
                <div class="form-input-group">
                    <input type="email" id="email">
                    <i class="fa-solid fa-envelope"></i>
                </div>
            </div>
            <div class="form-group">
                <label for="phone">Phone</label>
                <div class="form-input-group">
                    <input type="tel" id="phone">
                    <i class="fa-solid fa-phone"></i>
                </div>
            </div>
            <div class="form-group">
                <label for="person">Person</label>
                <div class="form-input-group">
                    <select id="person">
                        <option>1 person</option>
                        <option>2 person</option>
                        <option>3 person</option>
                        <option>4 person</option>
                        <option>5+ persons</option>
                    </select>
                </div>
            </div>
            <div class="form-group">
                <label for="date">Date</label>
                <div class="form-input-group">
                    <input type="date" id="date">
                </div>
            </div>
            <div class="form-group">
                <label for="time">Time</label>
                <div class="form-input-group">
                    <input type="time" id="time">
                </div>
            </div>
            <div class="form-group">
                <button>Reserve Now</button>
            </div>
        </form>
    </div>
</template>