---
title: About continuous deployment
intro: 'You can create custom continuous deployment (CD) workflows directly in your {% data variables.product.prodname_dotcom %} repository with {% data variables.product.prodname_actions %}.'
product: '{% data reusables.gated-features.actions %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
type: overview
topics:
  - CD
shortTitle: Continuous deployment
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}

## About continuous deployment

_Continuous deployment_ (CD) is the practice of using automation to publish and deploy software updates. As part of the typical CD process, the code is automatically built and tested before deployment.

Continuous deployment is often coupled with continuous integration. For more information about continuous integration, see "[About continuous integration](/actions/guides/about-continuous-integration)".

## About continuous deployment using {% data variables.product.prodname_actions %}

You can set up a {% data variables.product.prodname_actions %} workflow to deploy your software product. To verify that your product works as expected, your workflow can build the code in your repository and run your tests before deploying.

You can configure your CD workflow to run when a {% data variables.product.product_name %} event occurs (for example, when new code is pushed to the default branch of your repository), on a set schedule, manually, or when an external event occurs using the repository dispatch webhook. For more information about when your workflow can run, see "[Events that trigger workflows](/actions/reference/events-that-trigger-workflows)."

{% data variables.product.prodname_actions %} provides features that give you more control over deployments. For example, you can use environments to require approval for a job to proceed, restrict which branches can trigger a workflow, or limit access to secrets. You can use concurrency to limit your CD pipeline to a maximum of one in-progress deployment and one pending deployment. For more information about these features, see "[Deploying with GitHub Actions](/actions/deployment/deploying-with-github-actions)" and "[Using environments for deployment](/actions/deployment/using-environments-for-deployment)."

## Workflow templates and third party actions

{% data reusables.actions.cd-templates-actions %}

## 参考リンク

- [Deploying with GitHub Actions](/actions/deployment/deploying-with-github-actions)
- [Using environments for deployment](/actions/deployment/using-environments-for-deployment){% ifversion fpt %}
- 「[{% data variables.product.prodname_actions %} の支払いを管理する](/billing/managing-billing-for-github-actions)」
{% endif %}
