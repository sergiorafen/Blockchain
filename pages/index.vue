<template>

  <div class="container">
    <div class="container-fluid">
  <div class="row">
    <div class="col-sm-3 col-md-6 col-lg-6 text-justify" >
    <h3 class="text-center">Résumé</h3>
    <br><br>
      <p>Une blockchain est une technologie de stockage et de transmission d'informations sans organe de contrôle.</p>
    </div>
    <div class="col-sm-9 col-md-6 col-lg-6 text-justify">
      <h3 class="text-center">Abstract</h3>
      <br><br>
      <p >A blockchain is a growing list of records, called blocks, that are 
        linked together using cryptography.Each block contains a cryptographic 
        hash of the previous block, a timestamp, and transaction data (generally represented as a Merkle tree).</p>
    </div>
  </div>
</div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
