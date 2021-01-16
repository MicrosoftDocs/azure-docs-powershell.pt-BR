---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271555"
---
# <span data-ttu-id="fb906-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="fb906-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="fb906-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb906-102">SYNOPSIS</span></span>
<span data-ttu-id="fb906-103">Obtém os controles de Pontuação segura de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="fb906-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="fb906-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb906-104">SYNTAX</span></span>

### <span data-ttu-id="fb906-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb906-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb906-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fb906-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb906-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb906-107">EXAMPLES</span></span>

### <span data-ttu-id="fb906-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb906-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="fb906-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="fb906-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="fb906-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb906-110">PARAMETERS</span></span>

### <span data-ttu-id="fb906-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb906-111">-DefaultProfile</span></span>
<span data-ttu-id="fb906-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb906-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb906-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb906-113">-Name</span></span>
<span data-ttu-id="fb906-114">Nome da Pontuação segura.</span><span class="sxs-lookup"><span data-stu-id="fb906-114">Secure score name.</span></span>

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

### <span data-ttu-id="fb906-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb906-115">CommonParameters</span></span>
<span data-ttu-id="fb906-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb906-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb906-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb906-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb906-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb906-118">INPUTS</span></span>

### <span data-ttu-id="fb906-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fb906-119">System.String</span></span>

## <span data-ttu-id="fb906-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb906-120">OUTPUTS</span></span>

### <span data-ttu-id="fb906-121">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="fb906-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="fb906-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb906-122">NOTES</span></span>

## <span data-ttu-id="fb906-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb906-123">RELATED LINKS</span></span>
