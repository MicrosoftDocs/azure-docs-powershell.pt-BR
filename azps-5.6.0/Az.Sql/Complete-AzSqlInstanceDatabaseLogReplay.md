---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2237522cbf7b179358ea4fa9f7ed7608222782ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893099"
---
# <span data-ttu-id="2f4a7-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2f4a7-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="2f4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4a7-103">Conclui o serviço de Repetição de Log para o banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="2f4a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2f4a7-104">SYNTAX</span></span>

### <span data-ttu-id="2f4a7-105">LogReplayInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f4a7-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="2f4a7-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f4a7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2f4a7-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4a7-108">O cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** conclui o serviço de Repetição de Log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="2f4a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-109">EXAMPLES</span></span>

### <span data-ttu-id="2f4a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f4a7-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="2f4a7-111">Este comando concluirá o serviço de Repetição de Log para o banco de dados determinado após a restauração do último backup.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="2f4a7-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-112">PARAMETERS</span></span>

### <span data-ttu-id="2f4a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4a7-113">-DefaultProfile</span></span>
<span data-ttu-id="2f4a7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f4a7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f4a7-115">-InputObject</span></span>
<span data-ttu-id="2f4a7-116">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-116">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a7-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2f4a7-117">-InstanceName</span></span>
<span data-ttu-id="2f4a7-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a7-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="2f4a7-119">-LastBackupName</span></span>
<span data-ttu-id="2f4a7-120">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2f4a7-121">-Name</span></span>
<span data-ttu-id="2f4a7-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f4a7-123">-PassThru</span></span>
<span data-ttu-id="2f4a7-124">Define Se retornará o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="2f4a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f4a7-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f4a7-127">-Confirm</span></span>
<span data-ttu-id="2f4a7-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4a7-129">-WhatIf</span></span>
<span data-ttu-id="2f4a7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f4a7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4a7-132">CommonParameters</span></span>
<span data-ttu-id="2f4a7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4a7-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f4a7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4a7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-135">INPUTS</span></span>

### <span data-ttu-id="2f4a7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2f4a7-136">System.String</span></span>

### <span data-ttu-id="2f4a7-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2f4a7-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="2f4a7-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-138">OUTPUTS</span></span>

## <span data-ttu-id="2f4a7-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2f4a7-139">NOTES</span></span>

## <span data-ttu-id="2f4a7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f4a7-140">RELATED LINKS</span></span>
