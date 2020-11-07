---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940605"
---
# <span data-ttu-id="d748b-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d748b-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d748b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d748b-102">SYNOPSIS</span></span>
<span data-ttu-id="d748b-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="d748b-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="d748b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d748b-104">SYNTAX</span></span>

### <span data-ttu-id="d748b-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="d748b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d748b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d748b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d748b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d748b-107">DESCRIPTION</span></span>
<span data-ttu-id="d748b-108">O cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** Obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="d748b-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="d748b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d748b-109">EXAMPLES</span></span>

### <span data-ttu-id="d748b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d748b-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="d748b-111">Listar todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="d748b-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="d748b-112">OS</span><span class="sxs-lookup"><span data-stu-id="d748b-112">PARAMETERS</span></span>

### <span data-ttu-id="d748b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d748b-113">-DefaultProfile</span></span>
<span data-ttu-id="d748b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d748b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d748b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d748b-115">-Name</span></span>
<span data-ttu-id="d748b-116">Especifica o nome do mapeamento de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d748b-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="d748b-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="d748b-117">-StorageClassification</span></span>
<span data-ttu-id="d748b-118">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="d748b-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="d748b-119">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="d748b-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="d748b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d748b-120">CommonParameters</span></span>
<span data-ttu-id="d748b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d748b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d748b-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d748b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d748b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d748b-123">INPUTS</span></span>

### <span data-ttu-id="d748b-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d748b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d748b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d748b-125">OUTPUTS</span></span>

### <span data-ttu-id="d748b-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d748b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="d748b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d748b-127">NOTES</span></span>

## <span data-ttu-id="d748b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d748b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d748b-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d748b-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d748b-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d748b-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
