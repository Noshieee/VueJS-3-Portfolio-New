<template>
<section id="Contact">
    <h1 class="text-center fw-bold">Contact Me!</h1>
	    <div class="contact-box">
            <form action="https://formspree.io/f/xknyjryb" method="POST">
                <input type="text" name="Your Name" class="input-field" placeholder="Your Name">
                <input type="email" name="Your Email" class="input-field" placeholder="Your Email">
                <textarea type="text" name="Your Message" class="input-field textarea-field" placeholder="Your Message"></textarea>
                <button type="submit" class="btn">Send Message</button>    
            </form>
            <div class="socials">
		        <a class="btn btn-dark" href="https://www.linkedin.com/in/enosh-elliott-bab50a224/" target="_blank"><i class="fab fa-linkedin"></i></a>
		        <a class="btn btn-dark" href="https://github.com/Noshieee" target="_blank"><i class="fab fa-github"></i></a>
            </div>
        </div>

</section>
</template>

<script>
export default {
    name: 'Contact' ,
    components: {
    }
}
</script>

<style scoped>

.contact-box{
    width: 500px;
    box-shadow: 0 0 20px 0 rgb(10, 253, 213);
    /* top: 50%; */
    /* left: 50%; */
    /* transform: translate(100%,0%); */
    position: relative;
    background-image: url();
}

form{
    margin:35px;
}

.input-field{
    width: 400px;
    height: 40px;
    margin-top: 20px;
    padding-left: 10px;
    padding-right: 10px;
    border:1px solid #777;
    border-radius: 14px;
    outline: none;
    background-color:rgb(255, 255, 255);
}

.textarea-field{
    height:150px;
    padding-top: 10px;
}

.btn{
    border-radius: 20px;
    color: rgb(8, 255, 234);
    margin-top: 18px;
    padding: 10px;
    background-color: rgb(5, 5, 5);
    font-size: 12px;
    border: none;
    cursor: pointer;
    margin-bottom: 18px;
}

.btn:hover{
    color: rgb(12, 12, 12);
    background-color: rgb(7, 243, 223);
    transition: ease-in;
    transition-delay: 25ms;
}
</style>