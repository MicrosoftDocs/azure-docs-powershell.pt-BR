---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888799"
---
# <span data-ttu-id="d3688-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="d3688-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="d3688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3688-102">SYNOPSIS</span></span>
<span data-ttu-id="d3688-103">Obtém controles de pontuação segura de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d3688-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="d3688-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3688-104">SYNTAX</span></span>

### <span data-ttu-id="d3688-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3688-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3688-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d3688-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3688-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3688-107">EXAMPLES</span></span>

### <span data-ttu-id="d3688-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3688-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="d3688-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d3688-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="d3688-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3688-110">PARAMETERS</span></span>

### <span data-ttu-id="d3688-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3688-111">-DefaultProfile</span></span>
<span data-ttu-id="d3688-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3688-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3688-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d3688-113">-Name</span></span>
<span data-ttu-id="d3688-114">Nome da pontuação seguro.</span><span class="sxs-lookup"><span data-stu-id="d3688-114">Secure score name.</span></span>

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

### <span data-ttu-id="d3688-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3688-115">CommonParameters</span></span>
<span data-ttu-id="d3688-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3688-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3688-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3688-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3688-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3688-118">INPUTS</span></span>

### <span data-ttu-id="d3688-119">System.String</span><span class="sxs-lookup"><span data-stu-id="d3688-119">System.String</span></span>

## <span data-ttu-id="d3688-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3688-120">OUTPUTS</span></span>

### <span data-ttu-id="d3688-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="d3688-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="d3688-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3688-122">NOTES</span></span>

## <span data-ttu-id="d3688-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3688-123">RELATED LINKS</span></span>
