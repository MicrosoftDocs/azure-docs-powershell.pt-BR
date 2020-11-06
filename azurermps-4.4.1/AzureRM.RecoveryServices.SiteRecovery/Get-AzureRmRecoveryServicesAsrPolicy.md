---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440979"
---
# <span data-ttu-id="72636-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="72636-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="72636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72636-102">SYNOPSIS</span></span>
<span data-ttu-id="72636-103">Obtém políticas de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="72636-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72636-104">SYNTAX</span></span>

### <span data-ttu-id="72636-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="72636-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="72636-106">ByName</span><span class="sxs-lookup"><span data-stu-id="72636-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="72636-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="72636-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="72636-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72636-108">DESCRIPTION</span></span>
<span data-ttu-id="72636-109">O cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** Obtém a lista de políticas de replicação do Azure site Recovery configuradas ou uma política de replicação específica por nome.</span><span class="sxs-lookup"><span data-stu-id="72636-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="72636-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72636-110">EXAMPLES</span></span>

### <span data-ttu-id="72636-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72636-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="72636-112">Retruns a política de replicação com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="72636-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="72636-113">OS</span><span class="sxs-lookup"><span data-stu-id="72636-113">PARAMETERS</span></span>

### <span data-ttu-id="72636-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="72636-114">-FriendlyName</span></span>
<span data-ttu-id="72636-115">Especifica o nome amigável da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="72636-115">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72636-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="72636-116">-Name</span></span>
<span data-ttu-id="72636-117">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="72636-117">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72636-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72636-118">CommonParameters</span></span>
<span data-ttu-id="72636-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72636-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72636-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72636-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72636-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72636-121">INPUTS</span></span>

### <span data-ttu-id="72636-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72636-122">None</span></span>

## <span data-ttu-id="72636-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72636-123">OUTPUTS</span></span>

### <span data-ttu-id="72636-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="72636-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="72636-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72636-125">NOTES</span></span>

## <span data-ttu-id="72636-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72636-126">RELATED LINKS</span></span>

[<span data-ttu-id="72636-127">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="72636-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="72636-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="72636-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
