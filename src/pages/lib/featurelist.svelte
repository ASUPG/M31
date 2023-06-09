<script>
  import Feature from "./feature.svelte";
  export let name;
  let embeddabledesc = `We are trying to make the ${name} as small as possible so you can embedd it into your own application` 
</script>

<div class="flist">
  <h2>We Have these Features to offer you:</h2>
  <Feature
    name="Plugins"
    description="We offer you a Plugin system so you can store whatever you want with our database"
  />
  <Feature
    name="Read Mode and Write mode"
    description="Becuase of our Database's flexibility you can use our database like a document database which we call Read Mode or store every data in a single file which we call Write Mode"
  />
  <Feature
    name="Scalablity"
    description="Our database is designed to be fully scalable and flexible so you can make your application as big as possible"
  />
  <Feature
    name="Ease Of Use"
    description="We Provide SDKS for many diffrent languages so you can easily write your applications + We are also working on an Query Language Parser to overcome issues that you encounter with programming languages without an SDK"
  />
  <Feature
    name="Embeddable"
    description={embeddabledesc}
  />
  <Feature 
    name="Pre-Built Caching"
    description = "We Provide Pre-Built Cahcing in our Database so you don't have to worry about speed"
  />
  <Feature 
    name="Swap Queries"
    description = "If you had used Relational Databases if have heard about Transactions this is what this feature is you can swap two values together without writing bolierplate code"
   />
  <!-- <Feature
    name="Optitonal Schema"
    description="We Provide a System where you can define your schema to make your app predictable"
  /> -->
</div>

<style lang="scss">
  .flist {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 606px;
    margin-top: 50px;
    font-size: 21px;
    gap: 30px;
    height: auto;
  }
  // Responsivness
  @media only screen and (max-width: 757px) {
    .flist {
      width: 80vw;
      h2 {
        font-size: 4.2vw;
      }
    }
  }
</style>
