---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117000"
---
# <span data-ttu-id="0eb57-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="0eb57-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="0eb57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0eb57-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb57-103">Conclui o serviço de reprodução de log para o banco de dados fornecido.</span><span class="sxs-lookup"><span data-stu-id="0eb57-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="0eb57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eb57-104">SYNTAX</span></span>

### <span data-ttu-id="0eb57-105">LogReplayInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="0eb57-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0eb57-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0eb57-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0eb57-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb57-108">O cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** conclui o serviço de repetição de log em um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0eb57-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="0eb57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0eb57-109">EXAMPLES</span></span>

### <span data-ttu-id="0eb57-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0eb57-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="0eb57-111">Este comando concluirá o serviço de repetição de log concluir o último backup será restaurado.</span><span class="sxs-lookup"><span data-stu-id="0eb57-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="0eb57-112">OS</span><span class="sxs-lookup"><span data-stu-id="0eb57-112">PARAMETERS</span></span>

### <span data-ttu-id="0eb57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb57-113">-DefaultProfile</span></span>
<span data-ttu-id="0eb57-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb57-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb57-115">-InputObject</span></span>
<span data-ttu-id="0eb57-116">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="0eb57-116">The instance database object.</span></span>

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

### <span data-ttu-id="0eb57-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0eb57-117">-InstanceName</span></span>
<span data-ttu-id="0eb57-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="0eb57-118">The name of the instance.</span></span>

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

### <span data-ttu-id="0eb57-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="0eb57-119">-LastBackupName</span></span>
<span data-ttu-id="0eb57-120">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="0eb57-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="0eb57-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0eb57-121">-Name</span></span>
<span data-ttu-id="0eb57-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="0eb57-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="0eb57-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eb57-123">-PassThru</span></span>
<span data-ttu-id="0eb57-124">Define se retorna o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0eb57-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="0eb57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb57-125">-ResourceGroupName</span></span>
<span data-ttu-id="0eb57-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0eb57-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0eb57-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0eb57-127">-Confirm</span></span>
<span data-ttu-id="0eb57-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb57-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb57-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb57-129">-WhatIf</span></span>
<span data-ttu-id="0eb57-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0eb57-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eb57-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0eb57-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb57-132">CommonParameters</span></span>
<span data-ttu-id="0eb57-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb57-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eb57-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb57-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0eb57-135">INPUTS</span></span>

### <span data-ttu-id="0eb57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb57-136">System.String</span></span>

### <span data-ttu-id="0eb57-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0eb57-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0eb57-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0eb57-138">OUTPUTS</span></span>

## <span data-ttu-id="0eb57-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0eb57-139">NOTES</span></span>

## <span data-ttu-id="0eb57-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eb57-140">RELATED LINKS</span></span>
