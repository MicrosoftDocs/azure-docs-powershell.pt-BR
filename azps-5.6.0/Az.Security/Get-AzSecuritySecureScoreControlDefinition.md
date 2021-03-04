---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: e8ec0073eef8b8db95197e19f2bfd61d0bbcdafd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891081"
---
# <span data-ttu-id="ac2f6-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="ac2f6-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="ac2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2f6-103">Obtém definições de controle de pontuação segura de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ac2f6-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="ac2f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac2f6-104">SYNTAX</span></span>

### <span data-ttu-id="ac2f6-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac2f6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac2f6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ac2f6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac2f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ac2f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac2f6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="ac2f6-109">Obtém todas as definições de controle de pontuação segura de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ac2f6-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="ac2f6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ac2f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac2f6-111">-DefaultProfile</span></span>
<span data-ttu-id="ac2f6-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac2f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac2f6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac2f6-113">CommonParameters</span></span>
<span data-ttu-id="ac2f6-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac2f6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac2f6-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac2f6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac2f6-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-116">INPUTS</span></span>

### <span data-ttu-id="ac2f6-117">System.String</span><span class="sxs-lookup"><span data-stu-id="ac2f6-117">System.String</span></span>

## <span data-ttu-id="ac2f6-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-118">OUTPUTS</span></span>

### <span data-ttu-id="ac2f6-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="ac2f6-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="ac2f6-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac2f6-120">NOTES</span></span>

## <span data-ttu-id="ac2f6-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac2f6-121">RELATED LINKS</span></span>
