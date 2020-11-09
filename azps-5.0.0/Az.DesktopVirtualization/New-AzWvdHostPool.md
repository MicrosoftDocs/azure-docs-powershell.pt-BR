---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280562"
---
# <span data-ttu-id="32b32-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="32b32-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="32b32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32b32-102">SYNOPSIS</span></span>
<span data-ttu-id="32b32-103">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="32b32-103">Create or update a host pool.</span></span>

## <span data-ttu-id="32b32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32b32-104">SYNTAX</span></span>

### <span data-ttu-id="32b32-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="32b32-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32b32-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="32b32-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32b32-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32b32-107">DESCRIPTION</span></span>
<span data-ttu-id="32b32-108">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="32b32-108">Create or update a host pool.</span></span>

## <span data-ttu-id="32b32-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b32-109">EXAMPLES</span></span>

### <span data-ttu-id="32b32-110">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="32b32-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="32b32-111">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32b32-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="32b32-112">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="32b32-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="32b32-113">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32b32-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="32b32-114">OS</span><span class="sxs-lookup"><span data-stu-id="32b32-114">PARAMETERS</span></span>

### <span data-ttu-id="32b32-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="32b32-115">-CustomRdpProperty</span></span>
<span data-ttu-id="32b32-116">Propriedade RDP personalizada de HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b32-117">-DefaultProfile</span></span>
<span data-ttu-id="32b32-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32b32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b32-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="32b32-119">-Description</span></span>
<span data-ttu-id="32b32-120">Descrição de HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="32b32-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="32b32-122">Nome do grupo do aplicativo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="32b32-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="32b32-123">-ExpirationTime</span></span>
<span data-ttu-id="32b32-124">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="32b32-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="32b32-125">-FriendlyName</span></span>
<span data-ttu-id="32b32-126">Nome amigável de HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="32b32-127">-HostPoolType</span></span>
<span data-ttu-id="32b32-128">Tipo de HostPool para área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="32b32-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="32b32-129">-LoadBalancerType</span></span>
<span data-ttu-id="32b32-130">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="32b32-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-131">-Local</span><span class="sxs-lookup"><span data-stu-id="32b32-131">-Location</span></span>
<span data-ttu-id="32b32-132">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="32b32-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="32b32-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="32b32-133">-MaxSessionLimit</span></span>
<span data-ttu-id="32b32-134">O limite máximo da sessão de HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="32b32-135">-Name</span></span>
<span data-ttu-id="32b32-136">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="32b32-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="32b32-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="32b32-138">Tipo de PersonalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="32b32-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="32b32-140">O tipo de tipo de grupo de aplicativos preferencial, padrão para grupo de aplicativos de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="32b32-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="32b32-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="32b32-142">A cadeia de caracteres codificada em base64 do token de registro.</span><span class="sxs-lookup"><span data-stu-id="32b32-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="32b32-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="32b32-144">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="32b32-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b32-145">-ResourceGroupName</span></span>
<span data-ttu-id="32b32-146">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32b32-146">The name of the resource group.</span></span>
<span data-ttu-id="32b32-147">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32b32-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="32b32-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="32b32-148">-Ring</span></span>
<span data-ttu-id="32b32-149">O número de toques de HostPool.</span><span class="sxs-lookup"><span data-stu-id="32b32-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="32b32-150">-SsoContext</span></span>
<span data-ttu-id="32b32-151">Caminho para o keyvault que contém ssoContext segredo.</span><span class="sxs-lookup"><span data-stu-id="32b32-151">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32b32-152">-SubscriptionId</span></span>
<span data-ttu-id="32b32-153">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="32b32-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="32b32-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="32b32-154">-Tag</span></span>
<span data-ttu-id="32b32-155">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="32b32-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="32b32-156">-ValidationEnvironment</span></span>
<span data-ttu-id="32b32-157">É ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="32b32-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="32b32-158">-VMTemplate</span></span>
<span data-ttu-id="32b32-159">Modelo de VM para configuração do sessionhosts em hostpool.</span><span class="sxs-lookup"><span data-stu-id="32b32-159">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32b32-160">-WorkspaceName</span></span>
<span data-ttu-id="32b32-161">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="32b32-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b32-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32b32-162">-Confirm</span></span>
<span data-ttu-id="32b32-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b32-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b32-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b32-164">-WhatIf</span></span>
<span data-ttu-id="32b32-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32b32-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b32-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32b32-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b32-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b32-167">CommonParameters</span></span>
<span data-ttu-id="32b32-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b32-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b32-169">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32b32-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b32-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32b32-170">INPUTS</span></span>

## <span data-ttu-id="32b32-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32b32-171">OUTPUTS</span></span>

### <span data-ttu-id="32b32-172">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="32b32-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="32b32-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32b32-173">NOTES</span></span>

<span data-ttu-id="32b32-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="32b32-174">ALIASES</span></span>

## <span data-ttu-id="32b32-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b32-175">RELATED LINKS</span></span>

