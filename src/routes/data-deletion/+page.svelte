<script lang="ts">
    import Navbar from "$lib/components/Navbar.svelte";
    import Footer from "$lib/components/Footer.svelte";
    
    let email = "";
    let reason = "";
    let submitted = false;
    let error = "";

    async function handleSubmit() {
        error = "";
        
        if (!email || !email.includes("@")) {
            error = "Please enter a valid email address.";
            return;
        }

        if (!reason || reason.trim().length < 10) {
            error = "Please provide a reason (at least 10 characters).";
            return;
        }

        // In a real application, this would send a request to your backend
        // For now, we'll simulate a submission
        try {
            // Simulate API call
            await new Promise(resolve => setTimeout(resolve, 1000));
            submitted = true;
        } catch (err) {
            error = "An error occurred. Please try again later.";
        }
    }

    function resetForm() {
        email = "";
        reason = "";
        submitted = false;
        error = "";
    }
</script>

<Navbar />
<main>
    <div class="container">
        <div class="content">
            <h1>Data Deletion Request</h1>
            <p class="subtitle">
                You have the right to request deletion of your personal data. Please fill out the form below to submit your request.
            </p>

            {#if submitted}
                <div class="success-message">
                    <h2>Request Submitted Successfully</h2>
                    <p>
                        Thank you for your data deletion request. We have received your request and will process it within 30 days as required by applicable data protection laws.
                    </p>
                    <p>
                        You will receive a confirmation email at <strong>{email}</strong> with further instructions. If you don't receive an email within 24 hours, please check your spam folder or contact us directly.
                    </p>
                    <p>
                        <strong>Note:</strong> Some information may be retained for legal or regulatory purposes, such as transaction records required for tax or legal compliance.
                    </p>
                    <button on:click={resetForm} class="btn-secondary">Submit Another Request</button>
                </div>
            {:else}
                <div class="form-container">
                    <form on:submit|preventDefault={handleSubmit}>
                        <div class="form-group">
                            <label for="email">Email Address *</label>
                            <input
                                type="email"
                                id="email"
                                bind:value={email}
                                placeholder="your.email@example.com"
                                required
                            />
                            <p class="help-text">The email address associated with your Slick Ride account</p>
                        </div>

                        <div class="form-group">
                            <label for="reason">Reason for Deletion *</label>
                            <textarea
                                id="reason"
                                bind:value={reason}
                                placeholder="Please provide a brief reason for your data deletion request..."
                                rows="5"
                                required
                            ></textarea>
                            <p class="help-text">Minimum 10 characters required</p>
                        </div>

                        {#if error}
                            <div class="error-message">
                                {error}
                            </div>
                        {/if}

                        <div class="info-box">
                            <h3>What happens after you submit?</h3>
                            <ul>
                                <li>We will verify your identity using the email address provided</li>
                                <li>Your request will be processed within 30 days</li>
                                <li>You will receive a confirmation email with the status of your request</li>
                                <li>Some data may be retained for legal or regulatory compliance</li>
                            </ul>
                        </div>

                        <div class="form-actions">
                            <button type="submit" class="btn-primary">Submit Deletion Request</button>
                            <a href="/privacy" class="btn-link">View Privacy Policy</a>
                        </div>
                    </form>
                </div>

                <section class="additional-info">
                    <h2>Important Information</h2>
                    
                    <h3>What Data Will Be Deleted?</h3>
                    <p>Upon approval of your request, we will delete:</p>
                    <ul>
                        <li>Your account profile and personal information</li>
                        <li>Ride history and trip data</li>
                        <li>Payment information (after required retention periods)</li>
                        <li>App usage data and preferences</li>
                        <li>Communication records</li>
                    </ul>

                    <h3>What Data May Be Retained?</h3>
                    <p>We may retain certain information for legal or regulatory purposes:</p>
                    <ul>
                        <li>Transaction records required for tax compliance</li>
                        <li>Records required by law enforcement or regulatory authorities</li>
                        <li>Anonymized data used for analytics and service improvement</li>
                        <li>Information necessary to resolve disputes or enforce agreements</li>
                    </ul>

                    <h3>Alternative Options</h3>
                    <p>Before requesting complete deletion, you may want to consider:</p>
                    <ul>
                        <li><strong>Account Deactivation:</strong> Temporarily disable your account instead of permanent deletion</li>
                        <li><strong>Data Export:</strong> Request a copy of your data before deletion</li>
                        <li><strong>Privacy Settings:</strong> Adjust your privacy settings to limit data collection</li>
                    </ul>

                    <h3>Need Help?</h3>
                    <p>
                        If you have questions about data deletion or need assistance, please contact us at 
                        <a href="mailto:privacy@slickride.com">privacy@slickride.com</a>
                    </p>
                </section>
            {/if}
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
        max-width: 800px;
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

    .subtitle {
        color: var(--color-text-muted);
        font-size: 1.1rem;
        margin-bottom: 48px;
        line-height: 1.6;
    }

    .form-container {
        background: var(--color-surface);
        padding: 40px;
        border-radius: 16px;
        border: 1px solid rgba(255, 255, 255, 0.05);
        margin-bottom: 48px;
    }

    .form-group {
        margin-bottom: 32px;
    }

    label {
        display: block;
        color: var(--color-text-main);
        font-weight: 600;
        margin-bottom: 8px;
        font-size: 0.95rem;
    }

    input,
    textarea {
        width: 100%;
        padding: 14px 16px;
        background: var(--color-bg);
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 8px;
        color: var(--color-text-main);
        font-family: var(--font-body);
        font-size: 1rem;
        transition: all 0.2s ease;
    }

    input:focus,
    textarea:focus {
        outline: none;
        border-color: var(--color-primary);
        box-shadow: 0 0 0 3px rgba(0, 242, 255, 0.1);
    }

    textarea {
        resize: vertical;
        min-height: 120px;
    }

    .help-text {
        margin-top: 6px;
        font-size: 0.85rem;
        color: var(--color-text-muted);
    }

    .error-message {
        background: rgba(255, 59, 48, 0.1);
        border: 1px solid rgba(255, 59, 48, 0.3);
        color: #ff3b30;
        padding: 12px 16px;
        border-radius: 8px;
        margin-bottom: 24px;
        font-size: 0.95rem;
    }

    .success-message {
        background: var(--color-surface);
        padding: 40px;
        border-radius: 16px;
        border: 1px solid rgba(0, 242, 255, 0.2);
        margin-bottom: 48px;
    }

    .success-message h2 {
        color: var(--color-primary);
        margin-bottom: 16px;
        font-size: 1.8rem;
    }

    .success-message p {
        color: var(--color-text-muted);
        line-height: 1.8;
        margin-bottom: 16px;
    }

    .success-message strong {
        color: var(--color-text-main);
    }

    .info-box {
        background: rgba(0, 242, 255, 0.05);
        border: 1px solid rgba(0, 242, 255, 0.2);
        padding: 24px;
        border-radius: 12px;
        margin-bottom: 32px;
    }

    .info-box h3 {
        color: var(--color-primary);
        font-size: 1.1rem;
        margin-bottom: 12px;
    }

    .info-box ul {
        color: var(--color-text-muted);
        margin-left: 20px;
        line-height: 1.8;
    }

    .info-box li {
        margin-bottom: 8px;
    }

    .form-actions {
        display: flex;
        gap: 16px;
        flex-wrap: wrap;
        align-items: center;
    }

    .btn-primary {
        background: var(--color-primary);
        color: #000;
        padding: 14px 32px;
        border-radius: 100px;
        font-weight: 700;
        font-size: 1rem;
        transition: all 0.2s ease;
        box-shadow: 0 0 20px rgba(0, 242, 255, 0.2);
        cursor: pointer;
    }

    .btn-primary:hover {
        transform: translateY(-2px);
        box-shadow: 0 0 30px rgba(0, 242, 255, 0.4);
    }

    .btn-secondary {
        background: var(--color-surface);
        color: var(--color-text-main);
        padding: 14px 32px;
        border-radius: 100px;
        font-weight: 600;
        font-size: 1rem;
        border: 1px solid rgba(255, 255, 255, 0.1);
        transition: all 0.2s ease;
        cursor: pointer;
    }

    .btn-secondary:hover {
        background: var(--color-surface-hover);
        border-color: rgba(255, 255, 255, 0.2);
    }

    .btn-link {
        color: var(--color-primary);
        text-decoration: underline;
        font-weight: 500;
    }

    .btn-link:hover {
        opacity: 0.8;
    }

    .additional-info {
        margin-top: 48px;
    }

    .additional-info h2 {
        font-size: 1.8rem;
        font-weight: 700;
        margin-bottom: 24px;
        color: var(--color-text-main);
    }

    .additional-info h3 {
        font-size: 1.3rem;
        font-weight: 600;
        margin-top: 32px;
        margin-bottom: 12px;
        color: var(--color-text-main);
    }

    .additional-info p {
        color: var(--color-text-muted);
        line-height: 1.8;
        margin-bottom: 12px;
    }

    .additional-info ul {
        color: var(--color-text-muted);
        line-height: 1.8;
        margin-left: 24px;
        margin-bottom: 24px;
    }

    .additional-info li {
        margin-bottom: 8px;
    }

    .additional-info strong {
        color: var(--color-text-main);
        font-weight: 600;
    }

    .additional-info a {
        color: var(--color-primary);
        text-decoration: underline;
    }

    .additional-info a:hover {
        opacity: 0.8;
    }

    @media (max-width: 768px) {
        h1 {
            font-size: 2rem;
        }

        .form-container {
            padding: 24px;
        }

        .form-actions {
            flex-direction: column;
        }

        .btn-primary,
        .btn-secondary {
            width: 100%;
        }

        .content {
            padding: 0 16px;
        }
    }
</style>

