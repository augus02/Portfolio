<template>
    <main class="contact-page">
        <h1 class="pageTitle"> Contact </h1>
        <div class="formwrapper">
            <div class="contact-form">
                <form @submit.prevent="submitForm">
                    <label for="name">Name:</label>
                    <input type="text" id="name" v-model="name" required>

                    <label for="email">Email:</label>
                    <input type="email" id="email" v-model="email" required>

                    <label for="message">Message:</label>
                    <textarea id="message" v-model="message" required></textarea>

                    <button type="submit">Submit</button>
                </form>

                <div v-if="submitted" id="successMessage">
                    <p>Form submitted successfully!</p>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped>

.contact-form {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 8px;
}

input, textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 16px;
  box-sizing: border-box;
}

button {
  background-color: #007BFF;
  color: #fff;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

.hidden {
  display: none;
}

#successMessage {
  color: #28a745;
  margin-top: 16px;
}

.contact-page{
    flex-direction: row;
    text-align: center;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.pageTitle{
    color: azure;
    font: bold;
    text-align: center;
    padding-top: 48px;
    padding-bottom: 48px;
}

.formwrapper{
    width: 100%;
    height: 75%;
}
</style>
<script>
    export default{
            data() {
    return {
      name: '',
      email: '',
      message: '',
      submitted: false
    };
  },
  methods: {
    submitForm() {
      // You can perform form submission logic here
      // For simplicity, let's just show a success message

      // Display success message
      this.submitted = true;

      // Reset the form fields
      this.name = '';
      this.email = '';
      this.message = '';
    }
  }
}
</script>



