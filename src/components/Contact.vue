<script setup>
import { ref } from "vue";

let name = ref("");
let email = ref("");
let msg = ref("");

const handleSubmit = () => {
  console.log(name.value);
  console.log(email.value);
  console.log(msg.value);
};
</script>

<template>
  <div class="grax_tm_contact" id="contact">
    <div class="container">
      <div class="grax_tm_title_holder">
        <h3>Get in <span>Touch</span></h3>
      </div>
      <div class="contact_inner">
        <div class="left wow fadeInLeft" data-wow-duration="1s">
          <div class="text">
            <p
              >I kindly ask you to fill out the form in this section to get in
              touch with me. Please feel free to call between 9:00 a.m. and 8:00
              p.m. ET, Monday through Friday.</p
            >
          </div>
          <div class="info_list">
            <ul>
              <!-- <li>
                    <div class="list_inner">
                      <img class="svg" src="../../public/img/svg/location.svg" alt="" />
                      <p
                        ><span class="first">Address:</span
                        ><span class="second">Brook 103, New York, USA</span></p
                      >
                    </div>
                  </li> -->
              <li>
                <div class="list_inner">
                  <img
                    class="svg"
                    src="../../public/img/svg/email.svg"
                    alt=""
                  />
                  <p
                    ><span class="first">Email:</span
                    ><span class="second"
                      ><a href="#">fajarikasaputra@gmail.com</a></span
                    ></p
                  >
                </div>
              </li>
              <!-- <li>
                    <div class="list_inner">
                      <img class="svg" src="../../public/img/svg/phone.svg" alt="" />
                      <p
                        ><span class="first">Phone:</span
                        ><span class="second"
                          ><a href="#">+77 033 442 55 57</a></span
                        ></p
                      >
                    </div>
                  </li> -->
              <li>
                <div class="list_inner">
                  <img
                    class="svg"
                    src="../../public/img/svg/social/dribbble.svg"
                    alt=""
                  />
                  <p
                    ><span class="first">Website:</span
                    ><span class="second"
                      ><a href="#">www.ajangs-portfolio.vercel.app</a></span
                    ></p
                  >
                </div>
              </li>
              <!-- <li>
                    <div class="list_inner">
                      <img
                        class="svg"
                        src="../../public/img/svg/social/twitter.svg"
                        alt=""
                      />
                      <p
                        ><span class="first">Twitter:</span
                        ><span class="second"
                          ><a href="#">@twitternickname</a></span
                        ></p
                      >
                    </div>
                  </li> -->
              <!-- <li>
                    <div class="list_inner">
                      <img
                        class="svg"
                        src="../../public/img/svg/social/facebook.svg"
                        alt=""
                      />
                      <p
                        ><span class="first">Facebook:</span
                        ><span class="second"
                          ><a href="#">@facebooknickname</a></span
                        ></p
                      >
                    </div>
                  </li> -->
            </ul>
          </div>
        </div>
        <div
          class="right wow fadeInLeft"
          data-wow-duration="1s"
          data-wow-delay=".2s"
        >
          <div class="fields">
            <!-- <form
              action="/"
              method="post"
              class="contact_form"
              id="contact_form"
            > -->
            <form
              action="/"
              method="post"
              class="contact_form"
              id="contact_form"
            >
              <div
                class="returnmessage"
                data-success="Your message has been received, We will contact you soon."
              ></div>
              <div class="empty_notice"
                ><span>Please Fill Required Fields</span></div
              >
              <div class="first">
                <ul>
                  <li>
                    <input id="name" type="text" placeholder="Name" />
                  </li>
                  <li>
                    <input id="email" type="text" placeholder="Email" />
                  </li>
                </ul>
              </div>
              <div class="last">
                <textarea id="message" placeholder="Message"></textarea>
              </div>
              <div class="grax_tm_button">
                <a
                  type="submit"
                  id="send_message"
                  target="_blank"
                  rel="noopener noreferrer"
                  >Send Message</a
                >
              </div>

              <!-- If you want to change mail address to yours, please open modal.php and go to line 4 -->
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
