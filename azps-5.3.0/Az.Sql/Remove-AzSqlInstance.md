---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427915"
---
# <span data-ttu-id="57578-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="57578-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="57578-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57578-102">SYNOPSIS</span></span>
<span data-ttu-id="57578-103">Remove uma instância de banco de dados gerenciado do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="57578-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="57578-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57578-104">SYNTAX</span></span>

### <span data-ttu-id="57578-105">RemoveInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="57578-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57578-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="57578-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57578-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="57578-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57578-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57578-108">DESCRIPTION</span></span>
<span data-ttu-id="57578-109">O cmdlet **Remove-AzSqlInstance** remove uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="57578-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="57578-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57578-110">EXAMPLES</span></span>

### <span data-ttu-id="57578-111">Exemplo 1: remover instância</span><span class="sxs-lookup"><span data-stu-id="57578-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="57578-112">Esse comando Remove a instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="57578-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="57578-113">OS</span><span class="sxs-lookup"><span data-stu-id="57578-113">PARAMETERS</span></span>

### <span data-ttu-id="57578-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57578-114">-DefaultProfile</span></span>
<span data-ttu-id="57578-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57578-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57578-116">-Force</span><span class="sxs-lookup"><span data-stu-id="57578-116">-Force</span></span>
<span data-ttu-id="57578-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="57578-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="57578-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57578-118">-InputObject</span></span>
<span data-ttu-id="57578-119">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="57578-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="57578-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="57578-120">-Name</span></span>
<span data-ttu-id="57578-121">Nome da instância SQL.</span><span class="sxs-lookup"><span data-stu-id="57578-121">SQL instance name.</span></span>

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

### <span data-ttu-id="57578-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57578-122">-ResourceGroupName</span></span>
<span data-ttu-id="57578-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57578-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="57578-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57578-124">-ResourceId</span></span>
<span data-ttu-id="57578-125">A ID do recurso do objeto de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="57578-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="57578-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57578-126">-Confirm</span></span>
<span data-ttu-id="57578-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57578-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57578-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57578-128">-WhatIf</span></span>
<span data-ttu-id="57578-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57578-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57578-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57578-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57578-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57578-131">CommonParameters</span></span>
<span data-ttu-id="57578-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57578-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57578-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57578-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57578-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57578-134">INPUTS</span></span>

### <span data-ttu-id="57578-135">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="57578-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="57578-136">System. String</span><span class="sxs-lookup"><span data-stu-id="57578-136">System.String</span></span>

## <span data-ttu-id="57578-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57578-137">OUTPUTS</span></span>

### <span data-ttu-id="57578-138">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="57578-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="57578-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57578-139">NOTES</span></span>

## <span data-ttu-id="57578-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57578-140">RELATED LINKS</span></span>
