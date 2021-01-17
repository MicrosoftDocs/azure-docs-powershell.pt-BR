---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433269"
---
# <span data-ttu-id="efe1a-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="efe1a-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="efe1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efe1a-102">SYNOPSIS</span></span>
<span data-ttu-id="efe1a-103">Obtém pontuações seguras de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="efe1a-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="efe1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efe1a-104">SYNTAX</span></span>

### <span data-ttu-id="efe1a-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="efe1a-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efe1a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="efe1a-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efe1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efe1a-107">EXAMPLES</span></span>

### <span data-ttu-id="efe1a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="efe1a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="efe1a-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="efe1a-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="efe1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="efe1a-110">PARAMETERS</span></span>

### <span data-ttu-id="efe1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe1a-111">-DefaultProfile</span></span>
<span data-ttu-id="efe1a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efe1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efe1a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="efe1a-113">-Name</span></span>
<span data-ttu-id="efe1a-114">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="efe1a-114">Resource name.</span></span>

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

### <span data-ttu-id="efe1a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe1a-115">CommonParameters</span></span>
<span data-ttu-id="efe1a-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe1a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe1a-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efe1a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe1a-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efe1a-118">INPUTS</span></span>

### <span data-ttu-id="efe1a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="efe1a-119">System.String</span></span>

## <span data-ttu-id="efe1a-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efe1a-120">OUTPUTS</span></span>

### <span data-ttu-id="efe1a-121">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="efe1a-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="efe1a-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efe1a-122">NOTES</span></span>

## <span data-ttu-id="efe1a-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efe1a-123">RELATED LINKS</span></span>
