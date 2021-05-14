<template>
  <div class="body-bg">
        <div class="container">

        <div class="row">
            <div class="col-sm-s9 col-md-7 col-lg-5 mx-auto">
                <div class="card card-signin my-5 ">
                    <div class="card-body "> 
                        <div class="card bg-primary text-white text-center">
                                            <div class="card-body">Acheteur</div>
                                        </div>
                                        <hr class="my-2" />
                <b-form @submit="onSubmit" @reset="onReset" v-if="show">
                <b-form-group
                    id="input-group-1"
                    label-for="input-1">
                    <b-form-input
                    id="input-1"
                    v-model="nomAcheteur"
                    placeholder="Nom"
                    required
                    ></b-form-input>
                </b-form-group>

                <b-form-group 
                id="input-group-2">
                    <b-form-input
                    id="input-2"
                    v-model="prenomAcheteur"
                    placeholder="Prénom"
                    required
                    ></b-form-input>
                </b-form-group>
                </b-form>
            </div>
            </div>
            </div> 
       </div> 

       <div class="row">
            <div class="col-sm-s9 col-md-7 col-lg-5 mx-auto">
                <div class="card card-signin my-5 ">
                    <div class="card-body "> 
                        <div class="card bg-primary text-white text-center">
                                            <div class="card-body">Vendeur</div>
                                        </div>
                                        <hr class="my-2" />
                <b-form @submit="onSubmit" @reset="onReset" v-if="show">
                <b-form-group
                    id="input-group-1"
                    label-for="input-1">
                    <b-form-input
                    id="input-1"
                    v-model="nomVendeur"
                    placeholder="Nom"
                    required
                    ></b-form-input>
                </b-form-group>

                <b-form-group 
                id="input-group-2">
                    <b-form-input
                    id="input-2"
                    v-model="prenomVendeur"
                    placeholder="Prénom"
                    required
                    ></b-form-input>
                </b-form-group>
                </b-form>

            </div>
            </div>
            </div> 
       </div> 
                <b-button type="reset" variant="danger">Reset</b-button>
    <b-card class="mt-3">
      <pre class="m-0">Monsieur {{ prenomAcheteur }} {{nomAcheteur}}
          désire cèder à monsieur {{ prenomVendeur }} {{nomVendeur}}
          tout ou une partie de ces biens.
      </pre>
    </b-card>
    <br>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
          nomAcheteur: '',
          prenomAcheteur: '',
          nomVendeur: '',
          prenomVendeur: '',
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.prenomAcheteur = ''
        this.nomAcheteur = ''
        this.prenomVendeur = ''
        this.nomVendeur = ''
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>