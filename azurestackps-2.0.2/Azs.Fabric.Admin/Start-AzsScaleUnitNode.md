---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946698"
---
# <span data-ttu-id="f1f2d-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f1f2d-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f1f2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f2d-103">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="f1f2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1f2d-104">SYNTAX</span></span>

### <span data-ttu-id="f1f2d-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1f2d-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1f2d-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1f2d-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1f2d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="f1f2d-108">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="f1f2d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1f2d-109">EXAMPLES</span></span>

### <span data-ttu-id="f1f2d-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="f1f2d-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="f1f2d-111">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="f1f2d-112">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="f1f2d-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="f1f2d-113">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-113">Power on a scale unit node.</span></span> <span data-ttu-id="f1f2d-114">Como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-114">As a job.</span></span>

## <span data-ttu-id="f1f2d-115">OS</span><span class="sxs-lookup"><span data-stu-id="f1f2d-115">PARAMETERS</span></span>

### <span data-ttu-id="f1f2d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1f2d-116">-AsJob</span></span>
<span data-ttu-id="f1f2d-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f1f2d-117">Run the command as a job</span></span>

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

### <span data-ttu-id="f1f2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f2d-118">-DefaultProfile</span></span>
<span data-ttu-id="f1f2d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f2d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1f2d-120">-Force</span></span>
<span data-ttu-id="f1f2d-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f1f2d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f2d-122">-InputObject</span></span>
<span data-ttu-id="f1f2d-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f1f2d-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f1f2d-124">-Location</span></span>
<span data-ttu-id="f1f2d-125">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1f2d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1f2d-126">-Name</span></span>
<span data-ttu-id="f1f2d-127">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1f2d-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f1f2d-128">-NoWait</span></span>
<span data-ttu-id="f1f2d-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f1f2d-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1f2d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1f2d-130">-PassThru</span></span>
<span data-ttu-id="f1f2d-131">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f1f2d-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1f2d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f2d-132">-ResourceGroupName</span></span>
<span data-ttu-id="f1f2d-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1f2d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1f2d-134">-SubscriptionId</span></span>
<span data-ttu-id="f1f2d-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1f2d-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1f2d-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1f2d-137">-Confirm</span></span>
<span data-ttu-id="f1f2d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f2d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f2d-139">-WhatIf</span></span>
<span data-ttu-id="f1f2d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f2d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f2d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f2d-142">CommonParameters</span></span>
<span data-ttu-id="f1f2d-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f2d-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1f2d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f2d-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1f2d-145">INPUTS</span></span>

### <span data-ttu-id="f1f2d-146">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f1f2d-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f1f2d-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1f2d-147">OUTPUTS</span></span>

### <span data-ttu-id="f1f2d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1f2d-148">System.Boolean</span></span>

## <span data-ttu-id="f1f2d-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1f2d-149">NOTES</span></span>

<span data-ttu-id="f1f2d-150">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1f2d-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f1f2d-152">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f1f2d-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1f2d-153">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f1f2d-154">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f1f2d-155">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f1f2d-156">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f1f2d-157">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f1f2d-158">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f1f2d-159">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f1f2d-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1f2d-160">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f1f2d-161">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f1f2d-162">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f1f2d-163">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f1f2d-164">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f1f2d-165">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f1f2d-166">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f1f2d-167">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f1f2d-168">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f1f2d-169">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f1f2d-170">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f1f2d-171">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f1f2d-172">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f1f2d-173">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f1f2d-174">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f1f2d-175">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1f2d-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f1f2d-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1f2d-176">RELATED LINKS</span></span>
