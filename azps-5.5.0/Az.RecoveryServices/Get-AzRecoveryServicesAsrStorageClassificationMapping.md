---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114967"
---
# <span data-ttu-id="916be-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="916be-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="916be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="916be-102">SYNOPSIS</span></span>
<span data-ttu-id="916be-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="916be-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="916be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="916be-104">SYNTAX</span></span>

### <span data-ttu-id="916be-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="916be-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="916be-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="916be-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="916be-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="916be-107">DESCRIPTION</span></span>
<span data-ttu-id="916be-108">O cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="916be-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="916be-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="916be-109">EXAMPLES</span></span>

### <span data-ttu-id="916be-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="916be-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="916be-111">Liste todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="916be-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="916be-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="916be-112">PARAMETERS</span></span>

### <span data-ttu-id="916be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916be-113">-DefaultProfile</span></span>
<span data-ttu-id="916be-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="916be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="916be-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="916be-115">-Name</span></span>
<span data-ttu-id="916be-116">Especifica o nome do mapeamento de classificação de armazenamento para obter.</span><span class="sxs-lookup"><span data-stu-id="916be-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="916be-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="916be-117">-StorageClassification</span></span>
<span data-ttu-id="916be-118">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="916be-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="916be-119">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="916be-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="916be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916be-120">CommonParameters</span></span>
<span data-ttu-id="916be-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="916be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916be-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="916be-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916be-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="916be-123">INPUTS</span></span>

### <span data-ttu-id="916be-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="916be-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="916be-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="916be-125">OUTPUTS</span></span>

### <span data-ttu-id="916be-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="916be-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="916be-127">Notas</span><span class="sxs-lookup"><span data-stu-id="916be-127">NOTES</span></span>

## <span data-ttu-id="916be-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="916be-128">RELATED LINKS</span></span>

[<span data-ttu-id="916be-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="916be-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="916be-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="916be-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
