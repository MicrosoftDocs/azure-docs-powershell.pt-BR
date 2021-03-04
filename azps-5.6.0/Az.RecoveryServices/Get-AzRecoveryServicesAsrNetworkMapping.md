---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: c309b855b6ae8491e8b4a97301a902367a5377e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888608"
---
# <span data-ttu-id="17f75-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="17f75-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="17f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f75-102">SYNOPSIS</span></span>
<span data-ttu-id="17f75-103">Obtém informações sobre mapeamentos de rede de Recuperação de Site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="17f75-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="17f75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17f75-104">SYNTAX</span></span>

### <span data-ttu-id="17f75-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17f75-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f75-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="17f75-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f75-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17f75-107">DESCRIPTION</span></span>
<span data-ttu-id="17f75-108">O cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** obtém informações sobre os mapeamentos de rede de Recuperação de Site do Azure para o cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="17f75-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="17f75-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17f75-109">EXAMPLES</span></span>

### <span data-ttu-id="17f75-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17f75-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="17f75-111">Obtém todos os mapeamentos de redes para a Rede passada.</span><span class="sxs-lookup"><span data-stu-id="17f75-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="17f75-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17f75-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="17f75-113">Obtém o mapeamento de redes com o nome fornecido no fabric de recuperação de site do azure especificado.</span><span class="sxs-lookup"><span data-stu-id="17f75-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="17f75-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17f75-114">PARAMETERS</span></span>

### <span data-ttu-id="17f75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f75-115">-DefaultProfile</span></span>
<span data-ttu-id="17f75-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17f75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="17f75-117">-Name</span><span class="sxs-lookup"><span data-stu-id="17f75-117">-Name</span></span>
<span data-ttu-id="17f75-118">O nome do objeto de mapeamento de rede ASR a ser usado.</span><span class="sxs-lookup"><span data-stu-id="17f75-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="17f75-119">-Network</span><span class="sxs-lookup"><span data-stu-id="17f75-119">-Network</span></span>
<span data-ttu-id="17f75-120">Obter os mapeamentos de rede ASR correspondentes ao objeto ASR de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="17f75-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="17f75-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="17f75-121">-PrimaryFabric</span></span>
<span data-ttu-id="17f75-122">Obter os mapeamentos de rede ASR correspondentes ao objeto de malha principal especificado.</span><span class="sxs-lookup"><span data-stu-id="17f75-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="17f75-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f75-123">CommonParameters</span></span>
<span data-ttu-id="17f75-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f75-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f75-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17f75-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f75-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17f75-126">INPUTS</span></span>

### <span data-ttu-id="17f75-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="17f75-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="17f75-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="17f75-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="17f75-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17f75-129">OUTPUTS</span></span>

### <span data-ttu-id="17f75-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="17f75-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="17f75-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="17f75-131">NOTES</span></span>

## <span data-ttu-id="17f75-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17f75-132">RELATED LINKS</span></span>

[<span data-ttu-id="17f75-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="17f75-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="17f75-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="17f75-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
