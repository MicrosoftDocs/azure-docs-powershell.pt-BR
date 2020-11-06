---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5e0c3627616ae7310785943f73ed7c07f0f263b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599659"
---
# <span data-ttu-id="fd149-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd149-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="fd149-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd149-102">SYNOPSIS</span></span>
<span data-ttu-id="fd149-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="fd149-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="fd149-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd149-104">SYNTAX</span></span>

### <span data-ttu-id="fd149-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd149-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd149-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="fd149-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd149-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="fd149-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd149-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd149-108">DESCRIPTION</span></span>
<span data-ttu-id="fd149-109">O cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** cria um plano de recuperação do Azure site Recovery no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="fd149-110">Um plano de recuperação reúne máquinas virtuais que pertencem a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="fd149-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="fd149-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd149-111">EXAMPLES</span></span>

### <span data-ttu-id="fd149-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd149-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="fd149-113">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="fd149-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fd149-114">OS</span><span class="sxs-lookup"><span data-stu-id="fd149-114">PARAMETERS</span></span>

### <span data-ttu-id="fd149-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="fd149-115">-Azure</span></span>
<span data-ttu-id="fd149-116">{{Preencher descrição do Azure}}</span><span class="sxs-lookup"><span data-stu-id="fd149-116">{{Fill Azure Description}}</span></span>

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

### <span data-ttu-id="fd149-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd149-117">-DefaultProfile</span></span>
<span data-ttu-id="fd149-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd149-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fd149-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="fd149-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="fd149-120">Especifica o modelo de implantação de failover (clássico ou o Gerenciador de recursos) dos itens protegidos de replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="fd149-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd149-121">-Name</span></span>
<span data-ttu-id="fd149-122">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-122">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="fd149-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fd149-123">-Path</span></span>
<span data-ttu-id="fd149-124">Especifica o caminho para o arquivo JSON de definição do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="fd149-125">Uma definição do plano de recuperação JSON pode ser usada para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="fd149-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="fd149-126">-PrimaryFabric</span></span>
<span data-ttu-id="fd149-127">Especifica o objeto de malha ASR para a malha ASR primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="fd149-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="fd149-128">-RecoveryFabric</span></span>
<span data-ttu-id="fd149-129">Especifica o objeto de malha ASR para a malha ASR de recuperação dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="fd149-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fd149-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fd149-131">A lista de itens protegidos de replicação a serem adicionados ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd149-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="fd149-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd149-132">-Confirm</span></span>
<span data-ttu-id="fd149-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd149-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd149-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd149-134">-WhatIf</span></span>
<span data-ttu-id="fd149-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd149-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd149-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd149-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd149-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd149-137">CommonParameters</span></span>
<span data-ttu-id="fd149-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd149-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd149-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd149-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd149-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd149-140">INPUTS</span></span>

### <span data-ttu-id="fd149-141">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="fd149-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="fd149-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd149-142">OUTPUTS</span></span>

### <span data-ttu-id="fd149-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fd149-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fd149-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd149-144">NOTES</span></span>

## <span data-ttu-id="fd149-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd149-145">RELATED LINKS</span></span>

[<span data-ttu-id="fd149-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd149-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd149-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd149-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd149-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd149-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


