<template>
    <div class="courses">
        <div class="hero is-info">
            <div class="hero-body has-text-centered">
                <h1 class="title">Courses</h1>
            </div>
        </div>

        <section class="section">
            <div class="container">
                <div class="columns">
                    <div class="column is-2">
                        <aside class="menu">
                            <p class="menu-label">Categories</p>

                            <ul class="menu-list">
                                <li><a class="is-active">All Courses</a></li>
                                <li><a>Zumba</a></li>
                                <li><a>Aqua</a></li>
                                <li><a>Katabox</a></li>
                                <li><a>Hiit</a></li>
                                <li><a>Cardio</a></li>
                                <li><a>Strength Training</a></li>
                                <li><a>Boxing</a></li>
                                <li><a>Muay Thai</a></li>
                                <li><a>Nutrition</a></li>
                            </ul>
                        </aside>
                    </div>

                    <div class="column is-10">
                        <div class="columns is-multiline">
                            <!-- <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Zumba Dance 101 Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Zumba Kids is a specialized program of Zumba Fitness 
                                                that is geared toward our youngsters, teaching fun 
                                                dances to international rhythms, keeping them active, 
                                                and burning off energy in an exciting way!Our instructors 
                                                incorporate their passion for helping kids express 
                                                themselves through dance, and enjoying fun, age 
                                                appropriate music into every class....
                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Aqua 101 Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Aqua fitness is a terrific low impact fitness training program that builds 
                                                strength and endurance. Many people swear by this type of training. 
                                                Water provides natural resistance and keeps you cool during the class. 
                                                We offer a variety of water classes at multiple locations. Check our locations
                                                and our calendars and grab a two day pass to give it a shot.
                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Katabox Brilliant Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Katabox which is similar to aerobics, has its origins in the 
                                                martial arts. So, someone has used their martial arts training or 
                                                ability to devise an exercise routine, which can be instructed just 
                                                like aerobics. People may use it for fitness rather than self-defense, 
                                                while focusing on endurance, strength, intervals, high intensity (race days) 
                                                and recovery...
                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div> -->

                            <div 
                                class="column is-4"
                                v-for="course in courses"
                                v-bind:key="course.id"
                            >
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>{{ course.title }}</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                {{ course.short_description }}
                                            </p>

                                            <router-link :to="{name: 'Course', params: {slug: course.slug}}">More</router-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
<!-- 
                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>HIIT 101 Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                As you can tell from the name, high-intensity interval 
                                                training (HIIT) is challenging. It takes your cardio 
                                                workout to another level, as you push your pace out of 
                                                your comfort zone.You can use HIIT with any type of cardio 
                                                workout, whether it's running, using a stair climbing machine,
                                                rowing, or jumping rope.You’ll work up a sweat fast, working at 
                                                a very intense level and then backing off for a slower recovery period, 
                                                followed by another round of high intensity.
                                                That strategy can save you time: You don't have to 
                                                work out as long as you would if you were keeping a 
                                                steady pace.You’ll lose weight, build muscle, and 
                                                boost your metabolism. Plus there’s a post-workout 
                                                bonus: Your body will burn calories for about 2 hours 
                                                fter you exercise.
                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Cardio 101 Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Cardio fitness measures how well your body can 
                                                perform a rhythmic, dynamic activity at a moderate to 
                                                high intensity for extended periods of time. While cardio 
                                                exercise is great for burning calories and losing weight, 
                                                it also improves your cardiovascular fitness.Your cardio 
                                                fitness refers to how well your heart, lungs, and organs 
                                                consume, transport, and use oxygen throughout your workout. 
                                                Your overall fitness depends on the relationship between your 
                                                cardiovascular system, respiratory system, and skeletal system.

                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Cardio 101 Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Cardio fitness measures how well your body can 
                                                perform a rhythmic, dynamic activity at a moderate to 
                                                high intensity for extended periods of time. While cardio 
                                                exercise is great for burning calories and losing weight, 
                                                it also improves your cardiovascular fitness.Your cardio 
                                                fitness refers to how well your heart, lungs, and organs 
                                                consume, transport, and use oxygen throughout your workout. 
                                                Your overall fitness depends on the relationship between your 
                                                cardiovascular system, respiratory system, and skeletal system.

                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Strength Training Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Strength training can help you tone your muscles and 
                                                improve your appearance. With a regular strength 
                                                training program, you can reduce your body fat, 
                                                increase bone strength, increase your lean muscle 
                                                mass and burn calories more efficiently.Better yet, 
                                                strength training doesn't have to take as long as you 
                                                might think. For most people, one set of strength 
                                                exercises for all the major muscle groups performed to 
                                                fatigue at the 12th to 15th repetition and performed at 
                                                least two times a week is sufficient.
                                                
                                                Strength training can be done at home or in the gym.
                                                Free weights and weight machines are popular strength 
                                                training tools, but they're not the only options.You 
                                                can do strength training with inexpensive resistance 
                                                tubing or even your own body weight. 
                                                With proper technique, you may enjoy noticeable 
                                                improvements in your strength and stamina over time.

                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>                                                                      
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Boxing Training Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                When you’re pressed for time in your fitness routine, 
                                                boxing may offer a solution.These heart-pumping activities 
                                                not only burn a lot of calories and help you achieve the 
                                                recommended 2.5 hoursTrusted Source of aerobic exercise per week. 
                                                You’ll also gain strength-training benefits, depending on your 
                                                specific routine.Boxing workouts can be done with or without a bag, 
                                                and they can also incorporate free weights and other equipment.
                                                
                                                Boxing routines are more than what you see on a televised match. 
                                                While still based on martial arts-inspired movements, the variations 
                                                in this exercise can offer challenges for all fitness levels. 
                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>                                                                      
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Muay Thai Training</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Did you know Muay Thai fighting comes with multiple benefits 
                                                or your heart? 
                                                
                                                The Muay Thai fitness training can beat all your cardio 
                                                workouts, CrossFit workouts, or HIIT personal workouts. 
                                                The Muay Thai history dates back centuries ago, and it is also 
                                                the national sport of Thailand. People of Thailand have been 
                                                practicing this super intense workout for hundreds of years now. 
                                                This combat style workout is also the absolute favorites of 
                                                celebrities like Ryan Gosling and Gina Rodriguez. 
                                                
                                                It demands full hands and legs to body contact that is you have 
                                                to attack using your fists, elbows, knees, and feet. This should 
                                                be your fitness regimen boys when you want to have a more grueling 
                                                workout. It not only helps you outdo the challenges faced by your 
                                                mind but also by your body!

                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>                                                                      
                                </div>
                            </div>

                            <div class="column is-4">
                                <div class="card">
                                    <div class="card-image">
                                        <figure class="image is-4by3">
                                            <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
                                        </figure>
                                    </div>
                                    
                                    <div class="card-content">
                                        <div class="media">
                                            <div class="media-content">
                                                <p class="is-size-5">
                                                    <strong>Nutrition Health Fitness</strong> 
                                                </p>
                                            </div>
                                        </div>

                                        <div class="content">
                                            <p>
                                                Importance Of nutrition In life! This section is for 
                                                people who want to find out about the science of 
                                                nutrition through life and how this affects health. 
                                                Health fitness nutrition plays a vital role. Just as 
                                                the damaging effects of malnutrition can pass from 
                                                one generation to the next, so can the benefits of 
                                                good nutrition. Giving a child a solid nutritional 
                                                start has an impact on life on her or his physical, 
                                                mental and social development. Regular exercise is 
                                                needed for fitness goals but nutrition also plays an 
                                                important role for a fit body. 
                                                
                                                The fitnesshealthforever provides you best information 
                                                about health fitness nutrition.

                                            </p>

                                            <a href="#">More</a>
                                        </div>
                                    </div>                                                                      
                                </div>
                            </div> -->

                            <div class="column is-12">
                                <nav class="pagination is-centered">
                                    <a class="pagination-previous">Previous</a>
                                    <a class="pagination-next">Next</a>

                                    <ul class="pagination-list">
                                        <li>
                                            <a class="pagination-link is-current">1</a>
                                        </li>
                                        <li>
                                            <a class="pagination-link">2</a>
                                        </li>
                                           <li>
                                            <a class="pagination-link">3</a>
                                        </li>
                                    </ul>

                                </nav>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </section> 

    </div>
</template>

<script>
import axios from 'axios'

export default {

    data(){
        return {
            courses: []
        }
    },

    mounted(){
       console.log('mounted')

       axios
            .get('/api/v1/courses/')
            .then(response => {
                console.log(response.data)

                this.courses = response.data
            })
    }
    
}
</script>