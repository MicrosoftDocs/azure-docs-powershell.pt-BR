---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: ec5ba90fd0c3dbdbf96ddf2370948de090306611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440310"
---
# <span data-ttu-id="ac241-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ac241-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ac241-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac241-102">SYNOPSIS</span></span>
<span data-ttu-id="ac241-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="ac241-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac241-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac241-104">SYNTAX</span></span>

### <span data-ttu-id="ac241-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac241-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac241-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ac241-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac241-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac241-107">DESCRIPTION</span></span>
<span data-ttu-id="ac241-108">O cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** Obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="ac241-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="ac241-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac241-109">EXAMPLES</span></span>

### <span data-ttu-id="ac241-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac241-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="ac241-111">Listar todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="ac241-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="ac241-112">OS</span><span class="sxs-lookup"><span data-stu-id="ac241-112">PARAMETERS</span></span>

### <span data-ttu-id="ac241-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac241-113">-DefaultProfile</span></span>
<span data-ttu-id="ac241-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac241-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ac241-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac241-115">-Name</span></span>
<span data-ttu-id="ac241-116">Especifica o nome do mapeamento de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="ac241-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="ac241-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="ac241-117">-StorageClassification</span></span>
<span data-ttu-id="ac241-118">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="ac241-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="ac241-119">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="ac241-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="ac241-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac241-120">CommonParameters</span></span>
<span data-ttu-id="ac241-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac241-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac241-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac241-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac241-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac241-123">INPUTS</span></span>

### <span data-ttu-id="ac241-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac241-124">None</span></span>

## <span data-ttu-id="ac241-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac241-125">OUTPUTS</span></span>

### <span data-ttu-id="ac241-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac241-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ac241-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac241-127">NOTES</span></span>

## <span data-ttu-id="ac241-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac241-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac241-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ac241-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ac241-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ac241-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
