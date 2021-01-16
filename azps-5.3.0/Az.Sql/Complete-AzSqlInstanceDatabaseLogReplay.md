---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271206"
---
# <span data-ttu-id="9cbfd-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9cbfd-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9cbfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbfd-103">Conclui o serviço de reprodução de log para o banco de dados fornecido.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="9cbfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cbfd-104">SYNTAX</span></span>

### <span data-ttu-id="9cbfd-105">LogReplayInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="9cbfd-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cbfd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9cbfd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cbfd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cbfd-107">DESCRIPTION</span></span>
<span data-ttu-id="9cbfd-108">O cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** conclui o serviço de repetição de log em um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="9cbfd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cbfd-109">EXAMPLES</span></span>

### <span data-ttu-id="9cbfd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9cbfd-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="9cbfd-111">Este comando concluirá o serviço de repetição de log concluir o último backup será restaurado.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="9cbfd-112">OS</span><span class="sxs-lookup"><span data-stu-id="9cbfd-112">PARAMETERS</span></span>

### <span data-ttu-id="9cbfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbfd-113">-DefaultProfile</span></span>
<span data-ttu-id="9cbfd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbfd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cbfd-115">-InputObject</span></span>
<span data-ttu-id="9cbfd-116">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-116">The instance database object.</span></span>

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

### <span data-ttu-id="9cbfd-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9cbfd-117">-InstanceName</span></span>
<span data-ttu-id="9cbfd-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-118">The name of the instance.</span></span>

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

### <span data-ttu-id="9cbfd-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="9cbfd-119">-LastBackupName</span></span>
<span data-ttu-id="9cbfd-120">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="9cbfd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cbfd-121">-Name</span></span>
<span data-ttu-id="9cbfd-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="9cbfd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cbfd-123">-PassThru</span></span>
<span data-ttu-id="9cbfd-124">Define se retorna o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="9cbfd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbfd-125">-ResourceGroupName</span></span>
<span data-ttu-id="9cbfd-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cbfd-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9cbfd-127">-Confirm</span></span>
<span data-ttu-id="9cbfd-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbfd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbfd-129">-WhatIf</span></span>
<span data-ttu-id="9cbfd-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cbfd-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbfd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbfd-132">CommonParameters</span></span>
<span data-ttu-id="9cbfd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbfd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbfd-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cbfd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbfd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cbfd-135">INPUTS</span></span>

### <span data-ttu-id="9cbfd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbfd-136">System.String</span></span>

### <span data-ttu-id="9cbfd-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9cbfd-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9cbfd-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cbfd-138">OUTPUTS</span></span>

## <span data-ttu-id="9cbfd-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cbfd-139">NOTES</span></span>

## <span data-ttu-id="9cbfd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cbfd-140">RELATED LINKS</span></span>
