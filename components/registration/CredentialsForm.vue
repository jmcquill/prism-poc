
<script setup>

const props = defineProps({
  formId: {
    type: String,
    default: 'credentials-create'
  },
  showDescription: {
    type: Boolean,
    default: true
  },
  isOauth: {
    type: Boolean,
    default: false
  }
})

const submitAction = ref('Registration/createCredentials')

// const unwantedPhrases = `${UNWANTED_PASSPHRASES.join(', ')}`

</script>

<template>
  <div>
    <!-- <PdlFormBase
      :ref="formId"
      :form-id="formId"
      :fields="fields"
      :opco="opco"
      :submit-action="submitAction"
      @success="onSubmitSuccess"
      @error="onError"
    >
      <template
        #before
      >
        <p
          v-if="showDescription"
          class="text-center text--secondary-dark"
        >
          Create an account to clip coupons, earn rewards, and shop for pickup or delivery.
        </p>
      </template>
      <template
        #after
      >
        <div class="flex-auto">
          <RecaptchaBlock
            v-if="recaptchaAllowed"
            :id="formId"
            :ref="recaptchaBlockID"
            class="flex flex-row justify-center"
            @recaptcha-loaded="onRecaptchaLoaded"
            @recaptcha-verify-change="onRecaptchaChange"
          />
          <p class="text text-sm leader--double">
            By selecting Continue, you agree to the <a
              :href="termsLink"
              class="link link--inline"
              target="_blank"
              rel="noopener noreferrer"
            >Terms &amp; Conditions</a> and acknowledge the <a
              :href="privacyLink"
              class="link link--inline"
              target="_blank"
              rel="noopener noreferrer"
            >{{ privacyLinkText }}</a>.
          </p>
        </div>
      </template>
    </PdlFormBase> -->
    <p class="text text-sm text-center leader--double">
      Already have an account?
      <a
        href="#"
        aria-haspopup="dialog"
        class="link link--inline"
        @click.prevent="onLoginClick"
      >
        Sign In
      </a>
    </p>
  </div>
</template>

