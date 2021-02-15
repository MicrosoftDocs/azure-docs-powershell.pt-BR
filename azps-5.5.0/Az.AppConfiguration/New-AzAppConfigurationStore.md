---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112293"
---
# <span data-ttu-id="2034e-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="2034e-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="2034e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2034e-102">SYNOPSIS</span></span>
<span data-ttu-id="2034e-103">Cria um armazenamento de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="2034e-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="2034e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2034e-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2034e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2034e-105">DESCRIPTION</span></span>
<span data-ttu-id="2034e-106">Cria um armazenamento de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="2034e-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="2034e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2034e-107">EXAMPLES</span></span>

### <span data-ttu-id="2034e-108">Exemplo 1: Criar um armazenamento de configuração de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2034e-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2034e-109">Esse comando cria um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2034e-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="2034e-110">Exemplo 2: Criar uma configuração de aplicativo com o IdentityType definido como "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="2034e-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2034e-111">Esse comando cria uma configuração de aplicativo e atribui uma identidade gerenciada atribuída pelo usuário a ele.</span><span class="sxs-lookup"><span data-stu-id="2034e-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="2034e-112">Confira o exemplo das `Update-AzAppConfigurationStore` etapas a seguir para habilitar o CMK (chave gerenciada por outro usuário).</span><span class="sxs-lookup"><span data-stu-id="2034e-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="2034e-113">Exemplo 3: Criar uma configuração de aplicativo com o IdentityType definido como "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="2034e-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2034e-114">Esse comando cria uma configuração de aplicativo e habilita a identidade gerenciada atribuída pelo sistema associada ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2034e-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="2034e-115">Confira o exemplo das `Update-AzAppConfigurationStore` etapas a seguir para habilitar o CMK (chave gerenciada por outro usuário).</span><span class="sxs-lookup"><span data-stu-id="2034e-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="2034e-116">Exemplo 4: Criar uma configuração de aplicativo com o IdentityType definido como "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="2034e-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="2034e-117">Você pode habilitar a identidade gerenciada atribuída pelo sistema e dar identidades atribuídas pelo usuário ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2034e-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="2034e-118">Confira o exemplo das `Update-AzAppConfigurationStore` etapas a seguir para habilitar o CMK (chave gerenciada por outro usuário).</span><span class="sxs-lookup"><span data-stu-id="2034e-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="2034e-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2034e-119">PARAMETERS</span></span>

### <span data-ttu-id="2034e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2034e-120">-AsJob</span></span>
<span data-ttu-id="2034e-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2034e-121">Run the command as a job</span></span>

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

### <span data-ttu-id="2034e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2034e-122">-DefaultProfile</span></span>
<span data-ttu-id="2034e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2034e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2034e-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2034e-124">-IdentityType</span></span>
<span data-ttu-id="2034e-125">O tipo de identidade gerenciada usada.</span><span class="sxs-lookup"><span data-stu-id="2034e-125">The type of managed identity used.</span></span>
<span data-ttu-id="2034e-126">O tipo "SystemAssignedAndUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2034e-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="2034e-127">O tipo "Nenhum" removerá as identidades.</span><span class="sxs-lookup"><span data-stu-id="2034e-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="2034e-128">-Local</span><span class="sxs-lookup"><span data-stu-id="2034e-128">-Location</span></span>
<span data-ttu-id="2034e-129">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2034e-129">The location of the resource.</span></span>
<span data-ttu-id="2034e-130">Isso não pode ser alterado depois que o recurso é criado.</span><span class="sxs-lookup"><span data-stu-id="2034e-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="2034e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2034e-131">-Name</span></span>
<span data-ttu-id="2034e-132">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="2034e-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="2034e-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2034e-133">-NoWait</span></span>
<span data-ttu-id="2034e-134">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="2034e-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2034e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2034e-135">-ResourceGroupName</span></span>
<span data-ttu-id="2034e-136">O nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="2034e-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="2034e-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="2034e-137">-Sku</span></span>
<span data-ttu-id="2034e-138">O nome da SKU do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="2034e-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="2034e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2034e-139">-SubscriptionId</span></span>
<span data-ttu-id="2034e-140">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2034e-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="2034e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="2034e-141">-Tag</span></span>
<span data-ttu-id="2034e-142">As marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="2034e-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="2034e-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2034e-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="2034e-144">A lista de identidades atribuídas pelo usuário associada ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2034e-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="2034e-145">As chaves do dicionário de identidade atribuídas pelo usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="2034e-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="2034e-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2034e-146">-Confirm</span></span>
<span data-ttu-id="2034e-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2034e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2034e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2034e-148">-WhatIf</span></span>
<span data-ttu-id="2034e-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2034e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2034e-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2034e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2034e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2034e-151">CommonParameters</span></span>
<span data-ttu-id="2034e-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2034e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2034e-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2034e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2034e-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="2034e-154">INPUTS</span></span>

## <span data-ttu-id="2034e-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="2034e-155">OUTPUTS</span></span>

### <span data-ttu-id="2034e-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="2034e-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="2034e-157">Notas</span><span class="sxs-lookup"><span data-stu-id="2034e-157">NOTES</span></span>

<span data-ttu-id="2034e-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="2034e-158">ALIASES</span></span>

## <span data-ttu-id="2034e-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2034e-159">RELATED LINKS</span></span>



[<span data-ttu-id="2034e-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2034e-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

