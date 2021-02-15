---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116201"
---
# <span data-ttu-id="73925-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="73925-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="73925-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73925-102">SYNOPSIS</span></span>
<span data-ttu-id="73925-103">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="73925-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="73925-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73925-104">SYNTAX</span></span>

### <span data-ttu-id="73925-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73925-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73925-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="73925-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73925-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="73925-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73925-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="73925-108">DESCRIPTION</span></span>
<span data-ttu-id="73925-109">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="73925-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="73925-110">Os metadados da Avaliação de Built-In incluem avaliações e tipos de avaliação personalizados que o usuário pode definir.</span><span class="sxs-lookup"><span data-stu-id="73925-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="73925-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73925-111">EXAMPLES</span></span>

### <span data-ttu-id="73925-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73925-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="73925-113">Obtém todas as avaliações internas e as avaliações personalizadas que foram configuradas na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="73925-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="73925-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73925-114">PARAMETERS</span></span>

### <span data-ttu-id="73925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73925-115">-DefaultProfile</span></span>
<span data-ttu-id="73925-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73925-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73925-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="73925-117">-Name</span></span>
<span data-ttu-id="73925-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="73925-118">Resource name.</span></span>

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

### <span data-ttu-id="73925-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73925-119">-ResourceId</span></span>
<span data-ttu-id="73925-120">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="73925-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="73925-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73925-121">CommonParameters</span></span>
<span data-ttu-id="73925-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73925-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73925-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73925-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73925-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="73925-124">INPUTS</span></span>

### <span data-ttu-id="73925-125">System.String</span><span class="sxs-lookup"><span data-stu-id="73925-125">System.String</span></span>

## <span data-ttu-id="73925-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="73925-126">OUTPUTS</span></span>

### <span data-ttu-id="73925-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="73925-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="73925-128">Notas</span><span class="sxs-lookup"><span data-stu-id="73925-128">NOTES</span></span>

## <span data-ttu-id="73925-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73925-129">RELATED LINKS</span></span>
