---
title: "SLURM*O*MATIC Cheat Sheet"
cheat: true
hide_sidebar: true
toc: false
permalink: cheatsheet.html
layout: page
---
<p>Welcome to the Slurm-O-Matic Cheat Sheet, a tool to help you interact with Slurm. </p>
<p>This tool will use your inputs to generate commands. When you find what you need, click the Copy to Clipboard button and paste into your terminal.</p>
  <fieldset class="">
    <div class="form-group">
      <div class="form-row align-items-top">
        <div class="col-auto">
          <label class="sr-only">SUnetID</label>
          <input type="text" class="form-control" name="sunetid" id="sunetid" placeholder="SUnetID" maxlength="8" />
        </div>
        <div class="col-auto">
          <label class="sr-only">JobID Number</label>
          <input type="text" class="form-control" name="jobid" id="jobid" placeholder="JobID" />
        </div>
        <div class="col-auto">
          <a class="btn btn-outline-info generate" id="generateBtn" title="Generate Commands"><i class="fa-solid fa-wand-magic-sparkles"></i> Generate!</a>
        </div>
      </div>
    </div>
    <small class="form-text text-muted">If you don't know your JobID, use the first command below to see your open jobs.</small>
  </fieldset>
  <fieldset class="tips">
    <h4>Check the status of your job and follow its evolution</h4>
    <div class="form-group">
      <div class="form-row align-items-center">
        <div class="col-auto tip-input">
          <input type="text" id="slurmStatus" class="form-control terminal" readonly placeholder="Add your SUnetID to see this one" />
        </div>
        <div class="col-auto tip-btn">
          <a class="btn btn-outline-info copy" title="Copy to Clipboard" data-target="slurmStatus"><i class="fa-regular fa-clipboard"></i></a>
        </div>
      </div>
    </div>
    <div class="form-group">
      <h4>Check the GPU Utilization of your job</h3>
      <div class="form-row align-items-center">
        <div class="col-auto tip-input">
          <input type="text" id="slurmGpuUtil" class="form-control terminal" readonly placeholder="Add your JobID to see this one" />
        </div>
        <div class="col-auto tip-btn">
          <a class="btn btn-outline-info copy" title="Copy to Clipboard" data-target="slurmGpuUtil"><i class="fa-regular fa-clipboard"></i></a>
        </div>
      </div>
    </div>
    <div class="form-group">
      <h4>Cancel your job</h3>
      <div class="form-row align-items-center">
        <div class="col-auto tip-input">
          <input type="text" id="slurmCancel" class="form-control terminal" readonly placeholder="Add your JobID to see this one" />
        </div>
        <div class="col-auto tip-btn">
          <a class="btn btn-outline-info copy"  title="Copy to Clipboard" data-target="slurmCancel"><i class="fa-regular fa-clipboard"></i></a>
        </div>
      </div>
    </div>          
    <div class="form-group">
      <h4>See the resources you have used across Slurm for a specific time period.</h4>
<label for="from">From</label>
<input type="text" id="from" name="from" class="dp-from">
<label for="to">to</label>
<input type="text" id="to" name="to">
      <div class="form-row align-items-center">
        <div class="col-auto tip-input">
          <input type="text" id="slurmHistory" class="form-control terminal" readonly placeholder="Add your SUnetID & choose dates to see this one" />
        </div>
        <div class="col-auto tip-btn">
          <a class="btn btn-outline-info copy" title="Copy to Clipboard" data-target="slurmHistory"><i class="fa-regular fa-clipboard"></i></a>
        </div>
      </div>
    </div>
  </fieldset>
</div>
</div>


</body>

</html>