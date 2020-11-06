---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430079"
---
# <span data-ttu-id="fce74-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="fce74-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="fce74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fce74-102">SYNOPSIS</span></span>
<span data-ttu-id="fce74-103">Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="fce74-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fce74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fce74-104">SYNTAX</span></span>

### <span data-ttu-id="fce74-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="fce74-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fce74-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fce74-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fce74-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fce74-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fce74-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fce74-108">DESCRIPTION</span></span>
<span data-ttu-id="fce74-109">O cmdlet **Get-AzureRmRecoveryServicesAsrNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="fce74-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fce74-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fce74-110">EXAMPLES</span></span>

### <span data-ttu-id="fce74-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fce74-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="fce74-112">Obtém todas as redes conhecidas na malha especificada.</span><span class="sxs-lookup"><span data-stu-id="fce74-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="fce74-113">OS</span><span class="sxs-lookup"><span data-stu-id="fce74-113">PARAMETERS</span></span>

### <span data-ttu-id="fce74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce74-114">-DefaultProfile</span></span>
<span data-ttu-id="fce74-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fce74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fce74-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="fce74-116">-Fabric</span></span>
<span data-ttu-id="fce74-117">Objeto de malha ASR</span><span class="sxs-lookup"><span data-stu-id="fce74-117">ASR fabric object</span></span>

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

### <span data-ttu-id="fce74-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fce74-118">-FriendlyName</span></span>
<span data-ttu-id="fce74-119">Nome amigável do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="fce74-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce74-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fce74-120">-Name</span></span>
<span data-ttu-id="fce74-121">Nome do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="fce74-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce74-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce74-122">CommonParameters</span></span>
<span data-ttu-id="fce74-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce74-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce74-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce74-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce74-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fce74-125">INPUTS</span></span>

### <span data-ttu-id="fce74-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fce74-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fce74-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fce74-127">OUTPUTS</span></span>

### <span data-ttu-id="fce74-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fce74-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fce74-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fce74-129">NOTES</span></span>

## <span data-ttu-id="fce74-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fce74-130">RELATED LINKS</span></span>