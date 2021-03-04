---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886862"
---
# <span data-ttu-id="016b0-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="016b0-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="016b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="016b0-102">SYNOPSIS</span></span>
<span data-ttu-id="016b0-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="016b0-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="016b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="016b0-104">SYNTAX</span></span>

### <span data-ttu-id="016b0-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="016b0-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="016b0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="016b0-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="016b0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="016b0-107">DESCRIPTION</span></span>
<span data-ttu-id="016b0-108">O cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="016b0-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="016b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="016b0-109">EXAMPLES</span></span>

### <span data-ttu-id="016b0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="016b0-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="016b0-111">Listar todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="016b0-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="016b0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="016b0-112">PARAMETERS</span></span>

### <span data-ttu-id="016b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016b0-113">-DefaultProfile</span></span>
<span data-ttu-id="016b0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="016b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="016b0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="016b0-115">-Name</span></span>
<span data-ttu-id="016b0-116">Especifica o nome do mapeamento de classificação de armazenamento a ser feito.</span><span class="sxs-lookup"><span data-stu-id="016b0-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b0-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="016b0-117">-StorageClassification</span></span>
<span data-ttu-id="016b0-118">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="016b0-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="016b0-119">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="016b0-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="016b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016b0-120">CommonParameters</span></span>
<span data-ttu-id="016b0-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016b0-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="016b0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016b0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="016b0-123">INPUTS</span></span>

### <span data-ttu-id="016b0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="016b0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="016b0-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="016b0-125">OUTPUTS</span></span>

### <span data-ttu-id="016b0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="016b0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="016b0-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="016b0-127">NOTES</span></span>

## <span data-ttu-id="016b0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="016b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="016b0-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="016b0-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="016b0-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="016b0-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
