---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428713"
---
# <span data-ttu-id="425c2-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="425c2-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="425c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="425c2-102">SYNOPSIS</span></span>
<span data-ttu-id="425c2-103">Obtém a política de retenção de longo prazo de um banco de dados gerenciado</span><span class="sxs-lookup"><span data-stu-id="425c2-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="425c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="425c2-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="425c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="425c2-105">DESCRIPTION</span></span>
<span data-ttu-id="425c2-106">O cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** Obtém a política de retenção de longo prazo registrada nesse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="425c2-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="425c2-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="425c2-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="425c2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="425c2-108">EXAMPLES</span></span>

### <span data-ttu-id="425c2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="425c2-109">Example 1</span></span>
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

<span data-ttu-id="425c2-110">Obtém a versão atual da política de retenção de longo prazo para o banco de dados</span><span class="sxs-lookup"><span data-stu-id="425c2-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="425c2-111">OS</span><span class="sxs-lookup"><span data-stu-id="425c2-111">PARAMETERS</span></span>

### <span data-ttu-id="425c2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="425c2-112">-DatabaseName</span></span>
<span data-ttu-id="425c2-113">O nome do banco de dados gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="425c2-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="425c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425c2-114">-DefaultProfile</span></span>
<span data-ttu-id="425c2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="425c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425c2-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="425c2-116">-InstanceName</span></span>
<span data-ttu-id="425c2-117">O nome da instância gerenciada do Azure à qual o banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="425c2-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="425c2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425c2-118">-ResourceGroupName</span></span>
<span data-ttu-id="425c2-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="425c2-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="425c2-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="425c2-120">-Confirm</span></span>
<span data-ttu-id="425c2-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="425c2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="425c2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="425c2-122">-WhatIf</span></span>
<span data-ttu-id="425c2-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="425c2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="425c2-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="425c2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="425c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425c2-125">CommonParameters</span></span>
<span data-ttu-id="425c2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425c2-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="425c2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425c2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="425c2-128">INPUTS</span></span>

### <span data-ttu-id="425c2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="425c2-129">System.String</span></span>

## <span data-ttu-id="425c2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="425c2-130">OUTPUTS</span></span>

### <span data-ttu-id="425c2-131">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="425c2-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="425c2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="425c2-132">NOTES</span></span>

## <span data-ttu-id="425c2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="425c2-133">RELATED LINKS</span></span>

[<span data-ttu-id="425c2-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="425c2-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="425c2-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="425c2-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="425c2-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="425c2-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="425c2-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="425c2-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)