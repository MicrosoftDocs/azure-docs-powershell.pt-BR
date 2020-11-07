---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalnetwork
schema: 2.0.0
ms.openlocfilehash: 8229e487cd7c616969e049bbbea0ba7a6a18a448
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777122"
---
# <span data-ttu-id="f9bea-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f9bea-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="f9bea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9bea-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bea-103">Retorna a rede lógica solicitada.</span><span class="sxs-lookup"><span data-stu-id="f9bea-103">Returns the requested logical network.</span></span>

## <span data-ttu-id="f9bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9bea-104">SYNTAX</span></span>

### <span data-ttu-id="f9bea-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9bea-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f9bea-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f9bea-106">Get</span></span>
```
Get-AzsLogicalNetwork -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f9bea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f9bea-107">GetViaIdentity</span></span>
```
Get-AzsLogicalNetwork -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f9bea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9bea-108">DESCRIPTION</span></span>
<span data-ttu-id="f9bea-109">Retorna a rede lógica solicitada.</span><span class="sxs-lookup"><span data-stu-id="f9bea-109">Returns the requested logical network.</span></span>

## <span data-ttu-id="f9bea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9bea-110">EXAMPLES</span></span>

### <span data-ttu-id="f9bea-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="f9bea-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="f9bea-112">Obter todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="f9bea-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="f9bea-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="f9bea-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A specific logical networks at a location based on a name.
```

<span data-ttu-id="f9bea-114">Obter redes lógicas específicas em um local com base em um nome.</span><span class="sxs-lookup"><span data-stu-id="f9bea-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="f9bea-115">OS</span><span class="sxs-lookup"><span data-stu-id="f9bea-115">PARAMETERS</span></span>

### <span data-ttu-id="f9bea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bea-116">-DefaultProfile</span></span>
<span data-ttu-id="f9bea-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9bea-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="f9bea-118">-Filter</span></span>
<span data-ttu-id="f9bea-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="f9bea-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="f9bea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9bea-120">-InputObject</span></span>
<span data-ttu-id="f9bea-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f9bea-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9bea-122">-Local</span><span class="sxs-lookup"><span data-stu-id="f9bea-122">-Location</span></span>
<span data-ttu-id="f9bea-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f9bea-123">Location of the resource.</span></span>

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

### <span data-ttu-id="f9bea-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9bea-124">-Name</span></span>
<span data-ttu-id="f9bea-125">Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="f9bea-125">Name of the logical network.</span></span>

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

### <span data-ttu-id="f9bea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9bea-126">-PassThru</span></span>
<span data-ttu-id="f9bea-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f9bea-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f9bea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bea-128">-ResourceGroupName</span></span>
<span data-ttu-id="f9bea-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9bea-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="f9bea-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9bea-130">-SubscriptionId</span></span>
<span data-ttu-id="f9bea-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bea-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9bea-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9bea-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f9bea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bea-133">CommonParameters</span></span>
<span data-ttu-id="f9bea-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9bea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bea-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9bea-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bea-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9bea-136">INPUTS</span></span>

### <span data-ttu-id="f9bea-137">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f9bea-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f9bea-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9bea-138">OUTPUTS</span></span>

### <span data-ttu-id="f9bea-139">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. ILogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f9bea-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalNetwork</span></span>



## <span data-ttu-id="f9bea-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9bea-140">NOTES</span></span>

<span data-ttu-id="f9bea-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f9bea-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9bea-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9bea-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f9bea-143">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f9bea-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9bea-144">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9bea-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f9bea-145">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="f9bea-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f9bea-146">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="f9bea-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f9bea-147">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="f9bea-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f9bea-148">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="f9bea-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f9bea-149">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="f9bea-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f9bea-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f9bea-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9bea-151">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f9bea-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f9bea-152">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f9bea-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f9bea-153">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f9bea-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f9bea-154">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="f9bea-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f9bea-155">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="f9bea-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f9bea-156">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="f9bea-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f9bea-157">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="f9bea-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f9bea-158">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9bea-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f9bea-159">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="f9bea-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f9bea-160">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f9bea-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f9bea-161">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="f9bea-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f9bea-162">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9bea-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f9bea-163">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9bea-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f9bea-164">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bea-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9bea-165">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9bea-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f9bea-166">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9bea-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f9bea-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9bea-167">RELATED LINKS</span></span>

