---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: f18cb699df3bd96a6b5705e09f6cb9ea924f3f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890959"
---
# <span data-ttu-id="8fdb2-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="8fdb2-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="8fdb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdb2-103">Remove um Cluster Virtual do Azure SQL Virtual.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8fdb2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8fdb2-104">SYNTAX</span></span>

### <span data-ttu-id="8fdb2-105">RemoveVirtualClusterFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8fdb2-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdb2-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdb2-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdb2-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8fdb2-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdb2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8fdb2-108">DESCRIPTION</span></span>
<span data-ttu-id="8fdb2-109">O cmdlet **Remove-AzSqlVirtualCluster** remove um Cluster Virtual do Azure SQL Virtual.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8fdb2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-110">EXAMPLES</span></span>

### <span data-ttu-id="8fdb2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fdb2-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="8fdb2-112">Este comando remove o cluster virtual chamado VirtualCluster1 atribuído ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8fdb2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-113">PARAMETERS</span></span>

### <span data-ttu-id="8fdb2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fdb2-114">-AsJob</span></span>
<span data-ttu-id="8fdb2-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8fdb2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fdb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdb2-116">-DefaultProfile</span></span>
<span data-ttu-id="8fdb2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdb2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fdb2-118">-InputObject</span></span>
<span data-ttu-id="8fdb2-119">O objeto instance a ser removido</span><span class="sxs-lookup"><span data-stu-id="8fdb2-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8fdb2-120">-Name</span></span>
<span data-ttu-id="8fdb2-121">O nome do cluster virtual.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdb2-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fdb2-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fdb2-124">-ResourceId</span></span>
<span data-ttu-id="8fdb2-125">A ID do recurso do objeto instance a ser removido</span><span class="sxs-lookup"><span data-stu-id="8fdb2-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fdb2-126">-Confirm</span></span>
<span data-ttu-id="8fdb2-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fdb2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdb2-128">-WhatIf</span></span>
<span data-ttu-id="8fdb2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fdb2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fdb2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdb2-131">CommonParameters</span></span>
<span data-ttu-id="8fdb2-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdb2-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fdb2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdb2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-134">INPUTS</span></span>

### <span data-ttu-id="8fdb2-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="8fdb2-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="8fdb2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8fdb2-136">System.String</span></span>

## <span data-ttu-id="8fdb2-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-137">OUTPUTS</span></span>

### <span data-ttu-id="8fdb2-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="8fdb2-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="8fdb2-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="8fdb2-139">NOTES</span></span>

## <span data-ttu-id="8fdb2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fdb2-140">RELATED LINKS</span></span>
