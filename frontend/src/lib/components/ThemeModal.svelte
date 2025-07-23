<script lang="ts">
  export let visible = false

  export let onThemeModal
  import { m } from '$lib/i18n/messages'
  // import { externalLinkProps, sanitize } from '$lib/utils/commons'
</script>

<button class="hidden" data-fr-opened="false" aria-controls="fr-modal-theme"> Hidden </button>
<dialog
  aria-labelledby="fr-modal-title-modal-theme"
  id="fr-modal-theme"
  class="fr-modal"
  data-fr-concealing-backdrop="false"
>
  <div class="fr-container fr-container--fluid fr-container-md">
    <div class="fr-grid-row fr-grid-row--center">
      <div class="fr-col-12 fr-col-md-8 fr-col-lg-6">
        <div class="fr-modal__body">
          <div class="fr-modal__header">
            <button
              class="fr-btn--close fr-btn"
              title="Fermer la fenêtre modale"
              aria-controls="fr-modal-theme"
              id="fr-modal-theme-close"
              onclick={() => (visible = false)}
            >
              {m['words.close']()}
            </button>
          </div>
          <div class="fr-modal__content">
            <h1 id="fr-theme-modal-title" class="fr-modal__title">Paramètres d’affichage</h1>
            <div id="fr-display" class="fr-display">
              <fieldset class="fr-fieldset" id="display-fieldset">
                <legend
                  class="fr-fieldset__legend--regular fr-fieldset__legend"
                  id="display-fieldset-legend"
                >
                  Choisissez un thème pour personnaliser l’apparence du site.
                </legend>
                <div class="fr-fieldset__element">
                  <div class="fr-radio-group fr-radio-rich">
                    <input
                      value="light"
                      type="radio"
                      id="fr-radios-theme-light"
                      name="fr-radios-theme"
                    /> <label class="fr-label" for="fr-radios-theme-light"> Thème clair </label>
                    <div class="fr-radio-rich__pictogram">
                      <svg
                        aria-hidden="true"
                        class="fr-artwork"
                        viewBox="0 0 80 80"
                        width="80px"
                        height="80px"
                      >
                        <use
                          class="fr-artwork-decorative"
                          href="/dsfr/artwork/pictograms/environment/sun.svg#artwork-decorative"
                        ></use>
                        <use
                          class="fr-artwork-minor"
                          href="/dsfr/artwork/pictograms/environment/sun.svg#artwork-minor"
                        ></use>
                        <use
                          class="fr-artwork-major"
                          href="/dsfr/artwork/pictograms/environment/sun.svg#artwork-major"
                        ></use>
                      </svg>
                    </div>
                  </div>
                </div>
                <div class="fr-fieldset__element">
                  <div class="fr-radio-group fr-radio-rich">
                    <input
                      value="dark"
                      type="radio"
                      id="fr-radios-theme-dark"
                      name="fr-radios-theme"
                    /> <label class="fr-label" for="fr-radios-theme-dark"> Thème sombre </label>
                    <div class="fr-radio-rich__pictogram">
                      <svg
                        aria-hidden="true"
                        class="fr-artwork"
                        viewBox="0 0 80 80"
                        width="80px"
                        height="80px"
                      >
                        <use
                          class="fr-artwork-decorative"
                          href="/dsfr/artwork/pictograms/environment/moon.svg#artwork-decorative"
                        ></use>
                        <use
                          class="fr-artwork-minor"
                          href="/dsfr/artwork/pictograms/environment/moon.svg#artwork-minor"
                        ></use>
                        <use
                          class="fr-artwork-major"
                          href="/dsfr/artwork/pictograms/environment/moon.svg#artwork-major"
                        ></use>
                      </svg>
                    </div>
                  </div>
                </div>
                <div class="fr-fieldset__element">
                  <div class="fr-radio-group fr-radio-rich">
                    <input
                      value="system"
                      type="radio"
                      id="fr-radios-theme-system"
                      name="fr-radios-theme"
                    />
                    <label class="fr-label" for="fr-radios-theme-system">
                      Système <span class="fr-hint-text">Utilise les paramètres système</span>
                    </label>
                    <div class="fr-radio-rich__pictogram">
                      <svg
                        aria-hidden="true"
                        class="fr-artwork"
                        viewBox="0 0 80 80"
                        width="80px"
                        height="80px"
                      >
                        <use
                          class="fr-artwork-decorative"
                          href="/dsfr/artwork/pictograms/system/system.svg#artwork-decorative"
                        ></use>
                        <use
                          class="fr-artwork-minor"
                          href="/dsfr/artwork/pictograms/system/system.svg#artwork-minor"
                        ></use>
                        <use
                          class="fr-artwork-major"
                          href="/dsfr/artwork/pictograms/system/system.svg#artwork-major"
                        ></use>
                      </svg>
                    </div>
                  </div>
                </div>
              </fieldset>
            </div>
          </div>
        </div>
        <div class="fr-modal__footer">
          <div
            class="fr-btns-group fr-btns-group--right fr-btns-group--inline-reverse fr-btns-group--inline-lg fr-btns-group--icon-left"
          >
            <button
              class="fr-btn purple-btn"
              data-fr-opened="false"
              aria-controls="fr-modal-theme"
              onclick={onThemeModal}
            >
              {m['words.send']()}
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</dialog>
