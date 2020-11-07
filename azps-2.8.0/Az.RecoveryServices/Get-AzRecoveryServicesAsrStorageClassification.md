---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 9f0021658784c767e35d903a0a191ba28932f57a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773026"
---
# <span data-ttu-id="970a4-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="970a4-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="970a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="970a4-102">SYNOPSIS</span></span>
<span data-ttu-id="970a4-103">Obtém as classificações de armazenamento ASR disponíveis (detectadas) no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="970a4-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="970a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="970a4-104">SYNTAX</span></span>

### <span data-ttu-id="970a4-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="970a4-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="970a4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="970a4-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="970a4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="970a4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="970a4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="970a4-108">DESCRIPTION</span></span>
<span data-ttu-id="970a4-109">O cmdlet **Get-AzRecoveryServicesAsrStorageClassification** Obtém detalhes das classificações de armazenamento ASR descobertos no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="970a4-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="970a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="970a4-110">EXAMPLES</span></span>

### <span data-ttu-id="970a4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="970a4-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="970a4-112">Listar as classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="970a4-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="970a4-113">OS</span><span class="sxs-lookup"><span data-stu-id="970a4-113">PARAMETERS</span></span>

### <span data-ttu-id="970a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970a4-114">-DefaultProfile</span></span>
<span data-ttu-id="970a4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="970a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="970a4-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="970a4-116">-Fabric</span></span>
<span data-ttu-id="970a4-117">Especifica um objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="970a4-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="970a4-118">O cmdlet obtém os detalhes das classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="970a4-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="970a4-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="970a4-119">-FriendlyName</span></span>
<span data-ttu-id="970a4-120">Especifica o nome amigável do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="970a4-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="970a4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="970a4-121">-Name</span></span>
<span data-ttu-id="970a4-122">Especifica o nome do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="970a4-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="970a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970a4-123">CommonParameters</span></span>
<span data-ttu-id="970a4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970a4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="970a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970a4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="970a4-126">INPUTS</span></span>

### <span data-ttu-id="970a4-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="970a4-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="970a4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="970a4-128">OUTPUTS</span></span>

### <span data-ttu-id="970a4-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="970a4-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="970a4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="970a4-130">NOTES</span></span>

## <span data-ttu-id="970a4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="970a4-131">RELATED LINKS</span></span>
