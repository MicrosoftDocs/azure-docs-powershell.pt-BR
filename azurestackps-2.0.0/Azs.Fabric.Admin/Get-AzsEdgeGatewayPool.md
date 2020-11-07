---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776037"
---
# <span data-ttu-id="b0d4e-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="b0d4e-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="b0d4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0d4e-102">SYNOPSIS</span></span>


## <span data-ttu-id="b0d4e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0d4e-103">SYNTAX</span></span>

### <span data-ttu-id="b0d4e-104">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0d4e-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b0d4e-105">Obter</span><span class="sxs-lookup"><span data-stu-id="b0d4e-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b0d4e-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0d4e-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0d4e-107">DESCRIPTION</span></span>


## <span data-ttu-id="b0d4e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0d4e-108">EXAMPLES</span></span>

### <span data-ttu-id="b0d4e-109">Exemplo 1: obter uma lista de todos os pools de gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="b0d4e-110">Obter uma lista de todos os pools de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="b0d4e-111">Exemplo 2: obter um pool específico do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="b0d4e-112">Obter um pool específico do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="b0d4e-113">OS</span><span class="sxs-lookup"><span data-stu-id="b0d4e-113">PARAMETERS</span></span>

### <span data-ttu-id="b0d4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d4e-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="b0d4e-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b0d4e-115">-Filter</span></span>


```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0d4e-116">-InputObject</span></span>
<span data-ttu-id="b0d4e-117">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b0d4e-118">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0d4e-119">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0d4e-120">-PassThru</span></span>


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

### <span data-ttu-id="b0d4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d4e-121">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0d4e-122">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b0d4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d4e-123">CommonParameters</span></span>
<span data-ttu-id="b0d4e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d4e-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d4e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d4e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0d4e-126">INPUTS</span></span>

### <span data-ttu-id="b0d4e-127">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b0d4e-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b0d4e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0d4e-128">OUTPUTS</span></span>

### <span data-ttu-id="b0d4e-129">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="b0d4e-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="b0d4e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0d4e-130">NOTES</span></span>

<span data-ttu-id="b0d4e-131">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0d4e-132">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b0d4e-133">INPUTobject <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="b0d4e-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="b0d4e-134">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b0d4e-135">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b0d4e-136">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b0d4e-137">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b0d4e-138">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b0d4e-139">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b0d4e-140">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b0d4e-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0d4e-141">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b0d4e-142">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b0d4e-143">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b0d4e-144">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b0d4e-145">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b0d4e-146">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b0d4e-147">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b0d4e-148">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b0d4e-149">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b0d4e-150">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b0d4e-151">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b0d4e-152">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b0d4e-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0d4e-154">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0d4e-155">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0d4e-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b0d4e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0d4e-156">RELATED LINKS</span></span>
