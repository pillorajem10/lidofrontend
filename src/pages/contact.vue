<template>
    <div class="contact">
      <h1>CONTACT US</h1>
        <form>
            <div class="nameFields">
                <div>
                    <label for="firstName">First Name:</label>
                    <input type="text" id="firstName" name="firstName" required>
                </div>

                <div>
                    <label for="lastName">Last Name:</label>
                    <input type="text" id="lastName" name="lastName" required>
                </div>
            </div>

            <div>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>

            <div>
                <label for="phone">Phone #:</label>
                <input type="tel" id="phone" name="phone" required>
            </div>

            <div>
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>
            </div>

            <button type="submit">Submit</button>
        </form>
    </div>
  </template>

<script>
export default {
  name: 'About'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.contact {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 5%;
}

.nameFields{
    display: flex;
    gap: 2rem;
}

label {
    font-weight: bold;
}

input, textarea {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
}

button {
    padding: 0.5rem 1rem;
    font-size: 1rem;
    background-color: #ffbb00;
    color: 002030;
    border: none;
    cursor: pointer;
    border-radius: 10px;
}

button:hover {
    background-color: #fff;
    color: #ffbb00;
    border: solid;
}

@media (max-width: 700px) {
    .nameFields {
        flex-direction: column;
        gap: 0;
    }

    .nameFields .fieldContainer {
        width: 100%;
    }

}
</style>
