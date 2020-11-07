---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945221"
---
# <span data-ttu-id="9254f-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="9254f-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="9254f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9254f-102">SYNOPSIS</span></span>
<span data-ttu-id="9254f-103">Repara um alerta.</span><span class="sxs-lookup"><span data-stu-id="9254f-103">Repairs an alert.</span></span>

## <span data-ttu-id="9254f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9254f-104">SYNTAX</span></span>

### <span data-ttu-id="9254f-105">Reparar (padrão)</span><span class="sxs-lookup"><span data-stu-id="9254f-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9254f-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9254f-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9254f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9254f-107">DESCRIPTION</span></span>
<span data-ttu-id="9254f-108">Repara um alerta.</span><span class="sxs-lookup"><span data-stu-id="9254f-108">Repairs an alert.</span></span>

## <span data-ttu-id="9254f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9254f-109">EXAMPLES</span></span>

### <span data-ttu-id="9254f-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="9254f-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="9254f-111">Repara um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="9254f-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="9254f-112">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="9254f-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="9254f-113">Repara um alerta por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="9254f-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="9254f-114">OS</span><span class="sxs-lookup"><span data-stu-id="9254f-114">PARAMETERS</span></span>

### <span data-ttu-id="9254f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9254f-115">-AsJob</span></span>
<span data-ttu-id="9254f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9254f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9254f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9254f-117">-DefaultProfile</span></span>
<span data-ttu-id="9254f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9254f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9254f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9254f-119">-InputObject</span></span>
<span data-ttu-id="9254f-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9254f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9254f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="9254f-121">-Location</span></span>
<span data-ttu-id="9254f-122">Nome da região</span><span class="sxs-lookup"><span data-stu-id="9254f-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9254f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9254f-123">-Name</span></span>
<span data-ttu-id="9254f-124">Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="9254f-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9254f-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9254f-125">-NoWait</span></span>
<span data-ttu-id="9254f-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9254f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9254f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9254f-127">-PassThru</span></span>
<span data-ttu-id="9254f-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9254f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9254f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9254f-129">-ResourceGroupName</span></span>
<span data-ttu-id="9254f-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9254f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9254f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9254f-131">-SubscriptionId</span></span>
<span data-ttu-id="9254f-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9254f-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9254f-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9254f-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9254f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9254f-134">-Confirm</span></span>
<span data-ttu-id="9254f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9254f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9254f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9254f-136">-WhatIf</span></span>
<span data-ttu-id="9254f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9254f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9254f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9254f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9254f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9254f-139">CommonParameters</span></span>
<span data-ttu-id="9254f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9254f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9254f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9254f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9254f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9254f-142">INPUTS</span></span>

### <span data-ttu-id="9254f-143">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9254f-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="9254f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9254f-144">OUTPUTS</span></span>

### <span data-ttu-id="9254f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9254f-145">System.Boolean</span></span>



## <span data-ttu-id="9254f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9254f-146">NOTES</span></span>

<span data-ttu-id="9254f-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9254f-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9254f-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9254f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9254f-149">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9254f-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9254f-150">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="9254f-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="9254f-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9254f-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9254f-152">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="9254f-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="9254f-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9254f-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9254f-154">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="9254f-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="9254f-155">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="9254f-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="9254f-156">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="9254f-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="9254f-157">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9254f-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9254f-158">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9254f-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9254f-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9254f-159">RELATED LINKS</span></span>

