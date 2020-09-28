---
title: Habilitar pesquisa unificada entre o GitHub Enterprise Server e o GitHub.com
intro: 'Após habilitar o {{ site.data.variables.product.prodname_github_connect }}, você pode permitir a pesquisa no {{ site.data.variables.product.prodname_dotcom_the_website }} pela {{ site.data.variables.product.product_location_enterprise }}.'
redirect_from:
  - /enterprise/admin/guides/developer-workflow/enabling-unified-search-between-github-enterprise-and-github-com/
  - /enterprise/admin/guides/developer-workflow/enabling-unified-search-between-github-enterprise-server-and-github-com/
  - /enterprise/admin/developer-workflow/enabling-unified-search-between-github-enterprise-server-and-githubcom/
  - /enterprise/admin/installation/enabling-unified-search-between-github-enterprise-server-and-githubcom
permissions: 'Administradores de sites para {{ site.data.variables.product.prodname_ghe_server }} que também são proprietários de uma conta corporativa ou organização conectada do {{ site.data.variables.product.prodname_ghe_cloud }} podem ativar a pesquisa unificada entre {{ site.data.variables.product.prodname_ghe_server }} e {{ site.data.variables.product.prodname_dotcom_the_website }}.'
versions:
  enterprise-server: '*'
---

Quando você habilita a pesquisa unificada, os usuários podem ver resultados em conteúdos públicos e privados no {{ site.data.variables.product.prodname_dotcom_the_website }} quando pesquisam pela {{ site.data.variables.product.product_location_enterprise }}.

Os usuários não conseguirão pesquisar na {{ site.data.variables.product.product_location_enterprise }} pelo {{ site.data.variables.product.prodname_dotcom_the_website }}, mesmo se tiverem acesso aos dois ambientes. Eles só poderão pesquisar nos repositórios privados em que você habilitou a {{ site.data.variables.product.prodname_unified_search }} e não terão acesso às organizações conectadas do {{ site.data.variables.product.prodname_ghe_cloud }}. Para obter mais informações, consulte "[Sobre a pesquisa no {{ site.data.variables.product.prodname_dotcom }}](/articles/about-searching-on-github/#searching-across-github-enterprise-and-githubcom-simultaneously)" e "[Habilitar a pesquisa em repositórios privados do {{ site.data.variables.product.prodname_dotcom_the_website }} na conta do {{ site.data.variables.product.prodname_ghe_server }}](/articles/enabling-private-github-com-repository-search-in-your-github-enterprise-server-account)".

A pesquisa via APIs REST e GraphQL não inclui resultados do {{ site.data.variables.product.prodname_dotcom_the_website }}. Não há suporte para a pesquisa avançada e a pesquisa de wikis no {{ site.data.variables.product.prodname_dotcom_the_website }}.

{{ site.data.reusables.github-connect.access-dotcom-and-enterprise }}
{{ site.data.reusables.enterprise_site_admin_settings.access-settings }}{{ site.data.reusables.enterprise_site_admin_settings.business }}
{{ site.data.reusables.enterprise-accounts.settings-tab }}
{{ site.data.reusables.enterprise-accounts.github-connect-tab }}
5. Em "Users can search {{ site.data.variables.product.prodname_dotcom_the_website }}" (Usuários podem pesquisar no {{ site.data.variables.product.prodname_dotcom_the_website }}), use o menu suspenso e clique em **Enabled** (Habilitado). ![Habilitar a opção de pesquisa no menu suspenso de pesquisa do GitHub.com](/assets/images/enterprise/site-admin-settings/github-dotcom-enable-search.png)
6. Em "Users can search private repositories on {{ site.data.variables.product.prodname_dotcom_the_website }}" (Usuários podem pesquisar em repositórios privados no {{ site.data.variables.product.prodname_dotcom_the_website }}), use o menu suspenso e clique em **Enabled** (Habilitado). ![Habilitar a opção de pesquisa em repositórios privados no menu suspenso de pesquisa do GitHub.com](/assets/images/enterprise/site-admin-settings/enable-private-search.png)

### Further reading

- [Conectar o {{ site.data.variables.product.prodname_ghe_server }} ao {{ site.data.variables.product.prodname_dotcom_the_website }}](/enterprise/admin/guides/developer-workflow/connecting-github-enterprise-server-to-github-com)