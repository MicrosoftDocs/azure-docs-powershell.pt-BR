---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430077"
---
# <span data-ttu-id="60c4d-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="60c4d-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="60c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="60c4d-103">Exclui o mapeamento de classificação de armazenamento ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="60c4d-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60c4d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="60c4d-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** exclui o mapeamento de classificação de armazenamento do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="60c4d-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="60c4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="60c4d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60c4d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="60c4d-109">Inicia a exclusão do mapeamento de classificação de armazenamento especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="60c4d-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="60c4d-110">OS</span><span class="sxs-lookup"><span data-stu-id="60c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="60c4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c4d-111">-DefaultProfile</span></span>
<span data-ttu-id="60c4d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60c4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="60c4d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60c4d-113">-InputObject</span></span>
<span data-ttu-id="60c4d-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de classificação de armazenamento ASR correspondente ao mapeamento de classificação de armazenamento ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="60c4d-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60c4d-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60c4d-115">-Confirm</span></span>
<span data-ttu-id="60c4d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c4d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c4d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c4d-117">-WhatIf</span></span>
<span data-ttu-id="60c4d-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60c4d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60c4d-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60c4d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c4d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c4d-120">CommonParameters</span></span>
<span data-ttu-id="60c4d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c4d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c4d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c4d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c4d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60c4d-123">INPUTS</span></span>

### <span data-ttu-id="60c4d-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="60c4d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="60c4d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60c4d-125">OUTPUTS</span></span>

### <span data-ttu-id="60c4d-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="60c4d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60c4d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60c4d-127">NOTES</span></span>

## <span data-ttu-id="60c4d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60c4d-128">RELATED LINKS</span></span>

[<span data-ttu-id="60c4d-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="60c4d-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="60c4d-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="60c4d-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)