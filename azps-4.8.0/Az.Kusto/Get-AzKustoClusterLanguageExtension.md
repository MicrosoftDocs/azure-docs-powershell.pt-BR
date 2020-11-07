---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955911"
---
# <span data-ttu-id="4b41a-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4b41a-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="4b41a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b41a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b41a-103">Retorna uma lista de extensões de idioma que podem ser executadas em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="4b41a-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4b41a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b41a-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b41a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b41a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b41a-106">Retorna uma lista de extensões de idioma que podem ser executadas em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="4b41a-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4b41a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b41a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b41a-108">Exemplo 1: listar todas as extensões de idioma definidas para um cluster</span><span class="sxs-lookup"><span data-stu-id="4b41a-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="4b41a-109">O comando acima retorna uma lista de extensões de idioma que podem ser executadas em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="4b41a-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4b41a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b41a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b41a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4b41a-111">-ClusterName</span></span>
<span data-ttu-id="4b41a-112">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4b41a-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4b41a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b41a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b41a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b41a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b41a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b41a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b41a-116">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4b41a-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4b41a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b41a-117">-SubscriptionId</span></span>
<span data-ttu-id="4b41a-118">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4b41a-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b41a-119">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4b41a-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4b41a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b41a-120">-Confirm</span></span>
<span data-ttu-id="4b41a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b41a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b41a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b41a-122">-WhatIf</span></span>
<span data-ttu-id="4b41a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b41a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b41a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b41a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b41a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b41a-125">CommonParameters</span></span>
<span data-ttu-id="4b41a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b41a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b41a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b41a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b41a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b41a-128">INPUTS</span></span>

## <span data-ttu-id="4b41a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b41a-129">OUTPUTS</span></span>

### <span data-ttu-id="4b41a-130">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4b41a-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="4b41a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b41a-131">NOTES</span></span>

<span data-ttu-id="4b41a-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4b41a-132">ALIASES</span></span>

## <span data-ttu-id="4b41a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b41a-133">RELATED LINKS</span></span>

