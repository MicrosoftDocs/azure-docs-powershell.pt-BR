---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940813"
---
# <span data-ttu-id="47a77-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="47a77-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="47a77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47a77-102">SYNOPSIS</span></span>
<span data-ttu-id="47a77-103">Obtém informações sobre mapeamentos de rede de recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="47a77-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="47a77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47a77-104">SYNTAX</span></span>

### <span data-ttu-id="47a77-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="47a77-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a77-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="47a77-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a77-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47a77-107">DESCRIPTION</span></span>
<span data-ttu-id="47a77-108">O cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** Obtém informações sobre os mapeamentos de rede do Azure site Recovery para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="47a77-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="47a77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47a77-109">EXAMPLES</span></span>

### <span data-ttu-id="47a77-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47a77-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="47a77-111">Obtém todos os mapeamentos de redes para a rede passada.</span><span class="sxs-lookup"><span data-stu-id="47a77-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="47a77-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47a77-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="47a77-113">Obtém o mapeamento de redes com o nome fornecido na malha especificada do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="47a77-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="47a77-114">OS</span><span class="sxs-lookup"><span data-stu-id="47a77-114">PARAMETERS</span></span>

### <span data-ttu-id="47a77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a77-115">-DefaultProfile</span></span>
<span data-ttu-id="47a77-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47a77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="47a77-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="47a77-117">-Name</span></span>
<span data-ttu-id="47a77-118">O nome do objeto de mapeamento de rede ASR a obter.</span><span class="sxs-lookup"><span data-stu-id="47a77-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="47a77-119">-Rede</span><span class="sxs-lookup"><span data-stu-id="47a77-119">-Network</span></span>
<span data-ttu-id="47a77-120">Obter os mapeamentos de rede ASR correspondentes ao objeto ASR de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="47a77-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="47a77-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="47a77-121">-PrimaryFabric</span></span>
<span data-ttu-id="47a77-122">Obter os mapeamentos de rede ASR correspondentes ao objeto de malha primária especificado.</span><span class="sxs-lookup"><span data-stu-id="47a77-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="47a77-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a77-123">CommonParameters</span></span>
<span data-ttu-id="47a77-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a77-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a77-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47a77-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a77-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47a77-126">INPUTS</span></span>

### <span data-ttu-id="47a77-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="47a77-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="47a77-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="47a77-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="47a77-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47a77-129">OUTPUTS</span></span>

### <span data-ttu-id="47a77-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="47a77-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="47a77-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47a77-131">NOTES</span></span>

## <span data-ttu-id="47a77-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47a77-132">RELATED LINKS</span></span>

[<span data-ttu-id="47a77-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="47a77-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="47a77-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="47a77-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
