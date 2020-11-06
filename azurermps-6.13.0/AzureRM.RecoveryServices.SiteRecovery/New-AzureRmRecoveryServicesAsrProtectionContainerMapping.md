---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 35e338d5e6fd9dccbee1a099bc4dabf234cd8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426298"
---
# <span data-ttu-id="9a05c-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9a05c-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="9a05c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a05c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a05c-103">Cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="9a05c-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a05c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a05c-104">SYNTAX</span></span>

### <span data-ttu-id="9a05c-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="9a05c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a05c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9a05c-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a05c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a05c-107">DESCRIPTION</span></span>
<span data-ttu-id="9a05c-108">O cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="9a05c-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="9a05c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a05c-109">EXAMPLES</span></span>

### <span data-ttu-id="9a05c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a05c-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="9a05c-111">Inicia a criação do mapeamento de contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9a05c-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9a05c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a05c-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="9a05c-113">Inicia a criação do mapeamento de contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9a05c-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9a05c-114">OS</span><span class="sxs-lookup"><span data-stu-id="9a05c-114">PARAMETERS</span></span>

### <span data-ttu-id="9a05c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a05c-115">-DefaultProfile</span></span>
<span data-ttu-id="9a05c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a05c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9a05c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a05c-117">-Name</span></span>
<span data-ttu-id="9a05c-118">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="9a05c-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="9a05c-119">-Política</span><span class="sxs-lookup"><span data-stu-id="9a05c-119">-Policy</span></span>
<span data-ttu-id="9a05c-120">Especifica o objeto da política de replicação ASR para a política de replicação a ser usada no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="9a05c-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="9a05c-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9a05c-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="9a05c-122">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção principal a ser usado no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="9a05c-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="9a05c-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9a05c-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="9a05c-124">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção de recuperação a ser usado no mapeamento (usado se estiver duplicando para um local de recuperação que não seja o Azure.)</span><span class="sxs-lookup"><span data-stu-id="9a05c-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="9a05c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a05c-125">-Confirm</span></span>
<span data-ttu-id="9a05c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a05c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a05c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a05c-127">-WhatIf</span></span>
<span data-ttu-id="9a05c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a05c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a05c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a05c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a05c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a05c-130">CommonParameters</span></span>
<span data-ttu-id="9a05c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a05c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a05c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a05c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a05c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a05c-133">INPUTS</span></span>

### <span data-ttu-id="9a05c-134">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="9a05c-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="9a05c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a05c-135">OUTPUTS</span></span>

### <span data-ttu-id="9a05c-136">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9a05c-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9a05c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a05c-137">NOTES</span></span>

## <span data-ttu-id="9a05c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a05c-138">RELATED LINKS</span></span>

[<span data-ttu-id="9a05c-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9a05c-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="9a05c-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9a05c-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
