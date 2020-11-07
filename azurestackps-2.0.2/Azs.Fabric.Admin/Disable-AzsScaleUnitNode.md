---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 532ca56646ae2cfa25f6e3480f9f924d918cfedc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946724"
---
# <span data-ttu-id="95e06-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="95e06-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="95e06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95e06-102">SYNOPSIS</span></span>


## <span data-ttu-id="95e06-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95e06-103">SYNTAX</span></span>

### <span data-ttu-id="95e06-104">Parar (padrão)</span><span class="sxs-lookup"><span data-stu-id="95e06-104">Stop (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95e06-105">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95e06-105">StopViaIdentity</span></span>
```
Disable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95e06-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95e06-106">DESCRIPTION</span></span>


## <span data-ttu-id="95e06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95e06-107">EXAMPLES</span></span>

### <span data-ttu-id="95e06-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="95e06-108">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsScaleUnitNode -Name "HC1n25r2236"

Enable maintenance mode for a scale unit node.
```

<span data-ttu-id="95e06-109">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="95e06-109">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="95e06-110">OS</span><span class="sxs-lookup"><span data-stu-id="95e06-110">PARAMETERS</span></span>

### <span data-ttu-id="95e06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95e06-111">-AsJob</span></span>


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

### <span data-ttu-id="95e06-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e06-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="95e06-113">-Force</span><span class="sxs-lookup"><span data-stu-id="95e06-113">-Force</span></span>


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

### <span data-ttu-id="95e06-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95e06-114">-InputObject</span></span>
<span data-ttu-id="95e06-115">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="95e06-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-116">-Local</span><span class="sxs-lookup"><span data-stu-id="95e06-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="95e06-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="95e06-118">-NoWait</span></span>


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

### <span data-ttu-id="95e06-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95e06-119">-PassThru</span></span>


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

### <span data-ttu-id="95e06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e06-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95e06-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95e06-122">-Confirm</span></span>
<span data-ttu-id="95e06-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e06-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e06-124">-WhatIf</span></span>
<span data-ttu-id="95e06-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95e06-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e06-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95e06-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95e06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e06-127">CommonParameters</span></span>
<span data-ttu-id="95e06-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e06-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95e06-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e06-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95e06-130">INPUTS</span></span>

### <span data-ttu-id="95e06-131">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="95e06-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="95e06-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95e06-132">OUTPUTS</span></span>

### <span data-ttu-id="95e06-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95e06-133">System.Boolean</span></span>



## <span data-ttu-id="95e06-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95e06-134">NOTES</span></span>

<span data-ttu-id="95e06-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="95e06-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95e06-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95e06-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="95e06-137">INPUTobject <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="95e06-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="95e06-138">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95e06-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="95e06-139">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="95e06-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="95e06-140">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="95e06-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="95e06-141">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="95e06-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="95e06-142">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="95e06-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="95e06-143">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="95e06-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="95e06-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="95e06-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95e06-145">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="95e06-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="95e06-146">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="95e06-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="95e06-147">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="95e06-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="95e06-148">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="95e06-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="95e06-149">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="95e06-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="95e06-150">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="95e06-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="95e06-151">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="95e06-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="95e06-152">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95e06-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="95e06-153">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="95e06-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="95e06-154">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="95e06-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="95e06-155">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="95e06-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="95e06-156">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95e06-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="95e06-157">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95e06-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="95e06-158">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="95e06-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="95e06-159">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95e06-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="95e06-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95e06-160">RELATED LINKS</span></span>

