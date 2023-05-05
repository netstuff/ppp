<template>
  <Dialog :open="isOpen" @close="setIsOpen" class="relative z-50">
    <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" aria-hidden="true" />
    <div class="fixed inset-0 flex items-center justify-center p-4">
      <div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
        <div class="relative transform overflow-hidden rounded-lg bg-white px-4 pb-4 pt-5 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-sm sm:p-6">
          <DialogPanel class="w-full max-w-sm rounded bg-white">
            <DialogTitle class="text-base font-semibold leading-6 text-gray-900">Тупой диалог</DialogTitle>
            <DialogDescription class="mt-2">
              <p class="text-sm text-gray-500">Привет! Я — тупое диалоговое окно и не умею ничего :(</p>
              <p class="text-sm text-gray-500">Если бы нашелся чоткэ-посан, который напрограммит мне вской логики, я было бы не такое тупое...</p>
            </DialogDescription>
            <button
              @click="setIsOpen(false)"
              class="inline-flex w-full justify-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >Убей меня</button>
          </DialogPanel>
        </div>
      </div>
    </div>
  </Dialog>
</template>

<script setup>
  import { ref } from 'vue'
  import {
    Dialog,
    DialogPanel,
    DialogTitle,
    DialogDescription,
  } from '@headlessui/vue'

  const isOpen = ref(true)

  function setIsOpen(value) {
    isOpen.value = value
  }
</script>