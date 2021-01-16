---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428467"
---
# <span data-ttu-id="8f7c1-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="8f7c1-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="8f7c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7c1-103">Cancela o serviço de reprodução de log ao descartar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="8f7c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f7c1-104">SYNTAX</span></span>

### <span data-ttu-id="8f7c1-105">LogReplayInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f7c1-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f7c1-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8f7c1-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f7c1-107">DESCRIPTION</span></span>
<span data-ttu-id="8f7c1-108">O cmdlet **Stop-AzSqlInstanceDatabaseLogReplay** descarta o banco de dados e, por isso, cancela o serviço de reprodução de log.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="8f7c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f7c1-109">EXAMPLES</span></span>

### <span data-ttu-id="8f7c1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f7c1-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="8f7c1-111">Esse comando cancelará o serviço de reprodução de logs no banco de dados fornecido.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="8f7c1-112">OS</span><span class="sxs-lookup"><span data-stu-id="8f7c1-112">PARAMETERS</span></span>

### <span data-ttu-id="8f7c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7c1-113">-DefaultProfile</span></span>
<span data-ttu-id="8f7c1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7c1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f7c1-115">-Force</span></span>
<span data-ttu-id="8f7c1-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="8f7c1-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8f7c1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f7c1-117">-InputObject</span></span>
<span data-ttu-id="8f7c1-118">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-118">The instance database object.</span></span>

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

### <span data-ttu-id="8f7c1-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8f7c1-119">-InstanceName</span></span>
<span data-ttu-id="8f7c1-120">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-120">The name of the instance.</span></span>

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

### <span data-ttu-id="8f7c1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f7c1-121">-Name</span></span>
<span data-ttu-id="8f7c1-122">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="8f7c1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f7c1-123">-PassThru</span></span>
<span data-ttu-id="8f7c1-124">Define se retorna o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="8f7c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f7c1-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f7c1-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f7c1-127">-Confirm</span></span>
<span data-ttu-id="8f7c1-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7c1-129">-WhatIf</span></span>
<span data-ttu-id="8f7c1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f7c1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c1-132">CommonParameters</span></span>
<span data-ttu-id="8f7c1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c1-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f7c1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f7c1-135">INPUTS</span></span>

### <span data-ttu-id="8f7c1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8f7c1-136">System.String</span></span>

### <span data-ttu-id="8f7c1-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8f7c1-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="8f7c1-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f7c1-138">OUTPUTS</span></span>

### <span data-ttu-id="8f7c1-139">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8f7c1-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="8f7c1-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f7c1-140">NOTES</span></span>

## <span data-ttu-id="8f7c1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7c1-141">RELATED LINKS</span></span>
