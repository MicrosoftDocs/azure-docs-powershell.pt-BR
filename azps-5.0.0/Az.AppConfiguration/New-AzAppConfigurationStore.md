---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116449"
---
# <span data-ttu-id="2350d-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="2350d-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="2350d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2350d-102">SYNOPSIS</span></span>
<span data-ttu-id="2350d-103">Cria um repositório de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="2350d-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="2350d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2350d-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2350d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2350d-105">DESCRIPTION</span></span>
<span data-ttu-id="2350d-106">Cria um repositório de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="2350d-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="2350d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2350d-107">EXAMPLES</span></span>

### <span data-ttu-id="2350d-108">Exemplo 1: criar um repositório de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2350d-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2350d-109">Esse comando cria um repositório de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2350d-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="2350d-110">Exemplo 2: criar uma configuração de aplicativo com o IdentityType definido como "userassigned"</span><span class="sxs-lookup"><span data-stu-id="2350d-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2350d-111">Esse comando cria uma configuração de aplicativo e atribui uma identidade gerenciada atribuída pelo usuário a ele.</span><span class="sxs-lookup"><span data-stu-id="2350d-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="2350d-112">Consulte o exemplo de `Update-AzAppConfigurationStore` para as etapas a seguir para habilitar o CMK (chave gerenciada cusomer).</span><span class="sxs-lookup"><span data-stu-id="2350d-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="2350d-113">Exemplo 3: criar uma configuração de aplicativo com o IdentityType definido como "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="2350d-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2350d-114">Esse comando cria uma configuração de aplicativo e habilita a identidade gerenciada atribuída pelo sistema associada ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2350d-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="2350d-115">Consulte o exemplo de `Update-AzAppConfigurationStore` para as etapas a seguir para habilitar o CMK (chave gerenciada cusomer).</span><span class="sxs-lookup"><span data-stu-id="2350d-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="2350d-116">Exemplo 4: criar uma configuração de aplicativo com o IdentityType definido como "SystemAssigned, userassigned"</span><span class="sxs-lookup"><span data-stu-id="2350d-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2350d-117">Você pode habilitar a identidade gerenciada pelo sistema e conceder identidades atribuídas ao usuário ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2350d-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="2350d-118">Consulte o exemplo de `Update-AzAppConfigurationStore` para as etapas a seguir para habilitar o CMK (chave gerenciada cusomer).</span><span class="sxs-lookup"><span data-stu-id="2350d-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="2350d-119">OS</span><span class="sxs-lookup"><span data-stu-id="2350d-119">PARAMETERS</span></span>

### <span data-ttu-id="2350d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2350d-120">-AsJob</span></span>
<span data-ttu-id="2350d-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2350d-121">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2350d-122">-DefaultProfile</span></span>
<span data-ttu-id="2350d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2350d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2350d-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2350d-124">-IdentityType</span></span>
<span data-ttu-id="2350d-125">O tipo de identidade gerenciada usado.</span><span class="sxs-lookup"><span data-stu-id="2350d-125">The type of managed identity used.</span></span>
<span data-ttu-id="2350d-126">O tipo ' SystemAssignedAndUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2350d-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="2350d-127">O tipo ' nenhum ' removerá todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="2350d-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-128">-Local</span><span class="sxs-lookup"><span data-stu-id="2350d-128">-Location</span></span>
<span data-ttu-id="2350d-129">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2350d-129">The location of the resource.</span></span>
<span data-ttu-id="2350d-130">Isso não pode ser alterado após a criação do recurso.</span><span class="sxs-lookup"><span data-stu-id="2350d-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="2350d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2350d-131">-Name</span></span>
<span data-ttu-id="2350d-132">O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="2350d-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="2350d-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2350d-133">-NoWait</span></span>
<span data-ttu-id="2350d-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="2350d-134">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2350d-135">-ResourceGroupName</span></span>
<span data-ttu-id="2350d-136">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="2350d-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="2350d-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="2350d-137">-Sku</span></span>
<span data-ttu-id="2350d-138">O nome do SKU do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="2350d-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="2350d-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2350d-139">-SubscriptionId</span></span>
<span data-ttu-id="2350d-140">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2350d-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="2350d-141">-Tag</span></span>
<span data-ttu-id="2350d-142">As marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="2350d-142">The tags of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2350d-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="2350d-144">A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2350d-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="2350d-145">As chaves de dicionário de identidade atribuídas pelo usuário serão as IDs de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="2350d-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2350d-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2350d-146">-Confirm</span></span>
<span data-ttu-id="2350d-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2350d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2350d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2350d-148">-WhatIf</span></span>
<span data-ttu-id="2350d-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2350d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2350d-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2350d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2350d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2350d-151">CommonParameters</span></span>
<span data-ttu-id="2350d-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2350d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2350d-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2350d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2350d-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2350d-154">INPUTS</span></span>

## <span data-ttu-id="2350d-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2350d-155">OUTPUTS</span></span>

### <span data-ttu-id="2350d-156">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="2350d-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="2350d-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2350d-157">NOTES</span></span>

<span data-ttu-id="2350d-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2350d-158">ALIASES</span></span>

## <span data-ttu-id="2350d-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2350d-159">RELATED LINKS</span></span>



[<span data-ttu-id="2350d-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2350d-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

