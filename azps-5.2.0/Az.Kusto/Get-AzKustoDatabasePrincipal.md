---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260926"
---
# <span data-ttu-id="75dbe-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="75dbe-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="75dbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="75dbe-103">Retorna uma lista de objetos de banco de dados do cluster e do banco de dados Kusto fornecidos.</span><span class="sxs-lookup"><span data-stu-id="75dbe-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="75dbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75dbe-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75dbe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="75dbe-106">Retorna uma lista de objetos de banco de dados do cluster e do banco de dados Kusto fornecidos.</span><span class="sxs-lookup"><span data-stu-id="75dbe-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="75dbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="75dbe-108">Exemplo 1: lista de entidades de banco de dados do cluster e do banco de dados Kusto fornecidos</span><span class="sxs-lookup"><span data-stu-id="75dbe-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="75dbe-109">O comando acima retorna uma lista de objetos de banco de dados do cluster e do banco de dados de Kusto fornecidos</span><span class="sxs-lookup"><span data-stu-id="75dbe-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="75dbe-110">OS</span><span class="sxs-lookup"><span data-stu-id="75dbe-110">PARAMETERS</span></span>

### <span data-ttu-id="75dbe-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="75dbe-111">-ClusterName</span></span>
<span data-ttu-id="75dbe-112">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="75dbe-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="75dbe-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75dbe-113">-DatabaseName</span></span>
<span data-ttu-id="75dbe-114">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="75dbe-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="75dbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dbe-115">-DefaultProfile</span></span>
<span data-ttu-id="75dbe-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75dbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75dbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="75dbe-118">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="75dbe-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="75dbe-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75dbe-119">-SubscriptionId</span></span>
<span data-ttu-id="75dbe-120">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75dbe-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75dbe-121">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="75dbe-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="75dbe-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75dbe-122">-Confirm</span></span>
<span data-ttu-id="75dbe-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75dbe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75dbe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75dbe-124">-WhatIf</span></span>
<span data-ttu-id="75dbe-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75dbe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75dbe-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75dbe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75dbe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dbe-127">CommonParameters</span></span>
<span data-ttu-id="75dbe-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75dbe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dbe-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75dbe-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dbe-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75dbe-130">INPUTS</span></span>

## <span data-ttu-id="75dbe-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75dbe-131">OUTPUTS</span></span>

### <span data-ttu-id="75dbe-132">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="75dbe-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="75dbe-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75dbe-133">NOTES</span></span>

<span data-ttu-id="75dbe-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="75dbe-134">ALIASES</span></span>

## <span data-ttu-id="75dbe-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75dbe-135">RELATED LINKS</span></span>

