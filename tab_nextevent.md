---

layout: col-sidebar
title: NextEvent
displaytext: Next Event
tab: true
tags: frankfurt
level: 1

---

## Next Events
OWASP Frankfurt Chapter upcoming events can be found on Meetup: [OWASP Frankfurt Chapter Meetup](https://www.meetup.com/OWASP-Frankfurt/)

{% include chapter_events.html group=page.meetup-group %}

<script type='text/javascript'>
  $(function(){
    $(".timeclass").hover(function() {
      utc_str = $(this).text();
      ndx = utc_str.indexOf(':');
      st_hour_str = utc_str.substring(0, ndx);
      st_min_str = utc_str.substring(ndx + 1, ndx + 3);
      utc_dt = luxon.DateTime.utc(2020, 06, 06, parseInt(st_hour_str), parseInt(st_min_str), 0);
      start_dt = utc_dt.setZone(luxon.DateTime.local().zoneName);

      ndx = utc_str.lastIndexOf(':');
      end_hour_str = utc_str.substring(ndx - 2, ndx - 1);
      end_min_str = utc_str.substring(ndx + 1, ndx + 3);
      utc_dt = luxon.DateTime.utc(2020, 06, 06, parseInt(end_hour_str), parseInt(end_min_str), 0);
      end_dt = utc_dt.setZone(luxon.DateTime.local().zoneName);
      popstr = start_dt.toLocaleString(luxon.DateTime.TIME_WITH_SECONDS) + ' to ' + end_dt.toLocaleString(luxon.DateTime.TIME_WITH_SHORT_OFFSET);
      $(this).prop('title', popstr);
    });
  });
</script>

Please follow OWASP Frankfurt on [Meetup](https://www.meetup.com/OWASP-Frankfurt/) or join the OWASP Germany [Mailing List](https://groups.google.com/a/owasp.org/forum/#!forum/germany-chapter) to be notified as soon as the next event date & location is announced!


## Call for Venues
We are looking for upcoming venues to host our OWASP Frankfurt Chapter, preferably in a central location in Frankfurt City which can host around 40-70 attendees.

## Call for Speakers
**We are always looking for presentations for the OWASP Frankfurt Chapter Events!** If you'd like to give a presentation, conduct a training workshop or volunteer for us, contact us the OWASP Frankfurt Chapter organisation. Or easily submit a CFP via Papercall.io: https://www.papercall.io/owasp-chapter-frankfurt