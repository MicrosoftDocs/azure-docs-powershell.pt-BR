---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 92858967d460785af151520c504a4e1cbdb4d3d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892717"
---
# <span data-ttu-id="3f402-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3f402-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3f402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f402-102">SYNOPSIS</span></span>
<span data-ttu-id="3f402-103">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f402-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="3f402-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f402-104">SYNTAX</span></span>

### <span data-ttu-id="3f402-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f402-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f402-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f402-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f402-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f402-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f402-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f402-108">DESCRIPTION</span></span>
<span data-ttu-id="3f402-109">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f402-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="3f402-110">Os metadados de Avaliação de Segurança incluem Built-In avaliações e tipos de avaliação personalizados que o usuário pode definir.</span><span class="sxs-lookup"><span data-stu-id="3f402-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="3f402-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f402-111">EXAMPLES</span></span>

### <span data-ttu-id="3f402-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f402-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="3f402-113">Obtém todas as avaliações internas e as avaliações personalizadas que foram configuradas na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3f402-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="3f402-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f402-114">PARAMETERS</span></span>

### <span data-ttu-id="3f402-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f402-115">-DefaultProfile</span></span>
<span data-ttu-id="3f402-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f402-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f402-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3f402-117">-Name</span></span>
<span data-ttu-id="3f402-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3f402-118">Resource name.</span></span>

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

### <span data-ttu-id="3f402-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f402-119">-ResourceId</span></span>
<span data-ttu-id="3f402-120">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="3f402-120">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f402-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f402-121">CommonParameters</span></span>
<span data-ttu-id="3f402-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f402-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f402-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f402-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f402-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f402-124">INPUTS</span></span>

### <span data-ttu-id="3f402-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3f402-125">System.String</span></span>

## <span data-ttu-id="3f402-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f402-126">OUTPUTS</span></span>

### <span data-ttu-id="3f402-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3f402-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3f402-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f402-128">NOTES</span></span>

## <span data-ttu-id="3f402-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f402-129">RELATED LINKS</span></span>
