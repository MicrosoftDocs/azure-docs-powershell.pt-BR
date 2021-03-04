---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 3b1c2865e6e5084f3108409d9afae0979ae635b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891586"
---
# <span data-ttu-id="8edd6-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8edd6-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="8edd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8edd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8edd6-103">Obtém a política de retenção de longo prazo de um banco de dados gerenciado</span><span class="sxs-lookup"><span data-stu-id="8edd6-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="8edd6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8edd6-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8edd6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8edd6-105">DESCRIPTION</span></span>
<span data-ttu-id="8edd6-106">O cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** obtém a política de retenção de longo prazo registrada nesse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8edd6-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="8edd6-107">A política é um recurso de Backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="8edd6-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="8edd6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8edd6-108">EXAMPLES</span></span>

### <span data-ttu-id="8edd6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8edd6-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="8edd6-110">Obtém a versão atual da política de retenção de longo prazo para o banco de dados</span><span class="sxs-lookup"><span data-stu-id="8edd6-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="8edd6-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8edd6-111">PARAMETERS</span></span>

### <span data-ttu-id="8edd6-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8edd6-112">-DatabaseName</span></span>
<span data-ttu-id="8edd6-113">O nome do Banco de Dados Gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="8edd6-113">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8edd6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8edd6-114">-DefaultProfile</span></span>
<span data-ttu-id="8edd6-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8edd6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8edd6-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8edd6-116">-InstanceName</span></span>
<span data-ttu-id="8edd6-117">O nome da Instância Gerenciada do Azure a que o banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="8edd6-117">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8edd6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8edd6-118">-ResourceGroupName</span></span>
<span data-ttu-id="8edd6-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8edd6-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8edd6-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8edd6-120">-Confirm</span></span>
<span data-ttu-id="8edd6-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8edd6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8edd6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8edd6-122">-WhatIf</span></span>
<span data-ttu-id="8edd6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8edd6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8edd6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8edd6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8edd6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8edd6-125">CommonParameters</span></span>
<span data-ttu-id="8edd6-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8edd6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8edd6-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8edd6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8edd6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8edd6-128">INPUTS</span></span>

### <span data-ttu-id="8edd6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8edd6-129">System.String</span></span>

## <span data-ttu-id="8edd6-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8edd6-130">OUTPUTS</span></span>

### <span data-ttu-id="8edd6-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8edd6-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8edd6-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="8edd6-132">NOTES</span></span>

## <span data-ttu-id="8edd6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8edd6-133">RELATED LINKS</span></span>

[<span data-ttu-id="8edd6-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8edd6-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8edd6-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8edd6-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8edd6-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8edd6-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8edd6-137">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="8edd6-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)