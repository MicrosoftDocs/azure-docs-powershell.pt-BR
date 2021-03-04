---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 0cce3e4e1aa0f5de93e9c54c00cfa1902a4c24b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891086"
---
# <span data-ttu-id="c71e1-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="c71e1-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="c71e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c71e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c71e1-103">Obtém pontuações seguras de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c71e1-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="c71e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c71e1-104">SYNTAX</span></span>

### <span data-ttu-id="c71e1-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c71e1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c71e1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c71e1-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c71e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c71e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c71e1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c71e1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="c71e1-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c71e1-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="c71e1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c71e1-110">PARAMETERS</span></span>

### <span data-ttu-id="c71e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71e1-111">-DefaultProfile</span></span>
<span data-ttu-id="c71e1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c71e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71e1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c71e1-113">-Name</span></span>
<span data-ttu-id="c71e1-114">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c71e1-114">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71e1-115">CommonParameters</span></span>
<span data-ttu-id="c71e1-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71e1-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c71e1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71e1-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c71e1-118">INPUTS</span></span>

### <span data-ttu-id="c71e1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="c71e1-119">System.String</span></span>

## <span data-ttu-id="c71e1-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c71e1-120">OUTPUTS</span></span>

### <span data-ttu-id="c71e1-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="c71e1-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="c71e1-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="c71e1-122">NOTES</span></span>

## <span data-ttu-id="c71e1-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c71e1-123">RELATED LINKS</span></span>
