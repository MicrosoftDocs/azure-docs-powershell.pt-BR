---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 443abbab086fe08ac0a667776a07c792115aa5dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440174"
---
# <span data-ttu-id="8ede0-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="8ede0-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="8ede0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ede0-102">SYNOPSIS</span></span>
<span data-ttu-id="8ede0-103">Obtém políticas de proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="8ede0-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ede0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ede0-104">SYNTAX</span></span>

### <span data-ttu-id="8ede0-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ede0-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ede0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ede0-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ede0-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ede0-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ede0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ede0-108">DESCRIPTION</span></span>
<span data-ttu-id="8ede0-109">O cmdlet **Get-AzureRmSiteRecoveryPolicy** Obtém a lista de políticas de proteção do Azure site Recovery configuradas ou uma política de proteção específica por nome.</span><span class="sxs-lookup"><span data-stu-id="8ede0-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="8ede0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ede0-110">EXAMPLES</span></span>

## <span data-ttu-id="8ede0-111">OS</span><span class="sxs-lookup"><span data-stu-id="8ede0-111">PARAMETERS</span></span>

### <span data-ttu-id="8ede0-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ede0-112">-FriendlyName</span></span>
<span data-ttu-id="8ede0-113">Especifica o nome amigável da política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="8ede0-113">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="8ede0-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ede0-114">-Name</span></span>
<span data-ttu-id="8ede0-115">Especifica o nome da política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="8ede0-115">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="8ede0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ede0-116">-DefaultProfile</span></span>
<span data-ttu-id="8ede0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ede0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ede0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ede0-118">CommonParameters</span></span>
<span data-ttu-id="8ede0-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ede0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ede0-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ede0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ede0-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ede0-121">INPUTS</span></span>

## <span data-ttu-id="8ede0-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ede0-122">OUTPUTS</span></span>

### <span data-ttu-id="8ede0-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="8ede0-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="8ede0-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ede0-124">NOTES</span></span>

## <span data-ttu-id="8ede0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ede0-125">RELATED LINKS</span></span>

[<span data-ttu-id="8ede0-126">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="8ede0-126">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="8ede0-127">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="8ede0-127">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
