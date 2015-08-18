 Infinite.prototype.setupHandler = function() {
    this.options.handler = $.proxy(function() {

      // The handler seemed to fire whenever it felt like it...
      // The onBeforePageLoad call would always happen whether there was any new content or not.
      // I added this check to see if there was actually any more content before doing anything.
      if (!this.$more) { return; }

      this.options.onBeforePageLoad();
      this.destroy();
      this.$container.addClass(this.options.loadingClass);

      $.get($(this.options.more).attr('href'), $.proxy(function(data) {
        var $data = $($.parseHTML(data, document, true));

        var $newMore = $data.find(this.options.more);

        this.$more.remove(); // always remove the existing more link before appending the new content
        this.$more = ($newMore.length) ? $newMore : null; // explicitly set the $more property to null if $newMore has a no length

        var $items = $data.find(this.options.items);
        if (!$items.length) {
          $items = $data.filter(this.options.items);
        }

        this.$container.append($items);
        this.$container.removeClass(this.options.loadingClass);

        // Replaced the original $newMore checks with this more succinct version
        if (this.$more) {
          this.waypoint = new Waypoint(this.options);
        }

        this.options.onAfterPageLoad();
      }, this))
    }, this)
  }