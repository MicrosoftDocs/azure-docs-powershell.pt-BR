---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: d4c69457b9932f76d002e3941af3015225345c8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773790"
---
# <span data-ttu-id="dfd22-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="dfd22-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="dfd22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfd22-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd22-103">Remove um cluster virtual do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dfd22-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="dfd22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfd22-104">SYNTAX</span></span>

### <span data-ttu-id="dfd22-105">RemoveVirtualClusterFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfd22-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfd22-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="dfd22-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfd22-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="dfd22-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd22-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfd22-108">DESCRIPTION</span></span>
<span data-ttu-id="dfd22-109">O cmdlet **Remove-AzSqlVirtualCluster** remove um cluster virtual do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd22-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="dfd22-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfd22-110">EXAMPLES</span></span>

### <span data-ttu-id="dfd22-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dfd22-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="dfd22-112">Esse comando Remove o cluster virtual nomeado VirtualCluster1 atribuído à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfd22-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="dfd22-113">OS</span><span class="sxs-lookup"><span data-stu-id="dfd22-113">PARAMETERS</span></span>

### <span data-ttu-id="dfd22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfd22-114">-AsJob</span></span>
<span data-ttu-id="dfd22-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dfd22-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfd22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd22-116">-DefaultProfile</span></span>
<span data-ttu-id="dfd22-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfd22-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfd22-118">-InputObject</span></span>
<span data-ttu-id="dfd22-119">O objeto de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="dfd22-119">The instance object to remove</span></span>

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

### <span data-ttu-id="dfd22-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfd22-120">-Name</span></span>
<span data-ttu-id="dfd22-121">O nome do cluster virtual.</span><span class="sxs-lookup"><span data-stu-id="dfd22-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="dfd22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd22-122">-ResourceGroupName</span></span>
<span data-ttu-id="dfd22-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfd22-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfd22-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfd22-124">-ResourceId</span></span>
<span data-ttu-id="dfd22-125">A ID do recurso do objeto de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="dfd22-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="dfd22-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfd22-126">-Confirm</span></span>
<span data-ttu-id="dfd22-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd22-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd22-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd22-128">-WhatIf</span></span>
<span data-ttu-id="dfd22-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfd22-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd22-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfd22-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd22-131">CommonParameters</span></span>
<span data-ttu-id="dfd22-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd22-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfd22-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd22-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfd22-134">INPUTS</span></span>

### <span data-ttu-id="dfd22-135">Microsoft. Azure. Commands. Sql. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="dfd22-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="dfd22-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd22-136">System.String</span></span>

## <span data-ttu-id="dfd22-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfd22-137">OUTPUTS</span></span>

### <span data-ttu-id="dfd22-138">Microsoft. Azure. Commands. Sql. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="dfd22-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="dfd22-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfd22-139">NOTES</span></span>

## <span data-ttu-id="dfd22-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfd22-140">RELATED LINKS</span></span>