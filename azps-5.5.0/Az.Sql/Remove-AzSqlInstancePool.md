---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117079"
---
# <span data-ttu-id="18a1f-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="18a1f-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="18a1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="18a1f-103">Remove um pool de instâncias SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="18a1f-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="18a1f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18a1f-104">SYNTAX</span></span>

### <span data-ttu-id="18a1f-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18a1f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a1f-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a1f-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a1f-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a1f-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18a1f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="18a1f-108">DESCRIPTION</span></span>
<span data-ttu-id="18a1f-109">O cmdlet **Remove-AzSqlInstancePool** remove um pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="18a1f-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="18a1f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18a1f-110">EXAMPLES</span></span>

### <span data-ttu-id="18a1f-111">Exemplo 1: Remover um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="18a1f-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="18a1f-112">Exemplo 2: Remover um pool de instâncias por seu identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="18a1f-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="18a1f-113">Exemplo 3: Remover um pool de instâncias por um objeto de pool de instância</span><span class="sxs-lookup"><span data-stu-id="18a1f-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="18a1f-114">Esse comando remove um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="18a1f-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="18a1f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18a1f-115">PARAMETERS</span></span>

### <span data-ttu-id="18a1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a1f-116">-DefaultProfile</span></span>
<span data-ttu-id="18a1f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18a1f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a1f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18a1f-118">-InputObject</span></span>
<span data-ttu-id="18a1f-119">O objeto de pool de instâncias a ser removido.</span><span class="sxs-lookup"><span data-stu-id="18a1f-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="18a1f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="18a1f-120">-Name</span></span>
<span data-ttu-id="18a1f-121">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="18a1f-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="18a1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="18a1f-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18a1f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="18a1f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18a1f-124">-ResourceId</span></span>
<span data-ttu-id="18a1f-125">A ID do recurso de pool de instâncias a ser removido.</span><span class="sxs-lookup"><span data-stu-id="18a1f-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="18a1f-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="18a1f-126">-Confirm</span></span>
<span data-ttu-id="18a1f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18a1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a1f-128">-WhatIf</span></span>
<span data-ttu-id="18a1f-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="18a1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a1f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18a1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a1f-131">CommonParameters</span></span>
<span data-ttu-id="18a1f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a1f-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a1f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a1f-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="18a1f-134">INPUTS</span></span>

### <span data-ttu-id="18a1f-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="18a1f-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="18a1f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="18a1f-136">System.String</span></span>

## <span data-ttu-id="18a1f-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="18a1f-137">OUTPUTS</span></span>

### <span data-ttu-id="18a1f-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="18a1f-138">System.Object</span></span>
## <span data-ttu-id="18a1f-139">Notas</span><span class="sxs-lookup"><span data-stu-id="18a1f-139">NOTES</span></span>

## <span data-ttu-id="18a1f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18a1f-140">RELATED LINKS</span></span>
