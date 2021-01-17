---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427844"
---
# <span data-ttu-id="3971c-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="3971c-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="3971c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3971c-102">SYNOPSIS</span></span>
<span data-ttu-id="3971c-103">Atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-103">Update a private cloud</span></span>

## <span data-ttu-id="3971c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3971c-104">SYNTAX</span></span>

### <span data-ttu-id="3971c-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="3971c-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3971c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3971c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3971c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3971c-107">DESCRIPTION</span></span>
<span data-ttu-id="3971c-108">Atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-108">Update a private cloud</span></span>

## <span data-ttu-id="3971c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3971c-109">EXAMPLES</span></span>

### <span data-ttu-id="3971c-110">Exemplo 1: atualizar o tamanho da nuvem privada por nome</span><span class="sxs-lookup"><span data-stu-id="3971c-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="3971c-111">Atualizar o tamanho da nuvem privada por nome</span><span class="sxs-lookup"><span data-stu-id="3971c-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="3971c-112">Exemplo 2: atualizar o tamanho da nuvem privada por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="3971c-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="3971c-113">Atualizar o tamanho da nuvem privada por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="3971c-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="3971c-114">OS</span><span class="sxs-lookup"><span data-stu-id="3971c-114">PARAMETERS</span></span>

### <span data-ttu-id="3971c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3971c-115">-AsJob</span></span>
<span data-ttu-id="3971c-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3971c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3971c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3971c-117">-DefaultProfile</span></span>
<span data-ttu-id="3971c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3971c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3971c-119">-Identityto</span><span class="sxs-lookup"><span data-stu-id="3971c-119">-IdentitySource</span></span>
<span data-ttu-id="3971c-120">vCenter fontes de identidade do vCenter Sign-on para construir, consulte a seção observações para propriedades de identidade ou criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3971c-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3971c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3971c-121">-InputObject</span></span>
<span data-ttu-id="3971c-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3971c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3971c-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="3971c-123">-Internet</span></span>
<span data-ttu-id="3971c-124">A conectividade com a Internet está habilitada ou desabilitada</span><span class="sxs-lookup"><span data-stu-id="3971c-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3971c-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="3971c-125">-ManagementClusterSize</span></span>
<span data-ttu-id="3971c-126">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="3971c-126">The cluster size</span></span>

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

### <span data-ttu-id="3971c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3971c-127">-Name</span></span>
<span data-ttu-id="3971c-128">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="3971c-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3971c-129">-NoWait</span></span>
<span data-ttu-id="3971c-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3971c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3971c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3971c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3971c-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3971c-132">The name of the resource group.</span></span>
<span data-ttu-id="3971c-133">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3971c-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3971c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3971c-134">-SubscriptionId</span></span>
<span data-ttu-id="3971c-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3971c-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3971c-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="3971c-136">-Tag</span></span>
<span data-ttu-id="3971c-137">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="3971c-137">Resource tags.</span></span>

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

### <span data-ttu-id="3971c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3971c-138">-Confirm</span></span>
<span data-ttu-id="3971c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3971c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3971c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3971c-140">-WhatIf</span></span>
<span data-ttu-id="3971c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3971c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3971c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3971c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3971c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3971c-143">CommonParameters</span></span>
<span data-ttu-id="3971c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3971c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3971c-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3971c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3971c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3971c-146">INPUTS</span></span>

### <span data-ttu-id="3971c-147">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="3971c-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="3971c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3971c-148">OUTPUTS</span></span>

### <span data-ttu-id="3971c-149">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="3971c-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="3971c-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3971c-150">NOTES</span></span>

<span data-ttu-id="3971c-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3971c-151">ALIASES</span></span>

<span data-ttu-id="3971c-152">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3971c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3971c-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3971c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3971c-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3971c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3971c-155">IDENTIDADEs <IIdentityie [] >: fontes de identidade do vCenter Single Sign-on</span><span class="sxs-lookup"><span data-stu-id="3971c-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="3971c-156">`[Alias <String>]`: O nome NetBIOS do domínio</span><span class="sxs-lookup"><span data-stu-id="3971c-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="3971c-157">`[BaseGroupDn <String>]`: O nome diferenciado da base para grupos</span><span class="sxs-lookup"><span data-stu-id="3971c-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="3971c-158">`[BaseUserDn <String>]`: O nome diferenciado da base dos usuários</span><span class="sxs-lookup"><span data-stu-id="3971c-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="3971c-159">`[Domain <String>]`: O nome DNS do domínio</span><span class="sxs-lookup"><span data-stu-id="3971c-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="3971c-160">`[Name <String>]`: O nome da fonte de identidade</span><span class="sxs-lookup"><span data-stu-id="3971c-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="3971c-161">`[Password <String>]`: A senha do usuário do Active Directory com um mínimo de acesso somente leitura ao DN base para usuários e grupos.</span><span class="sxs-lookup"><span data-stu-id="3971c-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="3971c-162">`[PrimaryServer <String>]`: URL do servidor primário</span><span class="sxs-lookup"><span data-stu-id="3971c-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="3971c-163">`[SecondaryServer <String>]`: URL do servidor secundário</span><span class="sxs-lookup"><span data-stu-id="3971c-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="3971c-164">`[Ssl <SslEnum?>]`: Proteger a comunicação LDAP usando o certificado SSL (LDAPs)</span><span class="sxs-lookup"><span data-stu-id="3971c-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="3971c-165">`[Username <String>]`: A ID de um usuário do Active Directory com um mínimo de acesso somente leitura ao DN base para usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="3971c-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="3971c-166">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3971c-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3971c-167">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="3971c-168">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="3971c-169">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="3971c-170">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3971c-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3971c-171">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="3971c-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="3971c-172">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="3971c-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="3971c-173">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3971c-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3971c-174">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3971c-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="3971c-175">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3971c-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3971c-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3971c-176">RELATED LINKS</span></span>

