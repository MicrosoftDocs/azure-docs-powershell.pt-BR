---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117233"
---
# <span data-ttu-id="80db5-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="80db5-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="80db5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80db5-102">SYNOPSIS</span></span>
<span data-ttu-id="80db5-103">Obtém informações sobre as redes gerenciadas pela Recuperação de Site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="80db5-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="80db5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80db5-104">SYNTAX</span></span>

### <span data-ttu-id="80db5-105">ByFabricObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80db5-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80db5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="80db5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80db5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="80db5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80db5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="80db5-108">DESCRIPTION</span></span>
<span data-ttu-id="80db5-109">O cmdlet **Get-AzRecoveryServicesAsrNetwork obtém** informações sobre redes de Recuperação de Sites do Azure para o cofre atual de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="80db5-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="80db5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80db5-110">EXAMPLES</span></span>

### <span data-ttu-id="80db5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80db5-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="80db5-112">Obtém todas as redes conhecidas na malha especificada.</span><span class="sxs-lookup"><span data-stu-id="80db5-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="80db5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80db5-113">PARAMETERS</span></span>

### <span data-ttu-id="80db5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80db5-114">-DefaultProfile</span></span>
<span data-ttu-id="80db5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80db5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="80db5-116">-Malha</span><span class="sxs-lookup"><span data-stu-id="80db5-116">-Fabric</span></span>
<span data-ttu-id="80db5-117">Objeto de malha ASR</span><span class="sxs-lookup"><span data-stu-id="80db5-117">ASR fabric object</span></span>

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

### <span data-ttu-id="80db5-118">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="80db5-118">-FriendlyName</span></span>
<span data-ttu-id="80db5-119">Nome amigável do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="80db5-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="80db5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="80db5-120">-Name</span></span>
<span data-ttu-id="80db5-121">Nome do objeto ASR de rede.</span><span class="sxs-lookup"><span data-stu-id="80db5-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="80db5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80db5-122">CommonParameters</span></span>
<span data-ttu-id="80db5-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80db5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80db5-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80db5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80db5-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="80db5-125">INPUTS</span></span>

### <span data-ttu-id="80db5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="80db5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="80db5-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="80db5-127">OUTPUTS</span></span>

### <span data-ttu-id="80db5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="80db5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="80db5-129">Notas</span><span class="sxs-lookup"><span data-stu-id="80db5-129">NOTES</span></span>

## <span data-ttu-id="80db5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80db5-130">RELATED LINKS</span></span>
