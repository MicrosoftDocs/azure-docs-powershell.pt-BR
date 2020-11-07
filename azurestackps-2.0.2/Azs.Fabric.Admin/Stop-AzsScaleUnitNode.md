---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946809"
---
# <span data-ttu-id="24451-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="24451-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="24451-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24451-102">SYNOPSIS</span></span>
<span data-ttu-id="24451-103">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="24451-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24451-104">SYNTAX</span></span>

### <span data-ttu-id="24451-105">PowerOff (padrão)</span><span class="sxs-lookup"><span data-stu-id="24451-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24451-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24451-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24451-107">Pré-desligamento</span><span class="sxs-lookup"><span data-stu-id="24451-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24451-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24451-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24451-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24451-109">DESCRIPTION</span></span>
<span data-ttu-id="24451-110">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="24451-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24451-111">EXAMPLES</span></span>

### <span data-ttu-id="24451-112">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="24451-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="24451-113">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="24451-114">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="24451-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="24451-115">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-115">Power down a scale unit node.</span></span> <span data-ttu-id="24451-116">Como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="24451-116">As a job.</span></span>

## <span data-ttu-id="24451-117">OS</span><span class="sxs-lookup"><span data-stu-id="24451-117">PARAMETERS</span></span>

### <span data-ttu-id="24451-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24451-118">-AsJob</span></span>
<span data-ttu-id="24451-119">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="24451-119">Run the command as a job</span></span>

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

### <span data-ttu-id="24451-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24451-120">-DefaultProfile</span></span>
<span data-ttu-id="24451-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24451-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24451-122">-Force</span><span class="sxs-lookup"><span data-stu-id="24451-122">-Force</span></span>
<span data-ttu-id="24451-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="24451-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="24451-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24451-124">-InputObject</span></span>
<span data-ttu-id="24451-125">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="24451-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24451-126">-Local</span><span class="sxs-lookup"><span data-stu-id="24451-126">-Location</span></span>
<span data-ttu-id="24451-127">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="24451-127">Location of the resource.</span></span>

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

### <span data-ttu-id="24451-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="24451-128">-Name</span></span>
<span data-ttu-id="24451-129">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="24451-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="24451-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="24451-130">-NoWait</span></span>
<span data-ttu-id="24451-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="24451-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24451-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24451-132">-PassThru</span></span>
<span data-ttu-id="24451-133">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="24451-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="24451-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24451-134">-ResourceGroupName</span></span>
<span data-ttu-id="24451-135">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="24451-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24451-136">-SubscriptionId</span></span>
<span data-ttu-id="24451-137">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24451-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24451-138">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="24451-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24451-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24451-139">-Confirm</span></span>
<span data-ttu-id="24451-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24451-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24451-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24451-141">-WhatIf</span></span>
<span data-ttu-id="24451-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24451-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24451-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24451-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24451-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24451-144">CommonParameters</span></span>
<span data-ttu-id="24451-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24451-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24451-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24451-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24451-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24451-147">INPUTS</span></span>

### <span data-ttu-id="24451-148">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="24451-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="24451-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24451-149">OUTPUTS</span></span>

### <span data-ttu-id="24451-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24451-150">System.Boolean</span></span>

## <span data-ttu-id="24451-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24451-151">NOTES</span></span>

<span data-ttu-id="24451-152">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="24451-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24451-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24451-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="24451-154">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="24451-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24451-155">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24451-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="24451-156">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="24451-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="24451-157">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="24451-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="24451-158">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="24451-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="24451-159">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="24451-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="24451-160">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="24451-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="24451-161">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="24451-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24451-162">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="24451-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="24451-163">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="24451-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="24451-164">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="24451-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="24451-165">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="24451-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="24451-166">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="24451-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="24451-167">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="24451-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="24451-168">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="24451-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="24451-169">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24451-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="24451-170">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="24451-171">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="24451-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="24451-172">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="24451-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="24451-173">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24451-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="24451-174">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24451-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="24451-175">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24451-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="24451-176">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="24451-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="24451-177">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24451-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="24451-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24451-178">RELATED LINKS</span></span>
