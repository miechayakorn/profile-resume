<template>
  <article class="col-md-12">
    <div class="container">
      <div class="row d-flex justify-content-center">
        <div class="col-md-5">
          <div class="card card-profile animated fadeInUp">
            <a
              style="position: absolute; left: 0; top: 0"
              class="p-2"
              target="_blank"
              href="https://drive.google.com/file/d/1AuTRmSVV4s78fV-oI8wP8Nav-j2SOPOR/view?usp=sharing"
            >
              Transcript
            </a>
            <a
              style="position: absolute; right: 0; top: 0"
              class="p-2"
              target="_blank"
              href="https://www.miechayakorn.tk/doc/Resume-miechayakorn.pdf"
            >
              Resume
            </a>
            <div class="card-avatar">
              <img class="img" src="@/assets/miechayakorn.jpg" />
            </div>

            <div class="table">
              <h4 class="card-caption">Chayakorn Pradchayakul</h4>
              <h6 class="card-description text-muted">
                I am a developer 🐻🧸
              </h6>
              <div class="card-description">
                School of Information Technology, KMUTT <br />
                ===== <br />
                <div>
                  <i class="fa fa-envelope"> miechayakorn@gmail.com</i>
                </div>
                <div>
                  <i class="fa fa-phone"> 088-9306924</i>
                </div>
                <div>
                  <i class="fa fa-map-marker">
                    40/224 Rama II Rd, Bang Mot, Chom Thong, Bangkok 10150</i
                  >
                </div>
              </div>
              <div class="ftr">
                <a
                  href="https://fb.com/MieChayakorn1"
                  class="btn btn-just-icon btn-facebook btn-round"
                  target="_blank"
                >
                  <i class="fa fa-facebook"></i>
                </a>
                <a
                  href="https://line.me/ti/p/VHm8IGfVBS"
                  style="background-color: #00b900"
                  class="btn btn-just-icon btn-round"
                  target="_blank"
                >
                  <img
                    src="https://www.miechayakorn.tk/pic/LINE_APP.png"
                    style="width: 20px"
                    alt=""
                  />
                </a>
                <a
                  href="https://instagram.com/mie_chayakorn"
                  style="background-color: #c13584; color: #f5f5f5"
                  class="btn btn-just-icon btn-instagram btn-round"
                  target="_blank"
                >
                  <i class="fa fa-instagram"></i>
                </a>
                <a
                  href="https://github.com/miechayakorn"
                  style="background-color: #554488; color: #f5f5f5"
                  class="btn btn-just-icon btn-github btn-round"
                  target="_blank"
                >
                  <i class="fa fa-github"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </article>
</template>
<script>
export default {
  name: "ProfileCard",
};
</script>
