<script lang="ts">
    import logo from "../assets/images/logo-universal.png";
    import { Dropdown, DropdownItem, DropdownDivider, Navbar } from "flowbite-svelte";
    import { CloseSolid, MinusSolid, ExpandSolid } from "flowbite-svelte-icons";
    
    export let title = 'Tricycle'
</script>

<Navbar
    navClass="py-1"
    navDivClass="flex flex-row md:mt-0 md:text-sm md:font-medium justify-between"
    fluid={true}>
    <span class="mx-1 flex flex-row space-x-4">
        <img src={logo} class="h-6" alt="Tricycle Logo" />

        <ul class="flex md:flex-row space-x-4">
            <li>
                <button
                    id="fileMenu"
                    class="hover:bg-gray-100 dark:hover:bg-gray-600 rounded-md cursor-default select-none"
                    unselectable="on">
                    File
                </button>
                <Dropdown
                    placement="bottom-start"
                    offset={0}
                    border={true}
                    class="z-20">
                    <DropdownItem defaultClass="py-1 px-2">New</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Open</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Save</DropdownItem>
                    <DropdownDivider />
                    <DropdownItem defaultClass="py-1 px-2">Settings</DropdownItem>
                    <DropdownDivider />
                    <DropdownItem defaultClass="py-1 px-2">Exit</DropdownItem>
                </Dropdown>
            </li>
            <li>
                <button
                    id="editMenu"
                    class="hover:bg-gray-100 dark:hover:bg-gray-600 px-1 rounded-md cursor-default select-none"
                    unselectable="on">
                    Edit
                </button>
                <Dropdown
                    placement="bottom-start"
                    offset={0}
                    border={true}
                    class="z-20">
                    <DropdownItem defaultClass="py-1 px-2">Undo</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Redo</DropdownItem>
                    <DropdownDivider />
                    <DropdownItem defaultClass="py-1 px-2">Cut</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Copy</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Paste</DropdownItem>
                    <DropdownDivider />
                    <DropdownItem defaultClass="py-1 px-2">Find</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Replace</DropdownItem>
                </Dropdown>
            </li>
            <li>
                <button
                    id="viewMenu"
                    class="hover:bg-gray-100 dark:hover:bg-gray-600 px-1 rounded-md cursor-default select-none"
                    unselectable="on">
                    View
                </button>
                <Dropdown
                    placement="bottom-start"
                    offset={0}
                    border={true}
                    class="z-20">
                    <DropdownItem defaultClass="py-1 px-2">Open Network Mointor Window</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Open Terminal Window</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Open Log Window</DropdownItem>
                    <DropdownDivider />
                    <DropdownItem defaultClass="py-1 px-2">Reset Layout</DropdownItem>
                </Dropdown>
            </li>
            <li>
                <button
                    id="helpMenu"
                    class="hover:bg-gray-100 dark:hover:bg-gray-600 px-1 rounded-md cursor-default select-none"
                    unselectable="on">
                    Help
                </button>
                <Dropdown
                    placement="bottom-start"
                    offset={0}
                    border={true}
                    class="z-20">
                    <DropdownItem defaultClass="py-1 px-2">Document</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Open Source License</DropdownItem>
                    <DropdownItem defaultClass="py-1 px-2">Report Issue</DropdownItem>
                </Dropdown>
            </li>
        </ul>
    </span>

    <p>{title}</p>

    <ul class="flex md:flex-row">
        <li>
            <button
                class="hover:bg-gray-200 dark:hover:bg-gray-600 px-2 py-1 cursor-default select-none" unselectable="on">
                <MinusSolid class="outline-none"/>
            </button>
        </li>
        <li>
            <button
                class="hover:bg-gray-200 dark:hover:bg-gray-600 px-2 py-1 cursor-default select-none" unselectable="on">
                <ExpandSolid class="outline-none"/>
            </button>
        </li>
        <li>
            <button
                class="hover:bg-red-600 hover:text-white px-2 py-1 cursor-default select-none" unselectable="on">
                <CloseSolid class="outline-none"/>
            </button>
        </li>
    </ul>
</Navbar>