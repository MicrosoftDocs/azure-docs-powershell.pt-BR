---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125786"
---
# <span data-ttu-id="376e7-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="376e7-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="376e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="376e7-102">SYNOPSIS</span></span>
<span data-ttu-id="376e7-103">Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="376e7-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="376e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="376e7-104">SYNTAX</span></span>

### <span data-ttu-id="376e7-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="376e7-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="376e7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="376e7-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="376e7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="376e7-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="376e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="376e7-108">DESCRIPTION</span></span>
<span data-ttu-id="376e7-109">O cmdlet **Get-AzRecoveryServicesAsrNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="376e7-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="376e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="376e7-110">EXAMPLES</span></span>

### <span data-ttu-id="376e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="376e7-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="376e7-112">Obtém todas as redes conhecidas na malha especificada.</span><span class="sxs-lookup"><span data-stu-id="376e7-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="376e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="376e7-113">PARAMETERS</span></span>

### <span data-ttu-id="376e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376e7-114">-DefaultProfile</span></span>
<span data-ttu-id="376e7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="376e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="376e7-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="376e7-116">-Fabric</span></span>
<span data-ttu-id="376e7-117">Objeto de malha ASR</span><span class="sxs-lookup"><span data-stu-id="376e7-117">ASR fabric object</span></span>

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

### <span data-ttu-id="376e7-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="376e7-118">-FriendlyName</span></span>
<span data-ttu-id="376e7-119">Nome amigável do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="376e7-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="376e7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="376e7-120">-Name</span></span>
<span data-ttu-id="376e7-121">Nome do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="376e7-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="376e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376e7-122">CommonParameters</span></span>
<span data-ttu-id="376e7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376e7-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="376e7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376e7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="376e7-125">INPUTS</span></span>

### <span data-ttu-id="376e7-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="376e7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="376e7-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="376e7-127">OUTPUTS</span></span>

### <span data-ttu-id="376e7-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="376e7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="376e7-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="376e7-129">NOTES</span></span>

## <span data-ttu-id="376e7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="376e7-130">RELATED LINKS</span></span>
