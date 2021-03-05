---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1aeaba2f4f25abd49f12d087b7390f5e92f19c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901595"
---
# <span data-ttu-id="75ba5-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75ba5-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="75ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="75ba5-103">Obter os detalhes de um Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="75ba5-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="75ba5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75ba5-104">SYNTAX</span></span>

### <span data-ttu-id="75ba5-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75ba5-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ba5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="75ba5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ba5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="75ba5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75ba5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75ba5-108">DESCRIPTION</span></span>
<span data-ttu-id="75ba5-109">O cmdlet **Get-AzRecoveryServicesAsrFabric** obtém as propriedades de um Azure Site Recovery Fabric especificado ou de todos os Malhas de Recuperação de Site do Azure em um cofre do Serviço de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="75ba5-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="75ba5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75ba5-110">EXAMPLES</span></span>

### <span data-ttu-id="75ba5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75ba5-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="75ba5-112">Retorna todos os malhas de Recuperação de Site do Azure no cofre.</span><span class="sxs-lookup"><span data-stu-id="75ba5-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="75ba5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75ba5-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="75ba5-114">Retornar o azure site recovery fabric com nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="75ba5-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="75ba5-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="75ba5-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="75ba5-116">Retornar o azure site recovery fabric com nome amigável xxxx.</span><span class="sxs-lookup"><span data-stu-id="75ba5-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="75ba5-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75ba5-117">PARAMETERS</span></span>

### <span data-ttu-id="75ba5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ba5-118">-DefaultProfile</span></span>
<span data-ttu-id="75ba5-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75ba5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ba5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="75ba5-120">-FriendlyName</span></span>
<span data-ttu-id="75ba5-121">Pesquise o tecido ASR pelo nome amigável do tecido.</span><span class="sxs-lookup"><span data-stu-id="75ba5-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="75ba5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="75ba5-122">-Name</span></span>
<span data-ttu-id="75ba5-123">Pesquise o tecido ASR pelo nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="75ba5-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="75ba5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ba5-124">CommonParameters</span></span>
<span data-ttu-id="75ba5-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ba5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ba5-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75ba5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ba5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75ba5-127">INPUTS</span></span>

### <span data-ttu-id="75ba5-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75ba5-128">None</span></span>

## <span data-ttu-id="75ba5-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75ba5-129">OUTPUTS</span></span>

### <span data-ttu-id="75ba5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="75ba5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="75ba5-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="75ba5-131">NOTES</span></span>

## <span data-ttu-id="75ba5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75ba5-132">RELATED LINKS</span></span>

[<span data-ttu-id="75ba5-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75ba5-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="75ba5-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75ba5-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
