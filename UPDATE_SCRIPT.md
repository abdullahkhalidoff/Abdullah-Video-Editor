# Remaining Updates for Premium Gold Theme + Mobile Responsive

## Work Experience Section
Replace line ~335 section opening with:
```tsx
<section id="work-experience" className="relative min-h-screen flex items-center justify-center px-4 sm:px-6 py-16 sm:py-20 z-0 bg-white/[0.02]">
  <div className="max-w-6xl w-full">
    <div className="text-center mb-12 sm:mb-16">
      <h2 className="text-4xl sm:text-5xl font-bold mb-4">
        Work <span className="text-primary">Experience</span>
      </h2>
      <p className="text-[#A3A3A3] text-base sm:text-lg">My professional journey as a video editor</p>
    </div>
```

## Experience Cards
Replace each card with gold theme + responsive:
```tsx
<div className="relative bg-[#1A1A1A]/60 backdrop-blur-sm rounded-3xl p-6 sm:p-8 md:p-10 border border-primary/10 hover:border-primary/30 hover:bg-[#1A1A1A]/80 transition-all duration-500 group hover:shadow-[0_12px_24px_-8px_rgba(212,175,55,0.15)]">
  <div className="absolute top-0 left-0 w-1 h-full bg-gradient-to-b from-[#F5C86B] via-[#D4AF37] to-[#B8941F] rounded-l-3xl"></div>
  <div className="flex flex-col gap-4 mb-6">
    <div>
      <h3 className="text-2xl sm:text-3xl font-bold text-white group-hover:text-primary transition-colors duration-500">Company Name</h3>
      <p className="text-lg sm:text-xl text-primary mt-1">Video Editor</p>
      <p className="text-sm sm:text-base text-[#A3A3A3] mt-2">Date Range</p>
    </div>
  </div>
  <ul className="space-y-3 sm:space-y-4 text-sm sm:text-base text-[#E5E5E5]">
    <li className="flex items-start gap-3">
      <span className="text-primary mt-1 text-xl flex-shrink-0">•</span>
      <span>Achievement text</span>
    </li>
  </ul>
</div>
```

## Portfolio Section - CRITICAL (Make Videos Hero!)
```tsx
<section id="portfolio" className="relative min-h-screen flex items-center justify-center px-4 sm:px-6 py-16 sm:py-20 z-0">
  <div className="max-w-6xl w-full">
    <div className="text-center mb-12 sm:mb-16">
      <h2 className="text-4xl sm:text-5xl font-bold mb-4">
        My <span className="text-primary">Portfolio</span>
      </h2>
      <p className="text-[#A3A3A3] text-base sm:text-lg">Showcasing my video editing projects</p>
    </div>

    {/* Short-Form Videos */}
    <div className="mb-12">
      <h3 className="text-xl sm:text-2xl font-bold text-white mb-6 text-center">
        Short-Form Content <span style={{color: 'var(--primary-light)'}}>(Shorts/Reels/TikTok)</span>
      </h3>
      <div className="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4 sm:gap-6 max-w-6xl mx-auto">
        {youtubeVideos.filter(video => video.isShort).map((video) => (
          <div
            key={video.id}
            className="group bg-[#1A1A1A]/40 backdrop-blur-sm rounded-2xl p-3 sm:p-4 border border-white/5 hover:border-primary/20 hover:bg-[#1A1A1A]/60 transition-all duration-500"
          >
            <div className="relative w-full aspect-[9/16] rounded-lg overflow-hidden border border-primary/15 group-hover:border-primary/30 transition-all duration-500 mb-3">
              <iframe ... />
            </div>
            <h4 className="text-xs sm:text-sm font-bold text-white group-hover:text-[#F5C86B] transition-colors duration-500 mb-1 line-clamp-2">
              {video.title}
            </h4>
            <p className="text-xs text-[#A3A3A3] line-clamp-2">{video.description}</p>
          </div>
        ))}
      </div>
    </div>
```

## Contact Section
```tsx
<section id="contact" className="relative min-h-screen flex items-center justify-center px-4 sm:px-6 py-16 sm:py-20 z-0">
  <div className="max-w-4xl w-full">
    <h2 className="text-4xl sm:text-5xl font-bold text-center mb-8 sm:mb-12">
      Get In <span className="text-primary">Touch</span>
    </h2>
    <div className="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8">
      <div className="bg-[#1A1A1A]/60 backdrop-blur-sm rounded-3xl p-6 sm:p-8 border border-primary/10 space-y-6">
        <h3 className="text-xl sm:text-2xl font-bold text-primary mb-6">Contact Info</h3>
        <div className="space-y-4">
          <div className="flex items-center gap-4">
            <div className="w-12 h-12 bg-primary/10 border border-primary/20 rounded-full flex items-center justify-center flex-shrink-0">
              <svg className="w-6 h-6 text-primary" ...>
            </div>
            <div>
              <p className="text-sm text-[#A3A3A3]">Label</p>
              <p className="text-white text-sm sm:text-base">Value</p>
            </div>
          </div>
        </div>
      </div>

      <div className="bg-[#1A1A1A]/60 backdrop-blur-sm rounded-3xl p-6 sm:p-8 border border-primary/10">
        <h3 className="text-xl sm:text-2xl font-bold text-primary mb-6">Send Message</h3>
        <form className="space-y-4">
          <input
            type="text"
            placeholder="Your Name"
            className="w-full px-4 py-3 bg-[#1A1A1A]/60 border border-white/10 rounded-xl text-white placeholder-[#737373] focus:outline-none focus:border-primary/40 focus:ring-2 focus:ring-primary/20 transition-all duration-300 text-sm sm:text-base"
          />
          <button
            type="submit"
            className="w-full px-6 sm:px-8 py-3 bg-gradient-to-b from-[#F5C86B] via-[#D4AF37] to-[#B8941F] hover:opacity-90 text-[#0A0A0A] font-semibold rounded-xl transition-all duration-500 hover:scale-[1.02] hover:shadow-[0_12px_32px_-8px_rgba(212,175,55,0.35)] text-sm sm:text-base"
          >
            Send Message
          </button>
        </form>
      </div>
    </div>
  </div>
</section>
```

## Footer
```tsx
<footer className="relative py-6 sm:py-8 px-4 sm:px-6 border-t border-primary/10 z-0">
  <div className="max-w-6xl mx-auto text-center text-[#A3A3A3]">
    <p className="text-sm sm:text-base">&copy; 2026 Abdullah Khalid. All rights reserved.</p>
    <p className="mt-2 text-xs sm:text-sm">
      Designed with <span className="text-primary">creativity</span> and{' '}
      <span className="text-primary">passion</span>
    </p>
  </div>
</footer>
```

## Global Mobile Responsive Classes to Add:
- `px-4 sm:px-6` instead of `px-6`
- `py-16 sm:py-20` instead of `py-20`
- `text-4xl sm:text-5xl` for headings
- `text-base sm:text-lg` for body text
- `grid-cols-1 sm:grid-cols-2 md:grid-cols-3` for grids
- `gap-4 sm:gap-6` for spacing
- `p-6 sm:p-8 md:p-10` for padding

