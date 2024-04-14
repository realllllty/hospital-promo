<template>
    <div class="row row--15 service-wrapper">
        <div class="col-lg-4 col-md-6 col-sm-6 col-12"
             v-for="(service, index) in serviceList"
             :key=index>
            <div :class="`service ${serviceStyle} ${checkTextAlign}`"
                 data-aos="fade-up"
                 data-aos-delay="70">
                <div class="icon">
                    <Icon :name="service.icon" :class="`size-${iconSize}`"/>
                </div>
                <div class="content">
                    <h4 class="title w-600">
                        <router-link to="/service-details" v-html="service.title"/>
                    </h4>
                    <p class="description b1 color-gray mb--0" v-html="service.description"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Icon from '../../icon/Icon'

    export default {
        name: 'ServiceOne',
        components: {Icon},
        props: {
            serviceStyle: {
                type: String
            },
            iconSize: {
                type: String|Number,
                default: 62
            },
            textAlign: {
                type: String,
                default: 'left'
            }
        },
        data() {
            return {
                serviceList: [
                    {
                        icon: 'activity',
                        title: '健康数据难以管理',
                        description: '老人日常检测数据如何快速获取，如何实现健康管理'
                    },
                    {
                        icon: 'cast',
                        title: '服务质量监管不力',
                        description: '服务人员的工单质量如何保证，是否存在弄虚作假'
                    },
                    {
                        icon: 'map',
                        title: '老人活动参与度低',
                        description: '如何让老人积极参与各项活动及事务，同时让更多老人加入到社区养老中来'
                    },
                ]
            }
        },
        computed: {
            checkTextAlign() {
                if (this.textAlign === 'left') return 'text-start';
                else if (this.textAlign === 'center') return 'text-center';
                else if (this.textAlign === 'end') return 'text-end';
                else return '';
            }
        }
    }
</script>
