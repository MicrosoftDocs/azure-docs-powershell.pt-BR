---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114021"
---
# <span data-ttu-id="7a81a-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7a81a-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="7a81a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a81a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a81a-103">Obtenha os detalhes de uma malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a81a-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="7a81a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a81a-104">SYNTAX</span></span>

### <span data-ttu-id="7a81a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a81a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a81a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7a81a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a81a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7a81a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a81a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a81a-108">DESCRIPTION</span></span>
<span data-ttu-id="7a81a-109">O cmdlet **Get-AzRecoveryServicesAsrFabric** Obtém as propriedades de uma malha de recuperação de site do Azure especificada ou todas as malhas do Azure site Recovery em um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7a81a-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="7a81a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a81a-110">EXAMPLES</span></span>

### <span data-ttu-id="7a81a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a81a-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="7a81a-112">Retorna todas as malhas do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="7a81a-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="7a81a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a81a-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="7a81a-114">Retorne a malha do Azure site Recovery com o nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="7a81a-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="7a81a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a81a-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="7a81a-116">Retorne a estrutura do Azure site Recovery com o nome amigável xxxx.</span><span class="sxs-lookup"><span data-stu-id="7a81a-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="7a81a-117">OS</span><span class="sxs-lookup"><span data-stu-id="7a81a-117">PARAMETERS</span></span>

### <span data-ttu-id="7a81a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a81a-118">-DefaultProfile</span></span>
<span data-ttu-id="7a81a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a81a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a81a-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7a81a-120">-FriendlyName</span></span>
<span data-ttu-id="7a81a-121">Procure a malha ASR pelo nome amigável da malha.</span><span class="sxs-lookup"><span data-stu-id="7a81a-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="7a81a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a81a-122">-Name</span></span>
<span data-ttu-id="7a81a-123">Procure a malha ASR pelo nome da malha.</span><span class="sxs-lookup"><span data-stu-id="7a81a-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="7a81a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a81a-124">CommonParameters</span></span>
<span data-ttu-id="7a81a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a81a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a81a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a81a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a81a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a81a-127">INPUTS</span></span>

### <span data-ttu-id="7a81a-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a81a-128">None</span></span>

## <span data-ttu-id="7a81a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a81a-129">OUTPUTS</span></span>

### <span data-ttu-id="7a81a-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7a81a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7a81a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a81a-131">NOTES</span></span>

## <span data-ttu-id="7a81a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a81a-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a81a-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7a81a-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="7a81a-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7a81a-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
