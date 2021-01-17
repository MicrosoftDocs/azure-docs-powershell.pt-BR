---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429411"
---
# <span data-ttu-id="9c247-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="9c247-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="9c247-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c247-102">SYNOPSIS</span></span>
<span data-ttu-id="9c247-103">Atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="9c247-103">Update a host pool.</span></span>

## <span data-ttu-id="9c247-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c247-104">SYNTAX</span></span>

### <span data-ttu-id="9c247-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c247-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c247-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9c247-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9c247-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c247-107">DESCRIPTION</span></span>
<span data-ttu-id="9c247-108">Atualizar um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="9c247-108">Update a host pool.</span></span>

## <span data-ttu-id="9c247-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c247-109">EXAMPLES</span></span>

### <span data-ttu-id="9c247-110">Exemplo 1: atualizar um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="9c247-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="9c247-111">Esse comando atualiza um HostPool de área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c247-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="9c247-112">OS</span><span class="sxs-lookup"><span data-stu-id="9c247-112">PARAMETERS</span></span>

### <span data-ttu-id="9c247-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="9c247-113">-CustomRdpProperty</span></span>
<span data-ttu-id="9c247-114">Propriedade RDP personalizada de HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-114">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c247-115">-DefaultProfile</span></span>
<span data-ttu-id="9c247-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c247-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c247-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9c247-117">-Description</span></span>
<span data-ttu-id="9c247-118">Descrição de HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-118">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c247-119">-FriendlyName</span></span>
<span data-ttu-id="9c247-120">Nome amigável de HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-120">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c247-121">-InputObject</span></span>
<span data-ttu-id="9c247-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9c247-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="9c247-123">-LoadBalancerType</span></span>
<span data-ttu-id="9c247-124">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="9c247-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="9c247-125">-MaxSessionLimit</span></span>
<span data-ttu-id="9c247-126">O limite máximo da sessão de HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c247-127">-Name</span></span>
<span data-ttu-id="9c247-128">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="9c247-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="9c247-130">Tipo de PersonalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="9c247-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="9c247-132">O tipo de tipo de grupo de aplicativos preferencial, padrão para grupo de aplicativos de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="9c247-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="9c247-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="9c247-134">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="9c247-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="9c247-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="9c247-136">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="9c247-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c247-137">-ResourceGroupName</span></span>
<span data-ttu-id="9c247-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c247-138">The name of the resource group.</span></span>
<span data-ttu-id="9c247-139">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9c247-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="9c247-140">-Ring</span></span>
<span data-ttu-id="9c247-141">O número de toques de HostPool.</span><span class="sxs-lookup"><span data-stu-id="9c247-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="9c247-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="9c247-143">URL para o servidor ADFS do cliente para autenticação de certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="9c247-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="9c247-144">-SsoClientId</span></span>
<span data-ttu-id="9c247-145">ClientId para a terceira parte confiável usada para emitir certificados de SSO do WVD.</span><span class="sxs-lookup"><span data-stu-id="9c247-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="9c247-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="9c247-147">Caminho para o cofre de chave do Azure que armazena o segredo usado para comunicação com o ADFS.</span><span class="sxs-lookup"><span data-stu-id="9c247-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="9c247-148">-SsoContext</span></span>
<span data-ttu-id="9c247-149">Caminho para o keyvault que contém ssoContext segredo.</span><span class="sxs-lookup"><span data-stu-id="9c247-149">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="9c247-150">-SsoSecretType</span></span>
<span data-ttu-id="9c247-151">O tipo de tipo de segredo de logon único.</span><span class="sxs-lookup"><span data-stu-id="9c247-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="9c247-152">-StartVMOnConnect</span></span>
<span data-ttu-id="9c247-153">O sinalizador para ativar/desativar o recurso StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="9c247-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="9c247-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c247-154">-SubscriptionId</span></span>
<span data-ttu-id="9c247-155">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9c247-155">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="9c247-156">-Tag</span></span>
<span data-ttu-id="9c247-157">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="9c247-157">tags to be updated</span></span>

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

### <span data-ttu-id="9c247-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c247-158">-ValidationEnvironment</span></span>
<span data-ttu-id="9c247-159">É ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="9c247-159">Is validation environment.</span></span>

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

### <span data-ttu-id="9c247-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="9c247-160">-VMTemplate</span></span>
<span data-ttu-id="9c247-161">Modelo de VM para configuração do sessionhosts em hostpool.</span><span class="sxs-lookup"><span data-stu-id="9c247-161">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c247-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c247-162">-Confirm</span></span>
<span data-ttu-id="9c247-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c247-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c247-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c247-164">-WhatIf</span></span>
<span data-ttu-id="9c247-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c247-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c247-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c247-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c247-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c247-167">CommonParameters</span></span>
<span data-ttu-id="9c247-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c247-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c247-169">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c247-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c247-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c247-170">INPUTS</span></span>

### <span data-ttu-id="9c247-171">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9c247-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9c247-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c247-172">OUTPUTS</span></span>

### <span data-ttu-id="9c247-173">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="9c247-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="9c247-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c247-174">NOTES</span></span>

<span data-ttu-id="9c247-175">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9c247-175">ALIASES</span></span>

<span data-ttu-id="9c247-176">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9c247-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c247-177">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9c247-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c247-178">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c247-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c247-179">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9c247-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c247-180">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="9c247-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9c247-181">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9c247-182">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9c247-183">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9c247-184">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9c247-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c247-185">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="9c247-186">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c247-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9c247-187">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9c247-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="9c247-188">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9c247-189">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9c247-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9c247-190">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="9c247-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9c247-191">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9c247-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9c247-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c247-192">RELATED LINKS</span></span>

