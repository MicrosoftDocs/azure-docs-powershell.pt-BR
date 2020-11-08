---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124430"
---
# <span data-ttu-id="e5f7c-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f7c-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="e5f7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f7c-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="e5f7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5f7c-104">SYNTAX</span></span>

### <span data-ttu-id="e5f7c-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5f7c-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f7c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e5f7c-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f7c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5f7c-107">DESCRIPTION</span></span>
<span data-ttu-id="e5f7c-108">O cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** Obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="e5f7c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5f7c-109">EXAMPLES</span></span>

### <span data-ttu-id="e5f7c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5f7c-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="e5f7c-111">Listar todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="e5f7c-112">OS</span><span class="sxs-lookup"><span data-stu-id="e5f7c-112">PARAMETERS</span></span>

### <span data-ttu-id="e5f7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f7c-113">-DefaultProfile</span></span>
<span data-ttu-id="e5f7c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5f7c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5f7c-115">-Name</span></span>
<span data-ttu-id="e5f7c-116">Especifica o nome do mapeamento de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="e5f7c-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="e5f7c-117">-StorageClassification</span></span>
<span data-ttu-id="e5f7c-118">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="e5f7c-119">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="e5f7c-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="e5f7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f7c-120">CommonParameters</span></span>
<span data-ttu-id="e5f7c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f7c-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5f7c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f7c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5f7c-123">INPUTS</span></span>

### <span data-ttu-id="e5f7c-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e5f7c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e5f7c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5f7c-125">OUTPUTS</span></span>

### <span data-ttu-id="e5f7c-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f7c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="e5f7c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5f7c-127">NOTES</span></span>

## <span data-ttu-id="e5f7c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5f7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5f7c-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f7c-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="e5f7c-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f7c-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
