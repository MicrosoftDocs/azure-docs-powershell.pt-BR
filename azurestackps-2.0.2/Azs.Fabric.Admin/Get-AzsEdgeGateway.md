---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946625"
---
# <span data-ttu-id="9b21e-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="9b21e-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="9b21e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b21e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b21e-103">Retorna o gateway de borda solicitado.</span><span class="sxs-lookup"><span data-stu-id="9b21e-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="9b21e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b21e-104">SYNTAX</span></span>

### <span data-ttu-id="9b21e-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b21e-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9b21e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9b21e-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9b21e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b21e-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9b21e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b21e-108">DESCRIPTION</span></span>
<span data-ttu-id="9b21e-109">Retorna o gateway de borda solicitado.</span><span class="sxs-lookup"><span data-stu-id="9b21e-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="9b21e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b21e-110">EXAMPLES</span></span>

### <span data-ttu-id="9b21e-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="9b21e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="9b21e-112">Retorna a lista de todos os gateways de borda em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="9b21e-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="9b21e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9b21e-113">PARAMETERS</span></span>

### <span data-ttu-id="9b21e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b21e-114">-DefaultProfile</span></span>
<span data-ttu-id="9b21e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b21e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b21e-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9b21e-116">-Filter</span></span>
<span data-ttu-id="9b21e-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="9b21e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="9b21e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b21e-118">-InputObject</span></span>
<span data-ttu-id="9b21e-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9b21e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b21e-120">-Local</span><span class="sxs-lookup"><span data-stu-id="9b21e-120">-Location</span></span>
<span data-ttu-id="9b21e-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9b21e-121">Location of the resource.</span></span>

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

### <span data-ttu-id="9b21e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b21e-122">-Name</span></span>
<span data-ttu-id="9b21e-123">Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="9b21e-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="9b21e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b21e-124">-PassThru</span></span>
<span data-ttu-id="9b21e-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9b21e-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9b21e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b21e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b21e-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b21e-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="9b21e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b21e-128">-SubscriptionId</span></span>
<span data-ttu-id="9b21e-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b21e-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9b21e-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9b21e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b21e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b21e-131">CommonParameters</span></span>
<span data-ttu-id="9b21e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b21e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b21e-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b21e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b21e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b21e-134">INPUTS</span></span>

### <span data-ttu-id="9b21e-135">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9b21e-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9b21e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b21e-136">OUTPUTS</span></span>

### <span data-ttu-id="9b21e-137">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="9b21e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="9b21e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b21e-138">NOTES</span></span>

<span data-ttu-id="9b21e-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9b21e-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b21e-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b21e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9b21e-141">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9b21e-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b21e-142">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b21e-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9b21e-143">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="9b21e-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9b21e-144">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="9b21e-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9b21e-145">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="9b21e-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9b21e-146">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="9b21e-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9b21e-147">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="9b21e-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9b21e-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9b21e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b21e-149">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="9b21e-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9b21e-150">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="9b21e-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9b21e-151">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9b21e-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9b21e-152">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="9b21e-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9b21e-153">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="9b21e-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9b21e-154">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="9b21e-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9b21e-155">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="9b21e-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9b21e-156">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b21e-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9b21e-157">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="9b21e-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9b21e-158">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="9b21e-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9b21e-159">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="9b21e-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9b21e-160">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b21e-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9b21e-161">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b21e-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9b21e-162">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b21e-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9b21e-163">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9b21e-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9b21e-164">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b21e-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9b21e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b21e-165">RELATED LINKS</span></span>

