---
title: 5 tips for better Pull Requests
template: post
subtitle: 5 tips for better Pull Requests
excerpt: 5 tips for better Pull Requests
date: 2022-04-20T01:06:16.962Z
image: /blog/pull-request.jpg
thumb_image: /blog/pull-request.jpg
image_position: right
author: src/data/authors/im.yaml
categories:
  - src/data/categories/git.yaml
tags:
  - src/data/tags/links.yaml
show_author_bio: true
related_posts:
  - src/pages/blog/webdev-setup.md
cmseditable: true
---

<!--StartFragment-->

# 5 tips for better Pull Requests

Writing good code is only part of the job. Here are 5 tips to improve your pull requests and help people review them:

1. Small pull requests The pull requests that get reviewed more thoroughly and confidently and are most often prioritized by developers with limited time are the smallest ones. Make sure you separate concerns into different pull requests (e.g. refactoring and feature implementation), while also keeping commits atomic and well-documented to make the changes easier to understand and review.
2. Good descriptions Always take the time to describe your code and any related tasks in your pull request. Explain the feature you are implementing or the bug you are fixing and provide images and steps to reproduce, if applicable. Note decisions made during implementation, your approach, as well as any limitations, findings and points of interest that might help others better understand your code.
3. Rebase onto master Always rebase your pull requests onto the `master` branch of the repository. This way you can always test your code against the latest changes and resolve merge conflicts, minimizing issues that might arise later on. Apart from that, reviewers will not have to deal with missing features or bug fixes that might have been deployed already, which can considerably speed up review times.
4. Review it yourself Before submitting your pull request for review, always take the time to review it yourself. That way you can handle some low-hanging fruits (typos, easy optimizations, leftover code etc.) and check things you would in other people’s pull requests. Self-reviewing has the added benefit of allowing you to reason about decisions and realize which ones might need clarification.
5. Respond to reviews Set some time aside to respond to reviews after submitting your pull request. Handle anything you can as soon as possible and start discussion whenever necessary to arrive to a solution. Use `--fixup` for changes suggested in review comments or add new commits to help reviewers parse new changes more easily. Finally, assume good intentions, be polite and thank your peers.

<!--EndFragment-->
