---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117098"
---
# <span data-ttu-id="16b94-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16b94-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="16b94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16b94-102">SYNOPSIS</span></span>
<span data-ttu-id="16b94-103">Obtém a política de retenção de longo prazo de um banco de dados gerenciado</span><span class="sxs-lookup"><span data-stu-id="16b94-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="16b94-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16b94-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16b94-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="16b94-105">DESCRIPTION</span></span>
<span data-ttu-id="16b94-106">O cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** obtém a política de retenção de longo prazo registrada nesse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="16b94-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="16b94-107">A política é um recurso de Backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="16b94-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="16b94-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16b94-108">EXAMPLES</span></span>

### <span data-ttu-id="16b94-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16b94-109">Example 1</span></span>
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

<span data-ttu-id="16b94-110">Obtém a versão atual da política de retenção de longo prazo para o banco de dados</span><span class="sxs-lookup"><span data-stu-id="16b94-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="16b94-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16b94-111">PARAMETERS</span></span>

### <span data-ttu-id="16b94-112">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="16b94-112">-DatabaseName</span></span>
<span data-ttu-id="16b94-113">O nome do Banco de Dados Gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="16b94-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="16b94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b94-114">-DefaultProfile</span></span>
<span data-ttu-id="16b94-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16b94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b94-116">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="16b94-116">-InstanceName</span></span>
<span data-ttu-id="16b94-117">O nome da Instância Gerenciada do Azure ao banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="16b94-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="16b94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b94-118">-ResourceGroupName</span></span>
<span data-ttu-id="16b94-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16b94-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="16b94-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16b94-120">-Confirm</span></span>
<span data-ttu-id="16b94-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16b94-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b94-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b94-122">-WhatIf</span></span>
<span data-ttu-id="16b94-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16b94-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b94-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16b94-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b94-125">CommonParameters</span></span>
<span data-ttu-id="16b94-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b94-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16b94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b94-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="16b94-128">INPUTS</span></span>

### <span data-ttu-id="16b94-129">System.String</span><span class="sxs-lookup"><span data-stu-id="16b94-129">System.String</span></span>

## <span data-ttu-id="16b94-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="16b94-130">OUTPUTS</span></span>

### <span data-ttu-id="16b94-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="16b94-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="16b94-132">Notas</span><span class="sxs-lookup"><span data-stu-id="16b94-132">NOTES</span></span>

## <span data-ttu-id="16b94-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16b94-133">RELATED LINKS</span></span>

[<span data-ttu-id="16b94-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="16b94-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="16b94-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="16b94-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="16b94-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16b94-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="16b94-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="16b94-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)