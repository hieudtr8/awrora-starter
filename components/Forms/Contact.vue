<template>
  <div class="page-wrap">
    <div class="cloud-deco">
      <div class="left-deco">
        <svg width="508px" height="222px" viewBox="0 0 508 222" class="cloud big">
          <g id="main" transform="translate(-504.000000, -461.000000)">
            <path id="Fill-1" d="M566.149658,683 C531.873114,683 504,655.129823 504,620.871939 C504,586.657508 531.873114,558.787331 566.149658,558.787331 C585.028642,558.787331 602.674735,567.260821 614.536559,582.056837 L628.266729,599.248244 L630.319737,577.363828 C636.47333,510.99359 691.394011,461 758.046166,461 C809.632066,461 856.025702,491.656651 876.202752,539.15708 L880.547743,549.363289 L889.563598,542.828925 C902.810388,533.317976 918.414335,528.282768 934.626581,528.282768 C977.299819,528.282768 1012,562.958895 1012,605.657679 C1012,648.318441 977.299819,683 934.626581,683 L566.149658,683 Z" />
          </g>
        </svg>
        <svg width="508px" height="222px" viewBox="0 0 508 222" class="cloud small">
          <g id="main" transform="translate(-504.000000, -461.000000)">
            <path id="Fill-1" d="M566.149658,683 C531.873114,683 504,655.129823 504,620.871939 C504,586.657508 531.873114,558.787331 566.149658,558.787331 C585.028642,558.787331 602.674735,567.260821 614.536559,582.056837 L628.266729,599.248244 L630.319737,577.363828 C636.47333,510.99359 691.394011,461 758.046166,461 C809.632066,461 856.025702,491.656651 876.202752,539.15708 L880.547743,549.363289 L889.563598,542.828925 C902.810388,533.317976 918.414335,528.282768 934.626581,528.282768 C977.299819,528.282768 1012,562.958895 1012,605.657679 C1012,648.318441 977.299819,683 934.626581,683 L566.149658,683 Z" />
          </g>
        </svg>
      </div>
      <div class="right-deco">
        <svg width="508px" height="222px" viewBox="0 0 508 222" class="cloud big">
          <g id="main" transform="translate(-504.000000, -461.000000)">
            <path id="Fill-1" d="M566.149658,683 C531.873114,683 504,655.129823 504,620.871939 C504,586.657508 531.873114,558.787331 566.149658,558.787331 C585.028642,558.787331 602.674735,567.260821 614.536559,582.056837 L628.266729,599.248244 L630.319737,577.363828 C636.47333,510.99359 691.394011,461 758.046166,461 C809.632066,461 856.025702,491.656651 876.202752,539.15708 L880.547743,549.363289 L889.563598,542.828925 C902.810388,533.317976 918.414335,528.282768 934.626581,528.282768 C977.299819,528.282768 1012,562.958895 1012,605.657679 C1012,648.318441 977.299819,683 934.626581,683 L566.149658,683 Z" />
          </g>
        </svg>
        <svg width="508px" height="222px" viewBox="0 0 508 222" class="cloud small">
          <g id="main" transform="translate(-504.000000, -461.000000)">
            <path id="Fill-1" d="M566.149658,683 C531.873114,683 504,655.129823 504,620.871939 C504,586.657508 531.873114,558.787331 566.149658,558.787331 C585.028642,558.787331 602.674735,567.260821 614.536559,582.056837 L628.266729,599.248244 L630.319737,577.363828 C636.47333,510.99359 691.394011,461 758.046166,461 C809.632066,461 856.025702,491.656651 876.202752,539.15708 L880.547743,549.363289 L889.563598,542.828925 C902.810388,533.317976 918.414335,528.282768 934.626581,528.282768 C977.299819,528.282768 1012,562.958895 1012,605.657679 C1012,648.318441 977.299819,683 934.626581,683 L566.149658,683 Z" />
          </g>
        </svg>
      </div>
    </div>
    <v-snackbar v-model="snackbar" location="top right" :timeout="1000000">
      <div class="notification">
        <div class="action">
          Message Sent
        </div>
        <v-btn text icon @click="snackbar = false">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </div>
    </v-snackbar>
    <v-container class="inner-wrap max-md">
      <div class="full-form-wrap">
        <div class="text-center">
          <h3 class="use-text-title title-contact pb-3 text-center use-text-primary">
            {{ $t('common.contact_title2') }}
          </h3>
          <p class="desc use-text-subtitle2 text-center">
            {{ $t('common.contact_subtitle') }}
          </p>
        </div>
        <div class="form">
          <v-form ref="form" v-model="valid">
            <v-row class="spacing6">
              <v-col cols="12" sm="6" class="px-6">
                <v-text-field v-model="name" :rules="nameRules" :label="$t('common.form_name')" color="white" required />
              </v-col>
              <v-col cols="12" sm="6" class="px-6">
                <v-text-field
                  v-model="email" :rules="emailRules" :label="$t('common.form_email')" color="white"
                  required
                />
              </v-col>
              <v-col cols="12" sm="6" class="px-6">
                <v-text-field v-model="phone" :label="$t('common.form_phone')" color="white" />
              </v-col>
              <v-col cols="12" sm="6" class="px-6">
                <v-text-field v-model="company" :label="$t('common.form_company')" color="white" />
              </v-col>
              <v-col cols="12" class="px-6">
                <v-textarea v-model="message" rows="6" color="white" :label="$t('common.form_message')" />
              </v-col>
            </v-row>
            <div class="btn-area flex">
              <div class="form-control-label">
                <v-checkbox
                  v-model="checkbox" color="secondary" :rules="[v => !!v || 'You must agree to continue!']" required
                >
                  <template #label>
                    <div>
                      {{ $t('common.form_terms') }}
                      <a href="#" class="link">
                        {{ $t('common.form_privacy') }}
                      </a>
                    </div>
                  </template>
                </v-checkbox>
              </div>
              <v-btn :block="isMobile" color="secondary" size="large" @click="validate">
                {{ $t('common.form_send') }}
              </v-btn>
            </div>
          </v-form>
        </div>
      </div>
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
@import './form-style.scss';
</style>

<script>
import logo from '@/assets/images/starter-logo.svg';
import brand from '@/assets/text/brand';
import link from '@/assets/text/link';

export default {
  data() {
    return {
      valid: true,
      snackbar: false,
      name: '',
      nameRules: [v => !!v || 'Name is required'],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      phone: '',
      company: '',
      message: '',
      checkbox: false,
      logo,
      brand,
      routeLink: link,
    };
  },
  computed: {
    isMobile() {
      const smDown = this.$vuetify.display.smAndDown;
      return smDown;
    },
  },
  methods: {
    validate() {
      if (this.$refs.form.validate()) {
        this.snackbar = true;
      }
    },
  },
};
</script>
