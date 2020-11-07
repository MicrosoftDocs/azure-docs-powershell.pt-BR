---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945228"
---
# <span data-ttu-id="64a98-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="64a98-101">Get-AzsDrive</span></span>

## <span data-ttu-id="64a98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64a98-102">SYNOPSIS</span></span>
<span data-ttu-id="64a98-103">Retorne a unidade de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="64a98-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="64a98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64a98-104">SYNTAX</span></span>

### <span data-ttu-id="64a98-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="64a98-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="64a98-106">Obter</span><span class="sxs-lookup"><span data-stu-id="64a98-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="64a98-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64a98-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="64a98-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64a98-108">DESCRIPTION</span></span>
<span data-ttu-id="64a98-109">Retorne a unidade de armazenamento solicitada.</span><span class="sxs-lookup"><span data-stu-id="64a98-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="64a98-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64a98-110">EXAMPLES</span></span>

### <span data-ttu-id="64a98-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="64a98-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="64a98-112">Obter uma lista de todos os drives de armazenamento de um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="64a98-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="64a98-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="64a98-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="64a98-114">Obter uma unidade de armazenamento por nome para um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="64a98-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="64a98-115">OS</span><span class="sxs-lookup"><span data-stu-id="64a98-115">PARAMETERS</span></span>

### <span data-ttu-id="64a98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a98-116">-DefaultProfile</span></span>
<span data-ttu-id="64a98-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64a98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a98-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="64a98-118">-Filter</span></span>
<span data-ttu-id="64a98-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="64a98-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="64a98-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a98-120">-InputObject</span></span>
<span data-ttu-id="64a98-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="64a98-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64a98-122">-Local</span><span class="sxs-lookup"><span data-stu-id="64a98-122">-Location</span></span>
<span data-ttu-id="64a98-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="64a98-123">Location of the resource.</span></span>

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

### <span data-ttu-id="64a98-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="64a98-124">-Name</span></span>
<span data-ttu-id="64a98-125">Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64a98-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="64a98-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64a98-126">-PassThru</span></span>
<span data-ttu-id="64a98-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="64a98-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64a98-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a98-128">-ResourceGroupName</span></span>
<span data-ttu-id="64a98-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64a98-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="64a98-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="64a98-130">-ScaleUnit</span></span>
<span data-ttu-id="64a98-131">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="64a98-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="64a98-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="64a98-132">-Skip</span></span>
<span data-ttu-id="64a98-133">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="64a98-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="64a98-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="64a98-134">-StorageSubSystem</span></span>
<span data-ttu-id="64a98-135">Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64a98-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="64a98-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64a98-136">-SubscriptionId</span></span>
<span data-ttu-id="64a98-137">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64a98-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64a98-138">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="64a98-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64a98-139">-Início</span><span class="sxs-lookup"><span data-stu-id="64a98-139">-Top</span></span>
<span data-ttu-id="64a98-140">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="64a98-140">OData top parameter.</span></span>

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

### <span data-ttu-id="64a98-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a98-141">CommonParameters</span></span>
<span data-ttu-id="64a98-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a98-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a98-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a98-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a98-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64a98-144">INPUTS</span></span>

### <span data-ttu-id="64a98-145">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="64a98-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="64a98-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64a98-146">OUTPUTS</span></span>

### <span data-ttu-id="64a98-147">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="64a98-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="64a98-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64a98-148">NOTES</span></span>

<span data-ttu-id="64a98-149">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="64a98-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64a98-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64a98-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="64a98-151">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="64a98-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64a98-152">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64a98-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="64a98-153">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="64a98-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="64a98-154">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="64a98-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="64a98-155">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="64a98-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="64a98-156">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="64a98-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="64a98-157">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="64a98-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="64a98-158">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="64a98-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64a98-159">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="64a98-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="64a98-160">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="64a98-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="64a98-161">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="64a98-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="64a98-162">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="64a98-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="64a98-163">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="64a98-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="64a98-164">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="64a98-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="64a98-165">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="64a98-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="64a98-166">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64a98-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="64a98-167">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="64a98-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="64a98-168">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="64a98-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="64a98-169">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="64a98-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="64a98-170">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64a98-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="64a98-171">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64a98-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64a98-172">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="64a98-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="64a98-173">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64a98-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="64a98-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64a98-174">RELATED LINKS</span></span>

