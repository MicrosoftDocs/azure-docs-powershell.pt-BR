---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945302"
---
# <span data-ttu-id="cbed1-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="cbed1-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="cbed1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbed1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbed1-103">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="cbed1-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="cbed1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbed1-104">SYNTAX</span></span>

### <span data-ttu-id="cbed1-105">RepairExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbed1-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cbed1-106">Conserto</span><span class="sxs-lookup"><span data-stu-id="cbed1-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cbed1-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbed1-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cbed1-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cbed1-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cbed1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbed1-109">DESCRIPTION</span></span>
<span data-ttu-id="cbed1-110">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="cbed1-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="cbed1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbed1-111">EXAMPLES</span></span>

### <span data-ttu-id="cbed1-112">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="cbed1-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="cbed1-113">Reparar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="cbed1-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="cbed1-114">OS</span><span class="sxs-lookup"><span data-stu-id="cbed1-114">PARAMETERS</span></span>

### <span data-ttu-id="cbed1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbed1-115">-AsJob</span></span>
<span data-ttu-id="cbed1-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cbed1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cbed1-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="cbed1-117">-BareMetalNode</span></span>
<span data-ttu-id="cbed1-118">Descrição de um nó bare metal usado para operação de dimensionamento em um cluster.</span><span class="sxs-lookup"><span data-stu-id="cbed1-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="cbed1-119">Para construir, consulte a seção notas para propriedades BAREMETALNODE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cbed1-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-120">-Biosversion</span><span class="sxs-lookup"><span data-stu-id="cbed1-120">-BiosVersion</span></span>
<span data-ttu-id="cbed1-121">Versão do BIOS da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="cbed1-122">-BmciPv4Address</span></span>
<span data-ttu-id="cbed1-123">Endereço BMC da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cbed1-124">-ClusterName</span></span>
<span data-ttu-id="cbed1-125">Nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="cbed1-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="cbed1-126">-ComputerName</span></span>
<span data-ttu-id="cbed1-127">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="cbed1-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbed1-128">-DefaultProfile</span></span>
<span data-ttu-id="cbed1-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbed1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbed1-130">-Force</span><span class="sxs-lookup"><span data-stu-id="cbed1-130">-Force</span></span>
<span data-ttu-id="cbed1-131">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="cbed1-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cbed1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbed1-132">-InputObject</span></span>
<span data-ttu-id="cbed1-133">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cbed1-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-134">-Local</span><span class="sxs-lookup"><span data-stu-id="cbed1-134">-Location</span></span>
<span data-ttu-id="cbed1-135">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbed1-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="cbed1-136">-MacAddress</span></span>
<span data-ttu-id="cbed1-137">Nome do endereço MAC do nó bare metal.</span><span class="sxs-lookup"><span data-stu-id="cbed1-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-138">-Model</span><span class="sxs-lookup"><span data-stu-id="cbed1-138">-Model</span></span>
<span data-ttu-id="cbed1-139">Modelo da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbed1-140">-Name</span></span>
<span data-ttu-id="cbed1-141">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="cbed1-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-142">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cbed1-142">-NoWait</span></span>
<span data-ttu-id="cbed1-143">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cbed1-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cbed1-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbed1-144">-PassThru</span></span>
<span data-ttu-id="cbed1-145">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cbed1-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cbed1-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbed1-146">-ResourceGroupName</span></span>
<span data-ttu-id="cbed1-147">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbed1-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="cbed1-148">-SerialNumber</span></span>
<span data-ttu-id="cbed1-149">Número de série do computador físico.</span><span class="sxs-lookup"><span data-stu-id="cbed1-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbed1-150">-SubscriptionId</span></span>
<span data-ttu-id="cbed1-151">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cbed1-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cbed1-152">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbed1-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-153">-Fornecedor</span><span class="sxs-lookup"><span data-stu-id="cbed1-153">-Vendor</span></span>
<span data-ttu-id="cbed1-154">Fornecedor da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cbed1-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbed1-155">-Confirm</span></span>
<span data-ttu-id="cbed1-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbed1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbed1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbed1-157">-WhatIf</span></span>
<span data-ttu-id="cbed1-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbed1-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbed1-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbed1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbed1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbed1-160">CommonParameters</span></span>
<span data-ttu-id="cbed1-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbed1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbed1-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbed1-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbed1-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbed1-163">INPUTS</span></span>

### <span data-ttu-id="cbed1-164">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="cbed1-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="cbed1-165">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cbed1-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cbed1-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbed1-166">OUTPUTS</span></span>

### <span data-ttu-id="cbed1-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbed1-167">System.Boolean</span></span>



## <span data-ttu-id="cbed1-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbed1-168">NOTES</span></span>

<span data-ttu-id="cbed1-169">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cbed1-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbed1-170">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbed1-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cbed1-171">BAREMETALNODE <IBareMetalNodeDescription> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="cbed1-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="cbed1-172">`[BiosVersion <String>]`: Versão do BIOS do computador físico.</span><span class="sxs-lookup"><span data-stu-id="cbed1-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="cbed1-173">`[BmciPv4Address <String>]`: BMC address da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="cbed1-174">`[ClusterName <String>]`: Nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="cbed1-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="cbed1-175">`[ComputerName <String>]`: Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="cbed1-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="cbed1-176">`[MacAddress <String>]`: Nome do endereço MAC do nó bare metal.</span><span class="sxs-lookup"><span data-stu-id="cbed1-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="cbed1-177">`[Model <String>]`: Modelo da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="cbed1-178">`[SerialNumber <String>]`: Número de série do computador físico.</span><span class="sxs-lookup"><span data-stu-id="cbed1-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="cbed1-179">`[Vendor <String>]`: Fornecedor da máquina física.</span><span class="sxs-lookup"><span data-stu-id="cbed1-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="cbed1-180">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="cbed1-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbed1-181">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbed1-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cbed1-182">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="cbed1-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cbed1-183">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="cbed1-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cbed1-184">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="cbed1-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cbed1-185">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="cbed1-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cbed1-186">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="cbed1-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cbed1-187">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cbed1-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbed1-188">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="cbed1-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cbed1-189">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="cbed1-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cbed1-190">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbed1-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cbed1-191">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="cbed1-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cbed1-192">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="cbed1-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cbed1-193">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="cbed1-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cbed1-194">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="cbed1-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cbed1-195">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbed1-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cbed1-196">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="cbed1-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cbed1-197">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="cbed1-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cbed1-198">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="cbed1-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cbed1-199">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbed1-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cbed1-200">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbed1-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cbed1-201">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cbed1-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cbed1-202">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbed1-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cbed1-203">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbed1-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cbed1-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbed1-204">RELATED LINKS</span></span>

