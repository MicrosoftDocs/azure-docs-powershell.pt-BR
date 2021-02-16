---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114010"
---
# <span data-ttu-id="a06d8-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="a06d8-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="a06d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a06d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a06d8-103">Obtém pontuações seguras de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a06d8-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="a06d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a06d8-104">SYNTAX</span></span>

### <span data-ttu-id="a06d8-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a06d8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06d8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a06d8-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06d8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a06d8-107">EXAMPLES</span></span>

### <span data-ttu-id="a06d8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a06d8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="a06d8-109">Obtém todas as pontuações seguras de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a06d8-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="a06d8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a06d8-110">PARAMETERS</span></span>

### <span data-ttu-id="a06d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06d8-111">-DefaultProfile</span></span>
<span data-ttu-id="a06d8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06d8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a06d8-113">-Name</span></span>
<span data-ttu-id="a06d8-114">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a06d8-114">Resource name.</span></span>

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

### <span data-ttu-id="a06d8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06d8-115">CommonParameters</span></span>
<span data-ttu-id="a06d8-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06d8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06d8-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a06d8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06d8-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="a06d8-118">INPUTS</span></span>

### <span data-ttu-id="a06d8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="a06d8-119">System.String</span></span>

## <span data-ttu-id="a06d8-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="a06d8-120">OUTPUTS</span></span>

### <span data-ttu-id="a06d8-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="a06d8-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="a06d8-122">Notas</span><span class="sxs-lookup"><span data-stu-id="a06d8-122">NOTES</span></span>

## <span data-ttu-id="a06d8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a06d8-123">RELATED LINKS</span></span>
