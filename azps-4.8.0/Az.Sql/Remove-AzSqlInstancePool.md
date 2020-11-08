---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113229"
---
# <span data-ttu-id="55c60-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="55c60-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="55c60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55c60-102">SYNOPSIS</span></span>
<span data-ttu-id="55c60-103">Remove um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="55c60-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="55c60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55c60-104">SYNTAX</span></span>

### <span data-ttu-id="55c60-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="55c60-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c60-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c60-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c60-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c60-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55c60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55c60-108">DESCRIPTION</span></span>
<span data-ttu-id="55c60-109">O cmdlet **Remove-AzSqlInstancePool** remove um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="55c60-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="55c60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55c60-110">EXAMPLES</span></span>

### <span data-ttu-id="55c60-111">Exemplo 1: remover um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="55c60-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="55c60-112">Exemplo 2: remover um pool de instâncias por seu identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="55c60-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="55c60-113">Exemplo 3: remover um pool de instâncias por um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="55c60-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="55c60-114">Esse comando Remove um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="55c60-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="55c60-115">OS</span><span class="sxs-lookup"><span data-stu-id="55c60-115">PARAMETERS</span></span>

### <span data-ttu-id="55c60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c60-116">-DefaultProfile</span></span>
<span data-ttu-id="55c60-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55c60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c60-118">-InputObject</span></span>
<span data-ttu-id="55c60-119">O objeto de pool de instâncias a ser removido.</span><span class="sxs-lookup"><span data-stu-id="55c60-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c60-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="55c60-120">-Name</span></span>
<span data-ttu-id="55c60-121">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="55c60-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c60-122">-ResourceGroupName</span></span>
<span data-ttu-id="55c60-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55c60-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c60-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c60-124">-ResourceId</span></span>
<span data-ttu-id="55c60-125">A ID de recurso do pool de instâncias a ser removida.</span><span class="sxs-lookup"><span data-stu-id="55c60-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c60-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55c60-126">-Confirm</span></span>
<span data-ttu-id="55c60-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c60-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c60-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c60-128">-WhatIf</span></span>
<span data-ttu-id="55c60-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55c60-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c60-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55c60-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c60-131">CommonParameters</span></span>
<span data-ttu-id="55c60-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c60-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55c60-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c60-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55c60-134">INPUTS</span></span>

### <span data-ttu-id="55c60-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="55c60-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="55c60-136">System. String</span><span class="sxs-lookup"><span data-stu-id="55c60-136">System.String</span></span>

## <span data-ttu-id="55c60-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55c60-137">OUTPUTS</span></span>

### <span data-ttu-id="55c60-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="55c60-138">System.Object</span></span>
## <span data-ttu-id="55c60-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55c60-139">NOTES</span></span>

## <span data-ttu-id="55c60-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55c60-140">RELATED LINKS</span></span>
