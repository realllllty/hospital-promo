<template>
    <Layout header-class="header-transparent" :show-newsletter="false" :show-cta="false">
        <!-- Start Slider Area -->
        <div class="slider-area slider-style-1 height-850 bg_image"
             data-black-overlay="7"
             :style="{'background-image': `url(${require(`@/assets/images/bg/bg-image-12.jpg`)})`}">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="inner pt--80 text-center">
                            <div>
                                <h3 class="rn-sub-badge" data-aos="fade-up" data-aos-delay="100">
                                    <span class="theme-gradient">智慧社区养老信息管理系统</span>
                                </h3>
                            </div>
                            <h1 class="title display-one" data-aos="fade-up" data-aos-delay="150">
                              社区养老解决方案 <br/>
                            </h1>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Slider Area -->

        <!-- Start Service Area -->
        <div class="service-area rn-section-gapTop">
            <div class="container">
                <div class="row">
                    <div class="col-lg-6">
                        <div class="content" data-aos="fade-up">
                            <h3 class="title">我们是致力于为老年人提供优质生活的社区服务机构。</h3>
                        </div>
                    </div>
                    <div class="col-lg-6">
                        <p class="mb--10" data-aos="fade-up">
                          从舒适的居住环境到全面的健康管理，我们全方位关注每一位长者的需求和幸福。在这里，每一天都是新的开始。我们相信，优质的养老服务不仅仅是提供一个居住的场所，更是一个充满爱、活力和尊重的社区。您的舒适和满意是我们不懈追求的目标。每一步成长，每一次微笑，我们都在其中。因为我们深知，服务的每一次卓越，都是对长者生活品质的真正提升。加入我们，让生活更美好，让关怀无处不在。
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Service Area -->

        <!-- Start Brand Area -->
<!--        <div class="rwt-brand-area pb&#45;&#45;60 pt&#45;&#45;30">-->
<!--            <div class="container">-->
<!--                <div class="row">-->
<!--                    <div class="col-lg-12 mt&#45;&#45;10">-->
<!--                        <Brand :brand-list="brandList" :brand-style="3"/>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </div>-->
        <!-- End Brand Area -->

        <Separator/>

        <!-- Start Service Area -->
        <div class="rn-service-area rn-section-gap">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <SectionTitle
                            text-align="center"
                            subtitle="我们可以为你做什么"
                            title="为您提供的服务"
                            description="社区养老管理为何这么难? 我们的解决方案如何帮助您解决这些问题?"
                            data-aos="fade-up"
                        />
                    </div>
                </div>
                <ServiceOne
                    service-style="service__style--1 bg-color-blackest radius mt--25"
                    icon-size="62"
                    text-align="center"
                />
            </div>
        </div>
        <!-- End Service Area -->

<!--        <div class="rwt-timeline-area rn-section-gapBottom">-->
<!--            <div class="container">-->
<!--                <div class="row">-->
<!--                    <div class="col-lg-12">-->
<!--                        <Timeline :timeline-data="timelineData" :timeline-style="3"/>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </div>-->

        <Separator/>

<!--        <AboutFour :image="require(`@/assets/images/about/contact-image.jpg`)"/>-->

        <!-- Start Elements Area -->
        <div class="rwt-counterup-area pb--100">
            <div class="container mt_dec--30">
                <Counter
                    :counter-style="5"
                    text-align="center"
                    :counter-data="counterData"
                    column="col-lg-3 col-md-6 col-sm-6 col-12"
                />
            </div>
        </div>
        <!-- End Elements Area -->

        <Separator/>

        <!-- Start Elements Area -->
        <div class="rwt-team-area rn-section-gap">
            <div class="container">
                <div class="row mb--20">
                    <div class="col-lg-12">
                        <SectionTitle
                            text-align="center"
                            subtitle="我们的杰作"
                            title="核心项目展示"
                            data-aos="fade-up"
                        />
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-6 col-xl-3 col-md-6 col-12 mt--30"
                         v-for="(teamMember, index) in teamData"
                         :key="index">
                        <Team :team-member="teamMember" :team-style="4"/>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Elements Area -->
    </Layout>
</template>

<script>
    import Layout from '../components/common/Layout'
    import Separator from '../components/elements/separator/Separator'
    import SectionTitle from '../components/elements/sectionTitle/SectionTitle'
    import AboutFour from '../components/elements/about/AboutFour'
    import ServiceOne from '../components/elements/service/ServiceOne'
    import Timeline from '../components/elements/timeline/Timeline'
    import Counter from '../components/elements/counterUp/Counter'
    import Brand from '../components/elements/brand/Brand'
    import Team from '../components/elements/team/Team'

    export default {
        name: 'About',
        components: {Team, Brand, Counter, Timeline, ServiceOne, AboutFour, SectionTitle, Separator, Layout},
        data() {
            return {
                brandList: [
                    {
                        image: require(`@/assets/images/brand/brand-01.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-02.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-03.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-04.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-05.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-06.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-07.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-08.png`)
                    },
                    {
                        image: require(`@/assets/images/brand/brand-01.png`)
                    },

                ],
                counterData: [
                    {
                        number: 199,
                        title: '合作客户',
                    },
                    {
                        number: 7,
                        title: '我们的员工',
                    },
                    {
                        number: 69,
                        title: '工程',
                    },
                    {
                        number: 500,
                        title: '核心项目',
                    }
                ],
                teamData: [
                    {
                        image: 'team-dark-01',
                        name: '北京',
                        designation: 'PK天街',
                        location: '朝阳区天生路2号',
                        description: 'Yes, I am a product designer. I have a passion for product design.'
                    },
                    {
                        image: 'team-dark-02',
                        name: '上海',
                        designation: 'SH天街',
                        location: '浦东新区天生路2号',
                        description: 'Yes, I am a product designer. I have a passion for product design.'
                    },
                    {
                        image: 'team-dark-03',
                        name: '广州',
                        designation: 'GZ天街',
                        location: '天河区天生路2号',
                        description: 'Yes, I am a product designer. I have a passion for product design.'
                    },
                    {
                        image: 'team-dark-04',
                        name: '深圳',
                        designation: 'SZ天街',
                        location: '南山区天生路2号',
                        description: 'Yes, I am a product designer. I have a passion for product design.'
                    },
                ]
            }
        }
    }
</script>
