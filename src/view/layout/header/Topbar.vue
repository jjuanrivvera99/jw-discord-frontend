<template>
  <div class="topbar">
    <!--begin: Notifications -->
    <b-dropdown
      size="sm"
      variant="link"
      toggle-class="topbar-item text-decoration-none"
      no-caret
      right
      no-flip
    >
      <template v-slot:button-content>
        <div
          class="btn btn-icon btn-clean btn-dropdown btn-lg mr-1 pulse pulse-primary"
        >
          <span class="svg-icon svg-icon-xl">
            <inline-svg src="media/svg/icons/Code/Compiling.svg" />
          </span>
          <span class="pulse-ring"></span>
        </div>
      </template>
      <b-dropdown-text tag="div" class="min-w-md-350px">
        <form>
          <KTDropdownNotification></KTDropdownNotification>
        </form>
      </b-dropdown-text>
    </b-dropdown>
    <!--end: Notifications -->

    <!--begin::User-->
    <KTQuickUser></KTQuickUser>
    <!--end::User-->
  </div>
</template>

<style lang="scss">
.topbar {
  .dropdown-toggle {
    padding: 0;
    &:hover {
      text-decoration: none;
    }

    &.dropdown-toggle-no-caret {
      &:after {
        content: none;
      }
    }
  }

  .dropdown-menu {
    margin: 0;
    padding: 0;
    outline: none;
    .b-dropdown-text {
      padding: 0;
    }
  }
}
</style>

<script>
import KTQuickUser from "@/view/layout/extras/offcanvas/QuickUser";
import KTDropdownNotification from "@/view/layout/extras/dropdown/DropdownNotification.vue";

export default {
  name: "Topbar",
  components: {
    KTQuickUser,
    KTDropdownNotification
  }
};
</script>
