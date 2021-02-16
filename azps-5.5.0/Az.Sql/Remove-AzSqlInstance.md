---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113948"
---
# <span data-ttu-id="579f3-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="579f3-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="579f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="579f3-102">SYNOPSIS</span></span>
<span data-ttu-id="579f3-103">Remove uma Instância de Banco de Dados Gerenciado pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="579f3-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="579f3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="579f3-104">SYNTAX</span></span>

### <span data-ttu-id="579f3-105">RemoveInstanceFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="579f3-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579f3-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="579f3-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579f3-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="579f3-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579f3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="579f3-108">DESCRIPTION</span></span>
<span data-ttu-id="579f3-109">O cmdlet **Remove-AzSqlInstance** remove uma Instância Gerenciada do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="579f3-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="579f3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="579f3-110">EXAMPLES</span></span>

### <span data-ttu-id="579f3-111">Exemplo 1: Remover instância</span><span class="sxs-lookup"><span data-stu-id="579f3-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="579f3-112">Esse comando remove a instância nomeada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="579f3-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="579f3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="579f3-113">PARAMETERS</span></span>

### <span data-ttu-id="579f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579f3-114">-DefaultProfile</span></span>
<span data-ttu-id="579f3-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="579f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579f3-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="579f3-116">-Force</span></span>
<span data-ttu-id="579f3-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="579f3-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="579f3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="579f3-118">-InputObject</span></span>
<span data-ttu-id="579f3-119">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="579f3-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="579f3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="579f3-120">-Name</span></span>
<span data-ttu-id="579f3-121">Nome da instância SQL.</span><span class="sxs-lookup"><span data-stu-id="579f3-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="579f3-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="579f3-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579f3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="579f3-124">-ResourceId</span></span>
<span data-ttu-id="579f3-125">A ID do recurso do objeto de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="579f3-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579f3-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="579f3-126">-Confirm</span></span>
<span data-ttu-id="579f3-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="579f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="579f3-128">-WhatIf</span></span>
<span data-ttu-id="579f3-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="579f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579f3-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="579f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579f3-131">CommonParameters</span></span>
<span data-ttu-id="579f3-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579f3-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="579f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579f3-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="579f3-134">INPUTS</span></span>

### <span data-ttu-id="579f3-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="579f3-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="579f3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="579f3-136">System.String</span></span>

## <span data-ttu-id="579f3-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="579f3-137">OUTPUTS</span></span>

### <span data-ttu-id="579f3-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="579f3-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="579f3-139">Notas</span><span class="sxs-lookup"><span data-stu-id="579f3-139">NOTES</span></span>

## <span data-ttu-id="579f3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="579f3-140">RELATED LINKS</span></span>
