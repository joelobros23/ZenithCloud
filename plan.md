# Project Plan: ZenithCloud

**Description:** A simple web hosting platform built on Ruby on Rails, offering basic domain management and user authentication.


## Development Goals

- [ ] Configure tailwindcss-rails by running `rails tailwindcss:install`.
- [ ] Customize the application layout (app/views/layouts/application.html.erb) to include Tailwind CSS classes for a basic navigation and header.
- [ ] Add model validations to the Domain model (app/models/domain.rb) to ensure name is present, unique, and matches a valid domain format, and plan is one of the available plans ('basic', 'pro', 'enterprise').
- [ ] Modify the Domains controller (app/controllers/domains_controller.rb) to ensure that only the logged-in user can create, edit, update, or delete their own domains. Use `before_action :authenticate_user!` and scope domain queries to `current_user.domains`.
- [ ] Implement the association between User and Domain models (app/models/user.rb: `has_many :domains`, app/models/domain.rb: `belongs_to :user`). Set the user_id when creating a new Domain.
- [ ] Modify the domain scaffold views (app/views/domains/*) to use Tailwind CSS for styling and display domain information in a user-friendly format. Consider using Tailwind UI components if available.
- [ ] Create a dashboard view (app/views/home/index.html.erb, controller: app/controllers/home_controller.rb) that displays a list of the current user's domains, along with their status and plan, and provides links to manage each domain.
- [ ] Implement domain status updates (e.g., 'active', 'pending', 'suspended'). Provide functionality (button in the view, action in controller) for admins to manually change a domain's status.
- [ ] Implement a basic plan selection during domain creation.
- [ ] Add seeds.rb file to create admin user and some sample domains for development
