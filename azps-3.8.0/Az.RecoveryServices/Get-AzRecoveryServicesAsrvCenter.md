---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940895"
---
# <span data-ttu-id="c5322-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="c5322-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="c5322-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5322-102">SYNOPSIS</span></span>
<span data-ttu-id="c5322-103">Obtém detalhes dos servidores vCenter registrados para descoberta no servidor de configuração especificado pela malha ASR.</span><span class="sxs-lookup"><span data-stu-id="c5322-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="c5322-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5322-104">SYNTAX</span></span>

### <span data-ttu-id="c5322-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5322-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5322-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5322-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5322-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c5322-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5322-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5322-108">DESCRIPTION</span></span>
<span data-ttu-id="c5322-109">O cmdlet **Get-AzRecoveryServicesAsrvCenter** Obtém detalhes dos servidores vCenter registrados para descoberta no servidor de configuração especificado pela malha ASR.</span><span class="sxs-lookup"><span data-stu-id="c5322-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="c5322-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5322-110">EXAMPLES</span></span>

### <span data-ttu-id="c5322-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5322-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="c5322-112">Obtenha o Azure site Recovery vCenter pelo nome da malha e pelo nome do vCenter.</span><span class="sxs-lookup"><span data-stu-id="c5322-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="c5322-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5322-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="c5322-114">Obtenha a lista de vCenter do Azure site Recovery por nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="c5322-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="c5322-115">OS</span><span class="sxs-lookup"><span data-stu-id="c5322-115">PARAMETERS</span></span>

### <span data-ttu-id="c5322-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5322-116">-DefaultProfile</span></span>
<span data-ttu-id="c5322-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5322-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5322-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c5322-118">-Fabric</span></span>
<span data-ttu-id="c5322-119">Objeto de malha ASR que representa o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="c5322-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5322-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5322-120">-Name</span></span>
<span data-ttu-id="c5322-121">Nome do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="c5322-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="c5322-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5322-122">-ResourceId</span></span>
<span data-ttu-id="c5322-123">Especifica o ResourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="c5322-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5322-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5322-124">CommonParameters</span></span>
<span data-ttu-id="c5322-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5322-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5322-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5322-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5322-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5322-127">INPUTS</span></span>

### <span data-ttu-id="c5322-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c5322-128">System.String</span></span>

### <span data-ttu-id="c5322-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c5322-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c5322-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5322-130">OUTPUTS</span></span>

### <span data-ttu-id="c5322-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="c5322-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="c5322-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5322-132">NOTES</span></span>

## <span data-ttu-id="c5322-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5322-133">RELATED LINKS</span></span>
