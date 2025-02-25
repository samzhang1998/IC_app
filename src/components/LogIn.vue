<template>
  <div id="login_home">
    <img src="../assets/IClogo.png" alt="logo" class="logo_home"/>
    <h1>Welcome Back to </h1>
    <h2>Infinity CAPITAL</h2>
    <p>Hello there, login to continue</p>
    <div class="sign_in">
      <div>
        <h3>Sign In</h3>
        <p>Sign in to my account</p>
        <div class="sign_in_input">
          <p>Email</p>
          <input 
            placeholder="My Email"
          />
          <p>Password</p>
          <input 
            placeholder="My Password"
          />
          <div class="login_option">
            <div class="remember">
              <input type="checkbox" v-model="isRemembered" :style="checkboxStyle" class="login_checkbox"/>
              <p>Remember me</p>
            </div>
            <p>Forgot Password</p>
          </div>
          <button>Sign In</button>        
        </div>
        <p>Don't have an account? Sign Up Here</p>
      </div>
      <label>
        <input type="checkbox" v-model="isAgreed" :style="checkboxStyle" class="login_checkbox"/>
        <span>I agree to the Terms & Conditions & Privacy Policy Set out by this site.</span>
      </label>
    </div>
  </div>
</template>

<script setup>
  import { ref, computed } from "vue";
  const isRemembered = ref(false);
  const isAgreed = ref(false);
  const checkboxStyle = computed(() => ({
    width: "15px",
    height: "15px",
    border: "2px solid #EFC462",
    borderRadius: "3px",
    backgroundColor: "#EFC4621A",
    appearance: "none",
    display: "inline-block",
    position: "relative",
    padding: "0",
    margin: "0",
    marginRight: "5px"
  }));
</script>

<style scoped>
  #login_home {
    width: 100%;
    height: 100vh;
    background: black;
    display: flex;
    flex-direction: column;
    justify-content: end;
  }
  .logo_home {
    width: 70%;
    margin-left: 5%;
  }
  h1 {
    margin-left: 5%;
    color: #fff;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    margin-bottom: 0;
    margin-top: 8%;
  }
  h2 {
    margin-left: 5%;
    color:#EFC462;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    margin-bottom: 0;
    margin-top: 2%;
  }
  p {
    margin-left: 5%;
    color: #fff;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    margin-top: 2%;
    margin-bottom: 8%;
  }
  .sign_in {
    width: 100%;
    height: 60vh;
    background: #fff;
    border-radius: 20px 20px 0 0;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  h3 {
    text-align: center;
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: 32px;
    margin-bottom: 0;
  }
  .sign_in p {
    color: #475467;
    text-align: center;
    margin: 0;
    margin-bottom: 3%;
  }
  .sign_in_input {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .sign_in_input p {
    width: 90%;
    font-size: 12px;
    text-align: start;
    margin: 0;
  }
  input {
    width: 83%;
    height: 20px;
    border-radius: 8px;
    padding: 12px;
    margin-bottom: 5%;
    border: 1px solid var(--Color-Gray-Gray-400, #98A2B3);
    box-shadow: 0px 1px 2px 0px rgba(16, 24, 40, 0.05);
  }
  .login_option {
    width: 90%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 5%;
  }
  .login_option p {
    width: auto;
    color: #EFC462;
  }
  .remember {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 40%;
  }
  .login_checkbox::after {
    content: "";
    position: absolute;
    display: none;
    left: 1.5px;
    top: 0;
    width: 5px;
    height: 8px;
    border: solid #EFC462;
    border-width: 0 2px 3px 0;
    transform: rotate(35deg);
  }
  .login_checkbox:checked::after {
    display: block;
  }
  .remember p {
    color: #000;
  }
  button {
    display: flex;
    width: 90%;
    height: 48px;
    padding: 12px 20px;
    margin-bottom: 5%;
    justify-content: center;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    border-radius: 100px;
    border: none;
    background: #EFC462;
    color: #fff;
    text-align: center;
    font-family: Nunito;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 20px;
    letter-spacing: 0.1px;
  }
  label {
    width: 90%;
    margin-left: 5%;
    margin-bottom: 5%;
    display: flex;
    flex-direction: row;
    align-items: center;
    font-size: 10px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    letter-spacing: -0.2px;
  }
</style>
