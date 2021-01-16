---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 0eacae818861b28bfd13e0354400673b26f8e23f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259437"
---
# <span data-ttu-id="f19c6-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="f19c6-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="f19c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f19c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f19c6-103">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="f19c6-103">Create or update a host pool.</span></span>

## <span data-ttu-id="f19c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f19c6-104">SYNTAX</span></span>

### <span data-ttu-id="f19c6-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f19c6-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f19c6-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="f19c6-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f19c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f19c6-107">DESCRIPTION</span></span>
<span data-ttu-id="f19c6-108">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="f19c6-108">Create or update a host pool.</span></span>

## <span data-ttu-id="f19c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f19c6-109">EXAMPLES</span></span>

### <span data-ttu-id="f19c6-110">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="f19c6-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="f19c6-111">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f19c6-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="f19c6-112">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="f19c6-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="f19c6-113">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f19c6-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="f19c6-114">OS</span><span class="sxs-lookup"><span data-stu-id="f19c6-114">PARAMETERS</span></span>

### <span data-ttu-id="f19c6-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="f19c6-115">-CustomRdpProperty</span></span>
<span data-ttu-id="f19c6-116">Propriedade RDP personalizada de HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="f19c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19c6-117">-DefaultProfile</span></span>
<span data-ttu-id="f19c6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f19c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19c6-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f19c6-119">-Description</span></span>
<span data-ttu-id="f19c6-120">Descrição de HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="f19c6-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="f19c6-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="f19c6-122">Nome do grupo do aplicativo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="f19c6-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="f19c6-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="f19c6-123">-ExpirationTime</span></span>
<span data-ttu-id="f19c6-124">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="f19c6-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="f19c6-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f19c6-125">-FriendlyName</span></span>
<span data-ttu-id="f19c6-126">Nome amigável de HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="f19c6-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="f19c6-127">-HostPoolType</span></span>
<span data-ttu-id="f19c6-128">Tipo de HostPool para área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f19c6-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="f19c6-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="f19c6-129">-LoadBalancerType</span></span>
<span data-ttu-id="f19c6-130">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f19c6-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="f19c6-131">-Local</span><span class="sxs-lookup"><span data-stu-id="f19c6-131">-Location</span></span>
<span data-ttu-id="f19c6-132">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="f19c6-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="f19c6-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="f19c6-133">-MaxSessionLimit</span></span>
<span data-ttu-id="f19c6-134">O limite máximo da sessão de HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="f19c6-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="f19c6-135">-Name</span></span>
<span data-ttu-id="f19c6-136">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="f19c6-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f19c6-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="f19c6-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="f19c6-138">Tipo de PersonalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="f19c6-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="f19c6-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="f19c6-140">O tipo de tipo de grupo de aplicativos preferencial, padrão para grupo de aplicativos de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="f19c6-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="f19c6-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="f19c6-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="f19c6-142">A cadeia de caracteres codificada em base64 do token de registro.</span><span class="sxs-lookup"><span data-stu-id="f19c6-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="f19c6-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="f19c6-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="f19c6-144">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="f19c6-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="f19c6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19c6-145">-ResourceGroupName</span></span>
<span data-ttu-id="f19c6-146">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f19c6-146">The name of the resource group.</span></span>
<span data-ttu-id="f19c6-147">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f19c6-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f19c6-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="f19c6-148">-Ring</span></span>
<span data-ttu-id="f19c6-149">O número de toques de HostPool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="f19c6-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="f19c6-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="f19c6-151">URL para o servidor ADFS do cliente para autenticação de certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="f19c6-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="f19c6-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="f19c6-152">-SsoClientId</span></span>
<span data-ttu-id="f19c6-153">ClientId para a terceira parte confiável usada para emitir certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="f19c6-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="f19c6-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="f19c6-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="f19c6-155">Caminho para o cofre de chave do Azure que armazena o segredo usado para comunicação com o ADFS.</span><span class="sxs-lookup"><span data-stu-id="f19c6-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="f19c6-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="f19c6-156">-SsoContext</span></span>
<span data-ttu-id="f19c6-157">Caminho para o keyvault que contém ssoContext segredo.</span><span class="sxs-lookup"><span data-stu-id="f19c6-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="f19c6-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="f19c6-158">-SsoSecretType</span></span>
<span data-ttu-id="f19c6-159">O tipo de tipo de segredo de logon único.</span><span class="sxs-lookup"><span data-stu-id="f19c6-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c6-160">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f19c6-160">-SubscriptionId</span></span>
<span data-ttu-id="f19c6-161">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f19c6-161">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f19c6-162">-Marca</span><span class="sxs-lookup"><span data-stu-id="f19c6-162">-Tag</span></span>
<span data-ttu-id="f19c6-163">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="f19c6-163">Resource tags.</span></span>

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

### <span data-ttu-id="f19c6-164">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="f19c6-164">-ValidationEnvironment</span></span>
<span data-ttu-id="f19c6-165">É ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="f19c6-165">Is validation environment.</span></span>

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

### <span data-ttu-id="f19c6-166">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="f19c6-166">-VMTemplate</span></span>
<span data-ttu-id="f19c6-167">Modelo de VM para configuração do sessionhosts em hostpool.</span><span class="sxs-lookup"><span data-stu-id="f19c6-167">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="f19c6-168">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f19c6-168">-WorkspaceName</span></span>
<span data-ttu-id="f19c6-169">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="f19c6-169">Workspace Name</span></span>

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

### <span data-ttu-id="f19c6-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f19c6-170">-Confirm</span></span>
<span data-ttu-id="f19c6-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19c6-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19c6-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19c6-172">-WhatIf</span></span>
<span data-ttu-id="f19c6-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f19c6-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19c6-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f19c6-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19c6-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19c6-175">CommonParameters</span></span>
<span data-ttu-id="f19c6-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19c6-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19c6-177">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f19c6-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19c6-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f19c6-178">INPUTS</span></span>

## <span data-ttu-id="f19c6-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f19c6-179">OUTPUTS</span></span>

### <span data-ttu-id="f19c6-180">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="f19c6-180">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="f19c6-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f19c6-181">NOTES</span></span>

<span data-ttu-id="f19c6-182">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f19c6-182">ALIASES</span></span>

## <span data-ttu-id="f19c6-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f19c6-183">RELATED LINKS</span></span>

