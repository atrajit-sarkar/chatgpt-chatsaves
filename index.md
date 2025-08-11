---
layout: home
---

<!-- Hero Section -->
<section class="hero-section">
    <div class="hero-background">
        <div class="hero-particles"></div>
        <div class="hero-grid"></div>
    </div>
    
    <div class="container">
        <div class="hero-content">
            <div class="hero-image-container">
                <div class="status-indicator">
                    <span class="status-dot"></span>
                    Friend Quest Active
                </div>
                <div class="dual-profile-container">
                    <img src="/atrajit.jpg" alt="User 1" class="hero-image profile-left">
                    <img src="/tukun.jpg" alt="User 2" class="hero-image profile-right">
                    <div class="connection-line"></div>
                </div>
                <div class="hero-glow"></div>
            </div>
            
            <div class="hero-text">
                <div class="typing-animation">
                    <h1 class="hero-title hero-with-logo">
                        <span class="hero-logo">
                            <img src="/assets/images/logo-all-in-ichi.svg" alt="All in いち logo" width="72" height="72" loading="eager" />
                        </span>
                        <span class="welcome-text">Welcome to</span>
                        <span class="text-gradient">All in いち</span>
                    </h1>
                    <div class="typing-container">
                        <span class="typing-text"></span>
                        <span class="cursor">|</span>
                    </div>
                </div>
                
                <p class="hero-description">
                    <strong>Where Conversations Live Forever ✨</strong><br>
                    Your personal archive for meaningful chats. 
                    Collect, save, and revisit every exchange in one place.
                </p>
                
                <div class="hero-stats">
                    <div class="stat-item">
                        <span class="stat-number">∞</span>
                        <span class="stat-label">Conversations</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">2+</span>
                        <span class="stat-label">Friends</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">24/7</span>
                        <span class="stat-label">Archive</span>
                    </div>
                </div>
                
                <div class="hero-actions">
                    <a href="/posts/" class="btn btn-primary">
                        <span>Browse Chat Archive</span>
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/>
                        </svg>
                    </a>
                    <a href="#features" class="btn btn-secondary">
                        <span>Learn More</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Features Section -->
<section class="features-section" id="features">
    <div class="container">
        <div class="section-header">
            <h2 class="section-title">
                <span class="section-emoji">✨</span>
                Why Save Your Conversations?
            </h2>
            <p class="section-description">
                Transform fleeting chats into lasting wisdom
            </p>
        </div>
        
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">
                    <span>💾</span>
                </div>
                <h3>Archive Forever</h3>
                <p>Never lose a valuable conversation again. Store all your chats in one secure place.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <span>👥</span>
                </div>
                <h3>Friend Quest</h3>
                <p>Share meaningful conversations with friends and explore how others interact with AI.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <span>🔍</span>
                </div>
                <h3>Smart Search</h3>
                <p>Find any conversation instantly with our powerful search features across all your saved chats.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <span>📚</span>
                </div>
                <h3>Knowledge Base</h3>
                <p>Build your personal knowledge library and revisit insights whenever you need them.</p>
            </div>
        </div>
    </div>
</section>

<!-- Recent Chats Section -->
<section class="recent-chats-section">
    <div class="container">
        <div class="section-header">
            <h2 class="section-title">
                <span class="section-emoji">💬</span>
                Recent Chat Saves
            </h2>
            <p class="section-description">
                Latest conversations from our community
            </p>
        </div>
        
        <div class="posts-grid">
            {% for post in site.posts limit:3 %}
            <article class="post-card">
                <div class="post-meta">
                    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
                    <div class="post-category">{{ post.categories | first | capitalize }}</div>
                </div>
                <h3 class="post-title">
                    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
                </h3>
                <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
                <div class="post-tags">
                    {% for tag in post.tags limit:3 %}
                    <span class="post-tag">{{ tag }}</span>
                    {% endfor %}
                </div>
                <a href="{{ post.url | relative_url }}" class="post-link">
                    Read Chat
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/>
                    </svg>
                </a>
            </article>
            {% endfor %}
        </div>
        
        <div class="section-cta">
            <a href="/posts/" class="btn btn-primary">View All Chats</a>
        </div>
    </div>
</section>
