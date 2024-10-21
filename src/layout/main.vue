<template>
  <!-- 定义一个全屏高度和全屏宽度的布局容器，使用flex布局 -->
  <div class="full-screen-container h-screen flex flex-col">
    <!-- 主布局 -->
    <t-layout>
      <!-- 头部区域 -->
      <t-header>
        <!-- 顶部菜单栏，设置初始选中项和高度 -->
        <t-head-menu value="item1" height="120px">
          <!-- 自定义logo区域 -->
          <template #logo>
            <img width="136" class="logo" src="https://www.tencent.com/img/index/menu_logo_hover.png" alt="logo" />
          </template>
          <!-- 菜单项 -->
          <t-menu-item value="item1"> 已选内容 </t-menu-item>
          <t-menu-item value="item2"> 菜单内容一 </t-menu-item>
          <t-menu-item value="item3"> 菜单内容二 </t-menu-item>
          <t-menu-item value="item4" :disabled="true"> 菜单内容三 </t-menu-item>
          <!-- 自定义操作区域 -->
          <template #operations>
            <a href="javascript:;"><t-icon class="t-menu__operations-icon" name="search" /></a>
            <a href="javascript:;"><t-icon class="t-menu__operations-icon" name="notification-filled" /></a>
            <a href="javascript:;"><t-icon class="t-menu__operations-icon" name="home" /></a>
          </template>
        </t-head-menu>
      </t-header>
      <!-- 中间布局，使用flex布局并设置溢出隐藏 -->
      <t-layout class="flex-grow  overflow-hidden">
        <!-- 侧边栏，设置顶部边框 -->
        <t-aside style="border-top: 1px solid var(--component-border)">
          <!-- 侧边菜单，设置主题、选中项、样式和高度 -->
          <t-menu theme="light" value="dashboard" style="margin-right: 50px" height="550px">
            <!-- 菜单项，包含图标和文本 -->
            <t-menu-item value="dashboard">
              <template #icon>
                <t-icon name="dashboard" />
              </template>
              仪表盘
            </t-menu-item>
            <!-- 其他菜单项类似，不再一一注释 -->
            <t-menu-item value="resource">
              <template #icon>
                <t-icon name="server" />
              </template>
              资源列表
            </t-menu-item>
            <t-menu-item value="root">
              <template #icon>
                <t-icon name="root-list" />
              </template>
              根目录
            </t-menu-item>
            <t-menu-item value="control-platform">
              <template #icon>
                <t-icon name="control-platform" />
              </template>
              调度平台
            </t-menu-item>
            <t-menu-item value="precise-monitor">
              <template #icon>
                <t-icon name="precise-monitor" />
              </template>
              调度平台
            </t-menu-item>
            <t-menu-item value="mail">
              <template #icon>
                <t-icon name="mail" />
              </template>
              消息区
            </t-menu-item>
            <t-menu-item value="user-circle">
              <template #icon>
                <t-icon name="user-circle" />
              </template>
              个人中心
            </t-menu-item>
            <t-menu-item value="play-circle">
              <template #icon>
                <t-icon name="play-circle" />
              </template>
              视频区
            </t-menu-item>
            <t-menu-item value="edit1">
              <template #icon>
                <t-icon name="edit-1" />
              </template>
              资源编辑
            </t-menu-item>
          </t-menu>
        </t-aside>
        <!-- 内容和底部布局 -->
        <t-layout>
          <t-content>
            <div>Content</div>
          </t-content>
          <t-footer>Copyright @ 2019-{{ new Date().getFullYear() }} Tencent. All Rights Reserved</t-footer>
        </t-layout>
      </t-layout>
    </t-layout>
  </div>
</template>