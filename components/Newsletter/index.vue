<template>
   <div class="newsletter-wrapper">
      <div class="title" style="margin: 0">
         <strong>Newsletter</strong>
      </div>
      <div class="content">
         <p class="text">Nie przegap okazji, dołącz do naszego newslettera.</p>
         <form action="/" class="form subscribe">
            <div class="field newsletter">
               <div class="control">
                  <label for="newsletter">
                     <input
                        name="email"
                        type="email"
                        id="newsletter"
                        placeholder="Podaj swój adres Email"
                        required
                     />
                  </label>
               </div>
            </div>
            <div class="field agree">
               <div class="control">
                  <label>
                     <input
                        type="checkbox"
                        name="rodoNewsletter"
                        value="1"
                        required
                     />
                     <span> Zapoznałem/am się z polityką prywatności </span>
                  </label>
               </div>
            </div>
            <div class="actions">
               <button
                  class="action subscribe primary"
                  title="Zapisz się!"
                  type="submit"
                  aria-label="Subscribe"
               >
                  <span>Zapisz się!</span>
               </button>
            </div>
         </form>
      </div>
   </div>
</template>

<style scoped lang="scss">
.newsletter-wrapper {
   background-color: #f9f7f4;
   margin-left: auto;
   margin-right: auto;
   max-width: 1190px;
   padding-left: 40px;
   padding-right: 40px;
   position: relative;
   text-align: center;
   padding-bottom: 10px;
}

.title strong {
   font-size: 4.1rem;
   font-weight: 300;
   line-height: 1.2;
   margin-bottom: 16px;
   margin-top: 0;
   display: block;
   letter-spacing: -0.5px;
}
.newsletter .text {
   color: #676767;
   font-size: 14px;
   line-height: 1.6;
   font-weight: 400;
   letter-spacing: 0;
   margin-bottom: 25px;
}

.form.subscribe {
   width: 100%;
   display: flex;
   justify-content: center;
   flex-direction: column;
   margin: 0 auto;
   max-width: 560px;
   align-items: flex-start;
}

.field.newsletter {
   margin: 0;
   width: 100%;
}

.newsletter input {
   font-size: 14px;
   padding-left: 15px;
   color: #676767;
   min-height: 46px;
   width: 100%;
}

.field.agree {
   text-align: left;
}

.field.agree span {
   padding-bottom: 0;
}

.actions {
   width: auto;
   margin-top: 25px;
}

.actions .subscribe {
   display: flex;
   align-items: center;
   text-decoration: none;
   justify-content: space-between;
   color: #fff;
   background: #d9cfce;
   border: 1px solid;
   border-color: #d9cfce;
   text-transform: uppercase;
   font-weight: 700;
   border-radius: 0;
   width: auto;
   box-shadow: none;
   min-height: 46px;
   width: auto;
   min-width: 145px;
   letter-spacing: 2.1px;
   padding: 0 15px;
}

@media (min-width: 708px) {
   .newsletter-wrapper {
      padding-top: 80px;
      padding-bottom: 80px;
   }

   .title strong {
      font-size: 4.8rem;
      letter-spacing: 0;
      margin-bottom: 13px;
   }

   .newsletter .text {
      margin-bottom: 28px;
   }
   .form.subscribe {
      flex-direction: row;
      max-width: 550px;
      flex-wrap: wrap;
   }

   .field.newsletter {
      flex: 1 0 auto;
      width: auto;
   }

   .form.subscribe .field.agree {
      flex: 0 0 100%;
      max-width: 100%;
      order: 2;
      margin-top: 5px;
   }

   .actions {
      margin-top: 0;
   }

   .actions .subscribe {
      min-width: 190px;
      padding: 0 20px;
   }
}
</style>
