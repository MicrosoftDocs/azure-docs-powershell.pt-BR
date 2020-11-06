---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602014"
---
# <span data-ttu-id="c741d-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c741d-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c741d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c741d-102">SYNOPSIS</span></span>
<span data-ttu-id="c741d-103">Cria um mapeamento de classificação de armazenamento ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c741d-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c741d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c741d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c741d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c741d-105">DESCRIPTION</span></span>
<span data-ttu-id="c741d-106">O cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cria um mapeamento de classificação de armazenamento do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c741d-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="c741d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c741d-107">EXAMPLES</span></span>

### <span data-ttu-id="c741d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c741d-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="c741d-109">Inicia a operação de criação do mapeamento de classificação de armazenamento com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="c741d-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c741d-110">OS</span><span class="sxs-lookup"><span data-stu-id="c741d-110">PARAMETERS</span></span>

### <span data-ttu-id="c741d-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c741d-111">-Confirm</span></span>
<span data-ttu-id="c741d-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c741d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c741d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c741d-113">-DefaultProfile</span></span>
<span data-ttu-id="c741d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c741d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c741d-115">-Name</span></span>
<span data-ttu-id="c741d-116">Especifica um nome para o mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="c741d-116">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="c741d-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c741d-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c741d-118">Especifica o objeto de classificação de armazenamento ASR primário para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="c741d-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c741d-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c741d-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c741d-120">Especifica o objeto de classificação de armazenamento ASR de recuperação para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="c741d-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c741d-121">-WhatIf</span></span>
<span data-ttu-id="c741d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c741d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c741d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c741d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c741d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c741d-124">CommonParameters</span></span>
<span data-ttu-id="c741d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c741d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c741d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c741d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c741d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c741d-127">INPUTS</span></span>

### <span data-ttu-id="c741d-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c741d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c741d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c741d-129">OUTPUTS</span></span>

### <span data-ttu-id="c741d-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c741d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c741d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c741d-131">NOTES</span></span>

## <span data-ttu-id="c741d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c741d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c741d-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c741d-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c741d-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c741d-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
