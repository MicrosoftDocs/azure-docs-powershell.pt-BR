---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: e7f7c1f7493123793a32163b4e8f37bec8706e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891415"
---
# <span data-ttu-id="83649-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="83649-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="83649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83649-102">SYNOPSIS</span></span>
<span data-ttu-id="83649-103">Obter ou listar os armazenamentos de configuração de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="83649-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="83649-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="83649-104">SYNTAX</span></span>

### <span data-ttu-id="83649-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="83649-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83649-106">Obter</span><span class="sxs-lookup"><span data-stu-id="83649-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83649-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83649-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83649-108">List1</span><span class="sxs-lookup"><span data-stu-id="83649-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83649-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="83649-109">DESCRIPTION</span></span>
<span data-ttu-id="83649-110">Obter ou listar os armazenamentos de configuração de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="83649-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="83649-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83649-111">EXAMPLES</span></span>

### <span data-ttu-id="83649-112">Exemplo 1: listar todos os armazenamentos de configuração de aplicativos em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="83649-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83649-113">Este comando lista todos os armazenamentos de configuração de aplicativo sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="83649-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="83649-114">Exemplo 2: listar todos os armazenamentos de configuração de aplicativos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="83649-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83649-115">Este comando lista todos os armazenamentos de configuração de aplicativos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="83649-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="83649-116">Exemplo 3: obter um armazenamento de configuração de aplicativo pelo nome</span><span class="sxs-lookup"><span data-stu-id="83649-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83649-117">Esse comando obtém um armazenamento de configuração de aplicativo pelo nome.</span><span class="sxs-lookup"><span data-stu-id="83649-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="83649-118">Exemplo 4: Obter um armazenamento de configuração de aplicativo por pipeline</span><span class="sxs-lookup"><span data-stu-id="83649-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83649-119">Esse comando obtém um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="83649-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="83649-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="83649-120">PARAMETERS</span></span>

### <span data-ttu-id="83649-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83649-121">-DefaultProfile</span></span>
<span data-ttu-id="83649-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83649-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83649-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83649-123">-InputObject</span></span>
<span data-ttu-id="83649-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="83649-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83649-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83649-125">-Name</span></span>
<span data-ttu-id="83649-126">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="83649-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="83649-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83649-127">-ResourceGroupName</span></span>
<span data-ttu-id="83649-128">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="83649-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="83649-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83649-129">-SubscriptionId</span></span>
<span data-ttu-id="83649-130">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83649-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="83649-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83649-131">CommonParameters</span></span>
<span data-ttu-id="83649-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83649-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83649-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83649-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83649-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83649-134">INPUTS</span></span>

### <span data-ttu-id="83649-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="83649-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="83649-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="83649-136">OUTPUTS</span></span>

### <span data-ttu-id="83649-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="83649-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="83649-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="83649-138">NOTES</span></span>

<span data-ttu-id="83649-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="83649-139">ALIASES</span></span>

<span data-ttu-id="83649-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="83649-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83649-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="83649-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83649-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83649-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83649-143">INPUTOBJECT <IAppConfigurationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="83649-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83649-144">`[ConfigStoreName <String>]`: O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="83649-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="83649-145">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="83649-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="83649-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="83649-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83649-147">`[PrivateEndpointConnectionName <String>]`: Nome da conexão do ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="83649-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="83649-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="83649-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="83649-149">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83649-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="83649-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83649-150">RELATED LINKS</span></span>

