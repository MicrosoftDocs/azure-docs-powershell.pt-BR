---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284342"
---
# <span data-ttu-id="1feb7-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="1feb7-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="1feb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1feb7-102">SYNOPSIS</span></span>
<span data-ttu-id="1feb7-103">Obter ou listar repositórios de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1feb7-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="1feb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1feb7-104">SYNTAX</span></span>

### <span data-ttu-id="1feb7-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="1feb7-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1feb7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1feb7-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1feb7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1feb7-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1feb7-108">List1</span><span class="sxs-lookup"><span data-stu-id="1feb7-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1feb7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1feb7-109">DESCRIPTION</span></span>
<span data-ttu-id="1feb7-110">Obter ou listar repositórios de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1feb7-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="1feb7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1feb7-111">EXAMPLES</span></span>

### <span data-ttu-id="1feb7-112">Exemplo 1: listar todos os repositórios de configuração do aplicativo em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="1feb7-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="1feb7-113">Esse comando lista todos os repositórios de configuração do aplicativo em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1feb7-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="1feb7-114">Exemplo 2: listar todos os repositórios de configuração do aplicativo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1feb7-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="1feb7-115">Esse comando lista todos os repositórios de configuração do aplicativo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1feb7-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="1feb7-116">Exemplo 3: obter uma loja de configuração de aplicativo por nome</span><span class="sxs-lookup"><span data-stu-id="1feb7-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="1feb7-117">Esse comando obtém um repositório de configuração de aplicativo por nome.</span><span class="sxs-lookup"><span data-stu-id="1feb7-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="1feb7-118">Exemplo 4: obter um repositório de configuração de aplicativo por pipeline</span><span class="sxs-lookup"><span data-stu-id="1feb7-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="1feb7-119">Esse comando obtém um repositório de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="1feb7-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="1feb7-120">OS</span><span class="sxs-lookup"><span data-stu-id="1feb7-120">PARAMETERS</span></span>

### <span data-ttu-id="1feb7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1feb7-121">-DefaultProfile</span></span>
<span data-ttu-id="1feb7-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1feb7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1feb7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1feb7-123">-InputObject</span></span>
<span data-ttu-id="1feb7-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1feb7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1feb7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1feb7-125">-Name</span></span>
<span data-ttu-id="1feb7-126">O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="1feb7-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="1feb7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1feb7-127">-ResourceGroupName</span></span>
<span data-ttu-id="1feb7-128">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="1feb7-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="1feb7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1feb7-129">-SubscriptionId</span></span>
<span data-ttu-id="1feb7-130">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1feb7-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="1feb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1feb7-131">CommonParameters</span></span>
<span data-ttu-id="1feb7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1feb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1feb7-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1feb7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1feb7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1feb7-134">INPUTS</span></span>

### <span data-ttu-id="1feb7-135">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="1feb7-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="1feb7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1feb7-136">OUTPUTS</span></span>

### <span data-ttu-id="1feb7-137">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="1feb7-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="1feb7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1feb7-138">NOTES</span></span>

<span data-ttu-id="1feb7-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1feb7-139">ALIASES</span></span>

<span data-ttu-id="1feb7-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="1feb7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1feb7-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1feb7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1feb7-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1feb7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1feb7-143">INPUTobject <IAppConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="1feb7-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1feb7-144">`[ConfigStoreName <String>]`: O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="1feb7-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="1feb7-145">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="1feb7-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="1feb7-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1feb7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1feb7-147">`[PrivateEndpointConnectionName <String>]`: Nome da conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="1feb7-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="1feb7-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="1feb7-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="1feb7-149">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1feb7-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="1feb7-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1feb7-150">RELATED LINKS</span></span>

