---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428410"
---
# <span data-ttu-id="46b0c-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="46b0c-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="46b0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="46b0c-103">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="46b0c-103">Create or update a host pool.</span></span>

## <span data-ttu-id="46b0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46b0c-104">SYNTAX</span></span>

### <span data-ttu-id="46b0c-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="46b0c-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46b0c-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="46b0c-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46b0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="46b0c-108">Criar ou atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="46b0c-108">Create or update a host pool.</span></span>

## <span data-ttu-id="46b0c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="46b0c-110">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="46b0c-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="46b0c-111">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46b0c-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="46b0c-112">Exemplo 1: criar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="46b0c-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="46b0c-113">Esse comando cria uma HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46b0c-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="46b0c-114">OS</span><span class="sxs-lookup"><span data-stu-id="46b0c-114">PARAMETERS</span></span>

### <span data-ttu-id="46b0c-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="46b0c-115">-CustomRdpProperty</span></span>
<span data-ttu-id="46b0c-116">Propriedade RDP personalizada de HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="46b0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b0c-117">-DefaultProfile</span></span>
<span data-ttu-id="46b0c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46b0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b0c-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="46b0c-119">-Description</span></span>
<span data-ttu-id="46b0c-120">Descrição de HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="46b0c-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="46b0c-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="46b0c-122">Nome do grupo do aplicativo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="46b0c-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="46b0c-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="46b0c-123">-ExpirationTime</span></span>
<span data-ttu-id="46b0c-124">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="46b0c-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="46b0c-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="46b0c-125">-FriendlyName</span></span>
<span data-ttu-id="46b0c-126">Nome amigável de HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="46b0c-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="46b0c-127">-HostPoolType</span></span>
<span data-ttu-id="46b0c-128">Tipo de HostPool para área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46b0c-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="46b0c-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="46b0c-129">-LoadBalancerType</span></span>
<span data-ttu-id="46b0c-130">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="46b0c-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="46b0c-131">-Local</span><span class="sxs-lookup"><span data-stu-id="46b0c-131">-Location</span></span>
<span data-ttu-id="46b0c-132">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="46b0c-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="46b0c-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="46b0c-133">-MaxSessionLimit</span></span>
<span data-ttu-id="46b0c-134">O limite máximo da sessão de HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="46b0c-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="46b0c-135">-Name</span></span>
<span data-ttu-id="46b0c-136">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="46b0c-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="46b0c-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="46b0c-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="46b0c-138">Tipo de PersonalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="46b0c-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="46b0c-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="46b0c-140">O tipo de tipo de grupo de aplicativos preferencial, padrão para grupo de aplicativos de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="46b0c-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="46b0c-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="46b0c-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="46b0c-142">A cadeia de caracteres codificada em base64 do token de registro.</span><span class="sxs-lookup"><span data-stu-id="46b0c-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="46b0c-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="46b0c-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="46b0c-144">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="46b0c-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="46b0c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b0c-145">-ResourceGroupName</span></span>
<span data-ttu-id="46b0c-146">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46b0c-146">The name of the resource group.</span></span>
<span data-ttu-id="46b0c-147">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46b0c-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="46b0c-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="46b0c-148">-Ring</span></span>
<span data-ttu-id="46b0c-149">O número de toques de HostPool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="46b0c-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="46b0c-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="46b0c-151">URL para o servidor ADFS do cliente para autenticação de certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="46b0c-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="46b0c-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="46b0c-152">-SsoClientId</span></span>
<span data-ttu-id="46b0c-153">ClientId para a terceira parte confiável usada para emitir certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="46b0c-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="46b0c-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="46b0c-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="46b0c-155">Caminho para o cofre de chave do Azure que armazena o segredo usado para comunicação com o ADFS.</span><span class="sxs-lookup"><span data-stu-id="46b0c-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="46b0c-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="46b0c-156">-SsoContext</span></span>
<span data-ttu-id="46b0c-157">Caminho para o keyvault que contém ssoContext segredo.</span><span class="sxs-lookup"><span data-stu-id="46b0c-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="46b0c-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="46b0c-158">-SsoSecretType</span></span>
<span data-ttu-id="46b0c-159">O tipo de tipo de segredo de logon único.</span><span class="sxs-lookup"><span data-stu-id="46b0c-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="46b0c-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="46b0c-160">-StartVMOnConnect</span></span>
<span data-ttu-id="46b0c-161">O sinalizador para ativar/desativar o recurso StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="46b0c-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="46b0c-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46b0c-162">-SubscriptionId</span></span>
<span data-ttu-id="46b0c-163">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="46b0c-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="46b0c-164">-Marca</span><span class="sxs-lookup"><span data-stu-id="46b0c-164">-Tag</span></span>
<span data-ttu-id="46b0c-165">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="46b0c-165">Resource tags.</span></span>

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

### <span data-ttu-id="46b0c-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="46b0c-166">-ValidationEnvironment</span></span>
<span data-ttu-id="46b0c-167">É ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="46b0c-167">Is validation environment.</span></span>

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

### <span data-ttu-id="46b0c-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="46b0c-168">-VMTemplate</span></span>
<span data-ttu-id="46b0c-169">Modelo de VM para configuração do sessionhosts em hostpool.</span><span class="sxs-lookup"><span data-stu-id="46b0c-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="46b0c-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46b0c-170">-WorkspaceName</span></span>
<span data-ttu-id="46b0c-171">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="46b0c-171">Workspace Name</span></span>

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

### <span data-ttu-id="46b0c-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46b0c-172">-Confirm</span></span>
<span data-ttu-id="46b0c-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b0c-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b0c-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b0c-174">-WhatIf</span></span>
<span data-ttu-id="46b0c-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46b0c-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b0c-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46b0c-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b0c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b0c-177">CommonParameters</span></span>
<span data-ttu-id="46b0c-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b0c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b0c-179">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46b0c-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b0c-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46b0c-180">INPUTS</span></span>

## <span data-ttu-id="46b0c-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46b0c-181">OUTPUTS</span></span>

### <span data-ttu-id="46b0c-182">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="46b0c-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="46b0c-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46b0c-183">NOTES</span></span>

<span data-ttu-id="46b0c-184">ALIASES</span><span class="sxs-lookup"><span data-stu-id="46b0c-184">ALIASES</span></span>

## <span data-ttu-id="46b0c-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46b0c-185">RELATED LINKS</span></span>

