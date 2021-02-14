---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115780"
---
# <span data-ttu-id="7dad4-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="7dad4-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="7dad4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dad4-102">SYNOPSIS</span></span>
<span data-ttu-id="7dad4-103">Conclui o serviço de Reprodução de Log para o banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="7dad4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dad4-104">SYNTAX</span></span>

### <span data-ttu-id="7dad4-105">LogReplayInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7dad4-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7dad4-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="7dad4-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dad4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dad4-107">DESCRIPTION</span></span>
<span data-ttu-id="7dad4-108">O cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** completa o serviço de Reprodução de Log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="7dad4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7dad4-109">EXAMPLES</span></span>

### <span data-ttu-id="7dad4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dad4-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="7dad4-111">Esse comando concluirá o serviço de Reprodução de Log para o banco de dados determinado após a restauração do último backup.</span><span class="sxs-lookup"><span data-stu-id="7dad4-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="7dad4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dad4-112">PARAMETERS</span></span>

### <span data-ttu-id="7dad4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dad4-113">-DefaultProfile</span></span>
<span data-ttu-id="7dad4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dad4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dad4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dad4-115">-InputObject</span></span>
<span data-ttu-id="7dad4-116">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="7dad4-116">The instance database object.</span></span>

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

### <span data-ttu-id="7dad4-117">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="7dad4-117">-InstanceName</span></span>
<span data-ttu-id="7dad4-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="7dad4-118">The name of the instance.</span></span>

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

### <span data-ttu-id="7dad4-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="7dad4-119">-LastBackupName</span></span>
<span data-ttu-id="7dad4-120">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="7dad4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dad4-121">-Name</span></span>
<span data-ttu-id="7dad4-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="7dad4-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="7dad4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dad4-123">-PassThru</span></span>
<span data-ttu-id="7dad4-124">Define se o grupo de sincronização deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="7dad4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dad4-125">-ResourceGroupName</span></span>
<span data-ttu-id="7dad4-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7dad4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7dad4-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7dad4-127">-Confirm</span></span>
<span data-ttu-id="7dad4-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dad4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dad4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dad4-129">-WhatIf</span></span>
<span data-ttu-id="7dad4-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dad4-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dad4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dad4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dad4-132">CommonParameters</span></span>
<span data-ttu-id="7dad4-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dad4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dad4-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dad4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dad4-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="7dad4-135">INPUTS</span></span>

### <span data-ttu-id="7dad4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7dad4-136">System.String</span></span>

### <span data-ttu-id="7dad4-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7dad4-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7dad4-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="7dad4-138">OUTPUTS</span></span>

## <span data-ttu-id="7dad4-139">Notas</span><span class="sxs-lookup"><span data-stu-id="7dad4-139">NOTES</span></span>

## <span data-ttu-id="7dad4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dad4-140">RELATED LINKS</span></span>
