<script lang="ts">
  import { Section, Register } from '$lib/components';
  import { ExampleDiv, SectionHeader, SectionBlock, MetaTag } from '../../utils';
  import { Button, Checkbox, Label, Input } from 'flowbite-svelte';
  const breadcrumb_title = 'Register Forms';
  const title = 'Register';
  const dir = 'marketing';
  const description =
    'Use a collection of register pages to let your users create an account on your website based on multiple layouts, social media authentication, and more.';
</script>

<MetaTag {breadcrumb_title} {title} {dir} {description} />

<Section name="register">
  <Register href="/">
    <div class="p-6 space-y-6 lg:py-6 md:space-y-6 sm:p-8">
      <form class="flex flex-col space-y-6" action="/">
        <h3 class="text-xl font-medium text-gray-900 dark:text-white p-0">Create and account</h3>
        <Label class="space-y-2">
          <span>Your name</span>
          <Input type="text" name="name" placeholder="홍길동" required />
        </Label>
        <Label class="space-y-2">
          <span>Your email</span>
          <Input type="email" name="email" placeholder="name@company.com" required />
        </Label>
        <Label class="space-y-2">
          <span>Your password</span>
          <Input type="password" name="password" placeholder="•••••" required />
        </Label>
        <Label class="space-y-2">
          <span>Confirm password</span>
          <Input type="password" name="confirm-password" placeholder="•••••" required />
        </Label>
        <div class="flex items-start">
          <Checkbox
            >I accept the <a
              class="font-medium text-primary-600 hover:underline dark:text-primary-500"
              href="/"
            >
              Terms and Conditions</a
            ></Checkbox
          >
        </div>
        <Button type="submit" class="w-full1">Create an account</Button>
        <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
          Already have an account? <a
            href="/"
            class="font-medium text-primary-600 hover:underline dark:text-primary-500">Login here</a
          >
        </div>
      </form>
    </div>
  </Register>
</Section>
