---
title: "SLURM*O*MATIC"
keywords: homepage
home: true
hide_sidebar: true
toc: false
permalink: index.html
layout: page
---
  <div class="slurm-page">
      <h2>Carina</h2>


Welcome to the Slurm-O-Matic, a tool to help you write your slurm sbatch scripts. When you like what you see, click the Copy to Clipboard button and paste the text into your text editor.

  ### Available Queues
  <table class="table table-bordered table-condensed" id="resource-table">
    <thead>
      <tr>
        <th>Queue Name</th>
        <th>CPUs</th>
        <th>Memory</th>
        <th>Nodes</th>
        <th>GPUs</th>
      </tr>
    </thead>
    <tbody></tbody>
  </table>
  <div class="row slurm-form">
  <div class="col-sm-6">
  <fieldset>
    <h3>Choose a Queue</h3>
    <div class="form-group">
      <div id="choose-queue"></div>
    </div>
    <div class="form-group gpu-group">
      <label>Specify GPUs</label>
      <div id="choose-gpu"></div>
    </div>
  </fieldset>
  <h3>Allocate Resources</h3>
  <fieldset>
  <div class="form-group">
    <label><span class="cpu-gpu">CPU</span> (cores)</label>
    <select id="cpu" class="form-control">
      <option selected value="<>">---</option>
    </select>
  </div>
  <div class="form-group">
    <label>Memory (GB)</label>
    <select id="memory" class="form-control">
      <option selected value="<>">---</option>
    </select>
  </div>
  <div class="form-group">
    <label>Nodes</label>
    <select id="nodes" class="form-control">
      <option selected value="<>">---</option>
    </select>
  </div>
  <div class="form-group gpu-group">
    <label>GPUs</label>
    <select id="gpu" class="form-control">
      <option selected value="<>">---</option>
    </select>
  </div>
  <div class="form-group" id="runtime">
    <label>Running Time</label>
    <div class="form-row form-inline runtime-form">
      <div class="col-auto">
        <label class="sr-only" for="runtimeHr">Hours</label>
        <select id="runtimeHr" class="form-control fancy-dropdown"></select>
        <small class="form-text text-muted text-center">Hours</small>
      </div>
      <div class="col-auto">
        <span class="separator">:</span>
      </div>
      <div class="col-auto"><label class="sr-only" for="runtimeMin">Minutes</label>
        <select id="runtimeMin" class="form-control fancy-dropdown"></select>
        <small class="form-text text-muted text-center">Minutes</small>
      </div>
    </div>
    </fieldset>
    <fieldset>
            <h3>Modules/Commands</h3>
            <div class="form-group">
              <label>Modules to load</label>
              <select id='modules' class="fancy-dropdown" multiple="multiple" style="width:100%">
              </select>
            </div>
            <div class="form-group">
              <label>Commands to run</label>
              <textarea class="form-control autoresizing" id="commands" rows="2" placeholder="srun hostname"></textarea>
            </div>
          </fieldset>
          <fieldset>
            <h3>Recommended Settings</h3>
            <div class="form-group">
              <label>SUnetID</label>
              <input type="text" class="form-control" name="sunetid" id="sunetid" placeholder="This will enable email notifications" maxlength="8" />
            </div>
            <div class="form-group">
              <label>Job Name</label>
              <input type="text" class="form-control" name="jobname" id="jobname" placeholder="Name this job" />
            </div>
            <div class="form-group">
              <label>Working directory</label>
              <input type="text" class="form-control" name="workingdir" id="workingdir" placeholder="/full/path/to/directory/" />
            </div>
          </fieldset>
        </div>
      </div>
      <div class="col-sm-6">
        <div class="form-horizontal">
          <fieldset>
            <h3>SLURM Script <a class="btn btn-outline-info float-right" id="copyBtn"><i class="fa-regular fa-clipboard"></i><span> Copy to Clipboard</span></a></h3>
            <textarea id="slurm" class="form-control form-control-plaintext" rows="16" readonly></textarea>
          </fieldset>
          <fieldset>
            <h3>Optional Settings</h3>
            <div class="form-group">
              <label>Std out file name</label>
              <input type="text" class="form-control" name="stdout" id="stdout" placeholder="Change output file name" />
            </div>
            <div class="form-group">
              <label>Std err file name</label>
              <input type="text" class="form-control" name="stderr" id="stderr" placeholder="Change error file name" />
            </div>
          </fieldset>
        </div>
      </div>
    </div>