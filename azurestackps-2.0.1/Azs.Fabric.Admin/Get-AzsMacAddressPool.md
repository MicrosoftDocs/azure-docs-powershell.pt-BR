---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsmacaddresspool
schema: 2.0.0
ms.openlocfilehash: f7a2ae035ff0985c84dc78a18131c46239bafd1f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945315"
---
# <span data-ttu-id="3710b-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="3710b-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="3710b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3710b-102">SYNOPSIS</span></span>
<span data-ttu-id="3710b-103">Retorna o pool de endereços MAC solicitado.</span><span class="sxs-lookup"><span data-stu-id="3710b-103">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="3710b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3710b-104">SYNTAX</span></span>

### <span data-ttu-id="3710b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3710b-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3710b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3710b-106">Get</span></span>
```
Get-AzsMacAddressPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3710b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3710b-107">GetViaIdentity</span></span>
```
Get-AzsMacAddressPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="3710b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3710b-108">DESCRIPTION</span></span>
<span data-ttu-id="3710b-109">Retorna o pool de endereços MAC solicitado.</span><span class="sxs-lookup"><span data-stu-id="3710b-109">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="3710b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3710b-110">EXAMPLES</span></span>

### <span data-ttu-id="3710b-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="3710b-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool

A list of all MAC address pools at a location.
```

<span data-ttu-id="3710b-112">Retorna uma lista de todos os pools de endereços MAC em um local.</span><span class="sxs-lookup"><span data-stu-id="3710b-112">Returns a list of all MAC address pools at a location.</span></span>

### <span data-ttu-id="3710b-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="3710b-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"

A specific MAC address pool at a location based on name.
```

<span data-ttu-id="3710b-114">Obtenha um pool de endereços MAC específico em um local com base no nome.</span><span class="sxs-lookup"><span data-stu-id="3710b-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="3710b-115">OS</span><span class="sxs-lookup"><span data-stu-id="3710b-115">PARAMETERS</span></span>

### <span data-ttu-id="3710b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3710b-116">-DefaultProfile</span></span>
<span data-ttu-id="3710b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3710b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3710b-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3710b-118">-Filter</span></span>
<span data-ttu-id="3710b-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3710b-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="3710b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3710b-120">-InputObject</span></span>
<span data-ttu-id="3710b-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3710b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3710b-122">-Local</span><span class="sxs-lookup"><span data-stu-id="3710b-122">-Location</span></span>
<span data-ttu-id="3710b-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3710b-123">Location of the resource.</span></span>

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

### <span data-ttu-id="3710b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3710b-124">-Name</span></span>
<span data-ttu-id="3710b-125">Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="3710b-125">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="3710b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3710b-126">-PassThru</span></span>
<span data-ttu-id="3710b-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3710b-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3710b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3710b-128">-ResourceGroupName</span></span>
<span data-ttu-id="3710b-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3710b-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="3710b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3710b-130">-SubscriptionId</span></span>
<span data-ttu-id="3710b-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3710b-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3710b-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3710b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3710b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3710b-133">CommonParameters</span></span>
<span data-ttu-id="3710b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3710b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3710b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3710b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3710b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3710b-136">INPUTS</span></span>

### <span data-ttu-id="3710b-137">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3710b-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3710b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3710b-138">OUTPUTS</span></span>

### <span data-ttu-id="3710b-139">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="3710b-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IMacAddressPool</span></span>



## <span data-ttu-id="3710b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3710b-140">NOTES</span></span>

<span data-ttu-id="3710b-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3710b-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3710b-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3710b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3710b-143">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3710b-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3710b-144">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3710b-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3710b-145">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="3710b-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3710b-146">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="3710b-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3710b-147">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="3710b-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3710b-148">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="3710b-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3710b-149">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="3710b-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3710b-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3710b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3710b-151">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="3710b-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3710b-152">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="3710b-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3710b-153">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3710b-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3710b-154">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3710b-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3710b-155">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="3710b-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3710b-156">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="3710b-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3710b-157">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="3710b-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3710b-158">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3710b-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3710b-159">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="3710b-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3710b-160">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3710b-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3710b-161">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="3710b-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3710b-162">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3710b-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="3710b-163">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3710b-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3710b-164">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3710b-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3710b-165">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3710b-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3710b-166">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3710b-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3710b-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3710b-167">RELATED LINKS</span></span>

