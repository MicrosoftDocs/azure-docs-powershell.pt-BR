---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776026"
---
# <span data-ttu-id="b315b-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="b315b-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="b315b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b315b-102">SYNOPSIS</span></span>
<span data-ttu-id="b315b-103">Retorna o local da malha solicitada.</span><span class="sxs-lookup"><span data-stu-id="b315b-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="b315b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b315b-104">SYNTAX</span></span>

### <span data-ttu-id="b315b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b315b-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b315b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b315b-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b315b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b315b-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b315b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b315b-108">DESCRIPTION</span></span>
<span data-ttu-id="b315b-109">Retorna o local da malha solicitada.</span><span class="sxs-lookup"><span data-stu-id="b315b-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="b315b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b315b-110">EXAMPLES</span></span>

### <span data-ttu-id="b315b-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="b315b-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="b315b-112">Obtenha uma lista de todos os locais da malha.</span><span class="sxs-lookup"><span data-stu-id="b315b-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="b315b-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="b315b-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="b315b-114">Obter um local com base no nome.</span><span class="sxs-lookup"><span data-stu-id="b315b-114">Get a location based on the name.</span></span>

## <span data-ttu-id="b315b-115">OS</span><span class="sxs-lookup"><span data-stu-id="b315b-115">PARAMETERS</span></span>

### <span data-ttu-id="b315b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b315b-116">-DefaultProfile</span></span>
<span data-ttu-id="b315b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b315b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b315b-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="b315b-118">-FabricLocation</span></span>
<span data-ttu-id="b315b-119">Localização do tecido.</span><span class="sxs-lookup"><span data-stu-id="b315b-119">Fabric location.</span></span>

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

### <span data-ttu-id="b315b-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b315b-120">-Filter</span></span>
<span data-ttu-id="b315b-121">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b315b-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="b315b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b315b-122">-InputObject</span></span>
<span data-ttu-id="b315b-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b315b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b315b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b315b-124">-PassThru</span></span>
<span data-ttu-id="b315b-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b315b-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b315b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b315b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b315b-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b315b-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="b315b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b315b-128">-SubscriptionId</span></span>
<span data-ttu-id="b315b-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b315b-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b315b-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b315b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b315b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b315b-131">CommonParameters</span></span>
<span data-ttu-id="b315b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b315b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b315b-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b315b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b315b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b315b-134">INPUTS</span></span>

### <span data-ttu-id="b315b-135">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b315b-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b315b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b315b-136">OUTPUTS</span></span>

### <span data-ttu-id="b315b-137">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="b315b-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="b315b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b315b-138">NOTES</span></span>

<span data-ttu-id="b315b-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b315b-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b315b-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b315b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b315b-141">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b315b-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b315b-142">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b315b-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b315b-143">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b315b-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b315b-144">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="b315b-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b315b-145">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="b315b-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b315b-146">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="b315b-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b315b-147">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="b315b-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b315b-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b315b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b315b-149">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b315b-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b315b-150">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b315b-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b315b-151">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b315b-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b315b-152">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b315b-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b315b-153">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b315b-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b315b-154">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="b315b-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b315b-155">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="b315b-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b315b-156">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b315b-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b315b-157">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="b315b-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b315b-158">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b315b-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b315b-159">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="b315b-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b315b-160">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b315b-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b315b-161">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b315b-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b315b-162">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b315b-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b315b-163">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b315b-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b315b-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b315b-164">RELATED LINKS</span></span>
