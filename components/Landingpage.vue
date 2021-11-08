<template>
<div>
    <div v-if="!$vuetify.breakpoint.mobile">
        <div style="position: relative;" fluid>
            <v-container style="position: absolute; z-index: 1" fluid>
                <v-alert width=100%  color="#DB2C27" class='top'>
                    <h4 class="white--text">เข้าร่วมกิจกรรม Workshop เพื่อร่วมเป็นหนึ่งในการพัฒนานวัตกรรมการศึกษา <u>คลิกที่นี่</u></h4>
                </v-alert>
                <v-container>
                    <v-row align="center" class="d-flex">
                        <img src="/public/logocut.png" class="cursor:pointer;" width="20%" />
                        <v-col class="tabs" cols="1">
                            <p>คุณสมบัติ</p>
                        </v-col>
                        <v-col class="tabs" cols="1">
                            <p>บทความ</p>
                        </v-col>
                        <v-col class="tabs" cols="2">
                            <p>ทดลองการใช้งาน</p>
                        </v-col>
                        <v-col cols="2"/>
                        <v-col class="tabs" cols="1">
                            <p>เข้าร่วมควิช</p>
                        </v-col>
                        <v-col cols="1">
                            <v-btn color="#DB2C27" class="rounded-lg" large dark>เข้าสู่ระบบ</v-btn>
                        </v-col>
                        <v-col cols="1">
                            <v-btn class="ma-2" outlined color="white">En</v-btn>
                        </v-col>
                    </v-row>
                </v-container>
                <v-container justify="center">
                    <v-row>
                        <v-col class="white--text" align="center">
                            <h1>SKOOLKIT จะทำให้ทุกคนในชั้นเรียน<br>มีส่วนร่วมในการเรียนรู้</h1>
                            <h4>เพราะเราเชื่อว่า " การเรียนรู้ที่ดีที่สุดคือการมีส่วนร่วมในการเรียนรู้ "</h4>
                            <v-btn color="#DB2C27" class="rounded-lg" large dark>ทดลองใช้งานฟรี</v-btn>
                            <v-btn class="ma-2 rounded-lg" outlined color="white" large>ดูวีดีโอ</v-btn>
                        </v-col>
                    </v-row>
                </v-container>
            </v-container>
        </div>
        <video src="/public/video1.mov" style="position: relative;" width=100% autoplay/>
    </div>
    <div v-else> <!-- for mobile -->
            <!-- <div style="position: relative;" fluid> -->
            <!-- <v-container style="position: absolute; z-index: 1" fluid> -->
                <v-alert width=100%  color="#DB2C27" class='top'>
                    <h4 class="white--text">เข้าร่วมกิจกรรม Workshop เพื่อร่วมเป็นหนึ่งในการพัฒนานวัตกรรมการศึกษา <u>คลิกที่นี่</u></h4>
                </v-alert>
                <v-container>
                    <img src="/public/logocut.png" width="100%" />
                    <v-row align="center">
                        <v-col>
                            <p class="tabs">คุณสมบัติ</p>
                            <br>
                            <p class="tabs">บทความ</p>
                            <br>
                            <p class="tabs">ทดลองการใช้งาน</p>
                        </v-col>
                        <v-col />
                        <v-col>
                            <p class="tabs">เข้าร่วมควิช</p>
                            <br>
                            <v-btn color="#DB2C27" class="rounded-lg" large dark>เข้าสู่ระบบ</v-btn>
                            <br>
                            <v-btn class="ma-2" outlined color="white">En</v-btn>
                        </v-col>
                    </v-row>
                </v-container>
                <v-container justify="center">
                    <v-row>
                        <v-col class="white--text" align="center">
                            <h1>SKOOLKIT จะทำให้ทุกคนในชั้นเรียนมีส่วนร่วมในการเรียนรู้</h1>
                            <h4>เพราะเราเชื่อว่า " การเรียนรู้ที่ดีที่สุดคือการมีส่วนร่วมในการเรียนรู้ "</h4>
                            <v-btn color="#DB2C27" class="rounded-lg" dark>ทดลองใช้งานฟรี</v-btn>
                            <v-btn class="ma-2 rounded-lg" outlined color="white">ดูวีดีโอ</v-btn>
                        </v-col>
                    </v-row>
                </v-container>
            <!-- </v-container> -->
        <!-- </div> -->
        <!-- <video src="/public/video1.mov" style="position: relative;" width="100%" autoplay/> -->
    </div>

    <v-container>
        <div v-if="!$vuetify.breakpoint.mobile" class="d-flex">
            <v-row>
                <v-col v-for="item in pic" :key="item" >
                        <v-img :src="item.img" max-width="95" />
                </v-col>
            </v-row>
        </div>
        <div v-else>
            <v-row align="center" justify="center">
                <v-col v-for="item in pic" :key="item">
                    <v-img :src="item.img" max-width="95" />
                </v-col>
            </v-row>
        </div>
    </v-container>
    <v-container class="text-center">
        <strong>
        <h1>SKOOLKIT รวบรวมเครื่องมือและสื่อ <br>สำหรับการจัดการเรียนการสอนแบบ Active Learning</h1>
        </strong>
        <v-row class="d-flex justify-center text-center">
            <v-col v-for="item in icon" :key="item" jusitfy="center" cols="1">
                    <v-img :src="item.img" max-width="100%" />
                    <h4 class="text-center">{{ item.text }}</h4>
            </v-col>
        </v-row>
        <v-img src="public\screen\รวม.png" />
    </v-container>
    <v-container>
        <div v-if="!$vuetify.breakpoint.mobile">
            <v-row align="center">
                <v-col cols="7">
                    <v-img src="public\screen\เช็คชื่อ 1.png" />
                </v-col>
                <v-col cols="5">
                    <strong><h1>เครื่องมือการจัดการสอน<br>ที่จำเป็นสำหรับคุณครู</h1></strong>
                    <p>ไม่ว่าจะเป็นการเช็คชื่อ การสุ่ม การแบ่งกลุ่ม<br>การโหวต และอื่นๆ ที่เต็มไปด้วยประสบการณ์ใหม่ๆ<br>ให้มีความสุขและน่าตื่นเต้น</p>
                    <p class="red--text"><u>ดูคุณสมบัติเพิ่มเติม</u></p>
                </v-col>
            </v-row>
        </div>
        <div v-else>
            <v-col align="center">
                    <v-img src="public\screen\เช็คชื่อ 1.png" />
                    <strong><h1>เครื่องมือการจัดการสอน<br>ที่จำเป็นสำหรับคุณครู</h1></strong>
                    <p>ไม่ว่าจะเป็นการเช็คชื่อ การสุ่ม การแบ่งกลุ่ม<br>การโหวต และอื่นๆ ที่เต็มไปด้วยประสบการณ์ใหม่ๆ<br>ให้มีความสุขและน่าตื่นเต้น</p>
                    <p class="red--text"><u>ดูคุณสมบัติเพิ่มเติม</u></p>
            </v-col>
        </div>
    </v-container>
    
    <v-container>
        <div v-if="!$vuetify.breakpoint.mobile">
            <v-row align="center">
                <v-col cols="5">
                    <strong><h1>รายงานผล</h1></strong>
                    <p>ระบบเก็บข้อมูลจากทุกกิจกรรมที่เกิดขึ้น ในห้องเรียน<br>ทุกคาบเรียน เพื่อให้ทั้งคุณครู นักเรียน และผู้อำนวยการ<br>โรงเรียนเข้าถึงข้อมูลเหล่านี้ เพื่อนำข้อมูลไปใช้ประโยชน์<br>ในการพัฒนาคุณภาพการเรียนการสอนต่อไป</p>
                </v-col>
                <v-col cols="7">
                    <v-img src="public\screen\รีพอร์ต 2.png" />
                </v-col>
            </v-row>
        </div>
        <div v-else>
            <v-col align="center">
                <v-img src="public\screen\รีพอร์ต 2.png" />
                <strong><h1>รายงานผล</h1></strong>
                <p>ระบบเก็บข้อมูลจากทุกกิจกรรมที่เกิดขึ้น ในห้องเรียนทุกคาบเรียน เพื่อให้ทั้งคุณครู นักเรียน และผู้อำนวยการโรงเรียนเข้าถึงข้อมูลเหล่านี้ เพื่อนำข้อมูลไปใช้ประโยชน์ในการพัฒนาคุณภาพการเรียนการสอนต่อไป</p>
            </v-col>
        </div>
    </v-container>

    <v-container align="center">
        <div v-if="!$vuetify.breakpoint.mobile">
            <v-row>
                <v-col cols="7">
                    <v-img src="public\screen\รีพอร์ต 2.png" />
                </v-col>
                <v-col cols="5">
                    <strong><h1>สื่อการเรียนการสอน<br>ในรูปแบบเกม</h1></strong>
                    <p>สื่อการสอนที่เน้นความรู้ และการปฏิสัมพันธ์ในชั้นเรียน<br>ออกแบบให้เหมาะสมกับทุกสถาณการณ์ ไม่ว่าจะเป็น<br> การเรียน on-site หรือ online โดยที่นักเรียน<br>ไม่จำเป็นต้องใช้อุปกรณ์อิเล็กทรอนิกส์ใด ๆ</p>
                </v-col>
            </v-row>
        </div>
        <div v-else>
            <v-col align="center">
                <v-img src="public\screen\รีพอร์ต 2.png" />
                <strong><h1>สื่อการเรียนการสอน<br>ในรูปแบบเกม</h1></strong>
                    <p>สื่อการสอนที่เน้นความรู้ และการปฏิสัมพันธ์ในชั้นเรียนออกแบบให้เหมาะสมกับทุกสถาณการณ์ ไม่ว่าจะเป็นการเรียน on-site หรือ online โดยที่นักเรียนไม่จำเป็นต้องใช้อุปกรณ์อิเล็กทรอนิกส์ใด ๆ</p>
            </v-col>
        </div>

    </v-container>

    <v-container class="text-center">
        <h1>และบทเรียนอีกมากมาย</h1>
        <p>รวมเนื้อหาในชั้นเรียน และข้อสอบจากสนามต่าง ๆ<br>สามารถกลับไปทบทวนย้อนหลังได้ทุกที่ ทุกเวลา</p>
    </v-container>
    <div class="d-flex flex-row" circle>
            <v-img v-for="item in subject1" :key="item" :src="item.img" width="14%" contain />
    </div>
    <div class="d-flex flex-row" circle>
            <v-img v-for="item in subject2" :key="item" :src="item.img" width="20%" contain />
    </div>

    <div id="example">
    <carousel-3d :disable3d="true" :space="365" :clickable="false" :controls-visible="true">
        <slide v-for="(img, i) in subject1" :key="i">
        <span class="title">You know</span>
        <p>You know, being a test pilot isn't always the healthiest business in the world.</p>
        </slide>
    </carousel-3d>
    </div>

    <v-container>
        <div v-if="!$vuetify.breakpoint.mobile">
            <v-card  tile color="#C4C4C4" class="mt-5">
                <v-row align="center">
                    <v-col cols="1" align="center">
                        <h1>"</h1>
                    </v-col>
                    <v-col justify="center" cols="4">
                        <v-img src="\public\review\รูปภาพ1.png" />
                    </v-col>
                    <v-col justify="center" cols="6">
                        <strong><h2>แพลตฟอร์มทำให้นักเรียนตั้งใจเรียนขึ้น ได้มากเลยทีเดียว เพราะเด็กๆสนใจสื่อ ประเภทนี้มาก</h2></strong>
                        <br>
                        <p>คุณครู กฤตภัทร อรุณดี , ได้รับรางวัล OBEC AWARD 2019</p>
                    </v-col>
                </v-row>
            </v-card>
        </div>
        <div v-else>
            <v-card  tile color="#C4C4C4" class="mx-auto">
                <v-col align="center">
                    <v-row cols="1" align="center">
                        <h1>"</h1>
                        <v-img src="\public\review\รูปภาพ1.png" width="95%" />
                    </v-row>
                    <br>
                    <strong><h2>แพลตฟอร์มทำให้นักเรียนตั้งใจเรียนขึ้น ได้มากเลยทีเดียว เพราะเด็กๆสนใจสื่อ ประเภทนี้มาก</h2></strong>
                    <br>
                    <p>คุณครู กฤตภัทร อรุณดี , ได้รับรางวัล OBEC AWARD 2019</p>
                </v-col>
            </v-card>
        </div>
    </v-container>

    <v-container class="text-center">
        <h1> การเรียนรู้เกิดขึ้นได้ตลอดเวลา <br> SKOOLKIT จึงเหมาะกับทุกคน</h1>
    </v-container>

    <v-container>
        <v-row v-if="!$vuetify.breakpoint.mobile">
            <v-col cols="4" justify="center" class="text-center">
                <v-img src="\public\icon\undraw_Detailed_analysis_re_tk6j.png" />
                <strong><p>ผู้อำนวยการโรงเรียน<br>และฝ่ายบริหารต่างๆ</p></strong>
                <br>
                <p>ยกระดับสถานศึกษาของท่านด้วยแพลตฟอร์มที่ตอบโจทย์ นโยบายการศึกษาประจำปี 2564 ( 5 จาก 12 นโยบาย )ได้แก่ ข้อ 1, 2, 3, 10 และ 12</p>
            </v-col>
            <v-col cols="4" justify="center" class="text-center">
                <v-img src="\public\icon\undraw_teacher_35j2.png" />
                <strong><p>คุณครูประจำรายวิชา หรือคุณครูประจำชั้น</p></strong>
                <br>
                <p> คุณครูสามารถจัดการเรียนการสอนแบบ Active Learning ช่วยส่งเสริมการจัดการเรียนการสอนอย่างมีประสิทธิภาพมากยิ่งขึ้นและยังติดตามผลการเรียนของนักเรียนรายบุคคลได้แบบ 100 % </p>
            </v-col>
            <v-col cols="4" justify="center" class="text-center">
                <v-img src="\public\icon\undraw_true_friends_c94g.png" />
                <strong><p>นักเรียน</p></strong>
                <br>
                <p>นักเรียนได้ฝึกทักษะแห่งศตวรรษที่ 21 เริ่มต้นจากการมีส่วนร่วมในการเรียนรู้สนุกสนานจากกิจกรรมในห้องเรียนและยังทราบจุดแข็ง จุดอ่อนของตนเองซึ่งส่งผลต่อการพัฒนาการเรียนรู้ของตนเอง</p>
            </v-col>
        </v-row>
        <v-row v-else>
            <v-col justify="center" class="text-center">
                <v-img src="\public\icon\undraw_Detailed_analysis_re_tk6j.png" />
                <strong><p>ผู้อำนวยการโรงเรียน<br>และฝ่ายบริหารต่างๆ</p></strong>
                <br>
                <p>ยกระดับสถานศึกษาของท่านด้วยแพลตฟอร์มที่ตอบโจทย์ นโยบายการศึกษาประจำปี 2564 ( 5 จาก 12 นโยบาย )ได้แก่ ข้อ 1, 2, 3, 10 และ 12</p>
            </v-col>
            <v-col justify="center" class="text-center">
                <v-img src="\public\icon\undraw_teacher_35j2.png" />
                <strong><p>คุณครูประจำรายวิชา หรือคุณครูประจำชั้น</p></strong>
                <br>
                <p> คุณครูสามารถจัดการเรียนการสอนแบบ Active Learning ช่วยส่งเสริมการจัดการเรียนการสอนอย่างมีประสิทธิภาพมากยิ่งขึ้นและยังติดตามผลการเรียนของนักเรียนรายบุคคลได้แบบ 100 % </p>
            </v-col>
            <v-col justify="center" class="text-center">
                <v-img src="\public\icon\undraw_true_friends_c94g.png" />
                <strong><p>นักเรียน</p></strong>
                <br>
                <p>นักเรียนได้ฝึกทักษะแห่งศตวรรษที่ 21 เริ่มต้นจากการมีส่วนร่วมในการเรียนรู้สนุกสนานจากกิจกรรมในห้องเรียนและยังทราบจุดแข็ง จุดอ่อนของตนเองซึ่งส่งผลต่อการพัฒนาการเรียนรู้ของตนเอง</p>
            </v-col>
        </v-row>
    </v-container>

    <v-container>
        <div v-if="!$vuetify.breakpoint.mobile">
            <v-card  tile color="#C4C4C4" class="mt-1">
                <v-row align="center">
                    <v-col cols="1" align="center">
                        <h1>"</h1>
                    </v-col>
                    <v-col justify="center" cols="4">
                        <v-img src="\public\review\รูปภาพ2.png" />
                    </v-col>
                    <v-col justify="center" cols="6">
                        <strong><h2>บางทีเราก็ลืมนึกถึงจิตใจเด็กๆ เพราะเรามุ่งแต่จะสอนให้จบ จนมองข้ามหัวใจของเด็กไป</h2></strong>
                        <br>
                        <p>ว่าที่ ร.ต.หญิง คุณครู อธิชญาณ์ ไข่สังข์ ปานะโปย หัวหน้าช่วงชั้นที่ 1 </p>
                    </v-col>
                </v-row>
            </v-card>
        </div>
        <div v-else>
                <v-card  tile color="#C4C4C4" class="mx-auto">
                <v-col align="center">
                    <v-row cols="1" align="center">
                        <h1>"</h1>
                        <v-img src="\public\review\รูปภาพ2.png" width="95%" />
                    </v-row>
                        <br>
                        <strong><h2>บางทีเราก็ลืมนึกถึงจิตใจเด็กๆ เพราะเรามุ่งแต่จะสอนให้จบ จนมองข้ามหัวใจของเด็กไป</h2></strong>
                        <br>
                        <p>ว่าที่ ร.ต.หญิง คุณครู อธิชญาณ์ ไข่สังข์ ปานะโปย หัวหน้าช่วงชั้นที่ 1 </p>
                </v-col>
            </v-card>
        </div>
    </v-container>

    <v-container class="text-center">
        <h1>ยกระดับโรงเรียนของคุณ <br> ให้พร้อมสำหรับศตวรรษที่ 21 ตั้งเเต่วันนี้ ก่อนจะสายเกินไป...</h1>
    </v-container>

    <v-container>
        <div align="center">
            <v-btn color="#DB2C27" class="rounded-lg" large dark>ทดลองใช้งานฟรี</v-btn>
        </div>
    </v-container>

    <v-footer color="black" class="white--text" v-if="!$vuetify.breakpoint.mobile">
        <v-container>
            <v-row>
                <v-col cols="4">
                    <v-col>
                        <p>คุณสมบัติ</p>
                    </v-col>
                    <v-col>
                        <p>บทความ</p>
                    </v-col>
                    <v-col>
                        <p>ทดลองการใช้งาน</p>
                    </v-col>
                </v-col>
                <v-col cols="4">
                    <v-col>
                        <strong><p>ติดต่อเรา</p></strong>
                    </v-col>
                    <v-col>
                        <p>SKOOLKIT</p>
                    </v-col>
                    <v-col>
                        <p>Contact@skoolkit.to</p>
                    </v-col>
                    <v-col>
                        <p>063-2329154</p>
                        <p>092-9529726</p>
                    </v-col>
                </v-col>
                <v-col cols="4">
                    <strong><p>เกี่ยวกับเรา</p></strong>
                    <img src="/public/BWlogocut.png" alt="" width=70%>
                    <p>บริษัท เดอะแฟลชโซลูชั่น จำกัด สำนักงานเลขที่ 401/62 หมู่ 3 ตำบลคูคต อำเภอลำลูกกา จังหวัดปทุมธานี รหัสไปรณีย์ 12130</p>
                </v-col>
            </v-row>
        </v-container>
        <v-container class="text-center">
                <h6>Copyright ©2021 SKOOLKIT All Right Reserved</h6>
        </v-container>
    </v-footer>
    <v-footer v-else color="black" class="white--text">
            <v-col>
                <v-col>
                    <p>คุณสมบัติ</p>
                </v-col>
                <v-col>
                    <p>บทความ</p>
                </v-col>
                <v-col>
                    <p>ทดลองการใช้งาน</p>
                </v-col>
            </v-col>
            <v-col>
                <v-col>
                    <strong><p>ติดต่อเรา</p></strong>
                </v-col>
                <v-col>
                    <p>SKOOLKIT</p>
                </v-col>
                <v-col>
                    <p>Contact@skoolkit.to</p>
                </v-col>
                <v-col>
                    <p>063-2329154</p>
                    <p>092-9529726</p>
                </v-col>
            </v-col>
            <v-col>
                <strong><p>เกี่ยวกับเรา</p></strong>
                <img src="/public/BWlogocut.png" alt="" width=70%>
                <p>บริษัท เดอะแฟลชโซลูชั่น จำกัด สำนักงานเลขที่ 401/62 หมู่ 3 ตำบลคูคต อำเภอลำลูกกา จังหวัดปทุมธานี รหัสไปรณีย์ 12130</p>
            </v-col>
            <v-container>
                <h6>Copyright ©2021 SKOOLKIT All Right Reserved</h6>
            </v-container>
    </v-footer>
</div>
</template>

<script>
export default {
    data() {
        return{
            tabs:[
                { tab:"คุณสมบัติ" },
                { tab:"บทความ" },  
                { tab:"ทดลองการใช้งาน" }
            ],
            pic:[
                { img:"/public/other/depa.png" },
                { img:"/public/other/DES.png" },
                { img:"/public/other/kris.png" },
                { img:"/public/other/SYSI.png" },
                { img:"/public/other/sss.png" },
                { img:"/public/other/StartupTH.png" },
                { img:"/public/other/STeP.png" }
            ],
            icon:[
                { 
                    img:"/public/icon/Group 2774.png",
                    text:"เช็คชื่อ"
                },
                { 
                    img:"/public/icon/Group 2775.png",
                    text:"สุ่ม" 
                },
                { 
                    img:"/public/icon/Group 2776.png",
                    text:"แบ่งกลุ่ม"
                },
                { 
                    img:"/public/icon/Group 2778.png",
                    text:"โหวต" 
                },
                { 
                    img:"/public/icon/Group 2798.png",
                    text:"ฟีดแบค" 
                },
                { 
                    img:"/public/icon/Group 2777.png",
                    text:"ควิซเกม"
                },
                { 
                    img:"/public/icon/Group 2779.png",
                    text:"รายงาน" 
                }
            ],
            subject1:[
                { img:"/public/subject/5.png" },
                { img:"/public/subject/6.png" },
                { img:"/public/subject/7.png" },
                { img:"/public/subject/8.png" },
                { img:"/public/subject/9.png" },
                { img:"/public/subject/10.png" },
                { img:"/public/subject/11.png" }
            ],
            subject2:[
                { img:"/public/subject/12.png" },
                { img:"/public/subject/13.png" },
                { img:"/public/subject/14.png" },
                { img:"/public/subject/15.png" },
                { img:"/public/subject/16.png" }
            ]
        }
    },
    components: {
        'carousel-3d': window['carousel-3d'].Carousel3d,
        'slide': window['carousel-3d'].Slide
    }
}
</script>

<style scoped>
.top{
    width: 100%;
    text-align: center;
    margin: 0px;
}
.tabs p{
    color: white;
}
.tabs:hover p{
    cursor: pointer;
    color: #DB2C27;
}
.video{
    position: absolute;
}
</style>