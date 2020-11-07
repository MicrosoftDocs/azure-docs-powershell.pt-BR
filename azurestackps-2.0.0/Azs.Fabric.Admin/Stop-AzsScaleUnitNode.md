---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777113"
---
# <span data-ttu-id="6e1b3-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6e1b3-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6e1b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1b3-103">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="6e1b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e1b3-104">SYNTAX</span></span>

### <span data-ttu-id="6e1b3-105">PowerOff (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e1b3-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e1b3-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e1b3-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e1b3-107">Pré-desligamento</span><span class="sxs-lookup"><span data-stu-id="6e1b3-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e1b3-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e1b3-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e1b3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e1b3-109">DESCRIPTION</span></span>
<span data-ttu-id="6e1b3-110">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="6e1b3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e1b3-111">EXAMPLES</span></span>

### <span data-ttu-id="6e1b3-112">Exemplo 1: {{adicionar título aqui}}</span><span class="sxs-lookup"><span data-stu-id="6e1b3-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="6e1b3-113">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="6e1b3-114">OS</span><span class="sxs-lookup"><span data-stu-id="6e1b3-114">PARAMETERS</span></span>

### <span data-ttu-id="6e1b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e1b3-115">-AsJob</span></span>
<span data-ttu-id="6e1b3-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6e1b3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6e1b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1b3-117">-DefaultProfile</span></span>
<span data-ttu-id="6e1b3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1b3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6e1b3-119">-Force</span></span>
<span data-ttu-id="6e1b3-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6e1b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e1b3-121">-InputObject</span></span>
<span data-ttu-id="6e1b3-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6e1b3-123">-Local</span><span class="sxs-lookup"><span data-stu-id="6e1b3-123">-Location</span></span>
<span data-ttu-id="6e1b3-124">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e1b3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e1b3-125">-Name</span></span>
<span data-ttu-id="6e1b3-126">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e1b3-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6e1b3-127">-NoWait</span></span>
<span data-ttu-id="6e1b3-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6e1b3-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e1b3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e1b3-129">-PassThru</span></span>
<span data-ttu-id="6e1b3-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6e1b3-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6e1b3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1b3-131">-ResourceGroupName</span></span>
<span data-ttu-id="6e1b3-132">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e1b3-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e1b3-133">-SubscriptionId</span></span>
<span data-ttu-id="6e1b3-134">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6e1b3-135">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e1b3-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e1b3-136">-Confirm</span></span>
<span data-ttu-id="6e1b3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e1b3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1b3-138">-WhatIf</span></span>
<span data-ttu-id="6e1b3-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e1b3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e1b3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1b3-141">CommonParameters</span></span>
<span data-ttu-id="6e1b3-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1b3-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e1b3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1b3-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e1b3-144">INPUTS</span></span>

### <span data-ttu-id="6e1b3-145">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6e1b3-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6e1b3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e1b3-146">OUTPUTS</span></span>

### <span data-ttu-id="6e1b3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e1b3-147">System.Boolean</span></span>



## <span data-ttu-id="6e1b3-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e1b3-148">NOTES</span></span>

<span data-ttu-id="6e1b3-149">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e1b3-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6e1b3-151">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6e1b3-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e1b3-152">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6e1b3-153">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6e1b3-154">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6e1b3-155">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6e1b3-156">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6e1b3-157">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6e1b3-158">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6e1b3-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e1b3-159">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6e1b3-160">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6e1b3-161">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6e1b3-162">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6e1b3-163">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6e1b3-164">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6e1b3-165">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6e1b3-166">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6e1b3-167">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6e1b3-168">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6e1b3-169">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6e1b3-170">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="6e1b3-171">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6e1b3-172">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6e1b3-173">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6e1b3-174">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6e1b3-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6e1b3-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e1b3-175">RELATED LINKS</span></span>

