---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 42c2fa289eef04734c0619ca7bf2a46ece19606e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892702"
---
# <span data-ttu-id="e9bf6-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e9bf6-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e9bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bf6-103">Cancela o serviço de Repetição de Log soltando o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="e9bf6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e9bf6-104">SYNTAX</span></span>

### <span data-ttu-id="e9bf6-105">LogReplayInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9bf6-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9bf6-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e9bf6-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9bf6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e9bf6-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bf6-108">O cmdlet **Stop-AzSqlInstanceDatabaseLogReplay** solta o banco de dados e, portanto, cancela o serviço de Repetição de Log.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="e9bf6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-109">EXAMPLES</span></span>

### <span data-ttu-id="e9bf6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9bf6-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="e9bf6-111">Esse comando cancelará o serviço de repetição de log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="e9bf6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-112">PARAMETERS</span></span>

### <span data-ttu-id="e9bf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bf6-113">-DefaultProfile</span></span>
<span data-ttu-id="e9bf6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bf6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9bf6-115">-Force</span></span>
<span data-ttu-id="e9bf6-116">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="e9bf6-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e9bf6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9bf6-117">-InputObject</span></span>
<span data-ttu-id="e9bf6-118">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-118">The instance database object.</span></span>

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

### <span data-ttu-id="e9bf6-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e9bf6-119">-InstanceName</span></span>
<span data-ttu-id="e9bf6-120">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-120">The name of the instance.</span></span>

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

### <span data-ttu-id="e9bf6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e9bf6-121">-Name</span></span>
<span data-ttu-id="e9bf6-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="e9bf6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9bf6-123">-PassThru</span></span>
<span data-ttu-id="e9bf6-124">Define Se retornará o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e9bf6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bf6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e9bf6-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9bf6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9bf6-127">-Confirm</span></span>
<span data-ttu-id="e9bf6-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9bf6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9bf6-129">-WhatIf</span></span>
<span data-ttu-id="e9bf6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9bf6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9bf6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bf6-132">CommonParameters</span></span>
<span data-ttu-id="e9bf6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bf6-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9bf6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bf6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-135">INPUTS</span></span>

### <span data-ttu-id="e9bf6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e9bf6-136">System.String</span></span>

### <span data-ttu-id="e9bf6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9bf6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e9bf6-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-138">OUTPUTS</span></span>

### <span data-ttu-id="e9bf6-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9bf6-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e9bf6-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="e9bf6-140">NOTES</span></span>

## <span data-ttu-id="e9bf6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-141">RELATED LINKS</span></span>
