---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776041"
---
# <span data-ttu-id="b50fc-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b50fc-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="b50fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b50fc-102">SYNOPSIS</span></span>


## <span data-ttu-id="b50fc-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b50fc-103">SYNTAX</span></span>

### <span data-ttu-id="b50fc-104">Shutdown (padrão)</span><span class="sxs-lookup"><span data-stu-id="b50fc-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b50fc-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b50fc-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b50fc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b50fc-106">DESCRIPTION</span></span>
<span data-ttu-id="b50fc-107">Desligar uma instância de função de infraestrutura para manutenção.</span><span class="sxs-lookup"><span data-stu-id="b50fc-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="b50fc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b50fc-108">EXAMPLES</span></span>

### <span data-ttu-id="b50fc-109">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="b50fc-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="b50fc-110">Desligar uma instância de função de infraestrutura para manutenção.</span><span class="sxs-lookup"><span data-stu-id="b50fc-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="b50fc-111">OS</span><span class="sxs-lookup"><span data-stu-id="b50fc-111">PARAMETERS</span></span>

### <span data-ttu-id="b50fc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b50fc-112">-AsJob</span></span>
<span data-ttu-id="b50fc-113">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b50fc-113">Run the command as a job</span></span>

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

### <span data-ttu-id="b50fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50fc-114">-DefaultProfile</span></span>
<span data-ttu-id="b50fc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b50fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50fc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b50fc-116">-Force</span></span>
<span data-ttu-id="b50fc-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b50fc-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b50fc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50fc-118">-InputObject</span></span>
<span data-ttu-id="b50fc-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b50fc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b50fc-120">-Local</span><span class="sxs-lookup"><span data-stu-id="b50fc-120">-Location</span></span>
<span data-ttu-id="b50fc-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b50fc-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b50fc-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b50fc-122">-Name</span></span>
<span data-ttu-id="b50fc-123">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b50fc-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b50fc-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b50fc-124">-NoWait</span></span>
<span data-ttu-id="b50fc-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b50fc-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b50fc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b50fc-126">-PassThru</span></span>
<span data-ttu-id="b50fc-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b50fc-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b50fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="b50fc-129">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="b50fc-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b50fc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b50fc-130">-SubscriptionId</span></span>
<span data-ttu-id="b50fc-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b50fc-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b50fc-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b50fc-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b50fc-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b50fc-133">-Confirm</span></span>
<span data-ttu-id="b50fc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50fc-135">-WhatIf</span></span>
<span data-ttu-id="b50fc-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b50fc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50fc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b50fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50fc-138">CommonParameters</span></span>
<span data-ttu-id="b50fc-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50fc-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b50fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50fc-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b50fc-141">INPUTS</span></span>

### <span data-ttu-id="b50fc-142">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b50fc-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b50fc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b50fc-143">OUTPUTS</span></span>

### <span data-ttu-id="b50fc-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b50fc-144">System.Boolean</span></span>



## <span data-ttu-id="b50fc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b50fc-145">NOTES</span></span>

<span data-ttu-id="b50fc-146">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b50fc-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b50fc-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b50fc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b50fc-148">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b50fc-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b50fc-149">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b50fc-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b50fc-150">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="b50fc-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b50fc-151">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="b50fc-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b50fc-152">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="b50fc-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b50fc-153">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="b50fc-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b50fc-154">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="b50fc-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b50fc-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b50fc-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b50fc-156">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b50fc-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b50fc-157">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="b50fc-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b50fc-158">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b50fc-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b50fc-159">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b50fc-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b50fc-160">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="b50fc-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b50fc-161">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="b50fc-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b50fc-162">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="b50fc-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b50fc-163">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b50fc-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b50fc-164">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="b50fc-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b50fc-165">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b50fc-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b50fc-166">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="b50fc-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b50fc-167">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b50fc-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="b50fc-168">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b50fc-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b50fc-169">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b50fc-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b50fc-170">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b50fc-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b50fc-171">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b50fc-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b50fc-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b50fc-172">RELATED LINKS</span></span>

