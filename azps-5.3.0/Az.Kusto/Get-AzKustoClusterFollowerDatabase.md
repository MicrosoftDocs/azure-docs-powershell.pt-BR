---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: ecc811e98545816e69f7baa6fc96ea92fbeb43d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427175"
---
# <span data-ttu-id="d9191-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="d9191-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="d9191-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9191-102">SYNOPSIS</span></span>
<span data-ttu-id="d9191-103">Retorna uma lista de bancos de dados pertencentes a este cluster e que foram seguidos por outro cluster.</span><span class="sxs-lookup"><span data-stu-id="d9191-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d9191-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9191-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9191-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9191-105">DESCRIPTION</span></span>
<span data-ttu-id="d9191-106">Retorna uma lista de bancos de dados pertencentes a este cluster e que foram seguidos por outro cluster.</span><span class="sxs-lookup"><span data-stu-id="d9191-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d9191-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9191-107">EXAMPLES</span></span>

### <span data-ttu-id="d9191-108">Exemplo 1: lista todos os bancos de dados seguidos</span><span class="sxs-lookup"><span data-stu-id="d9191-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="d9191-109">O comando acima lista todos os bancos de dados pertencentes a esse cluster e que foram seguidos por outro cluster.</span><span class="sxs-lookup"><span data-stu-id="d9191-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d9191-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9191-110">PARAMETERS</span></span>

### <span data-ttu-id="d9191-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9191-111">-ClusterName</span></span>
<span data-ttu-id="d9191-112">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9191-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9191-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9191-113">-DefaultProfile</span></span>
<span data-ttu-id="d9191-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9191-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9191-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9191-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9191-116">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d9191-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9191-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9191-117">-SubscriptionId</span></span>
<span data-ttu-id="d9191-118">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9191-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9191-119">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d9191-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9191-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9191-120">-Confirm</span></span>
<span data-ttu-id="d9191-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9191-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9191-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9191-122">-WhatIf</span></span>
<span data-ttu-id="d9191-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9191-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9191-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9191-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9191-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9191-125">CommonParameters</span></span>
<span data-ttu-id="d9191-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9191-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9191-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9191-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9191-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9191-128">INPUTS</span></span>

## <span data-ttu-id="d9191-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9191-129">OUTPUTS</span></span>

### <span data-ttu-id="d9191-130">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="d9191-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="d9191-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9191-131">NOTES</span></span>

<span data-ttu-id="d9191-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d9191-132">ALIASES</span></span>

## <span data-ttu-id="d9191-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9191-133">RELATED LINKS</span></span>

