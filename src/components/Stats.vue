<template>
  <section>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <p class="title mb-2">Creative Leader<span>.</span></p>
                <div class="line mb-3"></div>
                <p class="info mb-3">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ullam eum illum accusamus distinctio praesentium, fuga tempora eos repellendus quo pariatur natus veniam at dolorem eveniet reprehenderit nemo ad qui quisquam.</p>
                <p class="more">Read More</p>
            </div>

            <div class="col-6">
                <div class="argument">
                    <p class="d-flex justify-content-between mb-2">Mentorship <span>78%</span></p>
                    <div class="d-flex align-items-end">
                        <div class="full-bar-mentorship"></div>
                        <div class="empty-bar-mentorship"></div>
                    </div>
                </div>
                <div class="argument">
                    <p class="d-flex justify-content-between mb-2">Education <span>95%</span></p>
                    <div class="d-flex align-items-end">
                        <div class="full-bar-education"></div>
                        <div class="empty-bar-education"></div>
                    </div>
                </div>
                <div class="argument">
                    <p class="d-flex justify-content-between mb-2">Learning <span>65%</span></p>
                    <div class="d-flex align-items-end">
                        <div class="full-bar-learning"></div>
                        <div class="empty-bar-learning"></div>
                    </div>
                </div>
                <div class="argument">
                    <p class="d-flex justify-content-between mb-2">Motivation <span>83%</span></p>
                    <div class="d-flex align-items-end">
                        <div class="full-bar-motivation"></div>
                        <div class="empty-bar-motivation"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

    section > div{
        width: 70%;
        margin: 0 auto;
        padding: 80px 0;
    }
    .title{
        font-size: 35px;
        font-weight: bold;
        span{
            color: $textColorHover;
        }
    }
    .line{
        border: 1px solid $textColorHover;
        width: 10%;
    }
    .info{
        font-size: 14px;
        color: $textInfoColor;
    }
    .more{
        text-transform: uppercase;
        font-weight: bold;
        font-size: 12px;
    }
    .argument{
        margin-bottom: 15px;
        p{
            font-size: 20px;
            font-weight: bold;
        }
    }
    .full-bar-mentorship{
        border: 2px solid $textColorHover;
        width: 78%;
    }
    .empty-bar-mentorship{
        border: 1px solid $eventsMainTextColor;
        width: calc(100% - 78%);
    }
    .full-bar-education{
        border: 2px solid $textColorHover;
        width: 95%;
    }
    .empty-bar-education{
        border: 1px solid $eventsMainTextColor;
        width: calc(100% - 95%);
    }
    .full-bar-learning{
        border: 2px solid $textColorHover;
        width: 65%;
    }
    .empty-bar-learning{
        border: 1px solid $eventsMainTextColor;
        width: calc(100% - 65%);
    }
    .full-bar-motivation{
        border: 2px solid $textColorHover;
        width: 83%;
    }
    .empty-bar-motivation{
        border: 1px solid $eventsMainTextColor;
        width: calc(100% - 83%);
    }
</style>