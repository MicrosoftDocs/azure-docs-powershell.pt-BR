---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889621"
---
# <span data-ttu-id="1f580-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f580-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1f580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f580-102">SYNOPSIS</span></span>
<span data-ttu-id="1f580-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="1f580-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="1f580-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f580-104">SYNTAX</span></span>

### <span data-ttu-id="1f580-105">EnterpriseToEnterprise (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f580-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f580-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1f580-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f580-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="1f580-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f580-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="1f580-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f580-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f580-109">DESCRIPTION</span></span>
<span data-ttu-id="1f580-110">O cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** cria um Azure Site Recovery, plano de recuperação no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="1f580-111">Um plano de recuperação reúne máquinas virtuais pertencentes a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="1f580-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="1f580-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f580-112">EXAMPLES</span></span>

### <span data-ttu-id="1f580-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f580-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1f580-114">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="1f580-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1f580-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f580-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1f580-116">Inicia a operação de criação do plano de recuperação para zona do Azure para zonar itens replicados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="1f580-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1f580-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f580-117">PARAMETERS</span></span>

### <span data-ttu-id="1f580-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="1f580-118">-Azure</span></span>
<span data-ttu-id="1f580-119">O parâmetro Switch especifica o cenário do azure para recuperação de desastre do azure, criação de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="1f580-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="1f580-120">-AzureZoneToZone</span></span>
<span data-ttu-id="1f580-121">O parâmetro Switch especifica a criação do item replicado no cenário de zona do azure para zona.</span><span class="sxs-lookup"><span data-stu-id="1f580-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="1f580-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f580-122">-DefaultProfile</span></span>
<span data-ttu-id="1f580-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f580-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1f580-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="1f580-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="1f580-125">Especifica o modelo de implantação de failover (Clássico ou Gerenciador de Recursos) dos itens protegidos por replicação que serão parte desse plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1f580-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1f580-126">-Name</span></span>
<span data-ttu-id="1f580-127">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="1f580-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1f580-128">-Path</span></span>
<span data-ttu-id="1f580-129">Especifica o caminho para o arquivo json de definição de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="1f580-130">Um json de definição de plano de recuperação pode ser usado para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="1f580-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1f580-131">-PrimaryFabric</span></span>
<span data-ttu-id="1f580-132">Especifica o objeto de malha ASR para o tecido ASR principal dos itens protegidos de replicação que fará parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1f580-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="1f580-133">-PrimaryZone</span></span>
<span data-ttu-id="1f580-134">Especifica a zona Availabilty primária dos itens protegidos de replicação que fará parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1f580-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1f580-135">-RecoveryFabric</span></span>
<span data-ttu-id="1f580-136">Especifica o objeto de malha ASR para o fabrico ASR de recuperação dos itens protegidos pela replicação que fará parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1f580-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="1f580-137">-RecoveryZone</span></span>
<span data-ttu-id="1f580-138">Especifica a zona Availabilty primária dos itens protegidos de replicação que fará parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1f580-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f580-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1f580-140">A lista de itens protegidos de replicação para adicionar ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f580-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="1f580-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f580-141">-Confirm</span></span>
<span data-ttu-id="1f580-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f580-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f580-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f580-143">-WhatIf</span></span>
<span data-ttu-id="1f580-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f580-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f580-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f580-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f580-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f580-146">CommonParameters</span></span>
<span data-ttu-id="1f580-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f580-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f580-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f580-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f580-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f580-149">INPUTS</span></span>

### <span data-ttu-id="1f580-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="1f580-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="1f580-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f580-151">OUTPUTS</span></span>

### <span data-ttu-id="1f580-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1f580-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1f580-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f580-153">NOTES</span></span>

## <span data-ttu-id="1f580-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f580-154">RELATED LINKS</span></span>

[<span data-ttu-id="1f580-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f580-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f580-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f580-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f580-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f580-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


