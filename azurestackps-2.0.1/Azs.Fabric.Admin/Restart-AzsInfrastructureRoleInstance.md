---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945167"
---
# <span data-ttu-id="c2b6e-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c2b6e-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c2b6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b6e-103">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="c2b6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2b6e-104">SYNTAX</span></span>

### <span data-ttu-id="c2b6e-105">Reinicializar (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2b6e-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2b6e-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2b6e-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2b6e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2b6e-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b6e-108">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="c2b6e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2b6e-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b6e-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="c2b6e-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="c2b6e-111">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="c2b6e-112">OS</span><span class="sxs-lookup"><span data-stu-id="c2b6e-112">PARAMETERS</span></span>

### <span data-ttu-id="c2b6e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2b6e-113">-AsJob</span></span>
<span data-ttu-id="c2b6e-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c2b6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b6e-115">-DefaultProfile</span></span>
<span data-ttu-id="c2b6e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c2b6e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c2b6e-117">-Force</span></span>
<span data-ttu-id="c2b6e-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c2b6e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2b6e-119">-InputObject</span></span>
<span data-ttu-id="c2b6e-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RebootViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c2b6e-121">-Local</span><span class="sxs-lookup"><span data-stu-id="c2b6e-121">-Location</span></span>
<span data-ttu-id="c2b6e-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2b6e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2b6e-123">-Name</span></span>
<span data-ttu-id="c2b6e-124">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2b6e-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c2b6e-125">-NoWait</span></span>
<span data-ttu-id="c2b6e-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c2b6e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c2b6e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2b6e-127">-PassThru</span></span>
<span data-ttu-id="c2b6e-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c2b6e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c2b6e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b6e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2b6e-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```
### <span data-ttu-id="c2b6e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2b6e-131">-SubscriptionId</span></span>
<span data-ttu-id="c2b6e-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2b6e-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2b6e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2b6e-134">-Confirm</span></span>
<span data-ttu-id="c2b6e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b6e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b6e-136">-WhatIf</span></span>
<span data-ttu-id="c2b6e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b6e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b6e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b6e-139">CommonParameters</span></span>
<span data-ttu-id="c2b6e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b6e-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b6e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b6e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2b6e-142">INPUTS</span></span>

### <span data-ttu-id="c2b6e-143">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c2b6e-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c2b6e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2b6e-144">OUTPUTS</span></span>

### <span data-ttu-id="c2b6e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2b6e-145">System.Boolean</span></span>



## <span data-ttu-id="c2b6e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2b6e-146">NOTES</span></span>

<span data-ttu-id="c2b6e-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2b6e-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c2b6e-149">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c2b6e-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2b6e-150">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c2b6e-151">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c2b6e-152">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c2b6e-153">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c2b6e-154">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c2b6e-155">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c2b6e-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c2b6e-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2b6e-157">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c2b6e-158">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c2b6e-159">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c2b6e-160">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c2b6e-161">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c2b6e-162">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c2b6e-163">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c2b6e-164">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c2b6e-165">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c2b6e-166">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c2b6e-167">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c2b6e-168">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="c2b6e-169">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c2b6e-170">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c2b6e-171">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c2b6e-172">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c2b6e-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c2b6e-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2b6e-173">RELATED LINKS</span></span>

