---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602459"
---
# <span data-ttu-id="cd706-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cd706-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="cd706-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd706-102">SYNOPSIS</span></span>
<span data-ttu-id="cd706-103">Cria um mapeamento de classificação de armazenamento ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cd706-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd706-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd706-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd706-105">DESCRIPTION</span></span>
<span data-ttu-id="cd706-106">O cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cria um mapeamento de classificação de armazenamento do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cd706-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="cd706-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd706-107">EXAMPLES</span></span>

### <span data-ttu-id="cd706-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd706-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="cd706-109">Inicia a operação de criação do mapeamento de classificação de armazenamento com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="cd706-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cd706-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd706-110">PARAMETERS</span></span>

### <span data-ttu-id="cd706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd706-111">-DefaultProfile</span></span>
<span data-ttu-id="cd706-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd706-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cd706-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd706-113">-Name</span></span>
<span data-ttu-id="cd706-114">Especifica um nome para o mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="cd706-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="cd706-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="cd706-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="cd706-116">Especifica o objeto de classificação de armazenamento ASR primário para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="cd706-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd706-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="cd706-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="cd706-118">Especifica o objeto de classificação de armazenamento ASR de recuperação para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="cd706-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd706-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd706-119">-Confirm</span></span>
<span data-ttu-id="cd706-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd706-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd706-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd706-121">-WhatIf</span></span>
<span data-ttu-id="cd706-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd706-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd706-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd706-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd706-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd706-124">CommonParameters</span></span>
<span data-ttu-id="cd706-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd706-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd706-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd706-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd706-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd706-127">INPUTS</span></span>

### <span data-ttu-id="cd706-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="cd706-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="cd706-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd706-129">OUTPUTS</span></span>

### <span data-ttu-id="cd706-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cd706-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cd706-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd706-131">NOTES</span></span>

## <span data-ttu-id="cd706-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd706-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd706-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cd706-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="cd706-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="cd706-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
