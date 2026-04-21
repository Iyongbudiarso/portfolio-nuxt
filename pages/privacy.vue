<template>
  <div class="pt-32 pb-20 px-6 max-w-4xl mx-auto text-gray-300">
    <h1 class="text-4xl font-bold mb-8 text-white">Privacy Policy</h1>
    <p class="mb-4 italic">Last updated: April 21, 2026</p>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">1. Introduction</h2>
      <p class="mb-4">
        Welcome to iyongbudiarso.com ("we," "our," or "us"). We are committed to protecting your personal information and your right to privacy. This Privacy Policy explains how our Postiz integration interacts with your TikTok account and what data we collect.
      </p>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">2. Information We Collect</h2>
      <p class="mb-4">
        When you use our TikTok integration (via Postiz), we access specific information from your TikTok account through the official TikTok API:
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li><strong>Profile Information:</strong> We may access your TikTok display name, avatar, and unique identifier to help you identify which account you are managing.</li>
        <li><strong>Access Tokens:</strong> We store encrypted access tokens provided by TikTok to perform actions on your behalf (such as uploading videos). We do NOT store your TikTok password.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">3. How We Use Your Information</h2>
      <p class="mb-4">
        The information collected is used solely to provide the services you requested:
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li>To schedule and publish videos to your TikTok account as directed by you.</li>
        <li>To provide analytics or status updates regarding your posts.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">4. Data Sharing and Retention</h2>
      <p class="mb-4">
        We do not sell, trade, or otherwise transfer your personal information to outside parties. Your data is only shared with TikTok through their official API to facilitate the core functionality of the app.
      </p>
      <p>
        Tokens are stored securely and can be deleted by you at any time by disconnecting your TikTok account from our service or revoking permissions in your TikTok settings.
      </p>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">5. User Control</h2>
      <p class="mb-4">
        You have the right to revoke our access to your TikTok account at any time. You can do this via:
      </p>
      <ul class="list-disc pl-6 space-y-2">
        <li>The TikTok App: Settings and Privacy > Security > Manage app permissions.</li>
        <li>Our application dashboard: By removing your TikTok account link.</li>
      </ul>
    </section>

    <section class="mb-10">
      <h2 class="text-2xl font-semibold mb-4 text-white">6. Contact Us</h2>
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
