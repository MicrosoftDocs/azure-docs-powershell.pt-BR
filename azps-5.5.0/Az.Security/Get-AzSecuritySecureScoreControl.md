---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114006"
---
# <span data-ttu-id="09ac7-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="09ac7-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="09ac7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="09ac7-103">Obtém controles de pontuação seguros de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="09ac7-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="09ac7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09ac7-104">SYNTAX</span></span>

### <span data-ttu-id="09ac7-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09ac7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09ac7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="09ac7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09ac7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="09ac7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09ac7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="09ac7-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="09ac7-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="09ac7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="09ac7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ac7-111">-DefaultProfile</span></span>
<span data-ttu-id="09ac7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09ac7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ac7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="09ac7-113">-Name</span></span>
<span data-ttu-id="09ac7-114">Nome da pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="09ac7-114">Secure score name.</span></span>

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

### <span data-ttu-id="09ac7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ac7-115">CommonParameters</span></span>
<span data-ttu-id="09ac7-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ac7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ac7-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09ac7-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ac7-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="09ac7-118">INPUTS</span></span>

### <span data-ttu-id="09ac7-119">System.String</span><span class="sxs-lookup"><span data-stu-id="09ac7-119">System.String</span></span>

## <span data-ttu-id="09ac7-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="09ac7-120">OUTPUTS</span></span>

### <span data-ttu-id="09ac7-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="09ac7-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="09ac7-122">Notas</span><span class="sxs-lookup"><span data-stu-id="09ac7-122">NOTES</span></span>

## <span data-ttu-id="09ac7-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09ac7-123">RELATED LINKS</span></span>
