<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abu Dhabi Hudayriat Island - Instagram Carousel</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif;
            background: #f0f0f0;
            padding: 20px;
        }

        .slide-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .slide {
            width: 1080px;
            height: 1350px;
            background: #ffffff;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .slide-number {
            position: absolute;
            top: 30px;
            right: 30px;
            font-size: 14px;
            color: #999;
            font-weight: 300;
        }

        /* Slide 1 - Hook */
        .slide-1 {
            background: #0A1F44;
            color: #ffffff;
        }

        .slide-1 .main-text {
            font-size: 64px;
            font-weight: 300;
            line-height: 1.3;
            margin-bottom: 40px;
        }

        .slide-1 .highlight {
            font-size: 80px;
            font-weight: 700;
            color: #FFB627;
            display: block;
            margin: 20px 0;
        }

        .slide-1 .arrow {
            font-size: 72px;
            color: #FFB627;
            margin-top: 40px;
        }

        /* Slide 2 - Stats */
        .slide-2 {
            background: #F8F9FA;
        }

        .slide-2 .title {
            font-size: 48px;
            font-weight: 700;
            color: #0A1F44;
            margin-bottom: 80px;
        }

        .slide-2 .stat {
            font-size: 56px;
            font-weight: 700;
            color: #FFB627;
            margin: 30px 0 10px 0;
        }

        .slide-2 .stat-label {
            font-size: 36px;
            font-weight: 300;
            color: #2D3436;
            margin-bottom: 40px;
        }

        .slide-2 .conclusion {
            font-size: 42px;
            font-weight: 600;
            color: #0A1F44;
            margin-top: 60px;
        }

        /* Slide 3 - News Bomb */
        .slide-3 {
            background: #FFB627;
        }

        .slide-3 .badge {
            font-size: 32px;
            font-weight: 700;
            color: #0A1F44;
            background: #ffffff;
            padding: 15px 40px;
            border-radius: 50px;
            margin-bottom: 80px;
        }

        .slide-3 .main {
            font-size: 52px;
            font-weight: 300;
            color: #0A1F44;
            line-height: 1.4;
            margin-bottom: 40px;
        }

        .slide-3 .stake {
            font-size: 96px;
            font-weight: 900;
            color: #0A1F44;
            margin: 30px 0;
        }

        .slide-3 .conclusion {
            font-size: 38px;
            font-weight: 600;
            color: #0A1F44;
            margin-top: 60px;
            line-height: 1.5;
        }

        /* Slide 4 - Meaning */
        .slide-4 {
            background: #ffffff;
        }

        .slide-4 .amount {
            font-size: 72px;
            font-weight: 700;
            color: #FFB627;
            margin-bottom: 20px;
        }

        .slide-4 .text {
            font-size: 44px;
            font-weight: 300;
            color: #2D3436;
            line-height: 1.5;
            margin: 30px 0;
        }

        .slide-4 .not-buying {
            font-size: 48px;
            font-weight: 600;
            color: #0A1F44;
            margin: 60px 0 30px 0;
        }

        .slide-4 .buying {
            font-size: 52px;
            font-weight: 700;
            color: #FFB627;
            line-height: 1.3;
        }

        /* Slide 5 - Project Intro */
        .slide-5 {
            background: #0A1F44;
            color: #ffffff;
        }

        .slide-5 .title {
            font-size: 72px;
            font-weight: 700;
            color: #FFB627;
            margin-bottom: 60px;
            letter-spacing: 2px;
        }

        .slide-5 .feature {
            font-size: 36px;
            font-weight: 300;
            margin: 20px 0;
            line-height: 1.6;
        }

        .slide-5 .price {
            font-size: 64px;
            font-weight: 700;
            color: #FFB627;
            margin: 60px 0 40px 0;
        }

        .slide-5 .teaser {
            font-size: 38px;
            font-weight: 400;
            margin-top: 60px;
            line-height: 1.5;
        }

        /* Slide 6 - Unique Feature */
        .slide-6 {
            background: #F8F9FA;
        }

        .slide-6 .spec {
            font-size: 40px;
            font-weight: 300;
            color: #2D3436;
            margin: 25px 0;
            line-height: 1.5;
        }

        .slide-6 .spec strong {
            font-weight: 700;
            color: #FFB627;
        }

        .slide-6 .label {
            font-size: 36px;
            font-weight: 600;
            color: #0A1F44;
            margin: 60px 0 30px 0;
        }

        .slide-6 .guarantee {
            font-size: 56px;
            font-weight: 900;
            color: #0A1F44;
            margin: 30px 0;
            line-height: 1.3;
        }

        .slide-6 .forever {
            font-size: 42px;
            font-weight: 600;
            color: #FFB627;
            margin: 30px 0;
        }

        /* Slide 7 - Comparison */
        .slide-7 {
            background: #ffffff;
        }

        .slide-7 .header {
            font-size: 44px;
            font-weight: 300;
            color: #2D3436;
            margin-bottom: 60px;
        }

        .slide-7 .comparison {
            margin: 40px 0;
            text-align: left;
            width: 100%;
            max-width: 700px;
        }

        .slide-7 .location {
            font-size: 36px;
            font-weight: 400;
            color: #2D3436;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            border-bottom: 1px solid #e0e0e0;
        }

        .slide-7 .location:last-of-type {
            border-bottom: none;
        }

        .slide-7 .price-value {
            font-size: 48px;
            font-weight: 700;
            color: #FFB627;
        }

        .slide-7 .conclusion {
            font-size: 42px;
            font-weight: 600;
            color: #0A1F44;
            margin-top: 80px;
            line-height: 1.5;
        }

        /* Slide 8 - ROI */
        .slide-8 {
            background: #0A1F44;
            color: #ffffff;
        }

        .slide-8 .header {
            font-size: 48px;
            font-weight: 700;
            color: #FFB627;
            margin-bottom: 60px;
        }

        .slide-8 .roi {
            font-size: 96px;
            font-weight: 900;
            color: #FFB627;
            margin: 40px 0;
        }

        .slide-8 .timeline {
            font-size: 36px;
            font-weight: 300;
            margin-bottom: 80px;
        }

        .slide-8 .example {
            font-size: 38px;
            font-weight: 300;
            margin: 20px 0;
            line-height: 1.6;
        }

        .slide-8 .example strong {
            font-weight: 700;
            color: #FFB627;
        }

        .slide-8 .tagline {
            font-size: 40px;
            font-weight: 600;
            margin-top: 60px;
            line-height: 1.5;
        }

        /* Slide 9 - Game Changer */
        .slide-9 {
            background: #FFB627;
        }

        .slide-9 .title {
            font-size: 52px;
            font-weight: 700;
            color: #0A1F44;
            margin-bottom: 50px;
        }

        .slide-9 .step {
            font-size: 40px;
            font-weight: 400;
            color: #0A1F44;
            margin: 15px 0;
            line-height: 1.4;
        }

        .slide-9 .divider {
            width: 200px;
            height: 3px;
            background: #0A1F44;
            margin: 50px auto;
        }

        .slide-9 .example-label {
            font-size: 32px;
            font-weight: 600;
            color: #0A1F44;
            margin-bottom: 30px;
        }

        .slide-9 .calc {
            font-size: 36px;
            font-weight: 300;
            color: #0A1F44;
            margin: 12px 0;
        }

        .slide-9 .result {
            font-size: 64px;
            font-weight: 900;
            color: #0A1F44;
            margin: 40px 0 20px 0;
        }

        /* Slide 10 - Payment Plan */
        .slide-10 {
            background: #F8F9FA;
        }

        .slide-10 .title {
            font-size: 48px;
            font-weight: 700;
            color: #0A1F44;
            margin-bottom: 60px;
        }

        .slide-10 .payment-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            max-width: 700px;
            margin: 25px 0;
            padding: 20px 0;
            border-bottom: 2px solid #e0e0e0;
        }

        .slide-10 .payment-item:last-of-type {
            border-bottom: none;
        }

        .slide-10 .percentage {
            font-size: 72px;
            font-weight: 900;
            color: #FFB627;
        }

        .slide-10 .description {
            font-size: 32px;
            font-weight: 300;
            color: #2D3436;
            text-align: right;
        }

        .slide-10 .note {
            font-size: 36px;
            font-weight: 600;
            color: #0A1F44;
            margin-top: 60px;
            line-height: 1.6;
        }

        /* Slide 11 - Transaction Edge */
        .slide-11 {
            background: #ffffff;
        }

        .slide-11 .badge {
            font-size: 32px;
            font-weight: 700;
            color: #ffffff;
            background: #FFB627;
            padding: 15px 40px;
            border-radius: 50px;
            margin-bottom: 80px;
        }

        .slide-11 .comparison-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            max-width: 700px;
            margin: 30px 0;
        }

        .slide-11 .city {
            font-size: 40px;
            font-weight: 400;
            color: #2D3436;
        }

        .slide-11 .fee {
            font-size: 56px;
            font-weight: 700;
            color: #FFB627;
        }

        .slide-11 .savings {
            font-size: 48px;
            font-weight: 600;
            color: #0A1F44;
            margin: 60px 0 20px 0;
        }

        .slide-11 .amount {
            font-size: 72px;
            font-weight: 900;
            color: #FFB627;
            margin: 20px 0;
        }

        .slide-11 .tagline {
            font-size: 38px;
            font-weight: 300;
            color: #2D3436;
            margin-top: 60px;
            line-height: 1.5;
        }

        /* Slide 12 - Lifestyle */
        .slide-12 {
            background: #0A1F44;
            color: #ffffff;
        }

        .slide-12 .title {
            font-size: 64px;
            font-weight: 900;
            color: #FFB627;
            margin-bottom: 40px;
            line-height: 1.2;
        }

        .slide-12 .subtitle {
            font-size: 36px;
            font-weight: 300;
            margin-bottom: 80px;
        }

        .slide-12 .amenity {
            font-size: 40px;
            font-weight: 300;
            margin: 25px 0;
            line-height: 1.5;
        }

        .slide-12 .amenity-icon {
            font-size: 48px;
            margin-right: 20px;
        }

        .slide-12 .divider {
            width: 150px;
            height: 3px;
            background: #FFB627;
            margin: 60px auto;
        }

        .slide-12 .conclusion {
            font-size: 44px;
            font-weight: 600;
            margin-top: 40px;
            line-height: 1.5;
        }

        /* Slide 13 - Urgency */
        .slide-13 {
            background: #FFB627;
        }

        .slide-13 .item {
            margin: 40px 0;
        }

        .slide-13 .label {
            font-size: 32px;
            font-weight: 400;
            color: #0A1F44;
            margin-bottom: 15px;
        }

        .slide-13 .value {
            font-size: 64px;
            font-weight: 900;
            color: #0A1F44;
        }

        .slide-13 .divider {
            width: 200px;
            height: 3px;
            background: #0A1F44;
            margin: 60px auto;
        }

        .slide-13 .tagline {
            font-size: 48px;
            font-weight: 700;
            color: #0A1F44;
            margin-top: 40px;
            line-height: 1.4;
        }

        /* Slide 14 - CTA */
        .slide-14 {
            background: #0A1F44;
            color: #ffffff;
        }

        .slide-14 .title {
            font-size: 56px;
            font-weight: 700;
            color: #FFB627;
            margin-bottom: 60px;
        }

        .slide-14 .list-item {
            font-size: 32px;
            font-weight: 300;
            margin: 20px 0;
            line-height: 1.5;
        }

        .slide-14 .list-item::before {
            content: "•";
            color: #FFB627;
            font-weight: 700;
            margin-right: 15px;
        }

        .slide-14 .cta-box {
            background: #FFB627;
            color: #0A1F44;
            padding: 40px 60px;
            border-radius: 20px;
            margin: 60px 0;
        }

        .slide-14 .cta-text {
            font-size: 42px;
            font-weight: 700;
            margin-bottom: 20px;
        }

        .slide-14 .cta-action {
            font-size: 56px;
            font-weight: 900;
        }

        .slide-14 .final {
            font-size: 40px;
            font-weight: 600;
            margin-top: 60px;
            line-height: 1.5;
        }

        @media print {
            body {
                background: #ffffff;
                padding: 0;
            }
            .slide {
                page-break-after: always;
            }
        }
    </style>
</head>
<body>
    <div class="slide-container">
        
        <!-- Slide 1 -->
        <div class="slide slide-1">
            <div class="slide-number">01/14</div>
            <div class="main-text">
                Everyone's buying Dubai.
                <span class="highlight">The government is buying Abu Dhabi.</span>
                Guess who wins?
            </div>
            <div class="arrow">→</div>
        </div>

        <!-- Slide 2 -->
        <div class="slide slide-2">
            <div class="slide-number">02/14</div>
            <div class="title">ABU DHABI 2024:</div>
            <div>
                <div class="stat">+289,000</div>
                <div class="stat-label">new residents</div>
                <div class="stat">-10,000</div>
                <div class="stat-label">new homes</div>
            </div>
            <div class="conclusion">Do the math.</div>
        </div>

        <!-- Slide 3 -->
        <div class="slide slide-3">
            <div class="slide-number">03/14</div>
            <div class="badge">JUST HAPPENED</div>
            <div class="main">
                Abu Dhabi Government
            </div>
            <div class="stake">84.7%</div>
            <div class="main">stake in Modon</div>
            <div class="conclusion">
                They're not hoping.<br>
                They're guaranteeing.
            </div>
        </div>

        <!-- Slide 4 -->
        <div class="slide slide-4">
            <div class="slide-number">04/14</div>
            <div class="amount">£150 billion</div>
            <div class="text">
                sovereign wealth fund<br>
                takes<br>
                84.7% control
            </div>
            <div class="not-buying">You're not buying property.</div>
            <div class="buying">
                You're buying into<br>
                government strategy.
            </div>
        </div>

        <!-- Slide 5 -->
        <div class="slide slide-5">
            <div class="slide-number">05/14</div>
            <div class="title">HUDAYRIAT ISLAND</div>
            <div class="feature">17km pristine beachfront</div>
            <div class="feature">Same coastline as royalty</div>
            <div class="price">From AED 9M</div>
            <div class="feature">(≈ £1,900,000)</div>
            <div class="teaser">
                But it's not the price.<br>
                It's the structure →
            </div>
        </div>

        <!-- Slide 6 -->
        <div class="slide slide-6">
            <div class="slide-number">06/14</div>
            <div class="spec">Built on <strong>man-made hills</strong></div>
            <div class="spec"><strong>50-60 meters</strong> high</div>
            <div class="spec">Each villa: <strong>15m above</strong> the one below</div>
            <div class="label">Result?</div>
            <div class="guarantee">UNOBSTRUCTED<br>OCEAN VIEWS</div>
            <div class="forever">Forever guaranteed.</div>
            <div class="spec" style="margin-top: 40px;">Nobody can block you.</div>
        </div>

        <!-- Slide 7 -->
        <div class="slide slide-7">
            <div class="slide-number">07/14</div>
            <div class="header">Price per sqft:</div>
            <div class="comparison">
                <div class="location">
                    <span>Hudayriat</span>
                    <span class="price-value">£1,100</span>
                </div>
                <div class="location">
                    <span>Hidd Al Saadiyat</span>
                    <span class="price-value">£2,200</span>
                </div>
            </div>
            <div class="conclusion">
                50% cheaper.<br>
                Better location.<br>
                You're early.
            </div>
        </div>

        <!-- Slide 8 -->
        <div class="slide slide-8">
            <div class="slide-number">08/14</div>
            <div class="header">Conservative estimate:</div>
            <div class="roi">40-50%</div>
            <div class="timeline">ROI by 2028 handover</div>
            <div style="margin-top: 60px;">
                <div class="example">Saadiyat did this:</div>
                <div class="example"><strong>£6M → £25M+</strong> (400%)</div>
            </div>
            <div class="tagline" style="margin-top: 80px;">
                Same emirate.<br>
                Same playbook.<br>
                Better entry price.
            </div>
        </div>

        <!-- Slide 9 -->
        <div class="slide slide-9">
            <div class="slide-number">09/14</div>
            <div class="title">THE 20% RESALE CLAUSE</div>
            <div class="step">Pay 20%</div>
            <div class="step">Resell before completion</div>
            <div class="step">Keep the profit</div>
            <div class="divider"></div>
            <div class="example-label">Example:</div>
            <div class="calc">£380K down</div>
            <div class="calc">18 months later</div>
            <div class="calc">Sell for £2.2M</div>
            <div class="result">Profit: £300K</div>
            <div class="calc" style="margin-top: 30px; font-weight: 600;">75% return on YOUR capital deployed</div>
        </div>

        <!-- Slide 10 -->
        <div class="slide slide-10">
            <div class="slide-number">10/14</div>
            <div class="title">THE STRUCTURE</div>
            <div class="payment-item">
                <div class="percentage">10%</div>
                <div class="description">Booking</div>
            </div>
            <div class="payment-item">
                <div class="percentage">10%</div>
                <div class="description">Over 2 years</div>
            </div>
            <div class="payment-item">
                <div class="percentage">20%</div>
                <div class="description">Before handover</div>
            </div>
            <div class="payment-item">
                <div class="percentage">60%</div>
                <div class="description">On completion</div>
            </div>
            <div class="note">
                Milestone-based.<br>
                If they delay, you don't pay.
            </div>
        </div>

        <!-- Slide 11 -->
        <div class="slide slide-11">
            <div class="slide-number">11/14</div>
            <div class="badge">BONUS</div>
            <div class="comparison-row">
                <div class="city">Dubai charges</div>
                <div class="fee">4%</div>
            </div>
            <div class="comparison-row">
                <div class="city">Abu Dhabi charges</div>
                <div class="fee">2%</div>
            </div>
            <div class="savings">On £2M purchase:</div>
            <div class="amount">Save £40,000</div>
            <div class="savings" style="font-weight: 300; margin-top: 30px;">on day one</div>
            <div class="tagline">
                Little details.<br>
                Big differences.
            </div>
        </div>

        <!-- Slide 12 -->
        <div class="slide slide-12">
            <div class="slide-number">12/14</div>
            <div class="title">£10 BILLION DESTINATION</div>
            <div class="amenity"><span class="amenity-icon">🏄</span> World's largest surf pool</div>
            <div class="amenity"><span class="amenity-icon">🚴</span> Rooftop velodrome</div>
            <div class="amenity"><span class="amenity-icon">⛳</span> 3 golf courses</div>
            <div class="amenity"><span class="amenity-icon">🏇</span> Equestrian centers</div>
            <div class="divider"></div>
            <div class="conclusion">
                Not a villa community.<br>
                A lifestyle ecosystem.
            </div>
        </div>

        <!-- Slide 13 -->
        <div class="slide slide-13">
            <div class="slide-number">13/14</div>
            <div class="item">
                <div class="label">First handovers:</div>
                <div class="value">2028</div>
            </div>
            <div class="item">
                <div class="label">Current price:</div>
                <div class="value">£1,100/sqft</div>
            </div>
            <div class="divider"></div>
            <div class="tagline">
                Early = advantage.<br>
                Late = expensive.
            </div>
        </div>

        <!-- Slide 14 -->
        <div class="slide slide-14">
            <div class="slide-number">14/14</div>
            <div class="title">WANT THE NUMBERS?</div>
            <div style="text-align: left; max-width: 600px;">
                <div class="list-item">Payment breakdowns</div>
                <div class="list-item">Villa categories</div>
                <div class="list-item">ROI projections</div>
                <div class="list-item">Floor plans</div>
                <div class="list-item">Resale strategy</div>
            </div>
            <div class="cta-box">
                <div class="cta-text">👇 Comment</div>
                <div class="cta-action">"BROCHURE"</div>
            </div>
            <div class="final">
                Last chance to enter<br>
                UAE beachfront under £2M.
            </div>
        </div>

    </div>
</body>
</html>
