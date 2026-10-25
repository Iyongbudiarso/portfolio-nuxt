<template>
  <div class="pt-32 pb-20 px-6 max-w-4xl mx-auto text-gray-300">
    <h1 class="text-4xl font-bold mb-8 text-white">Privacy Policy</h1>
    <p class="mb-4 italic">Last updated: October 25, 2026</p>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">1. Introduction</h2>
      <p class="mb-4">
        This policy covers the services and applications operated by Iyong Budiarso under iyongbudiarso.com
        ("we," "our," or "us"). Two kinds of applications are covered:
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li><strong>Personal automation tools</strong> — including <em>Money Lover Auto Capture</em>, a private tool that reads bank transaction notification emails from the owner's own mailbox and records those transactions in the owner's personal ledger (Money Lover).</li>
        <li><strong>Social media scheduling tools</strong> — used to publish content to TikTok through the official TikTok API.</li>
      </ul>
      <p class="mt-4">
        Both are single-user tools operated by their owner. They are not offered as a public service, and no account
        data from third parties is collected.
      </p>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">2. Google User Data (Gmail)</h2>
      <p class="mb-4">
        <em>Money Lover Auto Capture</em> accesses Gmail through the Google API using a single scope:
        <code class="text-emerald-400">https://www.googleapis.com/auth/gmail.readonly</code> (read-only — the
        application cannot send, modify, or delete email).
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li><strong>What is accessed:</strong> messages from the owner's own mailbox that match a narrow sender filter (bank and payment notification addresses such as Bank Mandiri/Livin' and BCA), including subject, date, and message body needed to read the transaction amount, merchant, and time.</li>
        <li><strong>Why:</strong> to extract the transaction details and record them in the owner's personal bookkeeping ledger. Nothing else is done with the messages.</li>
        <li><strong>What is stored:</strong> the extracted transaction fields (date, amount, merchant, category) and an OAuth refresh token. Email bodies are processed in memory and are not archived or copied to a database.</li>
        <li><strong>Where:</strong> on a private, self-hosted server controlled by the owner. The OAuth token is stored in a file readable only by the owner's operating-system user (mode 0600).</li>
        <li><strong>No AI processing:</strong> extraction is deterministic (pattern matching and HTTP calls). No message content is sent to any AI model or third-party processor.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">3. How We Use Information</h2>
      <p class="mb-4">Information is used solely to provide the function the owner requested:</p>
      <ul class="list-disc pl-6 space-y-2">
        <li>To record the owner's own financial transactions in the owner's own ledger.</li>
        <li>To schedule and publish videos to the owner's TikTok account as directed.</li>
        <li>To report processing results (for example, transactions recorded or items needing review) to the owner.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">4. Data Sharing and Retention</h2>
      <p class="mb-4">
        We do not sell, rent, trade, or otherwise transfer personal information to outside parties. There are no
        advertisers, analytics providers, or data brokers involved. Data leaves the server only to the service the
        owner is intentionally writing to (the Money Lover API for transactions, the TikTok API for publishing),
        or when the owner requests it.
      </p>
      <p>
        Transaction records are retained until the owner deletes them. OAuth tokens are retained until revoked.
        Revoking access or deleting the token file stops all further access immediately.
      </p>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">5. Google API Limited Use Disclosure</h2>
      <p class="mb-4">
        Money Lover Auto Capture's use and transfer to any other app of information received from Google APIs will
        adhere to the
        <a href="https://developers.google.com/terms/api-services-user-data-policy" class="text-emerald-400" rel="noopener" target="_blank">Google API Services User Data Policy</a>,
        including the Limited Use requirements.
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li>Google user data is used only to provide the user-facing feature described above.</li>
        <li>It is not transferred to third parties except as necessary to provide that feature, to comply with applicable law, or as part of a merger or acquisition.</li>
        <li>It is not used for advertising, and it is not used to train or improve machine learning models.</li>
        <li>No humans read the data, except where the owner themself reviews a transaction, with the owner's consent, for security purposes, or to comply with law.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">6. TikTok Data</h2>
      <p class="mb-4">
        When you use our TikTok integration (via Postiz), we access specific information from your TikTok account
        through the official TikTok API:
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li><strong>Profile Information:</strong> display name, avatar, and unique identifier, to help you identify which account you are managing.</li>
        <li><strong>Access Tokens:</strong> tokens provided by TikTok to perform actions on your behalf (such as uploading videos). We do NOT store your TikTok password.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">7. Your Control</h2>
      <p class="mb-4">You can revoke access at any time:</p>
      <ul class="list-disc pl-6 space-y-2">
        <li><strong>Google:</strong> visit <a href="https://myaccount.google.com/permissions" class="text-emerald-400" rel="noopener" target="_blank">myaccount.google.com/permissions</a> and remove the application's access. Access stops immediately; the stored token becomes unusable.</li>
        <li><strong>TikTok:</strong> in the TikTok app, Settings and Privacy &gt; Security &gt; Manage app permissions.</li>
        <li>Or contact us to have stored records deleted.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">8. Contact Us</h2>
      <p>
        If you have questions or comments about this policy, you may email us at: <a href="mailto:contact@iyongbudiarso.com" class="text-emerald-400">contact@iyongbudiarso.com</a>
      </p>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: 'Privacy Policy - Iyong Budiarso',
  meta: [
    { name: 'robots', content: 'noindex, follow' }
  ]
})
</script>
