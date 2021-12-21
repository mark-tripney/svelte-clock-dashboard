<script>
  // Get local time (24hr, sans seconds) plus timezone abbreviation
  const localTimeArray = new Date()
    .toLocaleTimeString([], {
      hour: '2-digit',
      minute: '2-digit',
      timeZoneName: 'short',
    })
    .split(' ');
  // Get component parts of localTimeArray
  const localTime = localTimeArray[0];
  const timezone = localTimeArray[1];
</script>

<div class="clock">
  <p class="time">{localTime}</p>
  <p class="timezone">{timezone}</p>
</div>

<style>
  .clock {
    display: flex;
    align-items: baseline;
    gap: 1rem;
  }
  .time {
    font-size: 6.25rem;
    font-weight: 700;
    letter-spacing: -2.5px;
  }
  .timezone {
    font-size: 0.9375rem;
  }
</style>
