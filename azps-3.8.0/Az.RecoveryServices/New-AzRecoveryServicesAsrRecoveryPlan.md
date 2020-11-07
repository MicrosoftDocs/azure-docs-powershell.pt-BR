---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944688"
---
# <span data-ttu-id="1aa60-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1aa60-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1aa60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aa60-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa60-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="1aa60-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="1aa60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aa60-104">SYNTAX</span></span>

### <span data-ttu-id="1aa60-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="1aa60-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa60-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1aa60-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa60-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="1aa60-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1aa60-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa60-109">O cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** cria um plano de recuperação de site do Azure, um plano de recuperação no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="1aa60-110">Um plano de recuperação reúne máquinas virtuais que pertencem a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="1aa60-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="1aa60-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aa60-111">EXAMPLES</span></span>

### <span data-ttu-id="1aa60-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1aa60-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1aa60-113">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1aa60-114">OS</span><span class="sxs-lookup"><span data-stu-id="1aa60-114">PARAMETERS</span></span>

### <span data-ttu-id="1aa60-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="1aa60-115">-Azure</span></span>
<span data-ttu-id="1aa60-116">Parâmetro switch especifica o cenário do Azure para recuperação de desastres do Azure, criação de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="1aa60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa60-117">-DefaultProfile</span></span>
<span data-ttu-id="1aa60-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1aa60-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="1aa60-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="1aa60-120">Especifica o modelo de implantação de failover (clássico ou o Gerenciador de recursos) dos itens protegidos de replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1aa60-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aa60-121">-Name</span></span>
<span data-ttu-id="1aa60-122">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa60-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1aa60-123">-Path</span></span>
<span data-ttu-id="1aa60-124">Especifica o caminho para o arquivo JSON de definição do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="1aa60-125">Uma definição do plano de recuperação JSON pode ser usada para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="1aa60-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1aa60-126">-PrimaryFabric</span></span>
<span data-ttu-id="1aa60-127">Especifica o objeto de malha ASR para a malha ASR primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa60-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1aa60-128">-RecoveryFabric</span></span>
<span data-ttu-id="1aa60-129">Especifica o objeto de malha ASR para a malha ASR de recuperação dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1aa60-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1aa60-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1aa60-131">A lista de itens protegidos de replicação a serem adicionados ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1aa60-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="1aa60-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1aa60-132">-Confirm</span></span>
<span data-ttu-id="1aa60-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aa60-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa60-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa60-134">-WhatIf</span></span>
<span data-ttu-id="1aa60-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1aa60-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1aa60-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1aa60-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa60-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa60-137">CommonParameters</span></span>
<span data-ttu-id="1aa60-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa60-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa60-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aa60-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa60-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1aa60-140">INPUTS</span></span>

### <span data-ttu-id="1aa60-141">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="1aa60-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="1aa60-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1aa60-142">OUTPUTS</span></span>

### <span data-ttu-id="1aa60-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1aa60-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1aa60-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1aa60-144">NOTES</span></span>

## <span data-ttu-id="1aa60-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aa60-145">RELATED LINKS</span></span>

[<span data-ttu-id="1aa60-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1aa60-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1aa60-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1aa60-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1aa60-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1aa60-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


