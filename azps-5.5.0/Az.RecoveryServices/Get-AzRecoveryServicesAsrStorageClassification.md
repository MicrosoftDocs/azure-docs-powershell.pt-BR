---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117225"
---
# <span data-ttu-id="d1ec6-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d1ec6-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="d1ec6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ec6-103">Obtém as classificações de armazenamento ASR disponíveis(descobertas) no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="d1ec6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1ec6-104">SYNTAX</span></span>

### <span data-ttu-id="d1ec6-105">ByFabricObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1ec6-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ec6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d1ec6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ec6-107">ByObjectWithBjlyName</span><span class="sxs-lookup"><span data-stu-id="d1ec6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ec6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="d1ec6-109">O cmdlet **Get-AzRecoveryServicesAsrStorageClassification** obtém detalhes das classificações de armazenamento ASR descobertas no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="d1ec6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1ec6-110">EXAMPLES</span></span>

### <span data-ttu-id="d1ec6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1ec6-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="d1ec6-112">Liste as classificações de armazenamento descoberta correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="d1ec6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1ec6-113">PARAMETERS</span></span>

### <span data-ttu-id="d1ec6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ec6-114">-DefaultProfile</span></span>
<span data-ttu-id="d1ec6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d1ec6-116">-Malha</span><span class="sxs-lookup"><span data-stu-id="d1ec6-116">-Fabric</span></span>
<span data-ttu-id="d1ec6-117">Especifica um objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="d1ec6-118">O cmdlet obtém os detalhes das classificações de armazenamento descoberta correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="d1ec6-119">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="d1ec6-119">-FriendlyName</span></span>
<span data-ttu-id="d1ec6-120">Especifica o nome amigável do objeto de classificação de armazenamento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="d1ec6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1ec6-121">-Name</span></span>
<span data-ttu-id="d1ec6-122">Especifica o nome do objeto de classificação de armazenamento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="d1ec6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ec6-123">CommonParameters</span></span>
<span data-ttu-id="d1ec6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ec6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ec6-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1ec6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ec6-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1ec6-126">INPUTS</span></span>

### <span data-ttu-id="d1ec6-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d1ec6-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d1ec6-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1ec6-128">OUTPUTS</span></span>

### <span data-ttu-id="d1ec6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d1ec6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d1ec6-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d1ec6-130">NOTES</span></span>

## <span data-ttu-id="d1ec6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1ec6-131">RELATED LINKS</span></span>
