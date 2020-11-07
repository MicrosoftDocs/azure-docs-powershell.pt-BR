---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946629"
---
# <span data-ttu-id="3f810-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="3f810-101">Get-AzsDrive</span></span>

## <span data-ttu-id="3f810-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f810-102">SYNOPSIS</span></span>
<span data-ttu-id="3f810-103">Retorne a unidade de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="3f810-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="3f810-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f810-104">SYNTAX</span></span>

### <span data-ttu-id="3f810-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f810-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3f810-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3f810-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="3f810-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f810-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="3f810-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f810-108">DESCRIPTION</span></span>
<span data-ttu-id="3f810-109">Retorne a unidade de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="3f810-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="3f810-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f810-110">EXAMPLES</span></span>

### <span data-ttu-id="3f810-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="3f810-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="3f810-112">Obter uma lista de todos os drives de armazenamento de um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="3f810-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="3f810-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="3f810-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="3f810-114">Obter uma unidade de armazenamento por nome para um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="3f810-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="3f810-115">OS</span><span class="sxs-lookup"><span data-stu-id="3f810-115">PARAMETERS</span></span>

### <span data-ttu-id="3f810-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f810-116">-DefaultProfile</span></span>
<span data-ttu-id="3f810-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f810-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f810-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3f810-118">-Filter</span></span>
<span data-ttu-id="3f810-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3f810-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="3f810-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f810-120">-InputObject</span></span>
<span data-ttu-id="3f810-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3f810-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f810-122">-Local</span><span class="sxs-lookup"><span data-stu-id="3f810-122">-Location</span></span>
<span data-ttu-id="3f810-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3f810-123">Location of the resource.</span></span>

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

### <span data-ttu-id="3f810-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f810-124">-Name</span></span>
<span data-ttu-id="3f810-125">Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3f810-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="3f810-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f810-126">-PassThru</span></span>
<span data-ttu-id="3f810-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3f810-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3f810-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f810-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f810-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f810-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="3f810-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3f810-130">-ScaleUnit</span></span>
<span data-ttu-id="3f810-131">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="3f810-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="3f810-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="3f810-132">-Skip</span></span>
<span data-ttu-id="3f810-133">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="3f810-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="3f810-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="3f810-134">-StorageSubSystem</span></span>
<span data-ttu-id="3f810-135">Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3f810-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="3f810-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f810-136">-SubscriptionId</span></span>
<span data-ttu-id="3f810-137">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f810-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f810-138">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f810-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f810-139">-Início</span><span class="sxs-lookup"><span data-stu-id="3f810-139">-Top</span></span>
<span data-ttu-id="3f810-140">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="3f810-140">OData top parameter.</span></span>

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

### <span data-ttu-id="3f810-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f810-141">CommonParameters</span></span>
<span data-ttu-id="3f810-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f810-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f810-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f810-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f810-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f810-144">INPUTS</span></span>

### <span data-ttu-id="3f810-145">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3f810-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3f810-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f810-146">OUTPUTS</span></span>

### <span data-ttu-id="3f810-147">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="3f810-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="3f810-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f810-148">NOTES</span></span>

<span data-ttu-id="3f810-149">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3f810-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f810-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f810-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f810-151">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3f810-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f810-152">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3f810-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3f810-153">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="3f810-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3f810-154">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="3f810-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3f810-155">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="3f810-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3f810-156">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="3f810-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3f810-157">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="3f810-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3f810-158">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3f810-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f810-159">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="3f810-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3f810-160">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="3f810-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3f810-161">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3f810-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3f810-162">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3f810-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3f810-163">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3f810-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3f810-164">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="3f810-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3f810-165">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="3f810-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3f810-166">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f810-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3f810-167">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="3f810-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3f810-168">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3f810-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3f810-169">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="3f810-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3f810-170">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3f810-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3f810-171">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f810-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f810-172">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f810-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3f810-173">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3f810-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3f810-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f810-174">RELATED LINKS</span></span>

