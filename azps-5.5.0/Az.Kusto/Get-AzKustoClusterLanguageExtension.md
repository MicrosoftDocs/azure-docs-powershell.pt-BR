---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113036"
---
# <span data-ttu-id="5290f-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="5290f-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="5290f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5290f-102">SYNOPSIS</span></span>
<span data-ttu-id="5290f-103">Retorna uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="5290f-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="5290f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5290f-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5290f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5290f-105">DESCRIPTION</span></span>
<span data-ttu-id="5290f-106">Retorna uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="5290f-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="5290f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5290f-107">EXAMPLES</span></span>

### <span data-ttu-id="5290f-108">Exemplo 1: Listar todas as extensões de idioma definidas para um cluster</span><span class="sxs-lookup"><span data-stu-id="5290f-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="5290f-109">O comando acima retorna uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="5290f-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="5290f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5290f-110">PARAMETERS</span></span>

### <span data-ttu-id="5290f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5290f-111">-ClusterName</span></span>
<span data-ttu-id="5290f-112">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="5290f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5290f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5290f-113">-DefaultProfile</span></span>
<span data-ttu-id="5290f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5290f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5290f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5290f-116">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="5290f-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5290f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5290f-117">-SubscriptionId</span></span>
<span data-ttu-id="5290f-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5290f-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5290f-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5290f-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290f-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5290f-120">-Confirm</span></span>
<span data-ttu-id="5290f-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5290f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5290f-122">-WhatIf</span></span>
<span data-ttu-id="5290f-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5290f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5290f-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5290f-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5290f-125">CommonParameters</span></span>
<span data-ttu-id="5290f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5290f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5290f-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5290f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5290f-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="5290f-128">INPUTS</span></span>

## <span data-ttu-id="5290f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="5290f-129">OUTPUTS</span></span>

### <span data-ttu-id="5290f-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="5290f-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="5290f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="5290f-131">NOTES</span></span>

<span data-ttu-id="5290f-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="5290f-132">ALIASES</span></span>

## <span data-ttu-id="5290f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5290f-133">RELATED LINKS</span></span>

