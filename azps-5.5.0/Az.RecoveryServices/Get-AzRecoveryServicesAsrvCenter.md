---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114965"
---
# <span data-ttu-id="9a6c3-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9a6c3-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9a6c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6c3-103">Obtém detalhes dos servidores vCenter registrados para descoberta no servidor de configuração especificado pela malha ASR.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="9a6c3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a6c3-104">SYNTAX</span></span>

### <span data-ttu-id="9a6c3-105">ByFabricObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a6c3-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a6c3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6c3-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a6c3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9a6c3-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a6c3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a6c3-108">DESCRIPTION</span></span>
<span data-ttu-id="9a6c3-109">O cmdlet **Get-AzRecoveryServicesAsrvCenter** obtém detalhes dos servidores vCenter registrados para descoberta no servidor de configuração especificado pela malha ASR.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="9a6c3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a6c3-110">EXAMPLES</span></span>

### <span data-ttu-id="9a6c3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a6c3-111">Example 1</span></span>
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

<span data-ttu-id="9a6c3-112">Obter o vCenter de recuperação de site do azure por nome de tela e nome do vCenter.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="9a6c3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a6c3-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="9a6c3-114">Obter a lista vCenter de recuperação de site do azure por nome de malha.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="9a6c3-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a6c3-115">PARAMETERS</span></span>

### <span data-ttu-id="9a6c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6c3-116">-DefaultProfile</span></span>
<span data-ttu-id="9a6c3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a6c3-118">-Malha</span><span class="sxs-lookup"><span data-stu-id="9a6c3-118">-Fabric</span></span>
<span data-ttu-id="9a6c3-119">Objeto de malha ASR que representa o Servidor de Configuração.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="9a6c3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a6c3-120">-Name</span></span>
<span data-ttu-id="9a6c3-121">Nome do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="9a6c3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6c3-122">-ResourceId</span></span>
<span data-ttu-id="9a6c3-123">Especifica a resourceId do vCenter.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="9a6c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6c3-124">CommonParameters</span></span>
<span data-ttu-id="9a6c3-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6c3-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a6c3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6c3-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a6c3-127">INPUTS</span></span>

### <span data-ttu-id="9a6c3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9a6c3-128">System.String</span></span>

### <span data-ttu-id="9a6c3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9a6c3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9a6c3-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a6c3-130">OUTPUTS</span></span>

### <span data-ttu-id="9a6c3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9a6c3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9a6c3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="9a6c3-132">NOTES</span></span>

## <span data-ttu-id="9a6c3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a6c3-133">RELATED LINKS</span></span>
