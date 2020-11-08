---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111688"
---
# <span data-ttu-id="e26fc-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="e26fc-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="e26fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e26fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e26fc-103">Cria ou atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e26fc-103">Creates or updates a database.</span></span>

## <span data-ttu-id="e26fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e26fc-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e26fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e26fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e26fc-106">Cria ou atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e26fc-106">Creates or updates a database.</span></span>

## <span data-ttu-id="e26fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e26fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e26fc-108">Exemplo 1: criar um novo banco de dados do Kusto por nome</span><span class="sxs-lookup"><span data-stu-id="e26fc-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="e26fc-109">O comando acima cria um novo banco de dados Kusto chamado "mykustodatabase" no cluster existente "testnewkustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="e26fc-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="e26fc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e26fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e26fc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e26fc-111">-AsJob</span></span>
<span data-ttu-id="e26fc-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e26fc-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e26fc-113">-ClusterName</span></span>
<span data-ttu-id="e26fc-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e26fc-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e26fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26fc-115">-DefaultProfile</span></span>
<span data-ttu-id="e26fc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e26fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e26fc-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="e26fc-117">-HotCachePeriod</span></span>
<span data-ttu-id="e26fc-118">O tempo em que os dados devem ser mantidos em cache para consultas rápidas em TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="e26fc-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="e26fc-119">-Kind</span></span>
<span data-ttu-id="e26fc-120">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="e26fc-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-121">-Local</span><span class="sxs-lookup"><span data-stu-id="e26fc-121">-Location</span></span>
<span data-ttu-id="e26fc-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e26fc-122">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e26fc-123">-Name</span></span>
<span data-ttu-id="e26fc-124">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e26fc-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e26fc-125">-NoWait</span></span>
<span data-ttu-id="e26fc-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e26fc-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="e26fc-128">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e26fc-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e26fc-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="e26fc-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="e26fc-130">O tempo que os dados devem ser mantidos antes de deixar de ser acessível a consultas em TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="e26fc-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e26fc-131">-SubscriptionId</span></span>
<span data-ttu-id="e26fc-132">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e26fc-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e26fc-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e26fc-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fc-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e26fc-134">-Confirm</span></span>
<span data-ttu-id="e26fc-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e26fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e26fc-136">-WhatIf</span></span>
<span data-ttu-id="e26fc-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e26fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e26fc-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e26fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e26fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26fc-139">CommonParameters</span></span>
<span data-ttu-id="e26fc-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26fc-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e26fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26fc-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e26fc-142">INPUTS</span></span>

## <span data-ttu-id="e26fc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e26fc-143">OUTPUTS</span></span>

### <span data-ttu-id="e26fc-144">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="e26fc-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="e26fc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e26fc-145">NOTES</span></span>

<span data-ttu-id="e26fc-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e26fc-146">ALIASES</span></span>

## <span data-ttu-id="e26fc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e26fc-147">RELATED LINKS</span></span>

