---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117700"
---
# <span data-ttu-id="55b4e-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="55b4e-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="55b4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="55b4e-103">Criar ou atualizar um pool de host.</span><span class="sxs-lookup"><span data-stu-id="55b4e-103">Create or update a host pool.</span></span>

## <span data-ttu-id="55b4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55b4e-104">SYNTAX</span></span>

### <span data-ttu-id="55b4e-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="55b4e-105">CreateExpanded (Default)</span></span>
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

### <span data-ttu-id="55b4e-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="55b4e-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55b4e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55b4e-107">DESCRIPTION</span></span>
<span data-ttu-id="55b4e-108">Criar ou atualizar um pool de host.</span><span class="sxs-lookup"><span data-stu-id="55b4e-108">Create or update a host pool.</span></span>

## <span data-ttu-id="55b4e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55b4e-109">EXAMPLES</span></span>

### <span data-ttu-id="55b4e-110">Exemplo 1: Criar um HostPool da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="55b4e-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="55b4e-111">Esse comando cria um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="55b4e-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="55b4e-112">Exemplo 1: Criar um HostPool da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="55b4e-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="55b4e-113">Esse comando cria um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="55b4e-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="55b4e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55b4e-114">PARAMETERS</span></span>

### <span data-ttu-id="55b4e-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="55b4e-115">-CustomRdpProperty</span></span>
<span data-ttu-id="55b4e-116">Propriedade rdp personalizada do HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="55b4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b4e-117">-DefaultProfile</span></span>
<span data-ttu-id="55b4e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55b4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b4e-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="55b4e-119">-Description</span></span>
<span data-ttu-id="55b4e-120">Descrição do HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="55b4e-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="55b4e-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="55b4e-122">Nome do grupo aplicativo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="55b4e-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="55b4e-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="55b4e-123">-ExpirationTime</span></span>
<span data-ttu-id="55b4e-124">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="55b4e-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="55b4e-125">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="55b4e-125">-FriendlyName</span></span>
<span data-ttu-id="55b4e-126">Nome amigável do HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="55b4e-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="55b4e-127">-HostPoolType</span></span>
<span data-ttu-id="55b4e-128">Tipo hostPool para área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="55b4e-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="55b4e-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="55b4e-129">-LoadBalancerType</span></span>
<span data-ttu-id="55b4e-130">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55b4e-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="55b4e-131">-Local</span><span class="sxs-lookup"><span data-stu-id="55b4e-131">-Location</span></span>
<span data-ttu-id="55b4e-132">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="55b4e-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="55b4e-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="55b4e-133">-MaxSessionLimit</span></span>
<span data-ttu-id="55b4e-134">O limite máximo de sessão do HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="55b4e-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="55b4e-135">-Name</span></span>
<span data-ttu-id="55b4e-136">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="55b4e-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="55b4e-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="55b4e-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="55b4e-138">Tipo personalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="55b4e-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="55b4e-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="55b4e-140">O tipo de grupo de aplicativos preferido, padrão para o Grupo de Aplicativos da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="55b4e-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="55b4e-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="55b4e-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="55b4e-142">A cadeia de caracteres codificada do token de registro base64.</span><span class="sxs-lookup"><span data-stu-id="55b4e-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="55b4e-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="55b4e-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="55b4e-144">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="55b4e-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="55b4e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b4e-145">-ResourceGroupName</span></span>
<span data-ttu-id="55b4e-146">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55b4e-146">The name of the resource group.</span></span>
<span data-ttu-id="55b4e-147">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="55b4e-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55b4e-148">-Toque</span><span class="sxs-lookup"><span data-stu-id="55b4e-148">-Ring</span></span>
<span data-ttu-id="55b4e-149">O número do anel de HostPool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="55b4e-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="55b4e-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="55b4e-151">URL para o servidor ADFS do cliente para assinar certificados WVD SSO.</span><span class="sxs-lookup"><span data-stu-id="55b4e-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="55b4e-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="55b4e-152">-SsoClientId</span></span>
<span data-ttu-id="55b4e-153">ClientId para a Parte Subjacente registrada usada para emitir certificados SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="55b4e-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="55b4e-154">-SsoClientSecáticaKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="55b4e-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="55b4e-155">Caminho para o Azure KeyVault armazenar o segredo usado para comunicação com o ADFS.</span><span class="sxs-lookup"><span data-stu-id="55b4e-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="55b4e-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="55b4e-156">-SsoContext</span></span>
<span data-ttu-id="55b4e-157">Caminho para o keyvault contendo segredo de ssoContext.</span><span class="sxs-lookup"><span data-stu-id="55b4e-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="55b4e-158">-SsoSecsectype</span><span class="sxs-lookup"><span data-stu-id="55b4e-158">-SsoSecretType</span></span>
<span data-ttu-id="55b4e-159">O tipo de sinal único no Tipo Secreto.</span><span class="sxs-lookup"><span data-stu-id="55b4e-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="55b4e-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="55b4e-160">-StartVMOnConnect</span></span>
<span data-ttu-id="55b4e-161">O sinalizador para ativar/desativar o recurso StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="55b4e-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="55b4e-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55b4e-162">-SubscriptionId</span></span>
<span data-ttu-id="55b4e-163">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="55b4e-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55b4e-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="55b4e-164">-Tag</span></span>
<span data-ttu-id="55b4e-165">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="55b4e-165">Resource tags.</span></span>

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

### <span data-ttu-id="55b4e-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="55b4e-166">-ValidationEnvironment</span></span>
<span data-ttu-id="55b4e-167">É o ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="55b4e-167">Is validation environment.</span></span>

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

### <span data-ttu-id="55b4e-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="55b4e-168">-VMTemplate</span></span>
<span data-ttu-id="55b4e-169">Modelo VM para configuração de sessionhosts dentro do hostpool.</span><span class="sxs-lookup"><span data-stu-id="55b4e-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="55b4e-170">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="55b4e-170">-WorkspaceName</span></span>
<span data-ttu-id="55b4e-171">Nome do Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="55b4e-171">Workspace Name</span></span>

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

### <span data-ttu-id="55b4e-172">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55b4e-172">-Confirm</span></span>
<span data-ttu-id="55b4e-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b4e-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b4e-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b4e-174">-WhatIf</span></span>
<span data-ttu-id="55b4e-175">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55b4e-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b4e-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55b4e-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b4e-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b4e-177">CommonParameters</span></span>
<span data-ttu-id="55b4e-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b4e-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b4e-179">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b4e-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b4e-180">Entradas</span><span class="sxs-lookup"><span data-stu-id="55b4e-180">INPUTS</span></span>

## <span data-ttu-id="55b4e-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="55b4e-181">OUTPUTS</span></span>

### <span data-ttu-id="55b4e-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="55b4e-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="55b4e-183">Notas</span><span class="sxs-lookup"><span data-stu-id="55b4e-183">NOTES</span></span>

<span data-ttu-id="55b4e-184">Aliases</span><span class="sxs-lookup"><span data-stu-id="55b4e-184">ALIASES</span></span>

## <span data-ttu-id="55b4e-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55b4e-185">RELATED LINKS</span></span>

