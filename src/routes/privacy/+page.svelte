<script lang="ts">
    import Navbar from "$lib/components/Navbar.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<Navbar />
<main>
    <div class="container">
        <div class="content">
            <h1>Privacy Policy</h1>
            <p class="last-updated">Last Updated: {new Date().toLocaleDateString('en-US', { year: 'numeric', month: 'long', day: 'numeric' })}</p>

            <section>
                <h2>1. Introduction</h2>
                <p>
                    Welcome to Slick Ride ("we," "our," or "us"). We are committed to protecting your privacy and ensuring the security of your personal information. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application and related services.
                </p>
                <p>
                    By using Slick Ride, you agree to the collection and use of information in accordance with this policy. If you do not agree with our policies and practices, please do not use our services.
                </p>
            </section>

            <section>
                <h2>2. Information We Collect</h2>
                
                <h3>2.1 Personal Information</h3>
                <p>We may collect the following personal information:</p>
                <ul>
                    <li><strong>Account Information:</strong> Name, email address, phone number, profile photo</li>
                    <li><strong>Payment Information:</strong> Credit/debit card details, billing address (processed securely through third-party payment processors)</li>
                    <li><strong>Identity Verification:</strong> Government-issued ID, driver's license (for drivers)</li>
                    <li><strong>Location Data:</strong> Real-time location when using the app, trip history</li>
                </ul>

                <h3>2.2 Usage Information</h3>
                <p>We automatically collect information about how you interact with our services:</p>
                <ul>
                    <li>Device information (model, operating system, unique device identifiers)</li>
                    <li>App usage data (features used, time spent, pages viewed)</li>
                    <li>Log data (IP address, access times, error logs)</li>
                    <li>Cookies and similar tracking technologies</li>
                </ul>

                <h3>2.3 Communication Data</h3>
                <p>We collect information from your communications with us, including:</p>
                <ul>
                    <li>Customer support interactions</li>
                    <li>Feedback and reviews</li>
                    <li>Survey responses</li>
                </ul>
            </section>

            <section>
                <h2>3. How We Use Your Information</h2>
                <p>We use the collected information for the following purposes:</p>
                <ul>
                    <li><strong>Service Provision:</strong> To provide, maintain, and improve our ride-sharing services</li>
                    <li><strong>Matching:</strong> To connect riders with drivers and facilitate trips</li>
                    <li><strong>Safety:</strong> To ensure the safety and security of our platform and users</li>
                    <li><strong>Payment Processing:</strong> To process payments and prevent fraud</li>
                    <li><strong>Communication:</strong> To send you service updates, notifications, and promotional materials</li>
                    <li><strong>Legal Compliance:</strong> To comply with legal obligations and respond to legal requests</li>
                    <li><strong>Analytics:</strong> To analyze usage patterns and improve our services</li>
                </ul>
            </section>

            <section>
                <h2>4. Information Sharing and Disclosure</h2>
                <p>We may share your information in the following circumstances:</p>
                
                <h3>4.1 With Other Users</h3>
                <ul>
                    <li>Riders and drivers see limited information necessary to complete trips (name, rating, vehicle information)</li>
                    <li>Contact information may be shared after trip completion for communication purposes</li>
                </ul>

                <h3>4.2 With Service Providers</h3>
                <ul>
                    <li>Payment processors</li>
                    <li>Cloud hosting services</li>
                    <li>Analytics providers</li>
                    <li>Customer support platforms</li>
                </ul>

                <h3>4.3 Legal Requirements</h3>
                <p>We may disclose your information if required by law or to:</p>
                <ul>
                    <li>Comply with legal processes or government requests</li>
                    <li>Enforce our terms of service</li>
                    <li>Protect our rights, privacy, safety, or property</li>
                    <li>Respond to emergencies</li>
                </ul>

                <h3>4.4 Business Transfers</h3>
                <p>In the event of a merger, acquisition, or sale of assets, your information may be transferred to the acquiring entity.</p>
            </section>

            <section>
                <h2>5. Data Security</h2>
                <p>
                    We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the internet or electronic storage is 100% secure, and we cannot guarantee absolute security.
                </p>
                <p>Security measures include:</p>
                <ul>
                    <li>Encryption of data in transit and at rest</li>
                    <li>Regular security assessments</li>
                    <li>Access controls and authentication</li>
                    <li>Secure payment processing</li>
                </ul>
            </section>

            <section>
                <h2>6. Your Rights and Choices</h2>
                <p>You have the following rights regarding your personal information:</p>
                <ul>
                    <li><strong>Access:</strong> Request access to your personal data</li>
                    <li><strong>Correction:</strong> Request correction of inaccurate or incomplete data</li>
                    <li><strong>Deletion:</strong> Request deletion of your personal data (subject to legal requirements)</li>
                    <li><strong>Portability:</strong> Request transfer of your data to another service</li>
                    <li><strong>Opt-out:</strong> Opt-out of marketing communications</li>
                    <li><strong>Location:</strong> Control location sharing through device settings</li>
                </ul>
                <p>
                    To exercise these rights, please contact us using the information provided in the "Contact Us" section below, or visit our <a href="/data-deletion">Data Deletion</a> page.
                </p>
            </section>

            <section>
                <h2>7. Data Retention</h2>
                <p>
                    We retain your personal information for as long as necessary to provide our services, comply with legal obligations, resolve disputes, and enforce our agreements. When data is no longer needed, we will securely delete or anonymize it.
                </p>
                <p>Retention periods may vary based on:</p>
                <ul>
                    <li>Legal and regulatory requirements</li>
                    <li>Business needs</li>
                    <li>Account status</li>
                </ul>
            </section>

            <section>
                <h2>8. Children's Privacy</h2>
                <p>
                    Our services are not intended for individuals under the age of 18. We do not knowingly collect personal information from children. If you believe we have collected information from a child, please contact us immediately.
                </p>
            </section>

            <section>
                <h2>9. International Data Transfers</h2>
                <p>
                    Your information may be transferred to and processed in countries other than your country of residence. These countries may have different data protection laws. By using our services, you consent to the transfer of your information to these countries.
                </p>
            </section>

            <section>
                <h2>10. Changes to This Privacy Policy</h2>
                <p>
                    We may update this Privacy Policy from time to time. We will notify you of any material changes by posting the new policy on this page and updating the "Last Updated" date. Your continued use of our services after changes become effective constitutes acceptance of the updated policy.
                </p>
            </section>

            <section>
                <h2>11. Contact Us</h2>
                <p>If you have questions, concerns, or requests regarding this Privacy Policy or our data practices, please contact us:</p>
                <div class="contact-info">
                    <p><strong>Slick Ride / Remo Rides</strong></p>
                    <p>Plot 10-14, Toll Gate,<br>Sagamu, Ogun State,<br>Nigeria</p>
                    <p><strong>Email:</strong> privacy@slickride.com</p>
                    <p><strong>Powered by:</strong> SlickDot International Venture</p>
                </div>
            </section>
        </div>
    </div>
</main>
<Footer />

<style>
    main {
        padding-top: calc(var(--header-height) + 60px);
        padding-bottom: 60px;
        min-height: 100vh;
    }

    .content {
        max-width: 900px;
        margin: 0 auto;
    }

    h1 {
        font-size: 3rem;
        font-weight: 800;
        margin-bottom: 16px;
        background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .last-updated {
        color: var(--color-text-muted);
        font-size: 0.95rem;
        margin-bottom: 48px;
        padding-bottom: 32px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    }

    section {
        margin-bottom: 48px;
    }

    h2 {
        font-size: 1.8rem;
        font-weight: 700;
        margin-bottom: 20px;
        color: var(--color-text-main);
    }

    h3 {
        font-size: 1.3rem;
        font-weight: 600;
        margin-top: 24px;
        margin-bottom: 12px;
        color: var(--color-text-main);
    }

    p {
        color: var(--color-text-muted);
        line-height: 1.8;
        margin-bottom: 16px;
        font-size: 1rem;
    }

    ul {
        color: var(--color-text-muted);
        line-height: 1.8;
        margin-left: 24px;
        margin-bottom: 16px;
    }

    li {
        margin-bottom: 8px;
    }

    strong {
        color: var(--color-text-main);
        font-weight: 600;
    }

    a {
        color: var(--color-primary);
        text-decoration: underline;
    }

    a:hover {
        color: var(--color-primary);
        opacity: 0.8;
    }

    .contact-info {
        background: var(--color-surface);
        padding: 32px;
        border-radius: 12px;
        border: 1px solid rgba(255, 255, 255, 0.05);
        margin-top: 24px;
    }

    .contact-info p {
        margin-bottom: 12px;
    }

    .contact-info strong {
        color: var(--color-primary);
    }

    @media (max-width: 768px) {
        h1 {
            font-size: 2rem;
        }

        h2 {
            font-size: 1.5rem;
        }

        h3 {
            font-size: 1.1rem;
        }

        .content {
            padding: 0 16px;
        }
    }
</style>

