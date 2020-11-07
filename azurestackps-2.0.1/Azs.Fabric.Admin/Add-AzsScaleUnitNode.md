---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945379"
---
# <span data-ttu-id="6944d-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6944d-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6944d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6944d-102">SYNOPSIS</span></span>
<span data-ttu-id="6944d-103">Dimensiona uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="6944d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6944d-104">SYNTAX</span></span>

### <span data-ttu-id="6944d-105">ScaleExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="6944d-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6944d-106">Chegam</span><span class="sxs-lookup"><span data-stu-id="6944d-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6944d-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6944d-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6944d-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6944d-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6944d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6944d-109">DESCRIPTION</span></span>
<span data-ttu-id="6944d-110">Dimensiona uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="6944d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6944d-111">EXAMPLES</span></span>

### <span data-ttu-id="6944d-112">Exemplo 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6944d-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="6944d-113">Adicione um novo nó de unidade de escala ao seu cluster de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="6944d-114">OS</span><span class="sxs-lookup"><span data-stu-id="6944d-114">PARAMETERS</span></span>

### <span data-ttu-id="6944d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6944d-115">-AsJob</span></span>
<span data-ttu-id="6944d-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6944d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6944d-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="6944d-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="6944d-118">Sinalizador indica se a operação deve aguardar que o armazenamento convergesse antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="6944d-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6944d-119">-DefaultProfile</span></span>
<span data-ttu-id="6944d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6944d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6944d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6944d-121">-InputObject</span></span>
<span data-ttu-id="6944d-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6944d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-123">-Local</span><span class="sxs-lookup"><span data-stu-id="6944d-123">-Location</span></span>
<span data-ttu-id="6944d-124">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6944d-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="6944d-125">-NodeList</span></span>
<span data-ttu-id="6944d-126">Lista de nós na unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="6944d-127">Para construir, consulte a seção notas para propriedades NODELIST e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6944d-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6944d-128">-NoWait</span></span>
<span data-ttu-id="6944d-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6944d-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6944d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6944d-130">-PassThru</span></span>
<span data-ttu-id="6944d-131">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6944d-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6944d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6944d-132">-ResourceGroupName</span></span>
<span data-ttu-id="6944d-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6944d-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6944d-134">-ScaleUnit</span></span>
<span data-ttu-id="6944d-135">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="6944d-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="6944d-137">Uma lista de dados de entrada que permite adicionar um conjunto de nós de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="6944d-138">Para construir, consulte a seção notas para propriedades SCALEUNITNODEPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6944d-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6944d-139">-SubscriptionId</span></span>
<span data-ttu-id="6944d-140">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6944d-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6944d-141">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6944d-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6944d-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6944d-142">-Confirm</span></span>
<span data-ttu-id="6944d-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6944d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6944d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6944d-144">-WhatIf</span></span>
<span data-ttu-id="6944d-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6944d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6944d-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6944d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6944d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6944d-147">CommonParameters</span></span>
<span data-ttu-id="6944d-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6944d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6944d-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6944d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6944d-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6944d-150">INPUTS</span></span>

### <span data-ttu-id="6944d-151">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="6944d-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="6944d-152">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6944d-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6944d-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6944d-153">OUTPUTS</span></span>

### <span data-ttu-id="6944d-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6944d-154">System.Boolean</span></span>



## <span data-ttu-id="6944d-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6944d-155">NOTES</span></span>

<span data-ttu-id="6944d-156">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6944d-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6944d-157">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6944d-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6944d-158">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6944d-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6944d-159">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6944d-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6944d-160">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="6944d-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6944d-161">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="6944d-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6944d-162">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="6944d-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6944d-163">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="6944d-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6944d-164">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="6944d-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6944d-165">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6944d-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6944d-166">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6944d-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6944d-167">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6944d-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6944d-168">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6944d-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6944d-169">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="6944d-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6944d-170">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="6944d-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6944d-171">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="6944d-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6944d-172">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="6944d-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6944d-173">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6944d-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6944d-174">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6944d-175">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6944d-176">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="6944d-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6944d-177">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6944d-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6944d-178">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6944d-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6944d-179">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6944d-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6944d-180">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6944d-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="6944d-181">NODELIST <IScaleOutScaleUnitParameters [] >: lista de nós na unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="6944d-182">`[BmciPv4Address <String>]`: BMC address da máquina física.</span><span class="sxs-lookup"><span data-stu-id="6944d-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="6944d-183">`[ComputerName <String>]`: Nome de computador da máquina física.</span><span class="sxs-lookup"><span data-stu-id="6944d-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="6944d-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : uma lista de dados de entrada que permite adicionar um conjunto de nós de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="6944d-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indica se a operação deve aguardar até que o armazenamento convergesse antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="6944d-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="6944d-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Lista de nós na unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6944d-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="6944d-187">`[BmciPv4Address <String>]`: BMC address da máquina física.</span><span class="sxs-lookup"><span data-stu-id="6944d-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="6944d-188">`[ComputerName <String>]`: Nome de computador da máquina física.</span><span class="sxs-lookup"><span data-stu-id="6944d-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="6944d-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6944d-189">RELATED LINKS</span></span>

