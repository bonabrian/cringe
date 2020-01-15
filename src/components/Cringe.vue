<template>
    <div class="container my-5 text-center justify-content-center">
        <div class="row">
            <div class="col-md-12">
                <h2>Cringe</h2>
                <h5>{{ description }}</h5>
                <h5 class="mb-5">by <a href="https://github.com/bonabrian" target="_blank">bonabrian</a></h5>
            </div>
        </div>
        <div class="row justify-content-center mb-4">
            <div class="col-md-6">
                <div class="form-group">
                    <textarea placeholder="wadaw" v-model="cringe" cols="30" rows="5" class="form-control" :class="$style.cringe"></textarea>
                </div>
            </div>
        </div>
        <div class="row justify-content-center">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header text-center">
                        <h3 class="card-title">Hasil</h3>
                        <button data-clipboard-target="#cringe" class="btn btn-outline-success btn-sm font-weight-bold">
                            Salin
                        </button>
                    </div>
                    <div class="card-body">
                        <div class="form-group">
                            <textarea placeholder="widiw" id="cringe" cols="30" rows="5" class="form-control" v-model="this.generated" :class="$style.cringe"></textarea>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style module scoped lang="scss">
  @import './Cringe.module';
</style>

<script>
export default {
    data() {
        return {
            description: 'Untuk para idiotique sejati :)',
            cringe: ''
        }
    },
    computed: {
        generated() {
            let res
            res = this.cringe.replace(/a|i|u|e|o/gi, 'i')

            return res
        }
    }
}
</script>