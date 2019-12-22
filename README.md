# README

rails generate resource Users first_name last_name username email
rails generate resource Registration user:references conference:references
rails generate resource Scheduling user:references session:references
rails generate model Conferences name starts_on:date ends_on:date original_conference:references
rails generate model OriginalConference name city state starts_on:date ends_on:date
rails generate model Tracks name original_conference:references
rails generate model OriginalSession original_conference:references name description:text location
                starts_at:datetime ends_at:datetime track:references
rails generate model Sessions original_session:references
rails generate model Presenters first_name last_name
rails generate model Presentations original_session:references presenter:references
