---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429165"
---
# <span data-ttu-id="55f6a-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55f6a-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="55f6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="55f6a-103">Cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="55f6a-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55f6a-104">SYNTAX</span></span>

### <span data-ttu-id="55f6a-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="55f6a-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f6a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="55f6a-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f6a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="55f6a-108">O cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cria um mapeamento de contêiner de proteção do Azure site Recovery associando a política de replicação especificada ao contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="55f6a-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="55f6a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="55f6a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55f6a-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="55f6a-111">Inicia a criação do mapeamento de contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="55f6a-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="55f6a-112">OS</span><span class="sxs-lookup"><span data-stu-id="55f6a-112">PARAMETERS</span></span>

### <span data-ttu-id="55f6a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="55f6a-113">-Name</span></span>
<span data-ttu-id="55f6a-114">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="55f6a-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f6a-115">-Política</span><span class="sxs-lookup"><span data-stu-id="55f6a-115">-Policy</span></span>
<span data-ttu-id="55f6a-116">Especifica o objeto da política de replicação ASR para a política de replicação a ser usada no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="55f6a-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f6a-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="55f6a-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="55f6a-118">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção principal a ser usado no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="55f6a-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f6a-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="55f6a-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="55f6a-120">Especifica o objeto de contêiner de proteção ASR para o contêiner de proteção de recuperação a ser usado no mapeamento (usado se estiver duplicando para um local de recuperação que não seja o Azure.)</span><span class="sxs-lookup"><span data-stu-id="55f6a-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f6a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55f6a-121">-Confirm</span></span>
<span data-ttu-id="55f6a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f6a-123">-WhatIf</span></span>
<span data-ttu-id="55f6a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55f6a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55f6a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55f6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f6a-126">CommonParameters</span></span>
<span data-ttu-id="55f6a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f6a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f6a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55f6a-129">INPUTS</span></span>

### <span data-ttu-id="55f6a-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="55f6a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="55f6a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55f6a-131">OUTPUTS</span></span>

### <span data-ttu-id="55f6a-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="55f6a-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="55f6a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55f6a-133">NOTES</span></span>

## <span data-ttu-id="55f6a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55f6a-134">RELATED LINKS</span></span>

[<span data-ttu-id="55f6a-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55f6a-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="55f6a-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55f6a-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
