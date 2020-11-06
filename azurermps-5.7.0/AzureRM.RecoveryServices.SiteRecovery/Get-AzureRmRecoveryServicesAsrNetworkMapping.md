---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428840"
---
# <span data-ttu-id="3ff29-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3ff29-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3ff29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff29-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff29-103">Obtém informações sobre mapeamentos de rede de recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="3ff29-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff29-104">SYNTAX</span></span>

### <span data-ttu-id="3ff29-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ff29-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff29-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="3ff29-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff29-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ff29-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff29-108">O cmdlet **Get-AzureRmRecoveryServicesAsrNetworkMapping** Obtém informações sobre os mapeamentos de rede do Azure site Recovery para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3ff29-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="3ff29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ff29-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff29-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ff29-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="3ff29-111">Obtém todos os mapeamentos de redes para a rede passada.</span><span class="sxs-lookup"><span data-stu-id="3ff29-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="3ff29-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3ff29-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="3ff29-113">Obtém o mapeamento de redes com o nome fornecido na malha especificada do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3ff29-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="3ff29-114">OS</span><span class="sxs-lookup"><span data-stu-id="3ff29-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff29-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff29-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff29-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff29-117">-Name</span></span>
<span data-ttu-id="3ff29-118">O nome do objeto de mapeamento de rede ASR a obter.</span><span class="sxs-lookup"><span data-stu-id="3ff29-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff29-119">-Rede</span><span class="sxs-lookup"><span data-stu-id="3ff29-119">-Network</span></span>
<span data-ttu-id="3ff29-120">Obter os mapeamentos de rede ASR correspondentes ao objeto ASR de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="3ff29-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff29-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3ff29-121">-PrimaryFabric</span></span>
<span data-ttu-id="3ff29-122">Obter os mapeamentos de rede ASR correspondentes ao objeto de malha primária especificado.</span><span class="sxs-lookup"><span data-stu-id="3ff29-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff29-123">CommonParameters</span></span>
<span data-ttu-id="3ff29-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff29-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff29-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff29-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ff29-126">INPUTS</span></span>

### <span data-ttu-id="3ff29-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3ff29-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3ff29-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ff29-128">OUTPUTS</span></span>

### <span data-ttu-id="3ff29-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3ff29-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3ff29-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ff29-130">NOTES</span></span>

## <span data-ttu-id="3ff29-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff29-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ff29-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3ff29-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3ff29-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3ff29-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
