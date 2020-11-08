---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116561"
---
# <span data-ttu-id="8bd99-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8bd99-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="8bd99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bd99-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd99-103">Cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="8bd99-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="8bd99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bd99-104">SYNTAX</span></span>

### <span data-ttu-id="8bd99-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bd99-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bd99-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8bd99-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bd99-107">DESCRIPTION</span></span>
<span data-ttu-id="8bd99-108">O cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="8bd99-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="8bd99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bd99-109">EXAMPLES</span></span>

### <span data-ttu-id="8bd99-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bd99-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="8bd99-111">Inicia a criação do mapeamento de contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8bd99-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8bd99-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bd99-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="8bd99-113">Inicia a criação do mapeamento de contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8bd99-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8bd99-114">OS</span><span class="sxs-lookup"><span data-stu-id="8bd99-114">PARAMETERS</span></span>

### <span data-ttu-id="8bd99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd99-115">-DefaultProfile</span></span>
<span data-ttu-id="8bd99-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8bd99-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bd99-117">-Name</span></span>
<span data-ttu-id="8bd99-118">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="8bd99-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd99-119">-Política</span><span class="sxs-lookup"><span data-stu-id="8bd99-119">-Policy</span></span>
<span data-ttu-id="8bd99-120">Especifica o objeto da política de replicação ASR para a política de replicação a ser usada no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="8bd99-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd99-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8bd99-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="8bd99-122">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção principal a ser usado no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="8bd99-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd99-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8bd99-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="8bd99-124">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção de recuperação a ser usado no mapeamento (usado se estiver duplicando para um local de recuperação que não seja o Azure.)</span><span class="sxs-lookup"><span data-stu-id="8bd99-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd99-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bd99-125">-Confirm</span></span>
<span data-ttu-id="8bd99-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd99-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd99-127">-WhatIf</span></span>
<span data-ttu-id="8bd99-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bd99-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bd99-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bd99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd99-130">CommonParameters</span></span>
<span data-ttu-id="8bd99-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd99-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bd99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd99-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bd99-133">INPUTS</span></span>

### <span data-ttu-id="8bd99-134">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8bd99-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="8bd99-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bd99-135">OUTPUTS</span></span>

### <span data-ttu-id="8bd99-136">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8bd99-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8bd99-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bd99-137">NOTES</span></span>

## <span data-ttu-id="8bd99-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bd99-138">RELATED LINKS</span></span>

[<span data-ttu-id="8bd99-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8bd99-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="8bd99-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8bd99-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
