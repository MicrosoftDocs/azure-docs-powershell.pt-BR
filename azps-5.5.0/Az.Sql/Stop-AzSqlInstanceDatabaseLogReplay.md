---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118925"
---
# <span data-ttu-id="16e31-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="16e31-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="16e31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16e31-102">SYNOPSIS</span></span>
<span data-ttu-id="16e31-103">Cancela o serviço de Reprodução de Log soltando o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16e31-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="16e31-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e31-104">SYNTAX</span></span>

### <span data-ttu-id="16e31-105">LogReplayInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16e31-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16e31-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="16e31-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e31-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="16e31-107">DESCRIPTION</span></span>
<span data-ttu-id="16e31-108">O cmdlet **Stop-AzSqlInstanceDatabaseLogReplay** descarta o banco de dados e, portanto, cancela o serviço de Reprodução de Log.</span><span class="sxs-lookup"><span data-stu-id="16e31-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="16e31-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16e31-109">EXAMPLES</span></span>

### <span data-ttu-id="16e31-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16e31-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="16e31-111">Esse comando cancelará o serviço de reprodução de log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="16e31-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="16e31-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16e31-112">PARAMETERS</span></span>

### <span data-ttu-id="16e31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e31-113">-DefaultProfile</span></span>
<span data-ttu-id="16e31-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16e31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e31-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="16e31-115">-Force</span></span>
<span data-ttu-id="16e31-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="16e31-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="16e31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e31-117">-InputObject</span></span>
<span data-ttu-id="16e31-118">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="16e31-118">The instance database object.</span></span>

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

### <span data-ttu-id="16e31-119">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="16e31-119">-InstanceName</span></span>
<span data-ttu-id="16e31-120">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="16e31-120">The name of the instance.</span></span>

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

### <span data-ttu-id="16e31-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="16e31-121">-Name</span></span>
<span data-ttu-id="16e31-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="16e31-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="16e31-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e31-123">-PassThru</span></span>
<span data-ttu-id="16e31-124">Define se o grupo de sincronização deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="16e31-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="16e31-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e31-125">-ResourceGroupName</span></span>
<span data-ttu-id="16e31-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16e31-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="16e31-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16e31-127">-Confirm</span></span>
<span data-ttu-id="16e31-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e31-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e31-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e31-129">-WhatIf</span></span>
<span data-ttu-id="16e31-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16e31-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e31-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16e31-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e31-132">CommonParameters</span></span>
<span data-ttu-id="16e31-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e31-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e31-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e31-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="16e31-135">INPUTS</span></span>

### <span data-ttu-id="16e31-136">System.String</span><span class="sxs-lookup"><span data-stu-id="16e31-136">System.String</span></span>

### <span data-ttu-id="16e31-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="16e31-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="16e31-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="16e31-138">OUTPUTS</span></span>

### <span data-ttu-id="16e31-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="16e31-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="16e31-140">Notas</span><span class="sxs-lookup"><span data-stu-id="16e31-140">NOTES</span></span>

## <span data-ttu-id="16e31-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e31-141">RELATED LINKS</span></span>
