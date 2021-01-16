---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258259"
---
# <span data-ttu-id="dcdf8-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcdf8-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="dcdf8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcdf8-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdf8-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="dcdf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcdf8-104">SYNTAX</span></span>

### <span data-ttu-id="dcdf8-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcdf8-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcdf8-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="dcdf8-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcdf8-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="dcdf8-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcdf8-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="dcdf8-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcdf8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcdf8-109">DESCRIPTION</span></span>
<span data-ttu-id="dcdf8-110">O cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** cria um plano de recuperação de site do Azure, um plano de recuperação no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="dcdf8-111">Um plano de recuperação reúne máquinas virtuais que pertencem a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="dcdf8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcdf8-112">EXAMPLES</span></span>

### <span data-ttu-id="dcdf8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcdf8-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="dcdf8-114">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dcdf8-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dcdf8-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="dcdf8-116">Inicia a operação de criação do plano de recuperação do Azure Zone para zona replicada de itens e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dcdf8-117">OS</span><span class="sxs-lookup"><span data-stu-id="dcdf8-117">PARAMETERS</span></span>

### <span data-ttu-id="dcdf8-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="dcdf8-118">-Azure</span></span>
<span data-ttu-id="dcdf8-119">Parâmetro switch especifica o cenário do Azure para recuperação de desastres do Azure, criação de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="dcdf8-120">-AzureZoneToZone</span></span>
<span data-ttu-id="dcdf8-121">Parâmetro switch especifica a criação do item replicado no cenário zona para zona do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdf8-122">-DefaultProfile</span></span>
<span data-ttu-id="dcdf8-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="dcdf8-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="dcdf8-125">Especifica o modelo de implantação de failover (clássico ou o Gerenciador de recursos) dos itens protegidos de replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcdf8-126">-Name</span></span>
<span data-ttu-id="dcdf8-127">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="dcdf8-128">-Path</span></span>
<span data-ttu-id="dcdf8-129">Especifica o caminho para o arquivo JSON de definição do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="dcdf8-130">Uma definição do plano de recuperação JSON pode ser usada para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="dcdf8-131">-PrimaryFabric</span></span>
<span data-ttu-id="dcdf8-132">Especifica o objeto de malha ASR para a malha ASR primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="dcdf8-133">-PrimaryZone</span></span>
<span data-ttu-id="dcdf8-134">Especifica a zona Availabilty primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="dcdf8-135">-RecoveryFabric</span></span>
<span data-ttu-id="dcdf8-136">Especifica o objeto de malha ASR para a malha ASR de recuperação dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="dcdf8-137">-RecoveryZone</span></span>
<span data-ttu-id="dcdf8-138">Especifica a zona Availabilty primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dcdf8-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="dcdf8-140">A lista de itens protegidos de replicação a serem adicionados ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdf8-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcdf8-141">-Confirm</span></span>
<span data-ttu-id="dcdf8-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcdf8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcdf8-143">-WhatIf</span></span>
<span data-ttu-id="dcdf8-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcdf8-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcdf8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdf8-146">CommonParameters</span></span>
<span data-ttu-id="dcdf8-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdf8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdf8-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcdf8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdf8-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcdf8-149">INPUTS</span></span>

### <span data-ttu-id="dcdf8-150">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="dcdf8-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="dcdf8-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcdf8-151">OUTPUTS</span></span>

### <span data-ttu-id="dcdf8-152">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dcdf8-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dcdf8-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcdf8-153">NOTES</span></span>

## <span data-ttu-id="dcdf8-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcdf8-154">RELATED LINKS</span></span>

[<span data-ttu-id="dcdf8-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcdf8-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="dcdf8-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcdf8-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="dcdf8-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dcdf8-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


