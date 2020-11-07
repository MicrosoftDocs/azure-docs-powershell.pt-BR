---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944288"
---
# <span data-ttu-id="daf2c-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="daf2c-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="daf2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="daf2c-103">Obtém a política de retenção de longo prazo de um banco de dados gerenciado</span><span class="sxs-lookup"><span data-stu-id="daf2c-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="daf2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daf2c-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daf2c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daf2c-105">DESCRIPTION</span></span>
<span data-ttu-id="daf2c-106">O cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** Obtém a política de retenção de longo prazo registrada nesse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="daf2c-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="daf2c-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="daf2c-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="daf2c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daf2c-108">EXAMPLES</span></span>

### <span data-ttu-id="daf2c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="daf2c-109">Example 1</span></span>
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

<span data-ttu-id="daf2c-110">Obtém a versão atual da política de retenção de longo prazo para o banco de dados</span><span class="sxs-lookup"><span data-stu-id="daf2c-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="daf2c-111">OS</span><span class="sxs-lookup"><span data-stu-id="daf2c-111">PARAMETERS</span></span>

### <span data-ttu-id="daf2c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="daf2c-112">-DatabaseName</span></span>
<span data-ttu-id="daf2c-113">O nome do banco de dados gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="daf2c-113">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf2c-114">-DefaultProfile</span></span>
<span data-ttu-id="daf2c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daf2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="daf2c-116">-InstanceName</span></span>
<span data-ttu-id="daf2c-117">O nome da instância gerenciada do Azure à qual o banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="daf2c-117">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf2c-118">-ResourceGroupName</span></span>
<span data-ttu-id="daf2c-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daf2c-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="daf2c-120">-Confirm</span></span>
<span data-ttu-id="daf2c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf2c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf2c-122">-WhatIf</span></span>
<span data-ttu-id="daf2c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daf2c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf2c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daf2c-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf2c-125">CommonParameters</span></span>
<span data-ttu-id="daf2c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf2c-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daf2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf2c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daf2c-128">INPUTS</span></span>

### <span data-ttu-id="daf2c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="daf2c-129">System.String</span></span>

## <span data-ttu-id="daf2c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daf2c-130">OUTPUTS</span></span>

### <span data-ttu-id="daf2c-131">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="daf2c-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="daf2c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daf2c-132">NOTES</span></span>

## <span data-ttu-id="daf2c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daf2c-133">RELATED LINKS</span></span>

[<span data-ttu-id="daf2c-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="daf2c-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="daf2c-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="daf2c-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="daf2c-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="daf2c-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="daf2c-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="daf2c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)