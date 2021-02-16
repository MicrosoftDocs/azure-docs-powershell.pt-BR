---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117589"
---
# <span data-ttu-id="de14f-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="de14f-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="de14f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de14f-102">SYNOPSIS</span></span>
<span data-ttu-id="de14f-103">Cria ou atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de14f-103">Creates or updates a database.</span></span>

## <span data-ttu-id="de14f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de14f-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de14f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="de14f-105">DESCRIPTION</span></span>
<span data-ttu-id="de14f-106">Cria ou atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de14f-106">Creates or updates a database.</span></span>

## <span data-ttu-id="de14f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de14f-107">EXAMPLES</span></span>

### <span data-ttu-id="de14f-108">Exemplo 1: Criar um novo banco de dados Kusto por nome</span><span class="sxs-lookup"><span data-stu-id="de14f-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="de14f-109">O comando acima cria um novo banco de dados do Kusto chamado "mykustodatabase" no cluster existente "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="de14f-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="de14f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de14f-110">PARAMETERS</span></span>

### <span data-ttu-id="de14f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de14f-111">-AsJob</span></span>
<span data-ttu-id="de14f-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="de14f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="de14f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="de14f-113">-ClusterName</span></span>
<span data-ttu-id="de14f-114">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="de14f-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="de14f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de14f-115">-DefaultProfile</span></span>
<span data-ttu-id="de14f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de14f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de14f-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="de14f-117">-HotCachePeriod</span></span>
<span data-ttu-id="de14f-118">O tempo em que os dados devem ser mantidos em cache para consultas rápidas no TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="de14f-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="de14f-119">-Tipo</span><span class="sxs-lookup"><span data-stu-id="de14f-119">-Kind</span></span>
<span data-ttu-id="de14f-120">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="de14f-120">Kind of the database</span></span>

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

### <span data-ttu-id="de14f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="de14f-121">-Location</span></span>
<span data-ttu-id="de14f-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="de14f-122">Resource location.</span></span>

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

### <span data-ttu-id="de14f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="de14f-123">-Name</span></span>
<span data-ttu-id="de14f-124">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="de14f-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="de14f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de14f-125">-NoWait</span></span>
<span data-ttu-id="de14f-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="de14f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de14f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de14f-127">-ResourceGroupName</span></span>
<span data-ttu-id="de14f-128">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="de14f-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="de14f-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="de14f-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="de14f-130">O tempo em que os dados devem ser mantidos antes de deixar de ser acessíveis para consultas no TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="de14f-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="de14f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de14f-131">-SubscriptionId</span></span>
<span data-ttu-id="de14f-132">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de14f-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de14f-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="de14f-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de14f-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="de14f-134">-Confirm</span></span>
<span data-ttu-id="de14f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de14f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de14f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de14f-136">-WhatIf</span></span>
<span data-ttu-id="de14f-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="de14f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de14f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de14f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de14f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de14f-139">CommonParameters</span></span>
<span data-ttu-id="de14f-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de14f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de14f-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de14f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de14f-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="de14f-142">INPUTS</span></span>

## <span data-ttu-id="de14f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="de14f-143">OUTPUTS</span></span>

### <span data-ttu-id="de14f-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="de14f-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="de14f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="de14f-145">NOTES</span></span>

<span data-ttu-id="de14f-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="de14f-146">ALIASES</span></span>

## <span data-ttu-id="de14f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de14f-147">RELATED LINKS</span></span>

