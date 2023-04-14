<template>
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
        <div class="card">
            <div class="card-body">
                <div class="card-image">
                    <img :src="image" :alt="title" class="img-fluid">
                </div>
                <div class="card-title">
                    {{ title }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: ['image', 'title']
}
</script>

<style lang="scss" scoped></style>