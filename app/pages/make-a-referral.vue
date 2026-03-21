<script setup lang="ts">
import { siteEmail, siteLocation, sitePhone } from '~/composables/useSiteContent'

useHead({
  title: 'Make a Referral | Livora Care'
})

const referrerRoles = [
  'Support Coordinator',
  'Local Area Coordinator',
  'Occupational Therapist',
  'Behaviour Support Practitioner',
  'Social Worker',
  'Hospital / Health Service',
  'Family Member / Carer',
  'Other'
]

const servicesRequested = [
  'Supported Independent Living (SIL)',
  'Assistance with Daily Personal Activities',
  'Assistance with Daily Life Tasks in Shared Living',
  'Community Participation',
  'Development of Daily Living and Life Skills',
  'Household Tasks',
  'Transport Assistance',
  'Group or Centre-Based Activities',
  'Other'
]
</script>

<template>
  <div>
    <PageHero
      badge="Make a Referral"
      title="Make a referral for Livora Care services"
      subtitle="If you are a support coordinator, allied health professional, hospital discharge planner, community organisation or family member, you can refer a participant to Livora Care using the form below."
    />

    <section class="section">
      <div class="shell split-grid top-align">
        <div class="content-card">
          <h2>Contact details</h2>
          <p>{{ sitePhone }}</p>
          <p>{{ siteEmail }}</p>
          <p>{{ siteLocation }}</p>
          <p>
            Our team will review the referral and respond promptly to discuss service suitability and availability.
          </p>
        </div>

        <form class="form-card">
          <h2>Referral Form</h2>
          <div class="form-grid">
            <label>
              <span>Referrer First Name</span>
              <input type="text" />
            </label>
            <label>
              <span>Referrer Last Name</span>
              <input type="text" />
            </label>
            <label>
              <span>Organisation / Company</span>
              <input type="text" />
            </label>
            <label>
              <span>Role</span>
              <select>
                <option v-for="role in referrerRoles" :key="role">{{ role }}</option>
              </select>
            </label>
            <label>
              <span>Phone Number</span>
              <input type="tel" />
            </label>
            <label>
              <span>Email Address</span>
              <input type="email" />
            </label>
            <label>
              <span>Participant First Name</span>
              <input type="text" />
            </label>
            <label>
              <span>Participant Last Name</span>
              <input type="text" />
            </label>
            <label>
              <span>Date of Birth</span>
              <input type="date" />
            </label>
            <label>
              <span>Gender</span>
              <select>
                <option>Female</option>
                <option>Male</option>
                <option>Non-binary</option>
                <option>Prefer not to say</option>
                <option>Other</option>
              </select>
            </label>
            <label class="full-span">
              <span>Address / Suburb</span>
              <input type="text" />
            </label>
            <label>
              <span>Aboriginal or Torres Strait Islander</span>
              <select>
                <option>Yes</option>
                <option>No</option>
                <option>Prefer not to say</option>
              </select>
            </label>
            <label>
              <span>NDIS Number (optional)</span>
              <input type="text" />
            </label>
            <label>
              <span>NDIS Plan Start Date</span>
              <input type="date" />
            </label>
            <label>
              <span>NDIS Plan End Date</span>
              <input type="date" />
            </label>
            <label class="full-span">
              <span>Primary Disability / Diagnosis</span>
              <textarea rows="3"></textarea>
            </label>
            <label>
              <span>Funding Type</span>
              <select>
                <option>NDIS</option>
                <option>Private Funding</option>
                <option>Other</option>
              </select>
            </label>
            <label>
              <span>Plan Management</span>
              <select>
                <option>NDIA Managed</option>
                <option>Plan Managed</option>
                <option>Self Managed</option>
              </select>
            </label>
            <label class="full-span">
              <span>Plan Manager Name (if applicable)</span>
              <input type="text" />
            </label>
            <fieldset class="full-span checkbox-group">
              <legend>Services Requested</legend>
              <label v-for="service in servicesRequested" :key="service">
                <input type="checkbox" />
                <span>{{ service }}</span>
              </label>
            </fieldset>
            <label class="full-span">
              <span>Participant Support Needs</span>
              <textarea
                rows="4"
                placeholder="Support needs, daily routines, behavioural support, current supports, housing situation"
              ></textarea>
            </label>
            <label class="full-span">
              <span>Risk and Safety Considerations</span>
              <textarea
                rows="4"
                placeholder="Environmental risks, behavioural considerations and any other safety information"
              ></textarea>
            </label>
            <label class="full-span">
              <span>Participant Plan Documents</span>
              <input type="file" />
            </label>
            <label class="full-span">
              <span>Additional Information</span>
              <textarea rows="4"></textarea>
            </label>
            <label>
              <span>Name of Person Completing Referral</span>
              <input type="text" />
            </label>
            <label>
              <span>Role / Relationship to Participant</span>
              <select>
                <option>Support Coordinator</option>
                <option>Clinician</option>
                <option>Family member</option>
                <option>Other</option>
              </select>
            </label>
          </div>
          <button type="button" class="button button-primary">Submit Referral</button>
        </form>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>What happens next</h2>
          <ol class="ordered-list">
            <li>Our team reviews the information provided.</li>
            <li>We contact the referrer or participant to discuss suitability.</li>
            <li>We arrange a free initial consultation.</li>
            <li>If appropriate, we develop a service agreement and onboarding plan.</li>
          </ol>
        </div>
        <div class="consult-card">
          <h3>Prefer to discuss before referring?</h3>
          <p>If you would like to discuss a participant before submitting a referral, our team is happy to assist.</p>
          <NuxtLink to="/contact" class="button button-secondary">Book a Free Consultation</NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>
