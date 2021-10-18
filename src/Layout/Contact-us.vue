<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="row section-b-space">
        <div class="col-lg-7 map">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3648.3480783303107!2d90.38531421493555!3d23.87727278452697!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755c413f4b21791%3A0x96af459f1682f167!2sRd%20No%2014%2C%20Dhaka%201230!5e0!3m2!1sen!2sbd!4v1633936585831!5m2!1sen!2sbd" width="800" height="500" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>
        <div class="contact">
          <address>
			      <strong class="title">Office Location:</strong><br>
			      Sector: 11, Road: 14, House: 76<br>
			      Uttara, Dhaka<br>
		      </address>
			    <strong class="title">Phone:</strong> <br>01880089100<br>01880089101<br>01880089102<br>
			    <strong class="title">Email:</strong> <br>travelforing@gmail.com
          <div class="widget noborder notoppadding">
            <a href="https://www.facebook.com/travelforing/" target="_blank" class="social-icon si-small si-dark si-facebook">
				      <i class="icon-facebook"></i>
				      <i class="icon-facebook"></i>
			      </a>
            <a href="https://instagram.com/foringer_dol?utm_medium=copy_link" target="_blank" class="social-icon si-small si-dark si-facebook">
				      <i class="icon-instagram"></i>
				      <i class="icon-instagram"></i>
			      </a>
            <a href="https://youtube.com/channel/UC-CGAoKw4Cf4xJt8kT8B-ZQ" target="_blank" class="social-icon si-small si-dark si-facebook">
				     <i class="icon-youtube"></i>
				     <i class="icon-youtube"></i>
			      </a>
		  	  </div>
		    </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";

export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>
<style scoped>
.contact-icon{
    height: 30px;
    width: 30px;
}
.contact-icon h6{
    font-size: 2rem;
}
.container{
  display: flex;
}
.contact{
 position: relative;
 right:-35%;
 top: 15%;
 text-align: left;
}
.title{
  font-size: 2rem;
}
</style>