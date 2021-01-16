---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263305"
---
# <span data-ttu-id="3786b-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3786b-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3786b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3786b-102">SYNOPSIS</span></span>
<span data-ttu-id="3786b-103">Obtém informações sobre mapeamentos de rede de recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="3786b-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="3786b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3786b-104">SYNTAX</span></span>

### <span data-ttu-id="3786b-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="3786b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3786b-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="3786b-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3786b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3786b-107">DESCRIPTION</span></span>
<span data-ttu-id="3786b-108">O cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** Obtém informações sobre os mapeamentos de rede do Azure site Recovery para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3786b-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="3786b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3786b-109">EXAMPLES</span></span>

### <span data-ttu-id="3786b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3786b-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="3786b-111">Obtém todos os mapeamentos de redes para a rede passada.</span><span class="sxs-lookup"><span data-stu-id="3786b-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="3786b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3786b-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="3786b-113">Obtém o mapeamento de redes com o nome fornecido na malha especificada do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3786b-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="3786b-114">OS</span><span class="sxs-lookup"><span data-stu-id="3786b-114">PARAMETERS</span></span>

### <span data-ttu-id="3786b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3786b-115">-DefaultProfile</span></span>
<span data-ttu-id="3786b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3786b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3786b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3786b-117">-Name</span></span>
<span data-ttu-id="3786b-118">O nome do objeto de mapeamento de rede ASR a obter.</span><span class="sxs-lookup"><span data-stu-id="3786b-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3786b-119">-Rede</span><span class="sxs-lookup"><span data-stu-id="3786b-119">-Network</span></span>
<span data-ttu-id="3786b-120">Obter os mapeamentos de rede ASR correspondentes ao objeto ASR de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="3786b-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3786b-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3786b-121">-PrimaryFabric</span></span>
<span data-ttu-id="3786b-122">Obter os mapeamentos de rede ASR correspondentes ao objeto de malha primária especificado.</span><span class="sxs-lookup"><span data-stu-id="3786b-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3786b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3786b-123">CommonParameters</span></span>
<span data-ttu-id="3786b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3786b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3786b-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3786b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3786b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3786b-126">INPUTS</span></span>

### <span data-ttu-id="3786b-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3786b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="3786b-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3786b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3786b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3786b-129">OUTPUTS</span></span>

### <span data-ttu-id="3786b-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3786b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="3786b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3786b-131">NOTES</span></span>

## <span data-ttu-id="3786b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3786b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3786b-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3786b-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3786b-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3786b-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
