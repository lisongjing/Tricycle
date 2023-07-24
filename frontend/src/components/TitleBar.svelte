<script lang="ts">
    import logo from "../assets/images/logo-universal.png";
    import { Dropdown, DropdownItem, DropdownDivider } from "flowbite-svelte";
</script>

<nav
    class="bg-gray-50 dark:bg-gray-700 text-gray-900 dark:text-white border-gray-300 dark:border-gray-700 divide-gray-300 dark:divide-gray-700 py-0"
>
    <div class="mx-auto flex flex-wrap justify-between items-center h-8">
        <ul
            class="flex flex-row md:flex-row md:space-x-4 md:mt-0 md:text-sm md:font-medium"
        >
            <li><img src={logo} class="h-6" alt="Tricycle Logo" /></li>
            <li id="file-menu">File</li>
            <li id="edit-menu">Edit</li>
            <li id="view-menu">View</li>
            <li id="help-menu">Help</li>

            <Dropdown triggeredBy="#file-menu" class="w-44 z-20">
                <DropdownItem>New</DropdownItem>
                <DropdownItem>Open</DropdownItem>
                <DropdownItem>Save</DropdownItem>
                <DropdownItem>Settings</DropdownItem>
                <DropdownDivider />
                <DropdownItem>Exit</DropdownItem>
            </Dropdown>
            <Dropdown triggeredBy="#edit-menu" class="w-44 z-20">
                <DropdownItem>Undo</DropdownItem>
                <DropdownItem>Redo</DropdownItem>
                <DropdownDivider />
                <DropdownItem>Cut</DropdownItem>
                <DropdownItem>Copy</DropdownItem>
                <DropdownItem>Paste</DropdownItem>
                <DropdownDivider />
                <DropdownItem>Find</DropdownItem>
                <DropdownItem>Replace</DropdownItem>
                <DropdownItem>Select All</DropdownItem>
            </Dropdown>
            <Dropdown triggeredBy="#view-menu" class="w-44 z-20">
                <DropdownItem>Network Mointor</DropdownItem>
                <DropdownItem>Terminal</DropdownItem>
                <DropdownItem>Log</DropdownItem>
                <DropdownItem>Plugins</DropdownItem>
                <DropdownDivider />
                <DropdownItem>Reset Layout</DropdownItem>
            </Dropdown>
            <Dropdown triggeredBy="#help-menu" class="w-44 z-20">
                <DropdownItem>Document</DropdownItem>
                <DropdownItem>License</DropdownItem>
                <DropdownItem>Report Issue</DropdownItem>
            </Dropdown>
        </ul>
    </div>
</nav>
