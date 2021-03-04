---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889624"
---
# <span data-ttu-id="c1b2f-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c1b2f-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="c1b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b2f-103">Obtém as classificações de armazenamento ASR disponíveis(descobertas) no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="c1b2f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1b2f-104">SYNTAX</span></span>

### <span data-ttu-id="c1b2f-105">ByFabricObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1b2f-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1b2f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c1b2f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1b2f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c1b2f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b2f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1b2f-108">DESCRIPTION</span></span>
<span data-ttu-id="c1b2f-109">O cmdlet **Get-AzRecoveryServicesAsrStorageClassification** obtém detalhes das classificações de armazenamento ASR descobertas no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="c1b2f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-110">EXAMPLES</span></span>

### <span data-ttu-id="c1b2f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1b2f-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="c1b2f-112">Listar as classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="c1b2f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-113">PARAMETERS</span></span>

### <span data-ttu-id="c1b2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b2f-114">-DefaultProfile</span></span>
<span data-ttu-id="c1b2f-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c1b2f-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c1b2f-116">-Fabric</span></span>
<span data-ttu-id="c1b2f-117">Especifica um objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="c1b2f-118">O cmdlet obtém os detalhes das classificações de armazenamento descobertas correspondentes ao tecido ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b2f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c1b2f-119">-FriendlyName</span></span>
<span data-ttu-id="c1b2f-120">Especifica o nome amigável do objeto de classificação de armazenamento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b2f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1b2f-121">-Name</span></span>
<span data-ttu-id="c1b2f-122">Especifica o nome do objeto de classificação de armazenamento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="c1b2f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b2f-123">CommonParameters</span></span>
<span data-ttu-id="c1b2f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b2f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b2f-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1b2f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b2f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-126">INPUTS</span></span>

### <span data-ttu-id="c1b2f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c1b2f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c1b2f-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-128">OUTPUTS</span></span>

### <span data-ttu-id="c1b2f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c1b2f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c1b2f-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1b2f-130">NOTES</span></span>

## <span data-ttu-id="c1b2f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b2f-131">RELATED LINKS</span></span>
