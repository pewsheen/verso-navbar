<script>
  import { Button, Input } from 'flowbite-svelte';
  import PrevPageIcon from '@images/arrow-left.png';
  import NextPageIcon from '@images/arrow-right.png';
  import RefreshIcon from '@images/refresh.png';
  import CloseIcon from '@images/close.png';
  import MaximizeIcon from '@images/maximize.png';
  import MinimizeIcon from '@images/minimize.png';

  function onClickPrev() {
    console.log('click prev');
    window.prompt('PREV');
  }
  function onClickForward() {
    console.log('click forward');
    window.prompt('FORWARD');
  }
  function onClickRefresh() {
    console.log('click refresh');
    window.prompt('REFRESH');
  }
  function onClickClose() {
    console.log('close');
    window.close();
  }
  function onClickMinimize() {
    console.log('minimize');
    window.prompt('MINIMIZE');
  }
  function onClickMaximize() {
    console.log('maximize');
    window.prompt('MAXIMIZE');
  }
</script>

<div class="navbar box-border w-full">
  <div class="inline-block w-full">
    <div class="inline-block w-1/4">
      <Button
        on:click={onClickPrev}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="previous page" src={PrevPageIcon} /></Button
      >
      <Button
        on:click={onClickForward}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="forward page" src={NextPageIcon} /></Button
      >
      <Button
        on:click={onClickRefresh}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="refresh page" src={RefreshIcon} /></Button
      >
    </div>
    <div class="inline-block w-1/2">
      <Input
        class="h-7"
        type="text"
        placeholder="Search or enter website name"
      />
    </div>
    <div class="float-right inline-block">
      <Button
        on:click={onClickMinimize}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="minimize window" src={MinimizeIcon} /></Button
      >
      <Button
        on:click={onClickMaximize}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="maximize window" src={MaximizeIcon} /></Button
      >
      <Button
        on:click={onClickClose}
        class="btn bg-slate-50 hover:bg-slate-100 active:bg-slate-200 h-7 w-7 !p-2"
        ><img alt="close window" src={CloseIcon} /></Button
      >
    </div>
  </div>
</div>

<style lang="scss">
  :global(.btn) {
    background-color: #fafafa;
    &:hover {
      background-color: #f0f0f0;
    }
    &:active {
      background-color: #cdcdcd;
    }
  }
  .navbar {
    background-color: #fafafa;
    height: 38px;
    padding-top: 6px;
    padding-left: 80px;
    padding-right: 10px;
  }
</style>
