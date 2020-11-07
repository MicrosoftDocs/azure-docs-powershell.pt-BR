---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954699"
---
# <span data-ttu-id="00b0e-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="00b0e-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="00b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="00b0e-103">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="00b0e-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="00b0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00b0e-104">SYNTAX</span></span>

### <span data-ttu-id="00b0e-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="00b0e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b0e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="00b0e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b0e-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="00b0e-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00b0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00b0e-108">DESCRIPTION</span></span>
<span data-ttu-id="00b0e-109">Obtém tipos de avaliações de segurança e metadta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="00b0e-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="00b0e-110">Os metadados de avaliação de segurança incluem avaliações Built-In e tipos de avaliação personalizados que o usuário pode definir.</span><span class="sxs-lookup"><span data-stu-id="00b0e-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="00b0e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00b0e-111">EXAMPLES</span></span>

### <span data-ttu-id="00b0e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00b0e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="00b0e-113">Obtém todas as avaliações internas e as avaliações personalizadas que foram configuradas na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="00b0e-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="00b0e-114">OS</span><span class="sxs-lookup"><span data-stu-id="00b0e-114">PARAMETERS</span></span>

### <span data-ttu-id="00b0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b0e-115">-DefaultProfile</span></span>
<span data-ttu-id="00b0e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00b0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00b0e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="00b0e-117">-Name</span></span>
<span data-ttu-id="00b0e-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="00b0e-118">Resource name.</span></span>

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

### <span data-ttu-id="00b0e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00b0e-119">-ResourceId</span></span>
<span data-ttu-id="00b0e-120">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="00b0e-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="00b0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b0e-121">CommonParameters</span></span>
<span data-ttu-id="00b0e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b0e-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00b0e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b0e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00b0e-124">INPUTS</span></span>

### <span data-ttu-id="00b0e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="00b0e-125">System.String</span></span>

## <span data-ttu-id="00b0e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00b0e-126">OUTPUTS</span></span>

### <span data-ttu-id="00b0e-127">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="00b0e-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="00b0e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00b0e-128">NOTES</span></span>

## <span data-ttu-id="00b0e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00b0e-129">RELATED LINKS</span></span>
