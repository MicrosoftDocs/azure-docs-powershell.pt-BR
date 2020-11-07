---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945318"
---
# <span data-ttu-id="06415-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="06415-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="06415-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06415-102">SYNOPSIS</span></span>
<span data-ttu-id="06415-103">Retorna a sub-rede lógica solicitada.</span><span class="sxs-lookup"><span data-stu-id="06415-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="06415-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06415-104">SYNTAX</span></span>

### <span data-ttu-id="06415-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="06415-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="06415-106">Obter</span><span class="sxs-lookup"><span data-stu-id="06415-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="06415-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06415-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="06415-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06415-108">DESCRIPTION</span></span>
<span data-ttu-id="06415-109">Retorna a sub-rede lógica solicitada.</span><span class="sxs-lookup"><span data-stu-id="06415-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="06415-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06415-110">EXAMPLES</span></span>

### <span data-ttu-id="06415-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="06415-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="06415-112">Obter todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="06415-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="06415-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="06415-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="06415-114">Obter redes lógicas específicas em um local com base em um nome.</span><span class="sxs-lookup"><span data-stu-id="06415-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="06415-115">OS</span><span class="sxs-lookup"><span data-stu-id="06415-115">PARAMETERS</span></span>

### <span data-ttu-id="06415-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06415-116">-DefaultProfile</span></span>
<span data-ttu-id="06415-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06415-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06415-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="06415-118">-Filter</span></span>
<span data-ttu-id="06415-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="06415-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="06415-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06415-120">-InputObject</span></span>
<span data-ttu-id="06415-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="06415-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06415-122">-Local</span><span class="sxs-lookup"><span data-stu-id="06415-122">-Location</span></span>
<span data-ttu-id="06415-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="06415-123">Location of the resource.</span></span>

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

### <span data-ttu-id="06415-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="06415-124">-LogicalNetwork</span></span>
<span data-ttu-id="06415-125">Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="06415-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06415-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="06415-126">-Name</span></span>
<span data-ttu-id="06415-127">Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="06415-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="06415-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06415-128">-PassThru</span></span>
<span data-ttu-id="06415-129">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="06415-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06415-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06415-130">-ResourceGroupName</span></span>
<span data-ttu-id="06415-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06415-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="06415-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06415-132">-SubscriptionId</span></span>
<span data-ttu-id="06415-133">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06415-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06415-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="06415-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06415-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06415-135">CommonParameters</span></span>
<span data-ttu-id="06415-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06415-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06415-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06415-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06415-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06415-138">INPUTS</span></span>

### <span data-ttu-id="06415-139">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="06415-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="06415-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06415-140">OUTPUTS</span></span>

### <span data-ttu-id="06415-141">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. ILogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="06415-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="06415-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06415-142">NOTES</span></span>

<span data-ttu-id="06415-143">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="06415-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06415-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06415-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="06415-145">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="06415-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06415-146">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06415-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="06415-147">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="06415-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="06415-148">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="06415-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="06415-149">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="06415-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="06415-150">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="06415-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="06415-151">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="06415-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="06415-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="06415-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06415-153">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="06415-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="06415-154">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="06415-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="06415-155">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="06415-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="06415-156">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="06415-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="06415-157">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="06415-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="06415-158">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="06415-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="06415-159">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="06415-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="06415-160">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06415-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="06415-161">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="06415-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="06415-162">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="06415-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="06415-163">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="06415-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="06415-164">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06415-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="06415-165">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06415-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="06415-166">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06415-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06415-167">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="06415-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="06415-168">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06415-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="06415-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06415-169">RELATED LINKS</span></span>

