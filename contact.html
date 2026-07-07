/* =====================================================================
   GO DENTAL — Interactions
   Vanilla JS · no dependencies · progressive enhancement
   ===================================================================== */
(function () {
  "use strict";

  /* ---- Brand constants (single source of truth) ---- */
  var WA_NUMBER = "923332498977"; // +92 333 2498977 — WhatsApp format, digits only

  // expose for inline buttons that may build URLs at runtime
  window.GoDental = {
    wa: function (message) {
      var text = encodeURIComponent(message || "Hello Go Dental. I'd like to book a FREE consultation.");
      return "https://wa.me/" + WA_NUMBER + "?text=" + text;
    },
    waNumber: WA_NUMBER,
  };

  /* ---- Ripple effect on .btn ---- */
  function addRipple(btn, e) {
    var circle = document.createElement("span");
    var rect = btn.getBoundingClientRect();
    var size = Math.max(rect.width, rect.height);
    var x = (e.clientX || rect.left + rect.width / 2) - rect.left - size / 2;
    var y = (e.clientY || rect.top + rect.height / 2) - rect.top - size / 2;
    circle.className = "ripple";
    circle.style.width = circle.style.height = size + "px";
    circle.style.left = x + "px";
    circle.style.top = y + "px";
    btn.appendChild(circle);
    setTimeout(function () { circle.remove(); }, 650);
  }
  document.addEventListener("click", function (e) {
    var btn = e.target.closest(".btn");
    if (btn) addRipple(btn, e);
  });

  /* ---- WhatsApp links: wire any element with data-wa attribute ---- */
  function wireWhatsAppLinks() {
    var nodes = document.querySelectorAll("[data-wa]");
    nodes.forEach(function (el) {
      var msg = el.getAttribute("data-wa") || "Hello Go Dental. I'd like to book a FREE consultation.";
      el.setAttribute("href", window.GoDental.wa(msg));
      el.setAttribute("target", "_blank");
      el.setAttribute("rel", "noopener");
    });
  }

  /* ---- Navbar scroll state + mobile menu ---- */
  var nav = document.querySelector(".nav");
  function onScroll() {
    if (!nav) return;
    if (window.scrollY > 24) nav.classList.add("is-scrolled");
    else nav.classList.remove("is-scrolled");
  }
  window.addEventListener("scroll", onScroll, { passive: true });
  onScroll();

  var toggle = document.querySelector(".nav__toggle");
  function setMenu(open) {
    document.body.classList.toggle("menu-open", open);
    var btn = document.querySelector(".nav__toggle");
    if (btn) btn.setAttribute("aria-expanded", open ? "true" : "false");
  }
  if (toggle) {
    toggle.setAttribute("aria-label", "Open menu");
    toggle.setAttribute("aria-expanded", "false");
    toggle.addEventListener("click", function () {
      setMenu(!document.body.classList.contains("menu-open"));
    });
  }
  document.querySelectorAll(".mobile-menu a").forEach(function (a) {
    a.addEventListener("click", function () { setMenu(false); });
  });
  document.addEventListener("keydown", function (e) {
    if (e.key === "Escape") setMenu(false);
  });

  /* ---- Active nav link based on current page ---- */
  (function setActiveNav() {
    var path = location.pathname.split("/").pop() || "index.html";
    document.querySelectorAll(".nav__links a, .mobile-menu a").forEach(function (a) {
      var href = a.getAttribute("href");
      if (href === path || (path === "index.html" && href === "index.html")) {
        a.classList.add("is-active");
        a.setAttribute("aria-current", "page");
      }
    });
  })();

  /* ---- Scroll reveal via IntersectionObserver ---- */
  function setupReveal() {
    var els = document.querySelectorAll(".reveal");
    if (!("IntersectionObserver" in window) || !els.length) {
      els.forEach(function (el) { el.classList.add("in"); });
      return;
    }
    var io = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add("in");
          io.unobserve(entry.target);
        }
      });
    }, { threshold: 0.12, rootMargin: "0px 0px -8% 0px" });
    els.forEach(function (el) { io.observe(el); });
  }

  /* ---- Animated counters ---- */
  function setupCounters() {
    var nums = document.querySelectorAll("[data-count]");
    if (!nums.length) return;
    var run = function (el) {
      var target = parseFloat(el.getAttribute("data-count"));
      var suffix = el.getAttribute("data-suffix") || "";
      var dur = 1600, start = null;
      var isFloat = target % 1 !== 0;
      function tick(ts) {
        if (!start) start = ts;
        var p = Math.min((ts - start) / dur, 1);
        var eased = 1 - Math.pow(1 - p, 3);
        var val = target * eased;
        el.textContent = (isFloat ? val.toFixed(1) : Math.floor(val).toLocaleString()) + suffix;
        if (p < 1) requestAnimationFrame(tick);
        else el.textContent = (isFloat ? target.toFixed(1) : target.toLocaleString()) + suffix;
      }
      requestAnimationFrame(tick);
    };
    if (!("IntersectionObserver" in window)) { nums.forEach(run); return; }
    var io = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) { run(entry.target); io.unobserve(entry.target); }
      });
    }, { threshold: 0.4 });
    nums.forEach(function (n) { io.observe(n); });
  }

  /* ---- FAQ accordion ---- */
  function setupFAQ() {
    var items = document.querySelectorAll(".faq-item");
    items.forEach(function (item) {
      var q = item.querySelector(".faq-q");
      var a = item.querySelector(".faq-a");
      if (!q || !a) return;
      q.setAttribute("aria-expanded", "false");
      q.addEventListener("click", function () {
        var open = item.classList.contains("is-open");
        // close siblings within same accordion group
        var group = item.closest("[data-accordion]");
        if (group) {
          group.querySelectorAll(".faq-item.is-open").forEach(function (other) {
            if (other !== item) {
              other.classList.remove("is-open");
              other.querySelector(".faq-a").style.maxHeight = null;
              other.querySelector(".faq-q").setAttribute("aria-expanded", "false");
            }
          });
        }
        item.classList.toggle("is-open", !open);
        q.setAttribute("aria-expanded", open ? "false" : "true");
        a.style.maxHeight = open ? null : (a.scrollHeight + 12) + "px";
      });
    });
  }

  /* ---- Contact form (graceful, no backend) ---- */
  function setupForm() {
    var form = document.querySelector("[data-contact-form]");
    if (!form) return;
    var success = form.querySelector(".form-success");
    form.addEventListener("submit", function (e) {
      e.preventDefault();
      var name = (form.querySelector("[name=name]") || {}).value || "there";
      var service = (form.querySelector("[name=service]") || {}).value || "";
      var msg = "Hello Go Dental. I'd like to book an appointment.";
      if (name) msg = "Hello Go Dental, this is " + name + ". I'd like to book an appointment.";
      if (service) msg += " I'm interested in: " + service + ".";
      // open WhatsApp prefilled
      window.open(window.GoDental.wa(msg), "_blank", "noopener");
      if (success) {
        success.classList.add("show");
        success.setAttribute("role", "status");
      }
      form.reset();
    });
  }

  /* ---- Footer year ---- */
  function setYear() {
    document.querySelectorAll("[data-year]").forEach(function (el) {
      el.textContent = new Date().getFullYear();
    });
  }

  /* ---- Init ---- */
  function init() {
    wireWhatsAppLinks();
    setupReveal();
    setupCounters();
    setupFAQ();
    setupForm();
    setYear();
  }
  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", init);
  } else {
    init();
  }
})();
