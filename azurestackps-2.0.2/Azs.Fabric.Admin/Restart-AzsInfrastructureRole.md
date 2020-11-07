---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: 6e8b5f2dbfde62613a521fd7a49fba27c54ab498
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947127"
---
# <span data-ttu-id="596c8-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="596c8-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="596c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="596c8-102">SYNOPSIS</span></span>
<span data-ttu-id="596c8-103">Reinicia a função de infraestrutura solicitada.</span><span class="sxs-lookup"><span data-stu-id="596c8-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="596c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="596c8-104">SYNTAX</span></span>

### <span data-ttu-id="596c8-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="596c8-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="596c8-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="596c8-106">RestartViaIdentity</span></span>
```
Restart-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="596c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="596c8-107">DESCRIPTION</span></span>
<span data-ttu-id="596c8-108">Reinicia a função de infraestrutura solicitada.</span><span class="sxs-lookup"><span data-stu-id="596c8-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="596c8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="596c8-109">EXAMPLES</span></span>

### <span data-ttu-id="596c8-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="596c8-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRole -Name "Compute Controller"

```

<span data-ttu-id="596c8-111">Reinicie uma função de infraestrutura que tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="596c8-111">Restart an infrastructure role which has crashed.</span></span>



## <span data-ttu-id="596c8-112">OS</span><span class="sxs-lookup"><span data-stu-id="596c8-112">PARAMETERS</span></span>

### <span data-ttu-id="596c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="596c8-113">-AsJob</span></span>
<span data-ttu-id="596c8-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="596c8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="596c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596c8-115">-DefaultProfile</span></span>
<span data-ttu-id="596c8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="596c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596c8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="596c8-117">-Force</span></span>
<span data-ttu-id="596c8-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="596c8-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="596c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="596c8-119">-InputObject</span></span>
<span data-ttu-id="596c8-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="596c8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="596c8-121">-Local</span><span class="sxs-lookup"><span data-stu-id="596c8-121">-Location</span></span>
<span data-ttu-id="596c8-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="596c8-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="596c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="596c8-123">-Name</span></span>
<span data-ttu-id="596c8-124">Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="596c8-124">Infrastructure role name.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="596c8-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="596c8-125">-NoWait</span></span>
<span data-ttu-id="596c8-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="596c8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="596c8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="596c8-127">-PassThru</span></span>
<span data-ttu-id="596c8-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="596c8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="596c8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596c8-129">-ResourceGroupName</span></span>
<span data-ttu-id="596c8-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="596c8-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="596c8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="596c8-131">-SubscriptionId</span></span>
<span data-ttu-id="596c8-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="596c8-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="596c8-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="596c8-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="596c8-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="596c8-134">-Confirm</span></span>
<span data-ttu-id="596c8-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="596c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596c8-136">-WhatIf</span></span>
<span data-ttu-id="596c8-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="596c8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596c8-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="596c8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596c8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596c8-139">CommonParameters</span></span>
<span data-ttu-id="596c8-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596c8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596c8-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="596c8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596c8-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="596c8-142">INPUTS</span></span>

### <span data-ttu-id="596c8-143">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="596c8-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="596c8-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="596c8-144">OUTPUTS</span></span>

### <span data-ttu-id="596c8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="596c8-145">System.Boolean</span></span>



## <span data-ttu-id="596c8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="596c8-146">NOTES</span></span>

<span data-ttu-id="596c8-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="596c8-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="596c8-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="596c8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="596c8-149">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="596c8-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="596c8-150">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="596c8-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="596c8-151">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="596c8-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="596c8-152">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="596c8-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="596c8-153">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="596c8-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="596c8-154">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="596c8-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="596c8-155">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="596c8-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="596c8-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="596c8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="596c8-157">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="596c8-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="596c8-158">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="596c8-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="596c8-159">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="596c8-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="596c8-160">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="596c8-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="596c8-161">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="596c8-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="596c8-162">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="596c8-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="596c8-163">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="596c8-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="596c8-164">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="596c8-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="596c8-165">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="596c8-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="596c8-166">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="596c8-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="596c8-167">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="596c8-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="596c8-168">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="596c8-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="596c8-169">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="596c8-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="596c8-170">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="596c8-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="596c8-171">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="596c8-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="596c8-172">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="596c8-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="596c8-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="596c8-173">RELATED LINKS</span></span>

