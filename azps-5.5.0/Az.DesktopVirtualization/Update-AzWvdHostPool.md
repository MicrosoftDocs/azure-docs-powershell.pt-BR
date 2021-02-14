---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116839"
---
# <span data-ttu-id="76f17-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="76f17-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="76f17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76f17-102">SYNOPSIS</span></span>
<span data-ttu-id="76f17-103">Atualizar um pool de host.</span><span class="sxs-lookup"><span data-stu-id="76f17-103">Update a host pool.</span></span>

## <span data-ttu-id="76f17-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76f17-104">SYNTAX</span></span>

### <span data-ttu-id="76f17-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76f17-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="76f17-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76f17-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="76f17-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="76f17-107">DESCRIPTION</span></span>
<span data-ttu-id="76f17-108">Atualizar um pool de host.</span><span class="sxs-lookup"><span data-stu-id="76f17-108">Update a host pool.</span></span>

## <span data-ttu-id="76f17-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76f17-109">EXAMPLES</span></span>

### <span data-ttu-id="76f17-110">Exemplo 1: Atualizar um HostPool virtual da área de trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="76f17-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="76f17-111">Este comando atualiza um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="76f17-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="76f17-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76f17-112">PARAMETERS</span></span>

### <span data-ttu-id="76f17-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="76f17-113">-CustomRdpProperty</span></span>
<span data-ttu-id="76f17-114">Propriedade rdp personalizada do HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="76f17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f17-115">-DefaultProfile</span></span>
<span data-ttu-id="76f17-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76f17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f17-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="76f17-117">-Description</span></span>
<span data-ttu-id="76f17-118">Descrição do HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="76f17-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="76f17-119">-FriendlyName</span></span>
<span data-ttu-id="76f17-120">Nome amigável do HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="76f17-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76f17-121">-InputObject</span></span>
<span data-ttu-id="76f17-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="76f17-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76f17-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="76f17-123">-LoadBalancerType</span></span>
<span data-ttu-id="76f17-124">O tipo do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="76f17-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="76f17-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="76f17-125">-MaxSessionLimit</span></span>
<span data-ttu-id="76f17-126">O limite máximo de sessão do HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="76f17-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="76f17-127">-Name</span></span>
<span data-ttu-id="76f17-128">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="76f17-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="76f17-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="76f17-130">Tipo personalDesktopAssignment para HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="76f17-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="76f17-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="76f17-132">O tipo de grupo de aplicativos preferido, padrão para o Grupo de Aplicativos da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="76f17-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="76f17-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="76f17-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="76f17-134">Tempo de expiração do token de registro.</span><span class="sxs-lookup"><span data-stu-id="76f17-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="76f17-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="76f17-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="76f17-136">O tipo de redefinição do token.</span><span class="sxs-lookup"><span data-stu-id="76f17-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="76f17-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f17-137">-ResourceGroupName</span></span>
<span data-ttu-id="76f17-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76f17-138">The name of the resource group.</span></span>
<span data-ttu-id="76f17-139">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76f17-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76f17-140">-Toque</span><span class="sxs-lookup"><span data-stu-id="76f17-140">-Ring</span></span>
<span data-ttu-id="76f17-141">O número do anel de HostPool.</span><span class="sxs-lookup"><span data-stu-id="76f17-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="76f17-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="76f17-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="76f17-143">URL para o servidor ADFS do cliente para assinar certificados WVD SSO.</span><span class="sxs-lookup"><span data-stu-id="76f17-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="76f17-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="76f17-144">-SsoClientId</span></span>
<span data-ttu-id="76f17-145">ClientId para a Parte Subjacente registrada usada para emitir certificados SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="76f17-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="76f17-146">-SsoClientSecáticaKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="76f17-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="76f17-147">Caminho para o Azure KeyVault armazenar o segredo usado para comunicação com o ADFS.</span><span class="sxs-lookup"><span data-stu-id="76f17-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="76f17-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="76f17-148">-SsoContext</span></span>
<span data-ttu-id="76f17-149">Caminho para o keyvault contendo segredo de ssoContext.</span><span class="sxs-lookup"><span data-stu-id="76f17-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="76f17-150">-SsoSecsectype</span><span class="sxs-lookup"><span data-stu-id="76f17-150">-SsoSecretType</span></span>
<span data-ttu-id="76f17-151">O tipo de sinal único no Tipo Secreto.</span><span class="sxs-lookup"><span data-stu-id="76f17-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="76f17-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="76f17-152">-StartVMOnConnect</span></span>
<span data-ttu-id="76f17-153">O sinalizador para ativar/desativar o recurso StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="76f17-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="76f17-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76f17-154">-SubscriptionId</span></span>
<span data-ttu-id="76f17-155">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="76f17-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="76f17-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="76f17-156">-Tag</span></span>
<span data-ttu-id="76f17-157">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="76f17-157">tags to be updated</span></span>

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

### <span data-ttu-id="76f17-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="76f17-158">-ValidationEnvironment</span></span>
<span data-ttu-id="76f17-159">É o ambiente de validação.</span><span class="sxs-lookup"><span data-stu-id="76f17-159">Is validation environment.</span></span>

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

### <span data-ttu-id="76f17-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="76f17-160">-VMTemplate</span></span>
<span data-ttu-id="76f17-161">Modelo VM para configuração de sessionhosts dentro do hostpool.</span><span class="sxs-lookup"><span data-stu-id="76f17-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="76f17-162">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76f17-162">-Confirm</span></span>
<span data-ttu-id="76f17-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f17-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f17-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f17-164">-WhatIf</span></span>
<span data-ttu-id="76f17-165">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76f17-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f17-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76f17-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f17-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f17-167">CommonParameters</span></span>
<span data-ttu-id="76f17-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f17-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f17-169">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76f17-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f17-170">Entradas</span><span class="sxs-lookup"><span data-stu-id="76f17-170">INPUTS</span></span>

### <span data-ttu-id="76f17-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="76f17-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="76f17-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="76f17-172">OUTPUTS</span></span>

### <span data-ttu-id="76f17-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="76f17-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="76f17-174">Notas</span><span class="sxs-lookup"><span data-stu-id="76f17-174">NOTES</span></span>

<span data-ttu-id="76f17-175">Aliases</span><span class="sxs-lookup"><span data-stu-id="76f17-175">ALIASES</span></span>

<span data-ttu-id="76f17-176">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="76f17-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76f17-177">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="76f17-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76f17-178">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76f17-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76f17-179">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="76f17-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76f17-180">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="76f17-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="76f17-181">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="76f17-182">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="76f17-183">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="76f17-184">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="76f17-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76f17-185">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="76f17-186">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76f17-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76f17-187">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76f17-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="76f17-188">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="76f17-189">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="76f17-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76f17-190">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="76f17-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="76f17-191">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="76f17-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="76f17-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76f17-192">RELATED LINKS</span></span>

