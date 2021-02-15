---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118031"
---
# <span data-ttu-id="6d7df-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6d7df-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="6d7df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d7df-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7df-103">Obter ou listar lojas de configuração de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6d7df-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="6d7df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d7df-104">SYNTAX</span></span>

### <span data-ttu-id="6d7df-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d7df-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6d7df-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d7df-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d7df-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="6d7df-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d7df-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d7df-109">DESCRIPTION</span></span>
<span data-ttu-id="6d7df-110">Obter ou listar lojas de configuração de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6d7df-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="6d7df-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d7df-111">EXAMPLES</span></span>

### <span data-ttu-id="6d7df-112">Exemplo 1: Listar todas as lojas de configuração de aplicativos em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="6d7df-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6d7df-113">Esse comando lista todos os armazenamentos de configuração de aplicativos sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d7df-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="6d7df-114">Exemplo 2: Listar todos os armazenamentos de configuração de aplicativos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6d7df-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6d7df-115">Esse comando lista todos os armazenamentos de configuração de aplicativos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d7df-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="6d7df-116">Exemplo 3: Obter um armazenamento de configuração de aplicativo por nome</span><span class="sxs-lookup"><span data-stu-id="6d7df-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6d7df-117">Esse comando obtém um armazenamento de configuração de aplicativo por nome.</span><span class="sxs-lookup"><span data-stu-id="6d7df-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="6d7df-118">Exemplo 4: Obter um armazenamento de configuração de aplicativo por pipeline</span><span class="sxs-lookup"><span data-stu-id="6d7df-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6d7df-119">Esse comando obtém um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="6d7df-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="6d7df-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d7df-120">PARAMETERS</span></span>

### <span data-ttu-id="6d7df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7df-121">-DefaultProfile</span></span>
<span data-ttu-id="6d7df-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d7df-123">-InputObject</span></span>
<span data-ttu-id="6d7df-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6d7df-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d7df-125">-Name</span></span>
<span data-ttu-id="6d7df-126">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="6d7df-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7df-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d7df-128">O nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="6d7df-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d7df-129">-SubscriptionId</span></span>
<span data-ttu-id="6d7df-130">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7df-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7df-131">CommonParameters</span></span>
<span data-ttu-id="6d7df-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7df-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d7df-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7df-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d7df-134">INPUTS</span></span>

### <span data-ttu-id="6d7df-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6d7df-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6d7df-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d7df-136">OUTPUTS</span></span>

### <span data-ttu-id="6d7df-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6d7df-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="6d7df-138">Notas</span><span class="sxs-lookup"><span data-stu-id="6d7df-138">NOTES</span></span>

<span data-ttu-id="6d7df-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="6d7df-139">ALIASES</span></span>

<span data-ttu-id="6d7df-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6d7df-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d7df-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6d7df-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d7df-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d7df-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d7df-143">INPUTOBJECT: <IAppConfigurationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6d7df-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d7df-144">`[ConfigStoreName <String>]`: o nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="6d7df-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6d7df-145">`[GroupName <String>]`: o nome do grupo de recursos de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="6d7df-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6d7df-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6d7df-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d7df-147">`[PrivateEndpointConnectionName <String>]`: Nome de conexão do ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="6d7df-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6d7df-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="6d7df-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6d7df-149">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7df-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6d7df-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d7df-150">RELATED LINKS</span></span>

