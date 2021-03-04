---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: 2b524234b18e84247c3789119fbfe1d214514fec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889404"
---
# <span data-ttu-id="4369b-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="4369b-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="4369b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4369b-102">SYNOPSIS</span></span>
<span data-ttu-id="4369b-103">Criar novos recursos definidos pelo usuário para uma solução de segurança iot</span><span class="sxs-lookup"><span data-stu-id="4369b-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="4369b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4369b-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4369b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4369b-105">DESCRIPTION</span></span>
<span data-ttu-id="4369b-106">O cmdlet AzIotSecuritySolutionUserDefinedResourcesObject cria um novo objeto de recursos definidos pelo usuário para a solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="4369b-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="4369b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4369b-107">EXAMPLES</span></span>

### <span data-ttu-id="4369b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4369b-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="4369b-109">Criar novos recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4369b-109">Create new user defined resources</span></span>

## <span data-ttu-id="4369b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4369b-110">PARAMETERS</span></span>

### <span data-ttu-id="4369b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4369b-111">-DefaultProfile</span></span>
<span data-ttu-id="4369b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4369b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4369b-113">-Query</span><span class="sxs-lookup"><span data-stu-id="4369b-113">-Query</span></span>
<span data-ttu-id="4369b-114">Consulta.</span><span class="sxs-lookup"><span data-stu-id="4369b-114">Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4369b-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="4369b-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="4369b-116">Assinaturas de consulta.</span><span class="sxs-lookup"><span data-stu-id="4369b-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4369b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4369b-117">CommonParameters</span></span>
<span data-ttu-id="4369b-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4369b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4369b-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4369b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4369b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4369b-120">INPUTS</span></span>

### <span data-ttu-id="4369b-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4369b-121">None</span></span>

## <span data-ttu-id="4369b-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4369b-122">OUTPUTS</span></span>

### <span data-ttu-id="4369b-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="4369b-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="4369b-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="4369b-124">NOTES</span></span>

## <span data-ttu-id="4369b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4369b-125">RELATED LINKS</span></span>
