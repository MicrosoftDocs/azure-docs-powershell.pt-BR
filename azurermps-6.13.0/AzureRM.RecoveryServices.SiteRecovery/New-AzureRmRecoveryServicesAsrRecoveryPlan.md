---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: ceedd758a660828ed3ee93390384c1e212c55097
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426296"
---
# <span data-ttu-id="b28ab-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b28ab-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b28ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b28ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b28ab-103">Cria um plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="b28ab-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b28ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b28ab-104">SYNTAX</span></span>

### <span data-ttu-id="b28ab-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="b28ab-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b28ab-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b28ab-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b28ab-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b28ab-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b28ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b28ab-108">DESCRIPTION</span></span>
<span data-ttu-id="b28ab-109">O cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** cria um plano de recuperação do Azure site Recovery no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="b28ab-110">Um plano de recuperação reúne máquinas virtuais que pertencem a um aplicativo em uma unidade para permitir que elas sejam recuperadas juntas.</span><span class="sxs-lookup"><span data-stu-id="b28ab-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="b28ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b28ab-111">EXAMPLES</span></span>

### <span data-ttu-id="b28ab-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b28ab-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b28ab-113">Inicia a operação de criação do plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b28ab-114">OS</span><span class="sxs-lookup"><span data-stu-id="b28ab-114">PARAMETERS</span></span>

### <span data-ttu-id="b28ab-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="b28ab-115">-Azure</span></span>
<span data-ttu-id="b28ab-116">Parâmetro de opção para especificar que o local de recuperação para o plano de recuperação é o Azure.</span><span class="sxs-lookup"><span data-stu-id="b28ab-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

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

### <span data-ttu-id="b28ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28ab-117">-DefaultProfile</span></span>
<span data-ttu-id="b28ab-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b28ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ab-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b28ab-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="b28ab-120">Especifica o modelo de implantação de failover (clássico ou o Gerenciador de recursos) dos itens protegidos de replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b28ab-121">-Name</span></span>
<span data-ttu-id="b28ab-122">Nome do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-122">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b28ab-123">-Path</span></span>
<span data-ttu-id="b28ab-124">Especifica o caminho para o arquivo JSON de definição do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="b28ab-125">Uma definição do plano de recuperação JSON pode ser usada para criar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b28ab-126">-PrimaryFabric</span></span>
<span data-ttu-id="b28ab-127">Especifica o objeto de malha ASR para a malha ASR primária dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b28ab-128">-RecoveryFabric</span></span>
<span data-ttu-id="b28ab-129">Especifica o objeto de malha ASR para a malha ASR de recuperação dos itens protegidos pela replicação que farão parte deste plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b28ab-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b28ab-131">A lista de itens protegidos de replicação a serem adicionados ao primeiro grupo do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b28ab-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="b28ab-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b28ab-132">-Confirm</span></span>
<span data-ttu-id="b28ab-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b28ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28ab-134">-WhatIf</span></span>
<span data-ttu-id="b28ab-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b28ab-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b28ab-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b28ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b28ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28ab-137">CommonParameters</span></span>
<span data-ttu-id="b28ab-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28ab-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28ab-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28ab-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b28ab-140">INPUTS</span></span>

### <span data-ttu-id="b28ab-141">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="b28ab-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="b28ab-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b28ab-142">OUTPUTS</span></span>

### <span data-ttu-id="b28ab-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="b28ab-143">System.Object</span></span>

## <span data-ttu-id="b28ab-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b28ab-144">NOTES</span></span>

## <span data-ttu-id="b28ab-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b28ab-145">RELATED LINKS</span></span>

[<span data-ttu-id="b28ab-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b28ab-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b28ab-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b28ab-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b28ab-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b28ab-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


