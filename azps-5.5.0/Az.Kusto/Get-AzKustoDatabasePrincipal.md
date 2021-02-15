---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113023"
---
# <span data-ttu-id="499a6-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="499a6-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="499a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="499a6-102">SYNOPSIS</span></span>
<span data-ttu-id="499a6-103">Retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados.</span><span class="sxs-lookup"><span data-stu-id="499a6-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="499a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="499a6-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="499a6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="499a6-105">DESCRIPTION</span></span>
<span data-ttu-id="499a6-106">Retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados.</span><span class="sxs-lookup"><span data-stu-id="499a6-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="499a6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="499a6-107">EXAMPLES</span></span>

### <span data-ttu-id="499a6-108">Exemplo 1: Lista de entidades de banco de dados do cluster e banco de dados Kusto determinados</span><span class="sxs-lookup"><span data-stu-id="499a6-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="499a6-109">O comando acima retorna uma lista de entidades de banco de dados do cluster e banco de dados Kusto determinados</span><span class="sxs-lookup"><span data-stu-id="499a6-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="499a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="499a6-110">PARAMETERS</span></span>

### <span data-ttu-id="499a6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="499a6-111">-ClusterName</span></span>
<span data-ttu-id="499a6-112">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="499a6-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="499a6-113">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="499a6-113">-DatabaseName</span></span>
<span data-ttu-id="499a6-114">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="499a6-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="499a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499a6-115">-DefaultProfile</span></span>
<span data-ttu-id="499a6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="499a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="499a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="499a6-118">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="499a6-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="499a6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="499a6-119">-SubscriptionId</span></span>
<span data-ttu-id="499a6-120">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="499a6-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="499a6-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="499a6-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="499a6-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="499a6-122">-Confirm</span></span>
<span data-ttu-id="499a6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="499a6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="499a6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499a6-124">-WhatIf</span></span>
<span data-ttu-id="499a6-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="499a6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="499a6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="499a6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="499a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499a6-127">CommonParameters</span></span>
<span data-ttu-id="499a6-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499a6-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="499a6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499a6-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="499a6-130">INPUTS</span></span>

## <span data-ttu-id="499a6-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="499a6-131">OUTPUTS</span></span>

### <span data-ttu-id="499a6-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="499a6-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="499a6-133">Notas</span><span class="sxs-lookup"><span data-stu-id="499a6-133">NOTES</span></span>

<span data-ttu-id="499a6-134">Aliases</span><span class="sxs-lookup"><span data-stu-id="499a6-134">ALIASES</span></span>

## <span data-ttu-id="499a6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="499a6-135">RELATED LINKS</span></span>

