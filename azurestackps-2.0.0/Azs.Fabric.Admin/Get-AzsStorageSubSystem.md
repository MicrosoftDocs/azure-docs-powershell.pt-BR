---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776022"
---
# <span data-ttu-id="57f2c-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="57f2c-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="57f2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="57f2c-103">Retorne o subsistema de armazenamento solicitado.</span><span class="sxs-lookup"><span data-stu-id="57f2c-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="57f2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57f2c-104">SYNTAX</span></span>

### <span data-ttu-id="57f2c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="57f2c-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="57f2c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="57f2c-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="57f2c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57f2c-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="57f2c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="57f2c-109">Retorne o subsistema de armazenamento solicitado.</span><span class="sxs-lookup"><span data-stu-id="57f2c-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="57f2c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="57f2c-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="57f2c-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="57f2c-112">Obter todos os subsistemas de armazenamento a partir de uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="57f2c-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="57f2c-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="57f2c-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="57f2c-114">Obtenha um subsistema de armazenamento de acordo com uma unidade de escala e um nome.</span><span class="sxs-lookup"><span data-stu-id="57f2c-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="57f2c-115">OS</span><span class="sxs-lookup"><span data-stu-id="57f2c-115">PARAMETERS</span></span>

### <span data-ttu-id="57f2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f2c-116">-DefaultProfile</span></span>
<span data-ttu-id="57f2c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57f2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f2c-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="57f2c-118">-Filter</span></span>
<span data-ttu-id="57f2c-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="57f2c-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="57f2c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57f2c-120">-InputObject</span></span>
<span data-ttu-id="57f2c-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="57f2c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57f2c-122">-Local</span><span class="sxs-lookup"><span data-stu-id="57f2c-122">-Location</span></span>
<span data-ttu-id="57f2c-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="57f2c-123">Location of the resource.</span></span>

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

### <span data-ttu-id="57f2c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="57f2c-124">-Name</span></span>
<span data-ttu-id="57f2c-125">Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f2c-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="57f2c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57f2c-126">-PassThru</span></span>
<span data-ttu-id="57f2c-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="57f2c-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57f2c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f2c-128">-ResourceGroupName</span></span>
<span data-ttu-id="57f2c-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57f2c-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="57f2c-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="57f2c-130">-ScaleUnit</span></span>
<span data-ttu-id="57f2c-131">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="57f2c-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="57f2c-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="57f2c-132">-Skip</span></span>
<span data-ttu-id="57f2c-133">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="57f2c-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="57f2c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57f2c-134">-SubscriptionId</span></span>
<span data-ttu-id="57f2c-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57f2c-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57f2c-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="57f2c-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57f2c-137">-Início</span><span class="sxs-lookup"><span data-stu-id="57f2c-137">-Top</span></span>
<span data-ttu-id="57f2c-138">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="57f2c-138">OData top parameter.</span></span>

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

### <span data-ttu-id="57f2c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f2c-139">CommonParameters</span></span>
<span data-ttu-id="57f2c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f2c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f2c-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57f2c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f2c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57f2c-142">INPUTS</span></span>

### <span data-ttu-id="57f2c-143">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="57f2c-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="57f2c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57f2c-144">OUTPUTS</span></span>

### <span data-ttu-id="57f2c-145">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="57f2c-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="57f2c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57f2c-146">NOTES</span></span>

<span data-ttu-id="57f2c-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="57f2c-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57f2c-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57f2c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="57f2c-149">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="57f2c-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57f2c-150">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f2c-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="57f2c-151">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="57f2c-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="57f2c-152">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="57f2c-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="57f2c-153">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="57f2c-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="57f2c-154">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="57f2c-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="57f2c-155">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="57f2c-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="57f2c-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="57f2c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57f2c-157">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="57f2c-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="57f2c-158">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="57f2c-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="57f2c-159">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="57f2c-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="57f2c-160">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="57f2c-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="57f2c-161">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="57f2c-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="57f2c-162">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="57f2c-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="57f2c-163">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="57f2c-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="57f2c-164">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57f2c-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="57f2c-165">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="57f2c-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="57f2c-166">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="57f2c-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="57f2c-167">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="57f2c-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="57f2c-168">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f2c-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="57f2c-169">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57f2c-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57f2c-170">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="57f2c-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57f2c-171">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57f2c-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="57f2c-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57f2c-172">RELATED LINKS</span></span>

