---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946969"
---
# <span data-ttu-id="e9188-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="e9188-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="e9188-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9188-102">SYNOPSIS</span></span>
<span data-ttu-id="e9188-103">Retorne o pool de IP solicitado.</span><span class="sxs-lookup"><span data-stu-id="e9188-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="e9188-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9188-104">SYNTAX</span></span>

### <span data-ttu-id="e9188-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9188-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e9188-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e9188-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e9188-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e9188-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e9188-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9188-108">DESCRIPTION</span></span>
<span data-ttu-id="e9188-109">Retorne o pool de IP solicitado.</span><span class="sxs-lookup"><span data-stu-id="e9188-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="e9188-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9188-110">EXAMPLES</span></span>

### <span data-ttu-id="e9188-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="e9188-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="e9188-112">Obtenha todos os pools de IP da infra-estrutura.</span><span class="sxs-lookup"><span data-stu-id="e9188-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="e9188-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="e9188-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="e9188-114">Obter um pool de IP de infraestrutura com base no nome.</span><span class="sxs-lookup"><span data-stu-id="e9188-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="e9188-115">OS</span><span class="sxs-lookup"><span data-stu-id="e9188-115">PARAMETERS</span></span>

### <span data-ttu-id="e9188-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9188-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="e9188-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e9188-117">-Filter</span></span>
<span data-ttu-id="e9188-118">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e9188-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="e9188-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9188-119">-InputObject</span></span>
<span data-ttu-id="e9188-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e9188-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e9188-121">-Local</span><span class="sxs-lookup"><span data-stu-id="e9188-121">-Location</span></span>
<span data-ttu-id="e9188-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9188-122">Location of the resource.</span></span>

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

### <span data-ttu-id="e9188-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9188-123">-Name</span></span>
<span data-ttu-id="e9188-124">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="e9188-124">IP pool name.</span></span>

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

### <span data-ttu-id="e9188-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9188-125">-PassThru</span></span>
<span data-ttu-id="e9188-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e9188-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e9188-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9188-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9188-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9188-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="e9188-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9188-129">-SubscriptionId</span></span>
<span data-ttu-id="e9188-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e9188-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9188-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9188-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e9188-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9188-132">CommonParameters</span></span>
<span data-ttu-id="e9188-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9188-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9188-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9188-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9188-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9188-135">INPUTS</span></span>

### <span data-ttu-id="e9188-136">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e9188-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e9188-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9188-137">OUTPUTS</span></span>

### <span data-ttu-id="e9188-138">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="e9188-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="e9188-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9188-139">NOTES</span></span>

<span data-ttu-id="e9188-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e9188-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9188-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9188-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e9188-142">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e9188-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e9188-143">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9188-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e9188-144">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="e9188-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e9188-145">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="e9188-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e9188-146">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="e9188-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e9188-147">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="e9188-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e9188-148">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="e9188-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e9188-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e9188-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e9188-150">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="e9188-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e9188-151">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="e9188-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e9188-152">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9188-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e9188-153">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="e9188-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e9188-154">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="e9188-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e9188-155">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="e9188-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e9188-156">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="e9188-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e9188-157">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9188-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e9188-158">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="e9188-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e9188-159">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e9188-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e9188-160">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="e9188-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e9188-161">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9188-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="e9188-162">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9188-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e9188-163">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e9188-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e9188-164">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9188-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e9188-165">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9188-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e9188-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9188-166">RELATED LINKS</span></span>

