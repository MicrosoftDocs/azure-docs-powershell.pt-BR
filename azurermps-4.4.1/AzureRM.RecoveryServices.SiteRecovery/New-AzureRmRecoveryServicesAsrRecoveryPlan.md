---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602424"
---
# <span data-ttu-id="2e257-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e257-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2e257-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e257-102">SYNOPSIS</span></span>
<span data-ttu-id="2e257-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="2e257-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e257-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e257-104">SYNTAX</span></span>

### <span data-ttu-id="2e257-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e257-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e257-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="2e257-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e257-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="2e257-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e257-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e257-108">DESCRIPTION</span></span>
<span data-ttu-id="2e257-109">O cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** cria um plano de recuperação do Azure site Recovery no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="2e257-110">Um plano de recuperação reúne máquinas virtuais que pertencem a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="2e257-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="2e257-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e257-111">EXAMPLES</span></span>

### <span data-ttu-id="2e257-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e257-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="2e257-113">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="2e257-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2e257-114">OS</span><span class="sxs-lookup"><span data-stu-id="2e257-114">PARAMETERS</span></span>

### <span data-ttu-id="2e257-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="2e257-115">-Azure</span></span>
<span data-ttu-id="2e257-116">Parâmetro de opção para especificar que o local de recuperação para o plano de recuperação é o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e257-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="2e257-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="2e257-118">Especifica o modelo de implantação de failover (clássico ou o Gerenciador de recursos) dos itens protegidos de replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e257-119">-Name</span></span>
<span data-ttu-id="2e257-120">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2e257-121">-Path</span></span>
<span data-ttu-id="2e257-122">Especifica o caminho para o arquivo JSON de definição do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="2e257-123">Uma definição do plano de recuperação JSON pode ser usada para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="2e257-124">-PrimaryFabric</span></span>
<span data-ttu-id="2e257-125">Especifica o objeto de malha ASR para a malha ASR primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2e257-126">-RecoveryFabric</span></span>
<span data-ttu-id="2e257-127">Especifica o objeto de malha ASR para a malha ASR de recuperação dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e257-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2e257-129">A lista de itens protegidos de replicação a serem adicionados ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e257-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e257-130">-Confirm</span></span>
<span data-ttu-id="2e257-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e257-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e257-132">-WhatIf</span></span>
<span data-ttu-id="2e257-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e257-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e257-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e257-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e257-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e257-135">CommonParameters</span></span>
<span data-ttu-id="2e257-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e257-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e257-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e257-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e257-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e257-138">INPUTS</span></span>

### <span data-ttu-id="2e257-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="2e257-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="2e257-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e257-140">OUTPUTS</span></span>

### <span data-ttu-id="2e257-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="2e257-141">System.Object</span></span>

## <span data-ttu-id="2e257-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e257-142">NOTES</span></span>

## <span data-ttu-id="2e257-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e257-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e257-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e257-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2e257-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e257-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2e257-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2e257-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


