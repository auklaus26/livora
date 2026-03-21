<script setup lang="ts">
import { siteEmail, siteLocation, sitePhone } from '~/composables/useSiteContent'

useHead({
  title: 'Feedback, Complaints and Suggestions | Livora Care'
})
</script>

<template>
  <div>
    <PageHero
      badge="Feedback & Complaints"
      title="Your voice matters to us"
      subtitle="Livora Care welcomes feedback, suggestions, compliments, concerns and complaints. All feedback is handled respectfully and confidentially."
    />

    <section class="section">
      <div class="shell split-grid top-align">
        <div class="content-card">
          <h2>Contact information</h2>
          <p>If you prefer to speak with someone directly, you can contact us:</p>
          <p>{{ sitePhone }}</p>
          <p>{{ siteEmail }}</p>
          <p>{{ siteLocation }}</p>
          <p>You may also choose to submit feedback anonymously using the form.</p>
        </div>

        <form class="form-card">
          <h2>Tell us about your experience</h2>
          <div class="form-grid">
            <label>
              <span>Type of Feedback *</span>
              <select>
                <option>Compliment</option>
                <option>General Feedback</option>
                <option>Suggestion</option>
                <option>Concern</option>
                <option>Complaint</option>
              </select>
            </label>
            <label class="full-span">
              <span>Please describe your feedback or concern *</span>
              <textarea rows="6" placeholder="Tell us what happened, when it happened and how it affected you."></textarea>
            </label>
            <label class="full-span">
              <span>What outcome would you like? (optional)</span>
              <textarea rows="4" placeholder="Explanation, apology, service improvement or follow-up discussion"></textarea>
            </label>
            <label>
              <span>Name</span>
              <input type="text" />
            </label>
            <label>
              <span>Phone Number</span>
              <input type="tel" />
            </label>
            <label class="full-span">
              <span>Email Address</span>
              <input type="email" />
            </label>
            <label>
              <span>Relationship to Livora Care *</span>
              <select>
                <option>Participant</option>
                <option>Family Member / Carer</option>
                <option>Support Coordinator</option>
                <option>Allied Health Professional</option>
                <option>Community Member</option>
                <option>Staff Member</option>
                <option>Other</option>
              </select>
            </label>
            <label>
              <span>Preferred Contact Method</span>
              <select>
                <option>Phone</option>
                <option>Email</option>
                <option>No contact required</option>
              </select>
            </label>
            <fieldset class="full-span checkbox-group">
              <legend>Privacy and Consent</legend>
              <label>
                <input type="checkbox" />
                <span>I consent to Livora Care contacting me regarding this feedback or complaint.</span>
              </label>
              <label>
                <input type="checkbox" />
                <span>I prefer this feedback to remain anonymous.</span>
              </label>
            </fieldset>
            <label class="full-span">
              <span>Upload supporting documents (optional)</span>
              <input type="file" />
            </label>
          </div>
          <button type="button" class="button button-primary">Submit Feedback</button>
          <p class="fine-print">
            Thank you for sharing your feedback. A member of the Livora Care team will review your submission and
            respond if contact details have been provided.
          </p>
        </form>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>If you are not satisfied with our response</h2>
          <p>
            If you are not comfortable raising your concern with Livora Care, or if you are not satisfied with our
            response, you may contact the NDIS Quality and Safeguards Commission.
          </p>
          <p><strong>Phone:</strong> 1800 035 544</p>
          <p>
            <strong>Website:</strong>
            <a href="https://www.ndiscommission.gov.au" target="_blank" rel="noreferrer">www.ndiscommission.gov.au</a>
          </p>
        </div>
        <div class="consult-card">
          <h3>Speak-up culture</h3>
          <p>
            Livora Care promotes a speak-up culture where participants feel safe to raise concerns without fear of
            retaliation.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>
