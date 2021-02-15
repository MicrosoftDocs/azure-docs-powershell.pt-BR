---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118857"
---
# <span data-ttu-id="aec1c-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="aec1c-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="aec1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aec1c-102">SYNOPSIS</span></span>
<span data-ttu-id="aec1c-103">Atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-103">Update a private cloud</span></span>

## <span data-ttu-id="aec1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec1c-104">SYNTAX</span></span>

### <span data-ttu-id="aec1c-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aec1c-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aec1c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aec1c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aec1c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aec1c-107">DESCRIPTION</span></span>
<span data-ttu-id="aec1c-108">Atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-108">Update a private cloud</span></span>

## <span data-ttu-id="aec1c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aec1c-109">EXAMPLES</span></span>

### <span data-ttu-id="aec1c-110">Exemplo 1: Atualizar o tamanho da nuvem particular por nome</span><span class="sxs-lookup"><span data-stu-id="aec1c-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="aec1c-111">Tamanho da atualização da nuvem privada por nome</span><span class="sxs-lookup"><span data-stu-id="aec1c-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="aec1c-112">Exemplo 2: Tamanho da atualização da nuvem privada por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="aec1c-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="aec1c-113">Tamanho da atualização da nuvem privada por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="aec1c-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="aec1c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aec1c-114">PARAMETERS</span></span>

### <span data-ttu-id="aec1c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aec1c-115">-AsJob</span></span>
<span data-ttu-id="aec1c-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="aec1c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aec1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec1c-117">-DefaultProfile</span></span>
<span data-ttu-id="aec1c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aec1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec1c-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="aec1c-119">-IdentitySource</span></span>
<span data-ttu-id="aec1c-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="aec1c-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec1c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aec1c-121">-InputObject</span></span>
<span data-ttu-id="aec1c-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="aec1c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aec1c-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="aec1c-123">-Internet</span></span>
<span data-ttu-id="aec1c-124">A conectividade com a Internet está habilitada ou desabilitada</span><span class="sxs-lookup"><span data-stu-id="aec1c-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec1c-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="aec1c-125">-ManagementClusterSize</span></span>
<span data-ttu-id="aec1c-126">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="aec1c-126">The cluster size</span></span>

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

### <span data-ttu-id="aec1c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="aec1c-127">-Name</span></span>
<span data-ttu-id="aec1c-128">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec1c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aec1c-129">-NoWait</span></span>
<span data-ttu-id="aec1c-130">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="aec1c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aec1c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec1c-131">-ResourceGroupName</span></span>
<span data-ttu-id="aec1c-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aec1c-132">The name of the resource group.</span></span>
<span data-ttu-id="aec1c-133">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aec1c-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aec1c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aec1c-134">-SubscriptionId</span></span>
<span data-ttu-id="aec1c-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="aec1c-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aec1c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="aec1c-136">-Tag</span></span>
<span data-ttu-id="aec1c-137">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="aec1c-137">Resource tags.</span></span>

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

### <span data-ttu-id="aec1c-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aec1c-138">-Confirm</span></span>
<span data-ttu-id="aec1c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec1c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec1c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec1c-140">-WhatIf</span></span>
<span data-ttu-id="aec1c-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aec1c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec1c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aec1c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec1c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec1c-143">CommonParameters</span></span>
<span data-ttu-id="aec1c-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec1c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec1c-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aec1c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec1c-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="aec1c-146">INPUTS</span></span>

### <span data-ttu-id="aec1c-147">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="aec1c-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="aec1c-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="aec1c-148">OUTPUTS</span></span>

### <span data-ttu-id="aec1c-149">Microsoft.Azure.PowerShell.Cmdlets.VCloud.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="aec1c-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="aec1c-150">Notas</span><span class="sxs-lookup"><span data-stu-id="aec1c-150">NOTES</span></span>

<span data-ttu-id="aec1c-151">Aliases</span><span class="sxs-lookup"><span data-stu-id="aec1c-151">ALIASES</span></span>

<span data-ttu-id="aec1c-152">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="aec1c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aec1c-153">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="aec1c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aec1c-154">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aec1c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aec1c-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="aec1c-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="aec1c-156">`[Alias <String>]`: Nome do NetBIOS do domínio</span><span class="sxs-lookup"><span data-stu-id="aec1c-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="aec1c-157">`[BaseGroupDn <String>]`: O nome diferenciado da base para grupos</span><span class="sxs-lookup"><span data-stu-id="aec1c-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="aec1c-158">`[BaseUserDn <String>]`: O nome diferenciado da base para os usuários</span><span class="sxs-lookup"><span data-stu-id="aec1c-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="aec1c-159">`[Domain <String>]`: o nome dns do domínio</span><span class="sxs-lookup"><span data-stu-id="aec1c-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="aec1c-160">`[Name <String>]`: o nome da fonte de identidade</span><span class="sxs-lookup"><span data-stu-id="aec1c-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="aec1c-161">`[Password <String>]`: A senha do usuário do Active Directory com um mínimo de acesso somente leitura ao DN Base para usuários e grupos.</span><span class="sxs-lookup"><span data-stu-id="aec1c-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="aec1c-162">`[PrimaryServer <String>]`: URL do servidor principal</span><span class="sxs-lookup"><span data-stu-id="aec1c-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="aec1c-163">`[SecondaryServer <String>]`: URL do servidor secundário</span><span class="sxs-lookup"><span data-stu-id="aec1c-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="aec1c-164">`[Ssl <SslEnum?>]`: Proteger a comunicação LDAP usando certificado SSL (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="aec1c-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="aec1c-165">`[Username <String>]`: A ID de um usuário do Active Directory com acesso mínimo somente leitura ao DN Base para usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="aec1c-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="aec1c-166">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="aec1c-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aec1c-167">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="aec1c-168">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="aec1c-169">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="aec1c-170">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aec1c-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aec1c-171">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="aec1c-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="aec1c-172">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="aec1c-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="aec1c-173">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aec1c-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aec1c-174">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aec1c-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="aec1c-175">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="aec1c-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="aec1c-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aec1c-176">RELATED LINKS</span></span>

