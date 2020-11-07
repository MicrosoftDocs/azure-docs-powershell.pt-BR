---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942809"
---
# <span data-ttu-id="4431d-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4431d-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="4431d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4431d-102">SYNOPSIS</span></span>
<span data-ttu-id="4431d-103">Remove um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4431d-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="4431d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4431d-104">SYNTAX</span></span>

### <span data-ttu-id="4431d-105">RemoveInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="4431d-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4431d-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4431d-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4431d-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4431d-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4431d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4431d-108">DESCRIPTION</span></span>
<span data-ttu-id="4431d-109">O cmdlet **Remove-AzSqlInstanceDatabase** remove um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4431d-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="4431d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4431d-110">EXAMPLES</span></span>

### <span data-ttu-id="4431d-111">Exemplo 1: remover um banco de dados de uma instância</span><span class="sxs-lookup"><span data-stu-id="4431d-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4431d-112">Esse comando Remove o banco de dados chamado Database01 da instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="4431d-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="4431d-113">OS</span><span class="sxs-lookup"><span data-stu-id="4431d-113">PARAMETERS</span></span>

### <span data-ttu-id="4431d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4431d-114">-DefaultProfile</span></span>
<span data-ttu-id="4431d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4431d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4431d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4431d-116">-Force</span></span>
<span data-ttu-id="4431d-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="4431d-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4431d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4431d-118">-InputObject</span></span>
<span data-ttu-id="4431d-119">O objeto de banco de dados de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="4431d-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4431d-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4431d-120">-InstanceName</span></span>
<span data-ttu-id="4431d-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="4431d-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4431d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4431d-122">-Name</span></span>
<span data-ttu-id="4431d-123">O nome do banco de dados de instância SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4431d-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4431d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4431d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4431d-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4431d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4431d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4431d-126">-ResourceId</span></span>
<span data-ttu-id="4431d-127">A ID do recurso do objeto de banco de dados de instância a ser removida</span><span class="sxs-lookup"><span data-stu-id="4431d-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4431d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4431d-128">-Confirm</span></span>
<span data-ttu-id="4431d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4431d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4431d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4431d-130">-WhatIf</span></span>
<span data-ttu-id="4431d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4431d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4431d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4431d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4431d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4431d-133">CommonParameters</span></span>
<span data-ttu-id="4431d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4431d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4431d-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4431d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4431d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4431d-136">INPUTS</span></span>

### <span data-ttu-id="4431d-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4431d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="4431d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4431d-138">System.String</span></span>

## <span data-ttu-id="4431d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4431d-139">OUTPUTS</span></span>

### <span data-ttu-id="4431d-140">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4431d-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="4431d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4431d-141">NOTES</span></span>

## <span data-ttu-id="4431d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4431d-142">RELATED LINKS</span></span>
