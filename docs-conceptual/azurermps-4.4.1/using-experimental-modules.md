---
title: Usando módulos experimentais do Azure PowerShell
description: Entenda a filosofia e o uso dos módulos experimentais do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 30e57805dd59bd60d10c52422fcb68686563fadf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274663"
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="f4216-103">Usando módulos experimentais do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4216-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="f4216-104">Com ênfase nas ferramentas do desenvolvedor (especialmente as CLIs) no Azure, a equipe do Azure PowerShell está experimentando várias melhorias na experiência do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4216-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="f4216-105">Metodologia de experimentação</span><span class="sxs-lookup"><span data-stu-id="f4216-105">Experimentation methodology</span></span>

<span data-ttu-id="f4216-106">Para facilitar a experimentação, estamos criando novos módulos do Azure PowerShell que implementam a funcionalidade existente do SDK do Azure de formas novas e mais fáceis usar.</span><span class="sxs-lookup"><span data-stu-id="f4216-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="f4216-107">Na maioria dos casos, os cmdlets espelham exatamente os cmdlets existentes.</span><span class="sxs-lookup"><span data-stu-id="f4216-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="f4216-108">No entanto, os cmdlets experimentais fornecem uma notação abreviada e valores padrão mais inteligentes que facilitam criar e gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4216-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="f4216-109">Esses módulos podem ser instalados lado a lado com os módulos existentes do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4216-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="f4216-110">Os nomes do cmdlet foram reduzidos para fornecer nomes mais curtos e evitar conflitos de nomenclatura com os cmdlets existentes e não experimentais.</span><span class="sxs-lookup"><span data-stu-id="f4216-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="f4216-111">Os módulos experimentais usam a seguinte convenção de nomenclatura: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="f4216-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="f4216-112">Essa convenção de nomenclatura é semelhante à nomenclatura dos módulos de Visualização: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="f4216-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="f4216-113">Os módulos de Visualização são diferentes dos módulos experimentais.</span><span class="sxs-lookup"><span data-stu-id="f4216-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="f4216-114">Os módulos de Visualização implementam a nova funcionalidade de serviços do Azure, só disponível como uma oferta de Visualização.</span><span class="sxs-lookup"><span data-stu-id="f4216-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="f4216-115">Os módulos de Visualização substituem os módulos existentes do Azure PowerShell e usam os mesmos nomes do cmdlet e do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f4216-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="f4216-116">Como instalar um módulo experimental</span><span class="sxs-lookup"><span data-stu-id="f4216-116">How to install an experimental module</span></span>

<span data-ttu-id="f4216-117">Os módulos experimentais são publicados na Galeria do PowerShell como módulos existentes do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4216-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="f4216-118">Para ver uma lista de módulos experimentais, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f4216-118">To see a list of experimental modules, run the following command:</span></span>

```powershell-interactive
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="f4216-119">Para instalar o módulo experimental, use os seguintes comandos de uma sessão do PowerShell com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="f4216-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="f4216-120">Documentação e suporte</span><span class="sxs-lookup"><span data-stu-id="f4216-120">Documentation and support</span></span>

<span data-ttu-id="f4216-121">A documentação está incluída no pacote de instalação e é acessada usando o cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="f4216-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="f4216-122">Nenhuma documentação oficial é publicada para os módulos experimentais.</span><span class="sxs-lookup"><span data-stu-id="f4216-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="f4216-123">Incentivamos você a testar esses módulos.</span><span class="sxs-lookup"><span data-stu-id="f4216-123">We encourage you to test these modules.</span></span> <span data-ttu-id="f4216-124">Seus comentários nos permitam aumentar a utilização e responder às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="f4216-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="f4216-125">No entanto, sendo experimentais, o suporte para esses módulos é limitado.</span><span class="sxs-lookup"><span data-stu-id="f4216-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="f4216-126">As perguntas ou problemas podem ser enviados criando um [caso](https://github.com/Azure/azure-powershell/issues) no repositório do GitHub.</span><span class="sxs-lookup"><span data-stu-id="f4216-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="f4216-127">Experimentos e áreas de aprimoramento</span><span class="sxs-lookup"><span data-stu-id="f4216-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="f4216-128">Esses aperfeiçoamentos foram selecionados com base nos principais diferenciais dos produtos concorrentes.</span><span class="sxs-lookup"><span data-stu-id="f4216-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="f4216-129">Por exemplo,a CLI do Azure 2.0 fez questão de basear os comandos nos _cenários_, em vez da _área de superfície de API_.</span><span class="sxs-lookup"><span data-stu-id="f4216-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="f4216-130">A CLI do Azure 2.0 usa vários padrões inteligentes que facilitam os cenários de "introdução" para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="f4216-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="f4216-131">Principais melhorias</span><span class="sxs-lookup"><span data-stu-id="f4216-131">Core improvements</span></span>

<span data-ttu-id="f4216-132">As principais melhorias são consideradas de "bom senso" e pouca experimentação é necessária para continuar a implementar essas atualizações.</span><span class="sxs-lookup"><span data-stu-id="f4216-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="f4216-133">Cmdlets baseados em cenário - <em>\*All</em>- os cmdlets devem ser criados com base nos cenários, não no serviço REST do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4216-133">Scenario-based Cmdlets - <em>\*All</em>- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="f4216-134">Menor nomes - isso inclui os nomes dos cmdlets (por exemplo, `New-AzureRmVM` => `New-AzVm`) e os nomes dos parâmetros (por exemplo, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="f4216-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="f4216-135">Use aliases para ter compatibilidade com os cmdlets "antigos".</span><span class="sxs-lookup"><span data-stu-id="f4216-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="f4216-136">Forneça conjuntos de parâmetros _compatíveis com as versões anteriores_.</span><span class="sxs-lookup"><span data-stu-id="f4216-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="f4216-137">Padrões Inteligente - criam padrões inteligentes preencher as informações "obrigatórias".</span><span class="sxs-lookup"><span data-stu-id="f4216-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="f4216-138">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="f4216-138">For example:</span></span>
  - <span data-ttu-id="f4216-139">Grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4216-139">Resource Group</span></span>
  - <span data-ttu-id="f4216-140">Local padrão</span><span class="sxs-lookup"><span data-stu-id="f4216-140">Location</span></span>
  - <span data-ttu-id="f4216-141">Recursos dependentes</span><span class="sxs-lookup"><span data-stu-id="f4216-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="f4216-142">Melhorias experimentais</span><span class="sxs-lookup"><span data-stu-id="f4216-142">Experimental improvements</span></span>

<span data-ttu-id="f4216-143">As melhorias experimentais apresentam uma alteração significativa que a equipe deseja validar via experimentação.</span><span class="sxs-lookup"><span data-stu-id="f4216-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="f4216-144">Tipos simples - criam cenários que devem ficar longe dos tipos complexos e objetos de configuração.</span><span class="sxs-lookup"><span data-stu-id="f4216-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="f4216-145">Simplifique a configuração para um ou dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f4216-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="f4216-146">"Criação Inteligente" - todos que criam cenários que implementam a "Criação Inteligente" _não_ teriam parâmetros obrigatórios: todas as informações necessárias seriam escolhidas pelo Azure PowerShell de forma dogmática.</span><span class="sxs-lookup"><span data-stu-id="f4216-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="f4216-147">Parâmetros cinzas - em muitos casos, alguns parâmetros podem ser "cinza" ou semiopcionais.</span><span class="sxs-lookup"><span data-stu-id="f4216-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="f4216-148">Se o parâmetro não for especificado, será perguntado ao usuário se deseja o parâmetro gerado para ele.</span><span class="sxs-lookup"><span data-stu-id="f4216-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="f4216-149">Também faz sentido que os parâmetros cinzas deduzam um valor com base no contexto, com a autorização do usuário.</span><span class="sxs-lookup"><span data-stu-id="f4216-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="f4216-150">Por exemplo, talvez faça sentido que o parâmetro cinza sugira o valor usado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="f4216-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="f4216-151">`-Auto`Argumento - o argumento `-Auto` forneceria uma maneira de "aceitação" para que os usuários _tenham como padrão tudo_, mantendo a integridade dos parâmetros necessários no caminho principal.</span><span class="sxs-lookup"><span data-stu-id="f4216-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="f4216-152">Argumentos específicos do recurso</span><span class="sxs-lookup"><span data-stu-id="f4216-152">Feature-specific switches</span></span>

<span data-ttu-id="f4216-153">Por exemplo, o cenário de "Criar aplicativo Web" pode ter um argumento `-Git` ou `-AddRemote` que adicionaria automaticamente um "azure" remoto a um repositório git existente.</span><span class="sxs-lookup"><span data-stu-id="f4216-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="f4216-154">Padrões configuráveis - os usuários devem ter a capacidade de ter como padrão determinados parâmetros onipresentes como `-ResourceGroupName` e `-Location`.</span><span class="sxs-lookup"><span data-stu-id="f4216-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="f4216-155">Padrões de tamanho - o recurso "tamanhos" pode confundir os usuários, pois muitos Provedores de Recursos usam nomes diferentes (por exemplo, "Standard\_DS1\_v2" ou "S1").</span><span class="sxs-lookup"><span data-stu-id="f4216-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="f4216-156">No entanto, a maioria dos usuários se importa mais com o custo.</span><span class="sxs-lookup"><span data-stu-id="f4216-156">However, most users care more about cost.</span></span> <span data-ttu-id="f4216-157">Portanto, faz sentido para definir tamanhos "universais" com base em um agendamento de preços.</span><span class="sxs-lookup"><span data-stu-id="f4216-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="f4216-158">Os usuários podem escolher um tamanho específico ou deixar que o Azure PowerShell escolher a _melhor opção_ com base no recurso do orçamento.</span><span class="sxs-lookup"><span data-stu-id="f4216-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="f4216-159">Formato da saída - o Azure PowerShell atualmente retorna `PSObject`s e há pouca saída do console.</span><span class="sxs-lookup"><span data-stu-id="f4216-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="f4216-160">O Azure PowerShell pode precisar exibir algumas informações para o usuário em relação os "padrões inteligentes" usados.</span><span class="sxs-lookup"><span data-stu-id="f4216-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
