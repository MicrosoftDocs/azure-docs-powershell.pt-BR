---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125747"
---
# <span data-ttu-id="47c01-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="47c01-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="47c01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47c01-102">SYNOPSIS</span></span>
<span data-ttu-id="47c01-103">Criar novos recursos definidos pelo usuário para a solução de segurança da IOT</span><span class="sxs-lookup"><span data-stu-id="47c01-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="47c01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47c01-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47c01-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47c01-105">DESCRIPTION</span></span>
<span data-ttu-id="47c01-106">O cmdlet AzIotSecuritySolutionUserDefinedResourcesObject cria um novo objeto de recursos definidos pelo usuário para a solução de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="47c01-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="47c01-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47c01-107">EXAMPLES</span></span>

### <span data-ttu-id="47c01-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47c01-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="47c01-109">Criar novos recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="47c01-109">Create new user defined resources</span></span>

## <span data-ttu-id="47c01-110">OS</span><span class="sxs-lookup"><span data-stu-id="47c01-110">PARAMETERS</span></span>

### <span data-ttu-id="47c01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c01-111">-DefaultProfile</span></span>
<span data-ttu-id="47c01-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47c01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c01-113">-Consulta</span><span class="sxs-lookup"><span data-stu-id="47c01-113">-Query</span></span>
<span data-ttu-id="47c01-114">Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="47c01-114">Query.</span></span>

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

### <span data-ttu-id="47c01-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="47c01-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="47c01-116">Assinaturas de consulta.</span><span class="sxs-lookup"><span data-stu-id="47c01-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="47c01-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c01-117">CommonParameters</span></span>
<span data-ttu-id="47c01-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c01-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c01-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47c01-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c01-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47c01-120">INPUTS</span></span>

### <span data-ttu-id="47c01-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="47c01-121">None</span></span>

## <span data-ttu-id="47c01-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47c01-122">OUTPUTS</span></span>

### <span data-ttu-id="47c01-123">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="47c01-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="47c01-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47c01-124">NOTES</span></span>

## <span data-ttu-id="47c01-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47c01-125">RELATED LINKS</span></span>
