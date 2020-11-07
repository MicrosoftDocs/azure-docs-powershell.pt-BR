---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945166"
---
# <span data-ttu-id="25501-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="25501-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="25501-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25501-102">SYNOPSIS</span></span>
<span data-ttu-id="25501-103">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="25501-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25501-104">SYNTAX</span></span>

### <span data-ttu-id="25501-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="25501-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25501-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25501-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25501-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25501-107">DESCRIPTION</span></span>
<span data-ttu-id="25501-108">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="25501-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25501-109">EXAMPLES</span></span>

### <span data-ttu-id="25501-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="25501-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="25501-111">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="25501-112">OS</span><span class="sxs-lookup"><span data-stu-id="25501-112">PARAMETERS</span></span>

### <span data-ttu-id="25501-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25501-113">-AsJob</span></span>
<span data-ttu-id="25501-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="25501-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="25501-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25501-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="25501-116">-Force</span><span class="sxs-lookup"><span data-stu-id="25501-116">-Force</span></span>
<span data-ttu-id="25501-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="25501-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="25501-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25501-118">-InputObject</span></span>
<span data-ttu-id="25501-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="25501-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25501-120">-Local</span><span class="sxs-lookup"><span data-stu-id="25501-120">-Location</span></span>
<span data-ttu-id="25501-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="25501-121">Location of the resource.</span></span>

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

### <span data-ttu-id="25501-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="25501-122">-Name</span></span>
<span data-ttu-id="25501-123">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-123">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="25501-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="25501-124">-NoWait</span></span>
<span data-ttu-id="25501-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="25501-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25501-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25501-126">-PassThru</span></span>
<span data-ttu-id="25501-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="25501-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25501-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25501-128">-ResourceGroupName</span></span>
<span data-ttu-id="25501-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25501-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="25501-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25501-130">-SubscriptionId</span></span>
<span data-ttu-id="25501-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25501-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25501-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25501-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25501-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25501-133">-Confirm</span></span>
<span data-ttu-id="25501-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25501-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25501-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25501-135">-WhatIf</span></span>
<span data-ttu-id="25501-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25501-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25501-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25501-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25501-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25501-138">CommonParameters</span></span>
<span data-ttu-id="25501-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25501-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25501-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25501-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25501-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25501-141">INPUTS</span></span>

### <span data-ttu-id="25501-142">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="25501-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="25501-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25501-143">OUTPUTS</span></span>

### <span data-ttu-id="25501-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25501-144">System.Boolean</span></span>



## <span data-ttu-id="25501-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25501-145">NOTES</span></span>

<span data-ttu-id="25501-146">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="25501-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25501-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25501-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="25501-148">INPUTobject <IFabricAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="25501-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25501-149">`[Drive <String>]`: Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="25501-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="25501-150">`[EdgeGateway <String>]`: Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="25501-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="25501-151">`[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="25501-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="25501-152">`[FabricLocation <String>]`: Localização do fabric.</span><span class="sxs-lookup"><span data-stu-id="25501-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="25501-153">`[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="25501-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="25501-154">`[IPPool <String>]`: Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="25501-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="25501-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="25501-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25501-156">`[InfraRole <String>]`: Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="25501-157">`[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="25501-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="25501-158">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="25501-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="25501-159">`[LogicalNetwork <String>]`: Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="25501-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="25501-160">`[LogicalSubnet <String>]`: Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="25501-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="25501-161">`[MacAddressPool <String>]`: Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="25501-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="25501-162">`[Operation <String>]`: Identificador de operação.</span><span class="sxs-lookup"><span data-stu-id="25501-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="25501-163">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25501-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="25501-164">`[ScaleUnit <String>]`: Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="25501-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="25501-165">`[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="25501-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="25501-166">`[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="25501-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="25501-167">`[StoragePool <String>]`: Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="25501-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="25501-168">`[StorageSubSystem <String>]`: Nome do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="25501-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="25501-169">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25501-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25501-170">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25501-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="25501-171">`[Volume <String>]`: Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="25501-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="25501-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25501-172">RELATED LINKS</span></span>

