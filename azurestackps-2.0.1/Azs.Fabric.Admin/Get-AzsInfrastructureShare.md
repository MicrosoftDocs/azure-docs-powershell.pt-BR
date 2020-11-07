---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945320"
---
# <span data-ttu-id="d50cb-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="d50cb-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="d50cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d50cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d50cb-103">Retorna o compartilhamento de arquivo de malha solicitado.</span><span class="sxs-lookup"><span data-stu-id="d50cb-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="d50cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d50cb-104">SYNTAX</span></span>

### <span data-ttu-id="d50cb-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d50cb-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="d50cb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d50cb-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d50cb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d50cb-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d50cb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d50cb-108">DESCRIPTION</span></span>
<span data-ttu-id="d50cb-109">Retorna o compartilhamento de arquivo de malha solicitado.</span><span class="sxs-lookup"><span data-stu-id="d50cb-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="d50cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d50cb-110">EXAMPLES</span></span>

### <span data-ttu-id="d50cb-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="d50cb-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="d50cb-112">Retorna uma lista de todos os compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d50cb-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="d50cb-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="d50cb-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="d50cb-114">Retorna um compartilhamento de arquivos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="d50cb-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="d50cb-115">OS</span><span class="sxs-lookup"><span data-stu-id="d50cb-115">PARAMETERS</span></span>

### <span data-ttu-id="d50cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50cb-116">-DefaultProfile</span></span>
<span data-ttu-id="d50cb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d50cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d50cb-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d50cb-118">-Filter</span></span>
<span data-ttu-id="d50cb-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d50cb-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d50cb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d50cb-120">-InputObject</span></span>
<span data-ttu-id="d50cb-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d50cb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d50cb-122">-Local</span><span class="sxs-lookup"><span data-stu-id="d50cb-122">-Location</span></span>
<span data-ttu-id="d50cb-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d50cb-123">Location of the resource.</span></span>

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

### <span data-ttu-id="d50cb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d50cb-124">-Name</span></span>
<span data-ttu-id="d50cb-125">Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="d50cb-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="d50cb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d50cb-126">-PassThru</span></span>
<span data-ttu-id="d50cb-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d50cb-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d50cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d50cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="d50cb-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d50cb-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="d50cb-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="d50cb-130">-Skip</span></span>
<span data-ttu-id="d50cb-131">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="d50cb-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="d50cb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d50cb-132">-SubscriptionId</span></span>
<span data-ttu-id="d50cb-133">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d50cb-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d50cb-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d50cb-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d50cb-135">-Início</span><span class="sxs-lookup"><span data-stu-id="d50cb-135">-Top</span></span>
<span data-ttu-id="d50cb-136">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="d50cb-136">OData top parameter.</span></span>

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

### <span data-ttu-id="d50cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50cb-137">CommonParameters</span></span>
<span data-ttu-id="d50cb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50cb-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d50cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50cb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d50cb-140">INPUTS</span></span>

### <span data-ttu-id="d50cb-141">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d50cb-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d50cb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d50cb-142">OUTPUTS</span></span>

### <span data-ttu-id="d50cb-143">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="d50cb-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="d50cb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d50cb-144">NOTES</span></span>

<span data-ttu-id="d50cb-145">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d50cb-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d50cb-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d50cb-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d50cb-147">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d50cb-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d50cb-148">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d50cb-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d50cb-149">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="d50cb-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d50cb-150">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="d50cb-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d50cb-151">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="d50cb-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d50cb-152">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="d50cb-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d50cb-153">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="d50cb-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d50cb-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d50cb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d50cb-155">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d50cb-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d50cb-156">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d50cb-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d50cb-157">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d50cb-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d50cb-158">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="d50cb-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d50cb-159">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="d50cb-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d50cb-160">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="d50cb-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d50cb-161">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="d50cb-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d50cb-162">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d50cb-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d50cb-163">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="d50cb-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d50cb-164">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="d50cb-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d50cb-165">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="d50cb-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d50cb-166">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d50cb-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d50cb-167">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d50cb-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d50cb-168">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d50cb-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d50cb-169">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d50cb-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d50cb-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d50cb-170">RELATED LINKS</span></span>

