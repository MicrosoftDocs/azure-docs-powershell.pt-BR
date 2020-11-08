---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116448"
---
# <span data-ttu-id="87e84-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="87e84-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="87e84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87e84-102">SYNOPSIS</span></span>
<span data-ttu-id="87e84-103">Gera novamente uma tecla de acesso para o repositório de configuração especificado.</span><span class="sxs-lookup"><span data-stu-id="87e84-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="87e84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87e84-104">SYNTAX</span></span>

### <span data-ttu-id="87e84-105">RegenerateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="87e84-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87e84-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87e84-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87e84-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87e84-107">DESCRIPTION</span></span>
<span data-ttu-id="87e84-108">Gera novamente uma tecla de acesso para o repositório de configuração especificado.</span><span class="sxs-lookup"><span data-stu-id="87e84-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="87e84-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87e84-109">EXAMPLES</span></span>

### <span data-ttu-id="87e84-110">Exemplo 1: regenerar a chave de um repositório de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="87e84-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="87e84-111">Esse comando regenera a chave de um repositório de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87e84-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="87e84-112">Exemplo 2: regenerar a chave de uma loja de configuração de aplicativo por objeto</span><span class="sxs-lookup"><span data-stu-id="87e84-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="87e84-113">Esse comando regenera a chave de um repositório de configuração de aplicativo por objeto.</span><span class="sxs-lookup"><span data-stu-id="87e84-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="87e84-114">OS</span><span class="sxs-lookup"><span data-stu-id="87e84-114">PARAMETERS</span></span>

### <span data-ttu-id="87e84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e84-115">-DefaultProfile</span></span>
<span data-ttu-id="87e84-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87e84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e84-117">-ID</span><span class="sxs-lookup"><span data-stu-id="87e84-117">-Id</span></span>
<span data-ttu-id="87e84-118">A ID da chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="87e84-118">The id of the key to regenerate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87e84-119">-InputObject</span></span>
<span data-ttu-id="87e84-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="87e84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="87e84-121">-Name</span></span>
<span data-ttu-id="87e84-122">O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="87e84-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e84-123">-ResourceGroupName</span></span>
<span data-ttu-id="87e84-124">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="87e84-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87e84-125">-SubscriptionId</span></span>
<span data-ttu-id="87e84-126">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87e84-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87e84-127">-Confirm</span></span>
<span data-ttu-id="87e84-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87e84-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e84-129">-WhatIf</span></span>
<span data-ttu-id="87e84-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87e84-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e84-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87e84-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e84-132">CommonParameters</span></span>
<span data-ttu-id="87e84-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e84-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87e84-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e84-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87e84-135">INPUTS</span></span>

### <span data-ttu-id="87e84-136">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="87e84-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="87e84-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87e84-137">OUTPUTS</span></span>

### <span data-ttu-id="87e84-138">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="87e84-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="87e84-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87e84-139">NOTES</span></span>

<span data-ttu-id="87e84-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="87e84-140">ALIASES</span></span>

<span data-ttu-id="87e84-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="87e84-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87e84-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="87e84-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87e84-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87e84-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87e84-144">INPUTobject <IAppConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="87e84-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87e84-145">`[ConfigStoreName <String>]`: O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="87e84-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="87e84-146">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="87e84-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="87e84-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="87e84-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87e84-148">`[PrivateEndpointConnectionName <String>]`: Nome da conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="87e84-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="87e84-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="87e84-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="87e84-150">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87e84-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="87e84-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87e84-151">RELATED LINKS</span></span>

