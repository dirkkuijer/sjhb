<template>
  <div>
    <div class="footer">
      <p class="column first">
        KVK.nr: 67837484 <br>
        rek.nr: NL21 INGB 0651 7369 19
      </p>
      <p class="column">
        Meeuwenlaan 24 <br>
        3645 GH Vinkeveen
      </p>
      <p class="column">
        <a href="tel:+316334368550">06 3343 6850</a><br>
        <a href="mailto:info@sjhomebakery.nl" alt="Mail ons altijd als je vragen hebt">info@sjhomebakery.nl</a>
      </p>
    </div>
    <div class="copyright">
      <a :href="link" class="dirkFull" alt="Voor suggesties of vragen bereikbaar">&copy; Dirk Kuijer</a>
      <a :href="link" class="dirkshort" alt="Voor suggesties of vragen bereikbaar">&copy; DK</a>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      link: 'mailto:dirkkuijer@hotmail.com'
    }
  }
}
</script>

<style>

.footer {
    position: fixed;
    display: table;
    table-layout: fixed;
    bottom: 0px;
    background-color: #f2e4fe;;
    width: 100%;
    height: 75px;
    box-shadow: 3px 3px 15px black;
    z-index: 5;
}

.column {
    float: center;
    text-align: center;
    width: 33,33%;
    display: table-cell;
    padding: 3px 3px;
}

p {
    text-align: left;
    padding-left: 15px;
    padding-top: 15px;
    margin-top: 5px;
}

    a {
    text-decoration: underline;
    color: black;
    }

    a:active {
        font-weight: bold;
    }
.copyright, .dirk {
    position: fixed;
    right: 3px;
    bottom: 0px;
    color: black;
    font-size: small;
    z-index: 5;
}

  .dirkFull {
      display: none;
  }
 @media screen and (max-width: 490px) {
     .footer {
         table-layout: auto;
         height: 75px;
         display: table-caption;
     }
    .column {
        width: 100%;
        display: table-cell;
    }
    .first {
        display: none;
    }
    .column {
        width: 50%;
        padding: 15px 3px;
    }
    .dirkFull {
        display: none;
    }
    .dirkShort {
        display: inline-block;
        padding: 5px 5px;
        margin: 5px 5px;
    }
 }
 @media screen and (max-width: 840px) {
     .dirkShort, .column {
         display: none;
     }
     .footer {
         height: 25px;
     }
 }
</style>
