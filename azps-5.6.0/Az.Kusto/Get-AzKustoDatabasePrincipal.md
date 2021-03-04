---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 3380835b4ca8e51c8ba0952ef3ef4bd973fadea3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885444"
---
# <span data-ttu-id="f12d3-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f12d3-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f12d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f12d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f12d3-103">Retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados.</span><span class="sxs-lookup"><span data-stu-id="f12d3-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f12d3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f12d3-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f12d3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f12d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f12d3-106">Retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados.</span><span class="sxs-lookup"><span data-stu-id="f12d3-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f12d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f12d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f12d3-108">Exemplo 1: Lista de entidades de banco de dados do cluster e banco de dados kusto determinados</span><span class="sxs-lookup"><span data-stu-id="f12d3-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f12d3-109">O comando acima retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados</span><span class="sxs-lookup"><span data-stu-id="f12d3-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="f12d3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f12d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f12d3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f12d3-111">-ClusterName</span></span>
<span data-ttu-id="f12d3-112">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f12d3-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f12d3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f12d3-113">-DatabaseName</span></span>
<span data-ttu-id="f12d3-114">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f12d3-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f12d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12d3-115">-DefaultProfile</span></span>
<span data-ttu-id="f12d3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f12d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f12d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f12d3-118">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f12d3-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f12d3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f12d3-119">-SubscriptionId</span></span>
<span data-ttu-id="f12d3-120">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f12d3-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f12d3-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f12d3-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f12d3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f12d3-122">-Confirm</span></span>
<span data-ttu-id="f12d3-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f12d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f12d3-124">-WhatIf</span></span>
<span data-ttu-id="f12d3-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f12d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f12d3-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f12d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f12d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12d3-127">CommonParameters</span></span>
<span data-ttu-id="f12d3-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12d3-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f12d3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12d3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f12d3-130">INPUTS</span></span>

## <span data-ttu-id="f12d3-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f12d3-131">OUTPUTS</span></span>

### <span data-ttu-id="f12d3-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f12d3-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="f12d3-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="f12d3-133">NOTES</span></span>

<span data-ttu-id="f12d3-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f12d3-134">ALIASES</span></span>

## <span data-ttu-id="f12d3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f12d3-135">RELATED LINKS</span></span>

